local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()

local Window = OrionLib:MakeWindow({Name = "港夜综合脚本(搬运)", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})
local Tab = Window:MakeTab({
	Name = "通用功能",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "键盘",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/GGH52lan/GGH52lan/main/keyboard.txt"))()
  	end    
})

Tab:AddButton({
	Name = "无限跳跃",
	Callback = function()
local InfiniteJumpEnabled = true
game:GetService("UserInputService").JumpRequest:connect(function()
	if InfiniteJumpEnabled then
		game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass'Humanoid':ChangeState("Jumping")
	end
end)
  	end    
})

Tab:AddButton({
	Name = "改速度",
	Callback = function()
-- Variables
local speedValue = 16 -- Default speed value

-- Create GUI
local gui = Instance.new("ScreenGui")
gui.Name = "JN HH Gaming"
gui.Parent = game.Players.LocalPlayer.PlayerGui

local frame = Instance.new("Frame")
frame.Name = "SpeedFrame"
frame.Size = UDim2.new(0, 200, 0, 100)
frame.Position = UDim2.new(0, 10, 0, 10)
frame.BackgroundColor3 = Color3.new(0, 0, 0)
frame.BackgroundTransparency = 0.5
frame.Parent = gui

local speedLabel = Instance.new("TextLabel")
speedLabel.Name = "SpeedLabel"
speedLabel.Size = UDim2.new(0, 180, 0, 30)
speedLabel.Position = UDim2.new(0, 10, 0, 10)
speedLabel.BackgroundColor3 = Color3.new(0, 0, 0)
speedLabel.TextColor3 = Color3.new(1, 1, 1)
speedLabel.TextSize = 18
speedLabel.Text = "Speed: " .. speedValue
speedLabel.Parent = frame

local decreaseButton = Instance.new("TextButton")
decreaseButton.Name = "DecreaseButton"
decreaseButton.Size = UDim2.new(0, 50, 0, 30)
decreaseButton.Position = UDim2.new(0, 10, 0, 50)
decreaseButton.BackgroundColor3 = Color3.new(0, 1, 0)
decreaseButton.TextColor3 = Color3.new(1, 1, 1)
decreaseButton.TextSize = 14
decreaseButton.Text = "-"
decreaseButton.Parent = frame

local increaseButton = Instance.new("TextButton")
increaseButton.Name = "IncreaseButton"
increaseButton.Size = UDim2.new(0, 50, 0, 30)
increaseButton.Position = UDim2.new(0, 140, 0, 50)
increaseButton.BackgroundColor3 = Color3.new(0, 1, 0)
increaseButton.TextColor3 = Color3.new(1, 1, 1)
increaseButton.TextSize = 14
increaseButton.Text = "+"
increaseButton.Parent = frame

-- Functions
local function updateSpeedLabel()
    speedLabel.Text = "Speed: " .. speedValue
end

local function decreaseSpeed()
    if speedValue > 1 then
        speedValue = speedValue - 1
        updateSpeedLabel()
    end
end

local function increaseSpeed()
    speedValue = speedValue + 1
    updateSpeedLabel()
end

local function onDecreaseButtonClicked()
    decreaseSpeed()
end

local function onIncreaseButtonClicked()
    increaseSpeed()
end

-- Event connections
decreaseButton.MouseButton1Click:Connect(onDecreaseButtonClicked)
increaseButton.MouseButton1Click:Connect(onIncreaseButtonClicked)

-- Main loop
while true do
    -- Modify the speed of the character (you need to replace this with the appropriate code for your specific game)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = speedValue
    wait(0.1) -- Adjust the wait time as desired
end
  	end    
})

Tab:AddButton({
	Name = "管理员脚本",
	Callback = function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
  	end    
})

Tab:AddButton({
	Name = "飞天",
	Callback = function()
loadstring("\108\111\97\100\115\116\114\105\110\103\40\103\97\109\101\58\72\116\116\112\71\101\116\40\40\39\104\116\116\112\115\58\47\47\103\105\115\116\46\103\105\116\104\117\98\117\115\101\114\99\111\110\116\101\110\116\46\99\111\109\47\109\101\111\122\111\110\101\89\84\47\98\102\48\51\55\100\102\102\57\102\48\97\55\48\48\49\55\51\48\52\100\100\100\54\55\102\100\99\100\51\55\48\47\114\97\119\47\101\49\52\101\55\52\102\52\50\53\98\48\54\48\100\102\53\50\51\51\52\51\99\102\51\48\98\55\56\55\48\55\52\101\98\51\99\53\100\50\47\97\114\99\101\117\115\37\50\53\50\48\120\37\50\53\50\48\102\108\121\37\50\53\50\48\50\37\50\53\50\48\111\98\102\108\117\99\97\116\111\114\39\41\44\116\114\117\101\41\41\40\41\10\10")()
  	end    
})

Tab:AddButton({
	Name = "重新加入服务器",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/GGH52lan/GGH52lan/main/Rejoin_Button.txt"))()
  	end    
})

local Tab = Window:MakeTab({
	Name = "床战",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "AIspoit（推荐）",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/AlSploit/AlSploit/main/Bedwars"))()
  	end    
})

Tab:AddButton({
	Name = "vape v4",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/7GrandDadPGN/VapeV4ForRoblox/main/NewMainScript.lua", true))()
  	end    
})

Tab:AddButton({
	Name = "Raven B4（脚本作者正在维护）",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/AlSploit/AlSploit/main/Bedwars"))()
  	end    
})

local Tab = Window:MakeTab({
	Name = "blox furits",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "hoho hub（有钥匙）",
	Callback = function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/acsu123/HOHO_H/main/Loading_UI'))()
  	end    
})

Tab:AddButton({
	Name = "apple hub（无钥匙）",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/ImTienNguyenZ/ImTienNguyenZ/main/obf_lc8NZP74x7Y0j6TZs4B8c2EF93mtOpRQZkarI3R8GiBRedSlkA2293QygddzqIWU.lua"))()
  	end    
})

Tab:AddButton({
	Name = "ZEN Hub(无钥匙)",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Zenhubtop/zenhubnextgen/main/Loader", true))()
  	end    
})

local Tab = Window:MakeTab({
	Name = "Break In two",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "脚本1",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/7GrandDadPGN/VapeV4ForRoblox/main/NewMainScript.lua", true))()
  	end    
})

Tab:AddButton({
	Name = "脚本2",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/RScriptz/RobloxScripts/main/BreakIn2.lua"))()
  	end    
})

local Tab = Window:MakeTab({
	Name = "刀刃球",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "Alchemy Hub",
	Callback = function()
loadstring(game:HttpGet("https://alchemyhub.xyz/v2"))()
  	end    
})

local Tab = Window:MakeTab({
	Name = "模仿者",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "脚本1",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/ph-hub/The-Mimic/main/WizardUi.lua",true))()
  	end    
})

Tab:AddButton({
	Name = "脚本2",
	Callback = function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/KTollT/KTollT/main/README.md'))()
  	end    
})

Tab:AddButton({
	Name = "脚本3",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Nicuse/FrightenedHub/main/Loader.lua", true))()
  	end    
})

local Tab = Window:MakeTab({
	Name = "伐木大亨2",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "脚本1",
	Callback = function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/Butterisgood/Butter/main/Root2.lua'))("")
  	end    
})

local OrionLib = loadstring(game:HttpGet(('https://hypernite.xyz/Backup/Orion/source.lua')))() -- Backed up to my host