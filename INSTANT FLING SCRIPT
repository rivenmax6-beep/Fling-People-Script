-- SAFE INSTANT FLING SCRIPT
local Players = game:GetService("Players")
local Player = Players.LocalPlayer

local function flingPlayer(targetPlayer)
    if targetPlayer.Character and targetPlayer.Character:FindFirstChild("HumanoidRootPart") then
        local hrp = targetPlayer.Character.HumanoidRootPart
        local bv = Instance.new("BodyVelocity")
        bv.Velocity = Vector3.new(math.random(-500,500),300,math.random(-500,500))
        bv.MaxForce = Vector3.new(1e5,1e5,1e5)
        bv.Parent = hrp
        game:GetService("Debris"):AddItem(bv,1)
    end
end

-- GUI
local gui = Instance.new("ScreenGui", Player:WaitForChild("PlayerGui"))
local frame = Instance.new("Frame")
frame.Size = UDim2.new(0,300,0,120)
frame.Position = UDim2.new(0.5,-150,0.5,-60)
frame.BackgroundColor3 = Color3.fromRGB(50,50,50)
frame.Parent = gui

local nameBox = Instance.new("TextBox")
nameBox.Size = UDim2.new(0,280,0,40)
nameBox.Position = UDim2.new(0,10,0,10)
nameBox.PlaceholderText = "Enter player name"
nameBox.Parent = frame

local button = Instance.new("TextButton")
button.Size = UDim2.new(0,280,0,50)
button.Position = UDim2.new(0,10,0,60)
button.Text = "FLING!"
button.BackgroundColor3 = Color3.fromRGB(200,50,50)
button.TextColor3 = Color3.new(1,1,1)
button.Parent = frame

button.MouseButton1Click:Connect(function()
    local targetName = nameBox.Text
    local targetPlayer = Players:FindFirstChild(targetName)
    if targetPlayer then
        flingPlayer(targetPlayer)
    else
        warn("Player not found!")
    end
end)
