-- Script básico para um hub de autofarm no Blox Fruits
-- Nome do hub: 4K Blox Hub

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local ToggleButton = Instance.new("TextButton")

ScreenGui.Name = "4KBloxHub"
ScreenGui.Parent = game.CoreGui

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(0, 0, 255) -- Cor azul
Frame.Position = UDim2.new(0.5, -100, 0.5, -50)
Frame.Size = UDim2.new(0, 200, 0, 100)

ToggleButton.Parent = Frame
ToggleButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ToggleButton.Position = UDim2.new(0.25, 0, 0.25, 0)
ToggleButton.Size = UDim2.new(0.5, 0, 0.5, 0)
ToggleButton.Text = "Ativar Autofarm"

local autofarmActive = false

ToggleButton.MouseButton1Click:Connect(function()
    autofarmActive = not autofarmActive
    if autofarmActive then
        ToggleButton.Text = "Desativar Autofarm"
        -- false
    else
        ToggleButton.Text = "Ativar Autofarm"
        -- getgenv().Team = "Pirates"
getgenv().AutoLoad = false --Will Load Script On Server Hop
getgenv().SlowLoadUi  = false
getgenv().ForceUseSilentAimDashModifier = false --Force turn on silent aim , if error then executor problem
getgenv().ForceUseWalkSpeedModifier = false --Force turn on Walk Speed Modifier , if error then executor problem

    end
end)
