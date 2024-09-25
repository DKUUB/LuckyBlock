local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/DKUUB/Orionui/refs/heads/main/README.md')))()

local Window = OrionLib:MakeWindow({Name = "DANGO HUB - ❓ LUCKY BLOCKS Battlegrounds", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})

local Tab = Window:MakeTab({
	Name = "Lucky blocks",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "Lucky block",
	Callback = function()
      		game:GetService("ReplicatedStorage").SpawnLuckyBlock:FireServer()
  	end    
})

Tab:AddButton({
	Name = "Super block",
	Callback = function()
      		game:GetService("ReplicatedStorage").SpawnSuperBlock:FireServer()
  	end    
})

Tab:AddButton({
	Name = "Diamond block",
	Callback = function()
      		game:GetService("ReplicatedStorage").SpawnDiamondBlock:FireServer()
  	end    
})

Tab:AddButton({
	Name = "Rainbow block",
	Callback = function()
      		game:GetService("ReplicatedStorage").SpawnRainbowBlock:FireServer()
  	end    
})

Tab:AddButton({
	Name = "Galaxy block",
	Callback = function()
      		game:GetService("ReplicatedStorage").SpawnGalaxyBlock:FireServer()
  	end    
})

Tab:AddButton({
	Name = "Get all weapons",
	Callback = function()
      		for i = 1, 30 do
game:GetService("ReplicatedStorage").SpawnGalaxyBlock:FireServer()
game:GetService("ReplicatedStorage").SpawnRainbowBlock:FireServer()
game:GetService("ReplicatedStorage").SpawnDiamondBlock:FireServer()
game:GetService("ReplicatedStorage").SpawnSuperBlock:FireServer()
end
  	end    
})

local Tab = Window:MakeTab({
	Name = "PVP",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})


Tab:AddTextbox({
	Name = "Reach sword",
	Default = "input",
	TextDisappear = true,
	Callback = function(Value)
for i,v in pairs(game:GetService'Players'.LocalPlayer.Character:GetChildren()) do
		if v:isA("Tool") then
			local a = Instance.new("SelectionBox",v.Handle)
			v.Handle.Massless = true
			v.Handle.Transparency = 1
			a.Adornee = v.Handle
			v.Handle.Size = Vector3.new(Value, Value, Value)
			local selectionBox = Instance.new("SelectionBox",v.Handle)
			selectionBox.Adornee = v.Handle
			selectionBox.Color3 = Color3.new(0, 0.313725, 0.47451)
		end
	end
	end	  
})

Tab:AddButton({
	Name = "Equip tools",
	Callback = function()
      		loadstring(game:HttpGet("https://pastebin.com/raw/gR4Zki4n"))()
  	end    
})

Tab:AddButton({
	Name = "Drop tools",
	Callback = function()
      		for i,v in pairs(game.Players.LocalPlayer.Backpack:GetDescendants()) do
   if v:IsA("Tool")  then
    wait(0.1)
    v.Parent = game.Players.LocalPlayer.Character
    wait(0.1)
    v.Parent = game.Workspace
end
end
  	end    
})

Tab:AddButton({
	Name = "Multi gear",
	Callback = function()
      		lp = game:GetService("Players").LocalPlayer

game:GetService("UserInputService").InputBegan:Connect(function(key)
	if key.KeyCode == Enum.KeyCode.E then
		for i,tool in pairs(lp.Backpack:GetChildren()) do
			if tool:IsA("Tool") then
				tool.Parent = lp.Character
				tool:Activate()
				task.wait()
				tool.Parent = lp.Backpack
			end
		end
	end
end)
  	end    
})


Tab:AddButton({
	Name = "Keyboard",
	Callback = function()
      		loadstring(game:HttpGet("https://raw.githubusercontent.com/advxzivhsjjdhxhsidifvsh/mobkeyboard/main/main.txt", true))()
  	end    
})

Tab:AddButton({
	Name = "I see you everywhere",
	Callback = function()
      		loadstring(game:HttpGet("https://pastebin.com/raw/daM0ut53"))()
  	end    
})

Tab:AddButton({
	Name = "Endless zoom",
	Callback = function()
      		plr.CameraMaxZoomDistance = 1e99
plr.CameraMinZoomDistance = 0
  	end    
})



Tab:AddButton({
	Name = "Fling punch",
	Callback = function()
      		loadstring(game:HttpGet("https://raw.githubusercontent.com/fedoratums/Base-Script/Base-Script/fedoratum punch fling",true))()
  	end    
})
