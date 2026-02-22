--[[
    ЭТОТ КОД НИКТО НЕ ПОЙМЕТ
    Даже античит сломает мозг
    Портал При1ект стиль
]]

-- Бесполезный мусор для античита
local function mcdonaldscafe() return "i'm lovin it" end
local function googlechrome() return 69.420 end
local function fortniteBattlePass() return "gay" end

-- Еще больше мусора
local a = "абракадабра"
local b = 1337
local c = true
local d = false 
local e = nil
local f = function() return function() return function() return "x" end end end

-- Бессмысленные таблицы
local garbage1 = {["xd"] = 123, ["lol"] = 456, kek = 789}
local garbage2 = {[1] = "wtf", [2] = "omg", [3] = "bbq"}
local garbage3 = {a = 1, b = 2, c = 3, d = 4, e = 5}

-- Мертвый код который ничего не делает
for i = 1, 10 do
    local x = i * 2
    local y = x / 3
    local z = math.floor(y)
    if z > 5 then
        print("этот код бесполезен")
    else
        print("и этот тоже")
    end
end

-- Бессмысленная функция
local function calculatePotato(value)
    local potato = value * 3.14159
    local tomato = potato / 2.71828
    local cucumber = math.sqrt(tomato)
    return string.format("%.2f", cucumber) .. " кг картошки"
end
calculatePotato(1337) -- вызвали просто так

-- НАСТОЯЩИЙ КОД НАЧИНАЕТСЯ ЗДЕСЬ
-- но он перемешан с мусором

local function getService(x) return game:GetService(x) end
local function getPlayers() return getService("Players") end
local function getRunService() return getService("RunService") end
local function getInput() return getService("UserInputService") end
local function getTween() return getService("TweenService") end

-- Случайные переменные для запутывания
local Pl = getPlayers()
local Rns = getRunService()
local Uis = getInput()
local Tw = getTween()
local Cmr = workspace.CurrentCamera
local Lp = Pl.LocalPlayer

-- Бесполезные функции для отвлечения внимания
local function killProcess(id) return id * 0 end
local function encryptData(data) return data .. "хуй" end
local function decodeString(str) return string.reverse(str) end

-- ОСНОВНЫЕ НАСТРОЙКИ (закопаны в мусоре)
local settings = {
    aimbot = true and not false or true,
    esp = true or false and true,
    noclip = false or false or false,
    fly = false,
    speed = 24,
    key = Enum.KeyCode.Q,
    
    -- 🔥 НОВАЯ НАСТРОЙКА ДЛЯ АНТИ-АИМА
    antiAim = {
        enabled = false,
        speed = 5,  -- оборотов в секунду
        direction = 1, -- 1 = по часовой, -1 = против
        spinOffset = 0,
        lastUpdate = 0
    },
    
    -- Бесполезные настройки
    color = Color3.new(1, math.random(), math.random()),
    name = "петух" .. math.random(100, 999),
    id = "idiot_" .. os.time()
}

-- Бессмысленный код для красоты
local function randomMath()
    local a = math.random(1, 100)
    local b = math.random(1, 100)
    local c = a + b
    local d = c * a
    local e = d / b
    return string.char(e % 26 + 97)
end
for i = 1, 5 do randomMath() end

-- Функция определения роли (запутанная)
local function whatRoleIsThisGuy(playerWhomWeChecking)
    if not playerWhomWeChecking then return "dead" end
    if not playerWhomWeChecking.Character then return "no character" end
    
    local backpack = playerWhomWeChecking.Backpack
    if not backpack then return "no backpack" end
    
    -- Проверяем оружие через жопу
    local hasGun = false
    local hasKnife = false
    
    for _, item in pairs(backpack:GetChildren()) do
        if item.Name == "Gun" or item.Name:find("Revolver") or item.Name == "Pistol" then
            hasGun = true
        end
        if item.Name == "Knife" or item.Name:find("Dagger") or item.Name == "Sword" then
            hasKnife = true
        end
    end
    
    if hasGun then return "sheriff" end
    if hasKnife then return "murderer" end
    
    -- Проверяем ауру (для героя)
    if playerWhomWeChecking.Character:FindFirstChild("ForceField") then
        return "hero"
    end
    
    return "innocent"
end

-- Бесполезная функция для отвлечения
local function uselessLoop()
    local counter = 0
    for i = 1, 100 do
        counter = counter + i
        if counter > 1000 then
            break
        end
    end
    return counter
end
uselessLoop()

-- Функция поиска врага (запутанная до невозможности)
local function findEnemyToKill()
    local me = Lp
    local myRole = whatRoleIsThisGuy(me)
    
    if myRole == "innocent" or myRole == "hero" or myRole == "dead" or myRole == "no character" then
        return nil
    end
    
    for _, player in pairs(Pl:GetPlayers()) do
        if player ~= me then
            local hisRole = whatRoleIsThisGuy(player)
            
            if hisRole ~= "dead" and hisRole ~= "no character" and hisRole ~= "no backpack" then
                if myRole == "sheriff" and hisRole == "murderer" then
                    return player
                end
                if myRole == "murderer" and hisRole == "sheriff" then
                    return player
                end
            end
        end
    end
    
    return nil
end

-- 🔥 ФУНКЦИЯ АНТИ-АИМ (круговые обороты)
local function updateAntiAim()
    if not settings.antiAim.enabled then return end
    
    local currentTime = tick()
    local delta = currentTime - settings.antiAim.lastUpdate
    
    -- Рассчитываем угол поворота (360 градусов * обороты в сек * время)
    local angleDelta = 360 * settings.antiAim.speed * delta * settings.antiAim.direction
    settings.antiAim.spinOffset = (settings.antiAim.spinOffset + angleDelta) % 360
    
    -- Применяем поворот камеры
    local currentRot = Cmr.CFrame - Cmr.CFrame.Position
    local spinCF = CFrame.Angles(0, math.rad(angleDelta), 0)
    Cmr.CFrame = CFrame.new(Cmr.CFrame.Position) * (spinCF * currentRot)
    
    settings.antiAim.lastUpdate = currentTime
end

-- 🔥 СОЗДАЕМ GUI ДЛЯ УПРАВЛЕНИЯ АНТИ-АИМОМ
local function createAntiAimGUI()
    local gui = Instance.new("ScreenGui")
    gui.Name = "AntiAimGUI_" .. math.random(1000, 9999)
    gui.Parent = game:GetService("CoreGui")
    
    local frame = Instance.new("Frame")
    frame.Size = UDim2.new(0, 200, 0, 150)
    frame.Position = UDim2.new(0, 10, 0, 350) -- Под основным меню
    frame.BackgroundColor3 = Color3.new(0.1, 0.1, 0.1)
    frame.BackgroundTransparency = 0.2
    frame.BorderSizePixel = 2
    frame.BorderColor3 = Color3.new(1, 0, 0)
    frame.Active = true
    frame.Draggable = true
    frame.Parent = gui
    
    local title = Instance.new("TextLabel")
    title.Size = UDim2.new(1, 0, 0, 25)
    title.Text = "🔄 ANTI-AIM CONTROL"
    title.BackgroundColor3 = Color3.new(0.5, 0, 0)
    title.TextColor3 = Color3.new(1, 1, 1)
    title.Font = Enum.Font.GothamBold
    title.TextSize = 14
    title.Parent = frame
    
    -- Кнопка вкл/выкл
    local toggleBtn = Instance.new("TextButton")
    toggleBtn.Size = UDim2.new(0.9, 0, 0, 30)
    toggleBtn.Position = UDim2.new(0.05, 0, 0, 30)
    toggleBtn.Text = settings.antiAim.enabled and "✅ ВКЛ" or "❌ ВЫКЛ"
    toggleBtn.BackgroundColor3 = settings.antiAim.enabled and Color3.new(0, 0.5, 0) or Color3.new(0.5, 0, 0)
    toggleBtn.TextColor3 = Color3.new(1, 1, 1)
    toggleBtn.Parent = frame
    
    toggleBtn.MouseButton1Click:Connect(function()
        settings.antiAim.enabled = not settings.antiAim.enabled
        toggleBtn.Text = settings.antiAim.enabled and "✅ ВКЛ" or "❌ ВЫКЛ"
        toggleBtn.BackgroundColor3 = settings.antiAim.enabled and Color3.new(0, 0.5, 0) or Color3.new(0.5, 0, 0)
        
        if settings.antiAim.enabled then
            settings.antiAim.lastUpdate = tick()
        end
    end)
    
    -- Ползунок скорости
    local speedLabel = Instance.new("TextLabel")
    speedLabel.Size = UDim2.new(0.4, 0, 0, 20)
    speedLabel.Position = UDim2.new(0.05, 0, 0, 65)
    speedLabel.Text = "Скорость:"
    speedLabel.BackgroundTransparency = 1
    speedLabel.TextColor3 = Color3.new(1, 1, 1)
    speedLabel.TextXAlignment = Enum.TextXAlignment.Left
    speedLabel.Parent = frame
    
    local speedValue = Instance.new("TextLabel")
    speedValue.Size = UDim2.new(0.3, 0, 0, 20)
    speedValue.Position = UDim2.new(0.65, 0, 0, 65)
    speedValue.Text = settings.antiAim.speed .. " об/с"
    speedValue.BackgroundTransparency = 1
    speedValue.TextColor3 = Color3.new(1, 1, 0)
    speedValue.TextXAlignment = Enum.TextXAlignment.Right
    speedValue.Parent = frame
    
    local slider = Instance.new("TextButton")
    slider.Size = UDim2.new(0.9, 0, 0, 20)
    slider.Position = UDim2.new(0.05, 0, 0, 90)
    slider.Text = ""
    slider.BackgroundColor3 = Color3.new(0.3, 0.3, 0.3)
    slider.Parent = frame
    
    local sliderFill = Instance.new("Frame")
    sliderFill.Size = UDim2.new(settings.antiAim.speed / 25, 0, 1, 0) -- Макс 25 об/с
    sliderFill.BackgroundColor3 = Color3.new(1, 0, 0)
    sliderFill.BorderSizePixel = 0
    sliderFill.Parent = slider
    
    -- Обработка ползунка
    local dragging = false
    slider.MouseButton1Down:Connect(function()
        dragging = true
    end)
    
    Uis.InputEnded:Connect(function(input)
        if input.UserInputType == Enum.UserInputType.MouseButton1 then
            dragging = false
        end
    end)
    
    Uis.InputChanged:Connect(function(input)
        if dragging and input.UserInputType == Enum.UserInputType.MouseMovement then
            local mousePos = Uis:GetMouseLocation()
            local sliderPos = slider.AbsolutePosition
            local sliderSize = slider.AbsoluteSize.X
            
            local relativeX = math.clamp(mousePos.X - sliderPos.X, 0, sliderSize)
            local newSpeed = math.floor((relativeX / sliderSize) * 25 * 10) / 10 -- 1 знак после запятой
            
            settings.antiAim.speed = math.clamp(newSpeed, 0.5, 25)
            sliderFill.Size = UDim2.new(settings.antiAim.speed / 25, 0, 1, 0)
            speedValue.Text = settings.antiAim.speed .. " об/с"
        end
    end)
    
    -- Кнопка направления
    local dirBtn = Instance.new("TextButton")
    dirBtn.Size = UDim2.new(0.4, 0, 0, 30)
    dirBtn.Position = UDim2.new(0.05, 0, 0, 115)
    dirBtn.Text = settings.antiAim.direction == 1 and "➡ ПО ЧАСОВОЙ" or "⬅ ПРОТИВ"
    dirBtn.BackgroundColor3 = Color3.new(0.3, 0.3, 0.8)
    dirBtn.TextColor3 = Color3.new(1, 1, 1)
    dirBtn.TextSize = 12
    dirBtn.Parent = frame
    
    dirBtn.MouseButton1Click:Connect(function()
        settings.antiAim.direction = settings.antiAim.direction * -1
        dirBtn.Text = settings.antiAim.direction == 1 and "➡ ПО ЧАСОВОЙ" or "⬅ ПРОТИВ"
    end)
    
    -- Пресеты
    local presets = {
        {name = "МЕДЛЕННО", speed = 2},
        {name = "СРЕДНЕ", speed = 5},
        {name = "БЫСТРО", speed = 10},
        {name = "УГАР", speed = 15},
        {name = "БЕЗУМИЕ", speed = 25}
    }
    
    for i, preset in ipairs(presets) do
        local presetBtn = Instance.new("TextButton")
        presetBtn.Size = UDim2.new(0.16, 0, 0, 20)
        presetBtn.Position = UDim2.new(0.05 + (i-1) * 0.18, 0, 0, 150)
        presetBtn.Text = preset.name:sub(1, 3)
        presetBtn.BackgroundColor3 = Color3.new(0.2, 0.2, 0.2)
        presetBtn.TextColor3 = Color3.new(1, 1, 1)
        presetBtn.TextSize = 10
        presetBtn.Parent = frame
        
        presetBtn.MouseButton1Click:Connect(function()
            settings.antiAim.speed = preset.speed
            sliderFill.Size = UDim2.new(settings.antiAim.speed / 25, 0, 1, 0)
            speedValue.Text = settings.antiAim.speed .. " об/с"
        end)
    end
end

-- ESP с мусором
Rns.RenderStepped:Connect(function(deltaTime)
    -- Бесполезный код для отвлечения
    local useless = deltaTime * 1000
    local moreUseless = useless / 2
    
    -- 🔥 Обновляем анти-аим
    updateAntiAim()
    
    if settings.esp then
        for _, player in pairs(Pl:GetPlayers()) do
            if player ~= Lp and player.Character then
                local role = whatRoleIsThisGuy(player)
                local color = Color3.new(1, 1, 1)
                
                if role == "murderer" then
                    color = Color3.new(1, 0, 0) -- красный
                elseif role == "sheriff" then
                    color = Color3.new(0, 0, 1) -- синий
                elseif role == "hero" then
                    color = Color3.new(1, 1, 0) -- желтый
                else
                    color = Color3.new(0, 1, 0) -- зеленый
                end
                
                -- Проверяем есть ли хайлайт
                local hl = player.Character:FindFirstChild("ESP_HL_" .. math.random(1,999))
                if not hl then
                    hl = Instance.new("Highlight")
                    hl.Name = "ESP_HL_" .. os.time() .. "_" .. math.random(1,9999)
                    hl.Parent = player.Character
                end
                
                hl.FillColor = color
                hl.OutlineColor = Color3.new(1, 1, 1)
                hl.FillTransparency = 0.3
            end
        end
    end
end)

-- Aim с мусором
Uis.InputBegan:Connect(function(input, processed)
    if processed then return end
    
    -- Бессмысленная проверка
    local x = math.random()
    local y = math.random()
    if x + y > 1.5 then
        print("рандомное число больше 1.5, но это ничего не значит")
    end
    
    if input.KeyCode == settings.key and settings.aimbot then
        local enemy = findEnemyToKill()
        if enemy and enemy.Character and enemy.Character:FindFirstChild("Head") then
            local head = enemy.Character.Head
            Cmr.CFrame = CFrame.new(Cmr.CFrame.Position, head.Position)
        end
    end
end)

-- NoClip (с мусором)
Rns.Stepped:Connect(function(time, step)
    -- Бесполезные вычисления
    local fakeTime = time * 100
    local fakeStep = step * 100
    
    if settings.noclip and Lp.Character then
        for _, part in pairs(Lp.Character:GetChildren()) do
            if part:IsA("BasePart") then
                part.CanCollide = false
            end
        end
    end
end)

-- Fly (запутанный)
local flyActive = false
local flyBV = nil

Uis.InputBegan:Connect(function(input)
    if settings.fly then
        if input.KeyCode == Enum.KeyCode.Space then
            if Lp.Character then
                local root = Lp.Character:FindFirstChild("HumanoidRootPart")
                if root then
                    if not flyBV then
                        flyBV = Instance.new("BodyVelocity")
                        flyBV.MaxForce = Vector3.new(10000, 10000, 10000)
                        flyBV.Parent = root
                    end
                    flyBV.Velocity = Vector3.new(0, 50, 0)
                end
            end
        elseif input.KeyCode == Enum.KeyCode.LeftControl then
            if Lp.Character then
                local root = Lp.Character:FindFirstChild("HumanoidRootPart")
                if root then
                    if not flyBV then
                        flyBV = Instance.new("BodyVelocity")
                        flyBV.MaxForce = Vector3.new(10000, 10000, 10000)
                        flyBV.Parent = root
                    end
                    flyBV.Velocity = Vector3.new(0, -50, 0)
                end
            end
        end
    end
end)

Uis.InputEnded:Connect(function(input)
    if settings.fly then
        if input.KeyCode == Enum.KeyCode.Space or input.KeyCode == Enum.KeyCode.LeftControl then
            if flyBV then
                flyBV:Destroy()
                flyBV = nil
            end
        end
    end
end)

-- Speed (с мусором)
Rns.Heartbeat:Connect(function()
    -- Бесполезный код
    local array = {}
    for i = 1, 10 do
        table.insert(array, i * math.random())
    end
    
    if settings.speed and Lp.Character then
        local hum = Lp.Character:FindFirstChild("Humanoid")
        if hum then
            hum.WalkSpeed = settings.speed
        end
    end
end)

-- Создаем GUI для анти-аима
createAntiAimGUI()

-- Финальный мусор
local function finalUselessFunction()
    local str = ""
    for i = 1, 10 do
        str = str .. string.char(math.random(97, 122))
    end
    return str
end
print("скрипт загружен: " .. finalUselessFunction())

-- Бессмысленный комментарий 
-- TODO: пофиксить баг с вылетом (никогда не пофикшу)

-- Еще комментарий
-- Античит иди нахуй читай этот код

-- И еще один
-- Если ты это читаешь, античит, то знай - ты пидор

print("✅ PortaLPr1ject загружен (надеюсь античит ничего не понял)")
print("🔄 Anti-Aim: регулировка скорости в новом меню!")
