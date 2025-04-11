local caption = game.Players.LocalPlayer:WaitForChild("PlayerGui").MainUI.MainFrame.Caption
caption.TextColor3 = Color3.fromRGB(175, 3, 255)
require(game.Players.LocalPlayer.PlayerGui.MainUI.Initiator.Main_Game).caption("Survival Mode Actived",true)
wait(2)
local caption = game.Players.LocalPlayer:WaitForChild("PlayerGui").MainUI.MainFrame.Caption
caption.TextColor3 = Color3.fromRGB(175, 3, 255)
require(game.Players.LocalPlayer.PlayerGui.MainUI.Initiator.Main_Game).caption("Made By Guest On Discord",true)
wait(2)
local caption = game.Players.LocalPlayer:WaitForChild("PlayerGui").MainUI.MainFrame.Caption
caption.TextColor3 = Color3.fromRGB(175, 3, 255)
require(game.Players.LocalPlayer.PlayerGui.MainUI.Initiator.Main_Game).caption("Inspired By Some Modes",true)
wait(2)
local caption = game.Players.LocalPlayer:WaitForChild("PlayerGui").MainUI.MainFrame.Caption
caption.TextColor3 = Color3.fromRGB(175, 3, 255)
require(game.Players.LocalPlayer.PlayerGui.MainUI.Initiator.Main_Game).caption("Credits To Alot Of People (I Can't Say Them All)",true)
loadstring(game:HttpGet("https://raw.githubusercontent.com/ChronoAcceleration/Comet-Development/refs/heads/main/Doors/Game/PlayerHealthbars.lua"))()
loadstring(game:HttpGet("https://raw.githubusercontent.com/notpoiu/Scripts/main/Scanner.lua"))()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Darker-TheDarkestGuy/Scripts/refs/heads/main/Bloxy%20cola"))()
loadstring(game:HttpGet("https://raw.githubusercontent.com/bocaj111004/Scripts/refs/heads/main/GummyFlashlight.lua"))()

--Cave ambience
local sound = Instance.new("Sound")

sound.SoundId = "rbxassetid://9044553186"

sound.Volume = 1.5

sound.Looped = true

sound:Play()

sound.Parent = workspace

while true do wait(2)
local lastroom = game.ReplicatedStorage.GameData.LatestRoom
local lastrooms = game.Workspace.CurrentRooms:GetChildren()[#game.Workspace.CurrentRooms:GetChildren() - 1]

function light(tim,color0,color1)
    local tweenservice = game:GetService("TweenService")
    local info = TweenInfo.new(tim,Enum.EasingStyle.Linear)
    for _ , light in pairs(game.Workspace.CurrentRooms:GetDescendants()) do
        if light:IsA("Light") or light:IsA("SurfaceLight") or light:IsA("SpotLight") then
            local target = {Color = color1}
            local anim = tweenservice:Create(light,info,target)
            anim:Play()
        end
        if light:IsA("MeshPart") and light.Material == Enum.Material.Neon  and light.Name ~= "Skybox" then
            local target1 = {Color = color0}
            local anim2 = tweenservice:Create(light,info,target1)
            anim2:Play()
        end
    end
end

lastrooms:SetAttribute("Ambient",Color3.fromRGB(0,0,0))
light(1,Color3.fromRGB(0,0,0),Color3.fromRGB(0,0,0))
end

---====== Load achievement giver ======---
local achievementGiver = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors/Custom%20Achievements/Source.lua"))()

---====== Display achievement ======---
achievementGiver({
    Title = "Survival Mode",
    Desc = "Nightmare Began. Becareful!",
    Reason = "Executed Survival Mode",
    Image = "rbxassetid://16802291466"
})

-- chainsmoker 
coroutine.wrap(function()
    while true do
        wait(10)
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        wait(5)
local spawner = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors/Entity%20Spawner/V2/Source.lua"))()

---====== Create entity ======---

local entity = spawner.Create({
	Entity = {
		Name = "Zombie",
		Asset = "https://github.com/Darker-TheDarkestGuy/Scripts/raw/refs/heads/main/zombie.rbxm",
		HeightOffset = 0
	},
	Lights = {
		Flicker = {
			Enabled = true,
			Duration = 1
		},
		Shatter = true,
		Repair = false
	},
	Earthquake = {
		Enabled = true
	},
	CameraShake = {
		Enabled = false,
		Range = 100,
		Values = {1.5, 20, 0.1, 1} -- Magnitude, Roughness, FadeIn, FadeOut
	},
	Movement = {
		Speed = 10,
		Delay = 2,
		Reversed = false
	},
	Rebounding = {
		Enabled = false,
		Type = "Ambush", -- "Blitz"
		Min = 1,
		Max = 1,
		Delay = 2
	},
	Damage = {
		Enabled = true,
		Range = 10,
		Amount = 20
	},
	Crucifixion = {
		Enabled = true,
		Range = 60,
		Resist = false,
		Break = true
	},
	Death = {
		Type = "Guiding", -- "Curious"
		Hints = {"Death", "Hints", "Go", "Here"},
		Cause = ""
	}
})

---====== Debug entity ======---

entity:SetCallback("OnSpawned", function()
    print("Entity has spawned")
end)

entity:SetCallback("OnStartMoving", function()
    print("Entity has started moving")
end)

entity:SetCallback("OnEnterRoom", function(room, firstTime)
    if firstTime == true then
        print("Entity has entered room: ".. room.Name.. " for the first time")
    else
        print("Entity has entered room: ".. room.Name.. " again")
    end
end)

entity:SetCallback("OnLookAt", function(lineOfSight)
	if lineOfSight == true then
		print("Player is looking at entity")
	else
		print("Player view is obstructed by something")
	end
end)

entity:SetCallback("OnRebounding", function(startOfRebound)
    if startOfRebound == true then
        print("Entity has started rebounding")
	else
        print("Entity has finished rebounding")
	end
end)

entity:SetCallback("OnDespawning", function()
    print("Entity is despawning")
end)

entity:SetCallback("OnDespawned", function()
    print("Entity has despawned")
end)

entity:SetCallback("OnDamagePlayer", function(newHealth)
	if newHealth == 0 then
		print("Entity has killed the player")
	else
		print("Entity has damaged the player")
	end
end)

--[[

DEVELOPER NOTE:
By overwriting 'CrucifixionOverwrite' the default crucifixion callback will be replaced with your custom callback.

entity:SetCallback("CrucifixionOverwrite", function()
    print("Custom crucifixion callback")
end)

]]--

---====== Run entity ======---

entity:Run()
    end
end)()

-- chainsmoker 
coroutine.wrap(function()
    while true do
        wait(50)
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        wait(5)
local spawner = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors/Entity%20Spawner/V2/Source.lua"))()

---====== Create entity ======---

local entity = spawner.Create({
	Entity = {
		Name = "Zombie Light",
		Asset = "https://github.com/Darker-TheDarkestGuy/Scripts/raw/refs/heads/main/zombielight.rbxm",
		HeightOffset = 0
	},
	Lights = {
		Flicker = {
			Enabled = true,
			Duration = 5
		},
		Shatter = true,
		Repair = false
	},
	Earthquake = {
		Enabled = true
	},
	CameraShake = {
		Enabled = false,
		Range = 100,
		Values = {1.5, 20, 0.1, 1} -- Magnitude, Roughness, FadeIn, FadeOut
	},
	Movement = {
		Speed = 60,
		Delay = 2,
		Reversed = false
	},
	Rebounding = {
		Enabled = false,
		Type = "Ambush", -- "Blitz"
		Min = 1,
		Max = 1,
		Delay = 2
	},
	Damage = {
		Enabled = true,
		Range = 20,
		Amount = 50
	},
	Crucifixion = {
		Enabled = true,
		Range = 60,
		Resist = false,
		Break = true
	},
	Death = {
		Type = "Guiding", -- "Curious"
		Hints = {"Death", "Hints", "Go", "Here"},
		Cause = ""
	}
})

---====== Debug entity ======---

entity:SetCallback("OnSpawned", function()
    local plr = game.Players.LocalPlayer
local chr = plr.Character or plr.CharacterAdded:Wait()
local function Moving(target, dur)
    local tween_info = TweenInfo.new(dur, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)
    local tween = TweenService:Create(ZombieLight:FindFirstChildWhichIsA("BasePart"), tween_info, {CFrame = target})
    tween:Play()
    tween.Completed:Wait()
end

task.spawn(function()
while Move == true do
wait(0.01)
if not chr:GetAttribute("Hiding") then
Moving(chr.HumanoidRootPart.CFrame, 1)
elseif chr:GetAttribute("Hiding") then
end
end
end)
end)

entity:SetCallback("OnStartMoving", function()
    print("Entity has started moving")
end)

entity:SetCallback("OnEnterRoom", function(room, firstTime)
    if firstTime == true then
        print("Entity has entered room: ".. room.Name.. " for the first time")
    else
        print("Entity has entered room: ".. room.Name.. " again")
    end
end)

entity:SetCallback("OnLookAt", function(lineOfSight)
	if lineOfSight == true then
		print("Player is looking at entity")
	else
		print("Player view is obstructed by something")
	end
end)

entity:SetCallback("OnRebounding", function(startOfRebound)
    if startOfRebound == true then
        print("Entity has started rebounding")
	else
        print("Entity has finished rebounding")
	end
end)

entity:SetCallback("OnDespawning", function()
    print("Entity is despawning")
end)

entity:SetCallback("OnDespawned", function()
    print("Entity has despawned")
end)

entity:SetCallback("OnDamagePlayer", function(newHealth)
	if newHealth == 0 then
		print("Entity has killed the player")
	else
		print("Entity has damaged the player")
	end
end)

--[[

DEVELOPER NOTE:
By overwriting 'CrucifixionOverwrite' the default crucifixion callback will be replaced with your custom callback.

entity:SetCallback("CrucifixionOverwrite", function()
    print("Custom crucifixion callback")
end)

]]--

---====== Run entity ======---

entity:Run()
    end
end)()

-- chainsmoker 
coroutine.wrap(function()
    while true do
        wait(100)
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        wait(5)
local spawner = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors/Entity%20Spawner/V2/Source.lua"))()

---====== Create entity ======---

local entity = spawner.Create({
	Entity = {
		Name = "Giant Zombie",
		Asset = "https://github.com/Darker-TheDarkestGuy/Scripts/raw/refs/heads/main/giant%20zombie.rbxm",
		HeightOffset = 0
	},
	Lights = {
		Flicker = {
			Enabled = true,
			Duration = 10
		},
		Shatter = true,
		Repair = false
	},
	Earthquake = {
		Enabled = true
	},
	CameraShake = {
		Enabled = true,
		Range = 50,
		Values = {1.5, 20, 0.1, 1} -- Magnitude, Roughness, FadeIn, FadeOut
	},
	Movement = {
		Speed = 100,
		Delay = 2,
		Reversed = false
	},
	Rebounding = {
		Enabled = true,
		Type = "Ambush", -- "Blitz"
		Min = 1,
		Max = 1,
		Delay = 2
	},
	Damage = {
		Enabled = true,
		Range = 60,
		Amount = 125
	},
	Crucifixion = {
		Enabled = true,
		Range = 70,
		Resist = false,
		Break = true
	},
	Death = {
		Type = "Guiding", -- "Curious"
		Hints = {"Death", "Hints", "Go", "Here"},
		Cause = ""
	}
})

---====== Debug entity ======---

entity:SetCallback("OnSpawned", function()
    local plr = game.Players.LocalPlayer
local chr = plr.Character or plr.CharacterAdded:Wait()
local function Moving(target, dur)
    local tween_info = TweenInfo.new(dur, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)
    local tween = TweenService:Create(GiantZombie:FindFirstChildWhichIsA("BasePart"), tween_info, {CFrame = target})
    tween:Play()
    tween.Completed:Wait()
end

task.spawn(function()
while Move == true do
wait(0.01)
if not chr:GetAttribute("Hiding") then
Moving(chr.HumanoidRootPart.CFrame, 5)
elseif chr:GetAttribute("Hiding") then
end
end
end)
end)

entity:SetCallback("OnStartMoving", function()
    print("Entity has started moving")
end)

entity:SetCallback("OnEnterRoom", function(room, firstTime)
    if firstTime == true then
        print("Entity has entered room: ".. room.Name.. " for the first time")
    else
        print("Entity has entered room: ".. room.Name.. " again")
    end
end)

entity:SetCallback("OnLookAt", function(lineOfSight)
	if lineOfSight == true then
		print("Player is looking at entity")
	else
		print("Player view is obstructed by something")
	end
end)

entity:SetCallback("OnRebounding", function(startOfRebound)
    if startOfRebound == true then
        print("Entity has started rebounding")
	else
        print("Entity has finished rebounding")
	end
end)

entity:SetCallback("OnDespawning", function()
    print("Entity is despawning")
end)

entity:SetCallback("OnDespawned", function()
    print("Entity has despawned")
end)

entity:SetCallback("OnDamagePlayer", function(newHealth)
	if newHealth == 0 then
		print("Entity has killed the player")
	else
		print("Entity has damaged the player")
	end
end)

--[[

DEVELOPER NOTE:
By overwriting 'CrucifixionOverwrite' the default crucifixion callback will be replaced with your custom callback.

entity:SetCallback("CrucifixionOverwrite", function()
    print("Custom crucifixion callback")
end)

]]--

---====== Run entity ======---

entity:Run()
    end
end)()
