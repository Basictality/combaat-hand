local USERNAME = game.Players.LocalPlayer.Name
local RunService = Game:GetService("RunService")

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

HeadDown(workspace[USERNAME].Torso['Left Shoulder'], math.rad(-15.5), 15, 2 / 3)

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

HeadDown(workspace[USERNAME].Torso['Right Shoulder'], math.rad(-15.5), 15, 2 / 3)

------------
while true do wait()
	size = "1"
	trans = "0.7"
	mat = "Neon"
	color = "Crimson"
	x = game.Players.LocalPlayer.Character
b=Instance.new("Part",x)
b.FormFactor = "Custom"
b.Size = Vector3.new(size,size,size)
b.Transparency=trans
b.Anchored = true
b.Material = mat
b.CanCollide = false
b.BrickColor = BrickColor.new(color)

z=Instance.new("Part",b)
z.FormFactor = "Custom"
z.Material = mat
z.Size = Vector3.new(size,size,size)
z.Transparency=trans
z.Anchored = true
z.CanCollide = false
z.BrickColor = BrickColor.new(color)
game.Debris:AddItem(b,1)
game.Debris:AddItem(z,1)



	z.CFrame = x['Right Arm'].CFrame * CFrame.new(0,-1,0) * CFrame.Angles(math.random(),math.random(),math.random())
	b.CFrame = x['Left Arm'].CFrame * CFrame.new(0,-1,0) * CFrame.Angles(math.random(),math.random(),math.random())
end
