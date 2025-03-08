
    
local Spawner = loadstring(game:HttpGet('https://raw.githubusercontent.com/MuhXd/DoorSuff/main/OtherSuff/DoorEntitySpawn%2BSource'))()


-- Create entity
local entity = Spawner.createEntity({
    CustomName = "PhilBad", -- Custom name of your entity
    Model = "rbxassetid://11295053158", -- Can be GitHub file or rbxassetid
    Speed = 0, -- Percentage, 100 = default Rush speed
    DelayTime = 0.95, -- Time before starting cycles (seconds)
    HeightOffset = 0,
    CanKill = false,
    NoDieOnCrouching = false,
    NoHiding = false,
    AntiCrucifix = false,
    KillRange = 0,
    OneRoom = true,
    DieOnLook = false,
    BreakLights = true,
    BackwardsMovement = false,
     MovementDeath = {
        false, -- Turned On?
        '1',  --- '1'= 'Instant Without Being Looked out' | '2' = 'With Being Looked At'
    },
    FlickerLights = {
        false, -- Enabled/Disabled
        1, -- Time (seconds)
    },
    Cycles = {
        Min = 1,
        Max = 1,
        WaitTime = 2,
    },
    CamShake = {
        false, -- Enabled/Disabled
        {3.5, 20, 0.1, 1}, -- Shake values (don't change if you don't know)
        100, -- Shake start distance (from Entity to you)
    },
    Jumpscare = {
        false, -- Enabled/Disabled
        {
            Type = "2", -- "Normal" or 1 | "Pop" or 2 | "endlessdoorsrebound" or "Rebound" or 3 | More coming Soon
            Image1 = "rbxassetid://10483855823", -- Image1 url
            Image2 = "rbxassetid://10483999903", -- Image2 url
            Shake = true,
            Sound1 = {
                "0", -- SoundId Link or Roblox ID
                { Volume = 5 }, -- Sound properties
            },
            Sound2 = {
                "0", -- SoundId Link or Roblox ID
                { Volume = 3 }, -- Sound properties
            },
            Flashing = {
                true, -- Enabled/Disabled
                Color3.fromRGB(255, 255, 255), -- Color
            },
            Tease = {
                true, -- Enabled/Disabled
                Min = 1,
                Max = 3,
            },
        },
    },
    Color = 'GuidingLight', -- CuriousLight ( Yellow ) | GuidingLight ( Blue )
    DiffrentMessages = false,
    CustomDialog = {  
        {"Claim has seen you.", "It will consume anyone on sight.", "It takes a bit to fully spawn in", "so you can use that to your advantage."}, -- Death Messages
        {"Stop Dieing"},
        {"Bruh", "Use what you have learned from Rush!"},
        {"It seems like Template is causing quite the ruckus...", "Hide in a closet or bed as quickly as possible!"},
         {"I have told You What to do", "YOU JUST HAVE A SKILL ISSUE"}
    }
})

-----[[ Advanced Sctipting ]]-----

entity.Debug.OnEntityMoving = function(Invincible,Hiding,plrCollisionPoint)
print("Invincible: "..tostring(Invincible))
print("Player to Entity Collision (None hiding Point): "..tostring(plrCollisionPoint))
print("Hiding: "..tostring(Hiding))
end
       
entity.Debug.OnEntitySpawned = function()
    print("Entity has spawned:")
    wait(1)
ModuleEvents = require(game:GetService("ReplicatedStorage").ClientModules.Module_Events)
ModuleEvents.shatter(workspace.CurrentRooms[game:GetService("ReplicatedStorage").GameData.LatestRoom.Value])
    workspace.PhilBad:Destroy()
		local CameraShaker = require(game.ReplicatedStorage.CameraShaker)
		local camara = game.Workspace.CurrentCamera
		local camShake = CameraShaker.new(Enum.RenderPriority.Camera.Value, function(shakeCf)
			camara.CFrame = camara.CFrame * shakeCf
		end)
		local camara = game.Workspace.CurrentCamera
		local camShake = CameraShaker.new(Enum.RenderPriority.Camera.Value, function(shakeCf)
			camara.CFrame = camara.CFrame * shakeCf
		end)
		camShake:Start()
		camShake:ShakeOnce(100,50,0.5,0.5)
        local roast = Instance.new("Sound")
    roast.Parent = workspace
    roast.Name = "Break2"
    roast.SoundId = "rbxassetid://6737582037"
    roast.Volume = 3
    local roast1 = Instance.new("Sound")
    roast1.Parent = workspace
    roast1.Name = "Break1"
    roast1.SoundId = "rbxassetid://9103909576"
    roast1.Volume = 3
    local roast2 = Instance.new("Sound")
    roast2.Parent = workspace
    roast2.Name = "Break2"
    roast2.SoundId = "rbxassetid://5961220911"
    roast2.Volume = 3
    roast2:Play()
    roast1:Play()
    roast:Play()
	local tweeninfo = TweenInfo.new(0.5)
	local info = {Color = Color3.new(0, 0, 0)}
	for i,v in pairs(game.Workspace.CurrentRooms:GetDescendants()) do
		if v:IsA("Light") then
			game.TweenService:Create(v,tweeninfo,info):Play()
			if v.Parent.Name == "LightFixture" then
				game.TweenService:Create(v.Parent,tweeninfo,info):Play()
			end
		end
	end
workspace.CurrentRooms[game.ReplicatedStorage.GameData.LatestRoom.Value].Assets.Rug:Destroy()
end

entity.Debug.OnEntityDespawned = function()
    print("Entity has despawned:")
end

entity.Debug.OnEntityStartMoving = function()
    print("Entity has started moving:")
firesignal(game.ReplicatedStorage.EntityInfo.UseEventModule.OnClientEvent, "tryp", workspace.CurrentRooms[game.ReplicatedStorage.GameData.LatestRoom.Value], 100)
room = game:GetService("ReplicatedStorage").GameData.LatestRoom.Value
for i, v in pairs(workspace.CurrentRooms[room].Parts:GetChildren()) do 
	if v.Name == "Wall" then
		v.Material = "Limestone"
		v.Color = Color3.new(0, 0, 0)
			if v:FindFirstChild("Wallpaper") ~= nil then
			v.Wallpaper:Destroy()
			end
	end
end
for i, v in pairs(workspace.CurrentRooms[room].Parts.DropCeiling:GetChildren()) do 
	if v.Name == "Ceiling" then
		v.Material = "Limestone"
		v.Color = Color3.new(0, 0, 0)
	end
end
for i, v in pairs(workspace.CurrentRooms[room].Parts.DropCeiling.Model:GetChildren()) do 
	v.Material = "Limestone"
	v.Color = Color3.new(0, 0, 0)
end
    for i,v in pairs(workspace.CurrentRooms[game.ReplicatedStorage.GameData.LatestRoom.Value].Parts:GetDescendants()) do
  if v:IsA("BasePart") and game.ReplicatedStorage.GameData.LatestRoom.Value < 90 then
        v.Material = Enum.Material.Limestone
        v.Color = Color3.new(0, 0, 0) -- sets the color
        end
    end
    
game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
firesignal(game.ReplicatedStorage.EntityInfo.UseEventModule.OnClientEvent, "tryp", workspace.CurrentRooms[game.ReplicatedStorage.GameData.LatestRoom.Value], 100)
room = game:GetService("ReplicatedStorage").GameData.LatestRoom.Value
for i, v in pairs(workspace.CurrentRooms[room].Parts:GetChildren()) do 
	if v.Name == "Wall" then
		v.Material = "Limestone"
		v.Color = Color3.new(0, 0, 0)
			if v:FindFirstChild("Wallpaper") ~= nil then
			v.Wallpaper:Destroy()
			end
	end
end
for i, v in pairs(workspace.CurrentRooms[room].Parts.DropCeiling:GetChildren()) do 
	if v.Name == "Ceiling" then
		v.Material = "Limestone"
		v.Color = Color3.new(0, 0, 0)
	end
end
for i, v in pairs(workspace.CurrentRooms[room].Parts.DropCeiling.Model:GetChildren()) do 
	v.Material = "Limestone"
	v.Color = Color3.new(0, 0, 0)
end
    for i,v in pairs(workspace.CurrentRooms[game.ReplicatedStorage.GameData.LatestRoom.Value].Parts:GetDescendants()) do
  if v:IsA("BasePart") and game.ReplicatedStorage.GameData.LatestRoom.Value < 90 then
        v.Material = Enum.Material.Limestone
        v.Color = Color3.new(0, 0, 0) -- sets the color
        end
    end
workspace.CurrentRooms[game.ReplicatedStorage.GameData.LatestRoom.Value].Assets.Rug:Destroy()
workspace.CurrentRooms[game.ReplicatedStorage.GameData.LatestRoom.Value].Assets.Light_Fixtures:Destroy()
end

entity.Debug.OnEntityFinishedRebound = function()
    print("Entity has finished rebound:")
end

entity.Debug.OnEntityEnteredRoom = function(entityTable, room)
    print("Entity:", "has entered room:",room)
end

entity.Debug.OnLookAtEntity = function()
    print("Player has looked at entity:")
end

entity.Debug.OnDeath = function()
    warn("Player has died.")
end

------------------------

-- Run the created entity
Spawner.runEntity(entity)
