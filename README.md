local blur = Instance.new('BlurEffect', game:GetService('Lighting'))
local ScriptWare = Instance.new('ScreenGui')
local Image = Instance.new('ImageLabel')
local Version = Instance.new('TextLabel')
ScriptWare.Name = 'Script Ware'
ScriptWare.Parent = game:GetService('CoreGui')
ScriptWare.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
Image.Name = 'Image'
Image.Parent = ScriptWare
Image.BackgroundColor3 = Color3.new(1, 1, 1)
Image.BackgroundTransparency = 1
Image.Position = UDim2.new(0.424242437, 0, 0.350417167, 0)
Image.Size = UDim2.new(0, 250, 0, 250)
Image.Image = 'rbxassetid://13063541789'
Image.ImageTransparency = 1
Version.Name = "Version"
Version.Parent = ScriptWare
Version.BackgroundColor3 = Color3.new(1, 1, 1)
Version.BackgroundTransparency = 1
Version.Position = UDim2.new(0.941818178, 0, 0.00834326539, 0)
Version.Size = UDim2.new(0, 89, 0, 12)
Version.Font = Enum.Font.Code
Version.Text = "version - v2"
Version.TextColor3 = Color3.new(0.239216, 0.239216, 0.239216)
Version.TextSize = 14
Version.TextTransparency = 1
Version.TextXAlignment = Enum.TextXAlignment.Right
local ts = game:GetService('TweenService')
local ti = TweenInfo.new(2, Enum.EasingStyle.Quint, Enum.EasingDirection.InOut, 0, false, 0)
local blurStart = ts:Create(blur, ti, {Size = 24})
local blurEnd = ts:Create(blur, ti, {Size = 0})
local imageStart = ts:Create(Image, ti, {ImageTransparency = 0})
local imageEnd = ts:Create(Image, ti, {ImageTransparency = 1})
local versionStart = ts:Create(Version, ti, {TextTransparency = 0})
local versionEnd = ts:Create(Version, ti, {TextTransparency = 1})

blur.Size = 0
blurStart:Play()
versionStart:Play()
wait(1)
imageStart:Play()
wait(2)
imageEnd:Play()
wait(1)
blurEnd:Play()
versionEnd:Play()
wait(2)
blur:Destroy()
ScriptWare:Destroy()
