--------looks
was=game.Players.LocalPlayer.Character
was.Humanoid.MaxHealth = "9e999"
print'Bas destroy! v[1] build[2]'
was.Head.Transparency = "1"
Head=Instance.new("Part",was)
Head.Name = "ExtraHead"
Head.Transparency="0"
Head.FormFactor = was.Head.FormFactor
Head.Size = was.Head.Size
Head.Color = was.Head.Color
meshhead=Instance.new("SpecialMesh",Head)
meshhead.Scale = was.Head.Mesh.Scale

weldHead=Instance.new("Weld",Head)
weldHead.Part0=was.Head
weldHead.Part1=Head

-----laser holder----
laserpocket = Instance.new('Part',was['Right Arm'])
laserpocket.Material = "SmoothPlastic"
laserpocket.FormFactor = "Custom"
laserpocket.Size = Vector3.new(0.5,0.7,0.7)
laserpocket.CanCollide = false

laserpocket1 = Instance.new('Part',laserpocket)
laserpocket1.Material = "SmoothPlastic"
laserpocket1.FormFactor = "Custom"
laserpocket1.Size = Vector3.new(.1,.1,.3)
laserpocket1.Color = Color3.new(0,0,0)
laserpocket1.CanCollide = false

laserpweld=Instance.new('Weld',laserpocket)
laserpweld.Part0=laserpocket
laserpweld.Part1=was['Right Arm']
laserpweld.C0=CFrame.new(-0.6,0,0)

laserpweld1=Instance.new('Weld',laserpocket)
laserpweld1.Part0=laserpocket
laserpweld1.Part1=laserpocket1
laserpweld1.C0=CFrame.new(0.1,-0.3,0)
---animations
local USERNAME = game.Players.LocalPlayer.Name
local RunService = Game:GetService("RunService")

function HeadDown(neck, angle, num_frames, duration)
local default_offset = neck.C0
for frame_index = 1, num_frames do
neck.C0 = default_offset * CFrame.Angles(frame_index / num_frames * angle, 0, 0)
RunService.Stepped:wait()
end
Wait()
for frame_index = 1, num_frames do
RunService.Stepped:wait()
end
end

HeadDown(workspace[USERNAME].Torso['Left Hip'], math.rad(-10.5), 15, 2 / 3)

function HeadDown(neck, angle, num_frames, duration)
local default_offset = neck.C0
for frame_index = 1, num_frames do
neck.C0 = default_offset * CFrame.Angles(frame_index / num_frames * angle, 0, 0)
RunService.Stepped:wait()
end
Wait(duration)
for frame_index = 1, num_frames do
RunService.Stepped:wait()
end
end

HeadDown(workspace[USERNAME].Torso['Right Hip'], math.rad(-10.5), 15, 2 / 3)

local armweld = Instance.new("Weld",was)
armweld.Part0=was.Torso
armweld.Part1=was['Left Arm']
armweld.C0=CFrame.new(-1.5,0,0) * CFrame.Angles(-0.3,0.1,-0.3)

local armweld1 = Instance.new("Weld",was)
armweld1.Part0=was.Torso
armweld1.Part1=was['Right Arm']
armweld1.C0=CFrame.new(1.5,0,0) * CFrame.Angles(-0.3,0.1,0.3)

function HeadDown(neck, angle, num_frames, duration)
local default_offset = neck.C0
for frame_index = 1, num_frames do
neck.C0 = default_offset * CFrame.Angles(frame_index / num_frames * angle, 0, 0)
RunService.Stepped:wait()
end
Wait()
for frame_index = 1, num_frames do
RunService.Stepped:wait()
end
end
------------
was=game.Players.LocalPlayer.Character
p=game.Players.LocalPlayer
c=p.Character
m=p:GetMouse()
Player = game:GetService("Players").LocalPlayer
mouse=Player:GetMouse()
Cha = Player.Character
mouse.KeyDown:connect(function(key)
key:lower()
if key == "e" then
blast=Instance.new("Part",was)
blast.Anchored = true
blast.BrickColor = BrickColor.new'Really red'
blast.CFrame = was.Torso.CFrame * CFrame.new(0,-3,0)
blastmesh=Instance.new("SpecialMesh",blast)
blastmesh.MeshType = "FileMesh"
blastmesh.MeshId = "http://www.roblox.com/asset/?id=20329976"
blastmesh.Scale = Vector3.new(3,1,3)
wasound = Instance.new("Sound",was)
wasound.SoundId = "http://www.roblox.com/asset/?id=159504677"
wasound.Pitch = 1
wasound.Volume = 1
wasound.Looped = false
wasound:Play()
was.Torso.Anchored = true
wait()
was.Torso.CFrame = was.Torso.CFrame + was.Torso.CFrame.lookVector * 10
was.Torso.Anchored = false
game.Debris:AddItem(blast,1)
end
end)

was=game.Players.LocalPlayer.Character
p=game.Players.LocalPlayer
c=p.Character
m=p:GetMouse()
Player = game:GetService("Players").LocalPlayer
mouse=Player:GetMouse()
Cha = Player.Character
mouse.KeyDown:connect(function(key)
key:lower()
if key == "t" then
v = game.Players.LocalPlayer
me = v.Character
w=Instance.new('Weld',me)
w.Part0=me.Torso
w.Part1=me['Left Arm']
w.C0=CFrame.new(-1.5,0.5,-0.5) * CFrame.Angles(1.5,0,-0.3)

w1=Instance.new('Weld',me)
w1.Part0=me.Torso
w1.Part1=me['Right Arm']
w1.C0=CFrame.new(1.5,0.5,-0.5) * CFrame.Angles(1.5,0,0.3)

pa2=Instance.new('Part',workspace)
pa2.Anchored = true
pa2.CFrame = me.Torso.CFrame * CFrame.new(0,0,-20)
pa2.Shape = "Ball"
pa2.CanCollide = false
pa2.Color = Color3.new(0,0,0)
pa2.Material = "SmoothPlastic"
game.Debris:AddItem(pa2,3)
			delay(3, function()
			for itrt = 0, 1, 0.1 do
				pa2.Transparency = itrt
				wait()
			end
			end)
			

function onTouched(part)		
	if part.Parent:FindFirstChild("Humanoid")~= nil then
		part.Parent:BreakJoints()
	end
end

pa2.Touched:connect(onTouched)
	

for iew = 3,500 do wait()
	pa2.Size = Vector3.new(iew,iew,iew)
	pa2.CFrame = me.Torso.CFrame * CFrame.new(0,0,-iew)
end
end
end)
