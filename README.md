ScreenGui = Instance.new("ScreenGui")
Skid = Instance.new("Frame")
Input = Instance.new("TextBox")
Execute = Instance.new("TextButton")
Clear = Instance.new("TextButton")
Name = Instance.new("TextLabel")
 
ScreenGui.Parent = game.CoreGui
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
 
Skid.Name = "Skid"
Skid.Parent = ScreenGui
Skid.BackgroundColor3 = Color3.new(0, 0.666667, 1)
Skid.BackgroundTransparency = 0.60000002384186
Skid.Position = UDim2.new(0.261363626, 0, 0.615537822, 0)
Skid.Size = UDim2.new(0, 435, 0, 133)
 
Input.Name = "Input"
Input.Parent = Skid
Input.BackgroundColor3 = Color3.new(0, 0, 0)
Input.BackgroundTransparency = 0.40000000596046
Input.Position = UDim2.new(0, 0, 0.165413529, 0)
Input.Size = UDim2.new(0, 435, 0, 61)
Input.Font = Enum.Font.Fantasy
Input.FontSize = Enum.FontSize.Size24
Input.Text = "Paste your require here."
Input.TextColor3 = Color3.new(1, 1, 1)
Input.TextSize = 23
Input.TextWrapped = true
 
Execute.Name = "Execute"
Execute.Parent = Skid
Execute.BackgroundColor3 = Color3.new(0, 0, 0)
Execute.BackgroundTransparency = 0.69999998807907
Execute.Position = UDim2.new(-0.000705341925, 0, 0.622981727, 0)
Execute.Size = UDim2.new(0, 223, 0, 50)
Execute.Font = Enum.Font.SciFi
Execute.FontSize = Enum.FontSize.Size14
Execute.Text = "Execute"
Execute.TextColor3 = Color3.new(0, 0, 0)
Execute.TextScaled = true
Execute.TextSize = 14
Execute.TextWrapped = true
 
Clear.Name = "Clear"
Clear.Parent = Skid
Clear.BackgroundColor3 = Color3.new(0, 0, 0)
Clear.BackgroundTransparency = 0.69999998807907
Clear.Position = UDim2.new(0.513270557, 0, 0.622981727, 0)
Clear.Size = UDim2.new(0, 211, 0, 50)
Clear.Font = Enum.Font.SciFi
Clear.FontSize = Enum.FontSize.Size14
Clear.Text = "Clear"
Clear.TextColor3 = Color3.new(0, 0, 0)
Clear.TextScaled = true
Clear.TextSize = 14
Clear.TextWrapped = true
 
Name.Name = "Name"
Name.Parent = Skid
Name.BackgroundColor3 = Color3.new(1, 1, 1)
Name.BackgroundTransparency = 1
Name.Size = UDim2.new(0, 434, 0, 22)
Name.Font = Enum.Font.Fantasy
Name.FontSize = Enum.FontSize.Size14
Name.Text = "ZacX ServerSide Executor v1.0"
Name.TextColor3 = Color3.new(0, 0, 0)
Name.TextScaled = true
Name.TextSize = 14
Name.TextWrapped = true
 
Execute.MouseButtonClick:connect(function()
    game.ReplicatedStorage.RemoteEvent:FireServer(Input.Text)
end)
