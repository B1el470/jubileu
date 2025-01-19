local noob = workspace:FindFirstChild("Noob")
local trash = workspace:FindFirstChild("Model"):FindFirstChild("Trash")

if noob and trash then
    local rightArm = noob:FindFirstChild("Right Arm")
    if rightArm then
        trash.CFrame = rightArm.CFrame * CFrame.new(0, -rightArm.Size.Y / 2, 0)
        trash.Parent = rightArm
    else
        warn("Right Arm not found")
    end
else
    warn("Noob or Trash not found")
end
