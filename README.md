if not game:IsLoaded() then 
game.Loaded:Wait() end 
repeat wait() until game:IsLoaded()

 
if game.PlaceId == 3565304751 then
game.Players.LocalPlayer.PlayerGui:WaitForChild("HUD")
game.Players.LocalPlayer.PlayerGui.HUD.Bottom.Stats.Visible = true
game.Players.LocalPlayer.PlayerGui.HUD.Bottom.Stats.Labvel.TextLabel.Text = "In queue....."
end

if game.PlaceId == 2050207304 then
game.Players.LocalPlayer.PlayerGui:WaitForChild("HUD")
game.Players.LocalPlayer.PlayerGui.HUD.Bottom.Stats.Visible = true
game.Players.LocalPlayer.PlayerGui.HUD.Bottom.Stats.Labvel.TextLabel.Text = "In Broly....."
if game.PlaceId == 2050207304 then
local plr = game.Players.LocalPlayer
game.Workspace:WaitForChild("Live")
game.Workspace.Live:WaitForChild(plr.Name)
game:GetService("RunService").RenderStepped:connect(
    function()
        game:GetService("Players").LocalPlayer.PlayerGui.HUD.Bottom.SP.Visible = true
        game:GetService("Players").LocalPlayer.PlayerGui.HUD.Bottom.SP.Text = " RejoinTime : " .. math.floor(Workspace.DistributedGameTime) .. " / " .. _G.RejoinTime .. " Broly Health : " .. math.floor(Workspace.Live["Broly BR"].Humanoid.Health) 
        game:GetService("Players").LocalPlayer.PlayerGui.HUD.Bottom.SP.BackgroundColor3 = Color3.new(0, 0, 0)
        game:GetService("Players").LocalPlayer.PlayerGui.HUD.Bottom.SP.BackgroundTransparency = 0.2 
 game:GetService("Players").LocalPlayer.PlayerGui.HUD.Bottom.SP.BorderColor3 = Color3.new(0, 0, 0)
end)
end
end





if game.PlaceId == 3565304751 then
local plr = game.Players.LocalPlayer
game.Workspace:WaitForChild("Live")
game.Workspace.Live:WaitForChild(plr.Name)
game:GetService("RunService").RenderStepped:connect(
    function()
        game:GetService("Players").LocalPlayer.PlayerGui.HUD.Bottom.SP.Visible = true
        game:GetService("Players").LocalPlayer.PlayerGui.HUD.Bottom.SP.Text = "Last Updated : 21/2/2022";
        game:GetService("Players").LocalPlayer.PlayerGui.HUD.Bottom.SP.BackgroundColor3 = Color3.new(777, 777, 777)
        game:GetService("Players").LocalPlayer.PlayerGui.HUD.Bottom.SP.BackgroundTransparency = 0.2 
 game:GetService("Players").LocalPlayer.PlayerGui.HUD.Bottom.SP.BorderColor3 = Color3.new(0, 0, 0)
end)
end




if not game:IsLoaded() then
    game.Loaded:Wait() end



game:GetService("StarterGui"):SetCore(
    "SendNotification",
    {
        Title = "Auto Broly V3";
        Text = "By Demoww#6235"
    })





    if _G.FreezeEXP == true then
			game:GetService("Workspace").Live[Client.name]:FindFirstChild("True"):Destroy()
		end

  local RejoinTime =
        coroutine.create(
        function()
            game:GetService("RunService").RenderStepped:Connect(
                function()
                    if game:GetService("Workspace").DistributedGameTime >= _G.RejoinTime then
                        game:GetService("TeleportService"):Teleport(3565304751, LocalPlayer)
                    end
                end
            )
        end
    )
    coroutine.resume(RejoinTime)   
local DamageChecker =
        coroutine.create(
        function()
            repeat
                wait()
            until game:GetService("Workspace").DistributedGameTime >= _G.GrabChecker
            if game:GetService("Workspace").Live["Broly BR"].Stats["Health-Max"].Value < 53589 then
                game:GetService("TeleportService"):Teleport(3565304751, LocalPlayer)
            end
        end
    )

    coroutine.resume(DamageChecker)

if game.PlaceId == 536102540 then
    game:GetService("TeleportService"):Teleport(3565304751)
end

function Twn(HRP, Place, Length)
    local Twn =
        game:GetService("TweenService"):Create(
        HRP,
        TweenInfo.new(Length, Enum.EasingStyle.Quad, Enum.EasingDirection.InOut),
        {CFrame = Place}
    )
    Twn:Play()
    Twn.Completed:Wait()
end
local Live = game:WaitForChild("Workspace").Live
local Char = Live:WaitForChild(game.Players.LocalPlayer.Name)
if game.PlaceId == 3565304751 then
    
    local Hum = game.Players.LocalPlayer.Character.Humanoid

local newHum = Hum:Clone()
newHum.Name = "Humanoid"
newHum.Parent = game.Players.LocalPlayer.Character
Hum:Destroy()
Workspace.CurrentCamera.CameraSubject = game.Players.LocalPlayer.Character.Humanoid
    
    Char.LowerTorso:Destroy()
    local Pads = {}
    for i, v in pairs(game:WaitForChild("Workspace"):GetChildren()) do
        if v.Name:find("BrolyTeleport") then
            table.insert(Pads, v)
        end
    end
    local pad = Pads[math.random(1, 7)]
    print(pad.Name)
    Twn(Char.HumanoidRootPart, pad.PrimaryPart.CFrame, 1)
    wait(25)
  local x = {}
    for _, v in ipairs(game:GetService("HttpService"):JSONDecode(game:HttpGetAsync("https://games.roblox.com/v1/games/" .. game.PlaceId .. "/servers/Public?sortOrder=Asc&limit=100")).data) do
        if type(v) == "table" and v.maxPlayers > v.playing and v.id ~= game.JobId then
            x[#x + 1] = v.id
        end
    end
    if #x > 0 then
        game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, x[math.random(1, #x)])
    end
end


if game.PlaceId == 2050207304 then
    local B = Live:WaitForChild("Broly BR")
    local plr = game.Players.LocalPlayer
    

if _G.LowGFX == true then
for i,v in pairs(game.Lighting:GetChildren()) do
if v:IsA("") or v:IsA("Sky") or v:IsA("BlurEffect") or v:IsA("BloomEffect") or v:IsA("SunRaysEffect") then
v:Destroy()
end
end

game.Lighting.Ambient = Color3.fromRGB(255, 255, 255)
game.Lighting.Brightness = 1
game.Lighting.ClockTime = 14
game.Lighting.ColorShift_Bottom = Color3.fromRGB(255, 255, 255)
game.Lighting.ColorShift_Top = Color3.fromRGB(255, 255, 255)
game.Lighting.ExposureCompensation = 0
game.Lighting.FogColor = Color3.fromRGB(255, 255, 255)
game.Lighting.FogEnd = 999999999
game.Lighting.GeographicLatitude = 41.733
game.Lighting.OutdoorAmbient = Color3.fromRGB(255, 255, 255)
game.Lighting.GlobalShadows = true
game.Lighting.Changed:Connect(function()
game.Lighting.Ambient = Color3.fromRGB(255, 255, 255)
game.Lighting.Brightness = 1
game.Lighting.ClockTime = 14
game.Lighting.ColorShift_Bottom = Color3.fromRGB(255, 255, 255)
game.Lighting.ColorShift_Top = Color3.fromRGB(255, 255, 255)
game.Lighting.ExposureCompensation = 0
game.Lighting.FogColor = Color3.fromRGB(255, 255, 255)
game.Lighting.FogEnd = 999999999
game.Lighting.GeographicLatitude = 41.733
game.Lighting.OutdoorAmbient = Color3.fromRGB(255, 255, 255)
game.Lighting.GlobalShadows = true
end)
game.Lighting.DescendantAdded:Connect(function(obj)
if obj:IsA("") or obj:IsA("Sky") or obj:IsA("BlurEffect") or obj:IsA("BloomEffect") or obj:IsA("SunRaysEffect") then
obj:Destroy()
end
end)
end

if _G.BadPc == true then
    wait(2)
    end


local plr = game.Players.LocalPlayer

    if _G.AntiLeech == true then
        if #game.Players:GetPlayers() > 1 then
            
            game:GetService("TeleportService"):Teleport(3565304751, LocalPlayer)
        end
    end


if _G.Forma == true then
             if not game:IsLoaded() then 
game.Loaded:Wait() end 


if game.PlaceId == 2050207304 then
    if #game.Players:GetPlayers() >= 10 then
        game.TeleportService:Teleport(3565304751, game.Players.LocalPlayer)
    end
    game.RunService.RenderStepped:Connect(function()
        if game.Players.LocalPlayer.Character.Ki.Value <= 690 then
            game.Players.LocalPlayer.Backpack.ServerTraits.Transform:FireServer("g")
        end
    end)
end


              
           
       game.Workspace.Camera.FieldOfView = 200
       

game.Players.LocalPlayer.PlayerGui.HUD.FullSize.Money.Text = "Autobroly Made By Demoww#6235 Version 3"
end

             


        Twn(Char.HumanoidRootPart, B.HumanoidRootPart.CFrame, 1)
        game:GetService("RunService").RenderStepped:connect(
            function()
                Char.Humanoid:ChangeState(11)
                game.Workspace.CurrentCamera.CFrame =
                    CFrame.new(Char.HumanoidRootPart.Position, B.HumanoidRootPart.Position) * CFrame.new(0, 2, 10)
                if Char:FindFirstChild("Attacking") then
                    Char.Attacking:Destroy()
                end
                if Char:FindFirstChild("Action") then
                    Char.Action:Destroy()
                end
                if Char:FindFirstChild("Slow") then
                    Char.Slow:Destroy()
                end
                if Char:FindFirstChild("Using") then
                    Char.Using:Destroy()
                end
                if Char:FindFirstChild("MoveStart") then
                    Char.MoveStart:Destroy()
                end
            
                if Char.Humanoid.Health < 1 then
                    game:GetService("TeleportService"):Teleport(3565304751)
                end
                game.Players.LocalPlayer.Backpack.ServerTraits.EatSenzu:FireServer(true)
                if _G.God == true then
                if Char.Humanoid.Health < 25 then
                    game.Players.LocalPlayer.Backpack.ServerTraits.Transform:FireServer("h")
                end end
                if _G.HardPunch == true then
                if game.Players.LocalPlayer.Character.Ki.Value < 32 then
                    _G.HardPunch = true
                    local A_1 = {
                        [1] = "m2"
                    }
                    local A_2 =
                        CFrame.new(
                        -5885.95947,
                        17.9874992,
                        -4159.84717,
                        -0.104352206,
                        0.396405816,
                        -0.912125587,
                        -0,
                        0.917132735,
                        0.398581922,
                        0.994540393,
                        0.0415929034,
                        -0.0957048237
                    )
                    local A_3 = nil
                    local A_4 = false
                    local Event = game:GetService("Players").LocalPlayer.Backpack.ServerTraits.Input
                    Event:FireServer(A_1, A_2, A_3, A_4)
                    wait()
                    _G.HardPunch = true
                end
                end
                Char.HumanoidRootPart.CFrame =
                    game.Workspace.Live["Broly BR"].HumanoidRootPart.CFrame * CFrame.new(0, 0, 4.20)
                Char.HumanoidRootPart.CFrame = CFrame.new(Char.HumanoidRootPart.Position, B.HumanoidRootPart.Position)
            end
        )
        game.Players.LocalPlayer.Backpack["Dragon Crush"].Parent = Char
    Char["Dragon Crush"].Activator["Flip"]:Destroy()
    Char["Dragon Crush"].Activator["Throw"]:Destroy()
    Char["Dragon Crush"].Activator["Blocked"]:Destroy()
    Char["Dragon Crush"].Activator["HitDown"]:Destroy()
    Char["Dragon Crush"].Activator["BoneBreak"]:Destroy()
    wait(0.2)
    Char["Dragon Crush"]:Activate()
    wait(0.2)
    Char["Dragon Crush"]:Deactivate()
    Char["Dragon Crush"].Parent = game.Players.LocalPlayer.Backpack
        if _G.Anchored == true then
	game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true

      
game.Workspace.Live['Broly BR'].LowerTorso.Anchored = true
game.Workspace.Live['Broly BR'].UpperTorso.Anchored = true
end
repeat
            game:GetService("RunService").RenderStepped:Wait()
            for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                if
                    v.Name == Move1 or v.Name == Move2 or v.Name == Move3 or v.Name == Move4 or v.Name == Move5 or
                        v.Name == Move6 or
                        v.Name == Move7 or
                        v.Name == Move8 or
                        v.Name == Move9 or
                        v.Name == Move10
                 then
                    v.Parent = game:GetService("Workspace").Live[game.Players.LocalPlayer.Name]
                    wait()
                    v:Activate()
                    v:Deactivate()
                    v.Parent = game.Players.LocalPlayer.Backpack
                end
            end
         
        until B.Humanoid.Health < .1
        game:GetService("TeleportService"):Teleport(3565304751)


end

