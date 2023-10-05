
_G.AutoFarmFast = value
        Type = 0

        spawn(function()  
            while task.wait() do
                pcall(function()
                if _G.Auto_Farm_Level then
                    local MyLevel = game.Players.LocalPlayer.Data.Level.Value
                    local QuestC = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest
                    if _G.AutoFarmFast and (MyLevel >= 10 and MyLevel <= 300) then
                      if MyLevel >= 10 and MyLevel <= 69 then
                        CFrameMon = CFrame.new(-4716.95703, 853.089722, -1933.92542, -0.93441087, -6.77488776e-09, -0.356197298, 1.12145182e-08, 1, -4.84390199e-08, 0.356197298, -4.92565206e-08, -0.93441087)
                        BringMobFarm = false
                        for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
                            if v.Name == "God's Guard [Lv. 450]" then
                                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                    repeat task.wait()
                                        EquipWeapon(_G.SelectWeapon)
                                        getgenv().noclip = true
                                        _G.AutoFarmLv = false
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid.WalkSpeed = 0
                                        v.Head.CanCollide = false
                                        BringMobFarm = true
                                        PosMon = v.HumanoidRootPart.CFrame
                                        v.HumanoidRootPart.Size = Vector3.new(100,100,100)
                                        v.HumanoidRootPart.Transparency = 1
                                        spawn(function()
                                                        while wait(.1) do
                                                            if Type == 1 then
                                                                getgenv().ToTarget(v.HumanoidRootPart.CFrame *CFrame.new(0,20,0))
                                                            elseif Type == 2 then
                                                                getgenv().ToTarget(v.HumanoidRootPart.CFrame *CFrame.new(0,20,-40))
                                                            elseif Type == 3 then
                                                                getgenv().ToTarget(v.HumanoidRootPart.CFrame *CFrame.new(40,20,0))
                                                            elseif Type == 4 then
                                                                getgenv().ToTarget(v.HumanoidRootPart.CFrame *CFrame.new(0,20,40))
                                                            elseif Type == 5 then
                                                                getgenv().ToTarget(v.HumanoidRootPart.CFrame *CFrame.new(-40,20,0))
                                                            elseif Type == 6 then
                                                                getgenv().ToTarget(v.HumanoidRootPart.CFrame *CFrame.new(0,20,0))
                                                            end
                                                        end
                                                    end)
                                        game:GetService'VirtualUser':CaptureController()
                                        game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                    until not _G.Auto_Farm_Level  or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        end
                        for i,v in pairs(game:GetService("ReplicatedStorage"):GetChildren()) do 
                            if v.Name == "God's Guard [Lv. 450]" then
                                getgenv().ToTarget(v.HumanoidRootPart.CFrame * CFrame.new(0,35,5))
                             else
                                 _G.AutoFarmLv = false
                                 BringMobFarm = false
                                 getgenv().noclip = false
                                CFrameMon = CFrame.new(-4716.95703, 853.089722, -1933.92542, -0.93441087, -6.77488776e-09, -0.356197298, 1.12145182e-08, 1, -4.84390199e-08, 0.356197298, -4.92565206e-08, -0.93441087)
                                getgenv().ToTarget(CFrameMon)
                                if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-4607.82275, 872.54248, -1667.55688))
                                    end
                                end
                           end
                        elseif MyLevel >= 70 and MyLevel <= 310 then
                            if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
                             end
                            if QuestC.Visible == false then
                            CFrameMon = CFrame.new(-4716.95703, 853.089722, -1933.92542, -0.93441087, -6.77488776e-09, -0.356197298, 1.12145182e-08, 1, -4.84390199e-08, 0.356197298, -4.92565206e-08, -0.93441087)
                             BringMobFarm = false
                             for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
                                 if v.Name == "God's Guard [Lv. 450]" then
                                     if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                         repeat task.wait()
                                             EquipWeapon(_G.SelectWeapon)
                                             getgenv().noclip = true
                                             _G.AutoFarmLv = true
                                             v.HumanoidRootPart.CanCollide = false
                                             v.Humanoid.WalkSpeed = 0
                                             v.Head.CanCollide = false
                                             v.HumanoidRootPart.Size = Vector3.new(100,100,100)
                                             v.HumanoidRootPart.Transparency = 1
                                             BringMobFarm = true
                                             PosMon = v.HumanoidRootPart.CFrame
         spawn(function()
            if RandomCFrame <= 1 then
                topos(v.HumanoidRootPart.CFrame * CFrame.new(0,20,50))
                RandomCFrame = RandomCFrame + 0.1
            elseif RandomCFrame >= 1 and RandomCFrame <= 2 then
                topos(v.HumanoidRootPart.CFrame * CFrame.new(50,20,0))
                RandomCFrame = RandomCFrame + 0.1
            elseif RandomCFrame >= 2 and RandomCFrame <= 3 then
                topos(v.HumanoidRootPart.CFrame *CFrame.new(0,20,-50))
                RandomCFrame = RandomCFrame + 0.1
            elseif RandomCFrame >= 3 and RandomCFrame <= 4  then
                topos(v.HumanoidRootPart.CFrame * CFrame.new(-50,20,0))
                RandomCFrame = RandomCFrame + 0.1
            elseif RandomCFrame >=4 and RandomCFrame <= 5 then
                topos(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                RandomCFrame = 0
            end
        end)
                                             game:GetService'VirtualUser':CaptureController()
                                             game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                         until not _G.Auto_Farm_Level  or not v.Parent or v.Humanoid.Health <= 0
                                     end
                                 end
                             end
                             for i,v in pairs(game:GetService("ReplicatedStorage"):GetChildren()) do 
                                 if v.Name == "God's Guard [Lv. 450]" then
                                     getgenv().ToTarget(v.HumanoidRootPart.CFrame * CFrame.new(0,35,5))
                                  else
                                      _G.AutoFarmLv = true
                                      BringMobFarm = false
                                      getgenv().noclip = false
                                     CFrameMon = CFrame.new(-4716.95703, 853.089722, -1933.92542, -0.93441087, -6.77488776e-09, -0.356197298, 1.12145182e-08, 1, -4.84390199e-08, 0.356197298, -4.92565206e-08, -0.93441087)
                                     getgenv().ToTarget(CFrameMon)
                                     if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
                                             game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-4607.82275, 872.54248, -1667.55688))
                                         end
                                     end
                                end
                           elseif QuestC.Visible == true then
                             _G.FastAttack = false
                             _G.FastAttackForKonMaimeFan = true
                             local quest = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text
                             local Player = string.split(quest," ")[2]
                              getgenv().SelectPly = string.split(quest," ")[2]
                              if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                                 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
                                 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
                                 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
                                 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
                                 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
                                 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
                             end
                              if string.find(quest,"Defeat") then
                                 repeat task.wait()
                                   if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                         game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                     end
                                     game:GetService("Players").LocalPlayer.PlayerGui.Main.InCombat.Visible = false
                                     game:GetService("Players").LocalPlayer.PlayerGui.Main.SafeZone.Visible = false
                                     if game:GetService("Players").LocalPlayer.PlayerGui.Main.PvpDisabled.Visible == true then
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EnablePvp")
                                    end
                                      EquipWeapon(_G.SelectWeapon)
                                      TPPlayer(game:GetService("Players")[getgenv().SelectPly].Character.HumanoidRootPart.CFrame*CFrame.new(0,0,5))
                                      game:GetService("VirtualUser"):CaptureController()
                                      game:GetService("VirtualUser"):Button1Down(Vector2.new(1280,672))
                                      game.Players:FindFirstChild(Player).Character.HumanoidRootPart.Size = Vector3.new(120,120,120)
                                      game:service('VirtualInputManager'):SendKeyEvent(true, "Z", false, game)
                                      game:service('VirtualInputManager'):SendKeyEvent(false, "Z", false, game)
                                      game:service('VirtualInputManager'):SendKeyEvent(true, "X", false, game)
                                      game:service('VirtualInputManager'):SendKeyEvent(false, "X", false, game)
                                 until game.Players:FindFirstChild(Player).Character.Humanoid.Health <= 0 or not game.Players:FindFirstChild(Player) or not FastFarm()
                                     if not game.Players:FindFirstChild(Player) then
                                         game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
                                     end   
                                else
                                     game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
                              end
                        end
                        elseif MyLevel >= 300 and MyLevel <= 2450 then
                     if QuestC.Visible == false then
                        _G.AutoFarmLv = true
                    else
                            _G.AutoFarmLv = true
                            end
                     else
                        _G.AutoFarmLv = true
                       end
                  end
                 if _G.AutoFarmLv then
                        CheckQuest()
                        if QuestC.Visible == false then
                            CheckQuest()
                            repeat wait() getgenv().ToTarget(CFrameMon) until (CFrameMon.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 30000 or not _G.Auto_Farm_Level
                            if (CFrameMon.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 30000 then
                                wait(.2)
                                BringMobFarm = false
                                getgenv().noclip = false
                                wait(.2)
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,LevelQuest)
                                wait(0.5)
                                getgenv().ToTarget(CFrameMon)
                            end
                        elseif QuestC.Visible == true then
                            CheckQuest()
                            if game:GetService("Workspace").Enemies:FindFirstChild(Mon) then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                        if v.Name == Mon then
                                            if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) then
                                                repeat game.RunService.Heartbeat:wait()
                                                    EquipWeapon(_G.SelectWeapon)
                                                    getgenv().noclip = true
                spawn(function()
            if RandomCFrame <= 1 then
                topos(v.HumanoidRootPart.CFrame * CFrame.new(0,20,50))
                RandomCFrame = RandomCFrame + 0.1
            elseif RandomCFrame >= 1 and RandomCFrame <= 2 then
                topos(v.HumanoidRootPart.CFrame * CFrame.new(50,20,0))
                RandomCFrame = RandomCFrame + 0.1
            elseif RandomCFrame >= 2 and RandomCFrame <= 3 then
                topos(v.HumanoidRootPart.CFrame *CFrame.new(0,20,-50))
                RandomCFrame = RandomCFrame + 0.1
            elseif RandomCFrame >= 3 and RandomCFrame <= 4  then
                topos(v.HumanoidRootPart.CFrame * CFrame.new(-50,20,0))
                RandomCFrame = RandomCFrame + 0.1
            elseif RandomCFrame >=4 and RandomCFrame <= 5 then
                topos(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                RandomCFrame = 0
            end
        end)
                                                    v.HumanoidRootPart.CanCollide = false
                                                    PosMon = v.HumanoidRootPart.CFrame
                                                    v.Humanoid.WalkSpeed = 20
                                                    v.Head.CanCollide = false
                                                    _G.FastAttackForKonMaimeFan = false
                                                    _G.FastAttack = true
                                                    BringMobFarm = true
                                                    CheckMon = false
                                                    v.HumanoidRootPart.Size = Vector3.new(100,100,100)
                                                    v.HumanoidRootPart.Transparency = 1
                                                    game:GetService'VirtualUser':CaptureController()
                                                    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                until not _G.Auto_Farm_Level or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                            else
                                                CheckQuest()
                                                getgenv().ToTarget(CFrameMon)
                                            end
                                        end
                                        if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                                        end
                                    end
                                end
                            else
                                BringMobFarm = false
                                getgenv().noclip = false
                                if game:GetService("ReplicatedStorage"):FindFirstChild(Mon) then
                                    getgenv().ToTarget(game:GetService("ReplicatedStorage"):FindFirstChild(Mon).HumanoidRootPart.CFrame * CFrame.new(5,10,7))
                                       else
                                             getgenv().ToTarget(CFrameMon)
                                             getgenv().noclip = false
                                            end
                                       end
                                  end
                             end
                        end
                   end)
             end
         end)

         Type = 1
        spawn(function()
            while wait(.1) do
                Type = 1
                wait(5)
                Type = 2
                wait(5)
                Type = 3
                wait(5)
                Type = 4
                wait(5)
                Type = 5
                wait(5)
            end
        end)
       
         spawn(function()
            while task.wait() do
            if _G.Auto_Farm_Level then
            function UseCode(Text)
                        game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer(Text)
                    end
                UseCode("Enyo_is_Pro")
                UseCode("Magicbus")
                UseCode("JCWK")
                UseCode("Starcodeheo")
                UseCode("Bluxxy")
                UseCode("fudd10_v2")
                UseCode("3BVISITS")
                UseCode("UPD16")
                UseCode("FUDD10")
                UseCode("BIGNEWS")
                UseCode("Sub2OfficialNoobie")
                UseCode("SUB2GAMERROBOT_EXP1")
                UseCode("StrawHatMaine")
                UseCode("SUB2NOOBMASTER123")
                UseCode("Sub2Daigrock")
                UseCode("Axiore")
                UseCode("TantaiGaming")
                UseCode("STRAWHATMAINE")
                UseCode("kittgaming")
                UseCode("Magicbus")
                UseCode("JCWK")
                UseCode("Starcodeheo")
                UseCode("Bluxxy")
                UseCode("fudd10_v2")
                UseCode("Enyu_is_Pro")
                UseCode("Sub2Fer999")
                UseCode("THEGREATACE")
                UseCode("SUB2GAMERROBOT_EXP1")
                UseCode("Sub2OfficialNoobie")
                UseCode("StrawHatMaine")
                UseCode("SUB2NOOBMASTER123")
                UseCode("Sub2Daigrock")
                UseCode("Axiore")
                UseCode("TantaiGaming")
                UseCode("STRAWHATMAINE")
                UseCode("JCWK")
                UseCode("Sub2Fer999")
                UseCode("Magicbus")
                UseCode("Starcodeheo")
                UseCode("Bluxxy")
                UseCode("Sub2Fer999")
                UseCode("GAMERROBOT_YT")
                    end
                end
            end)
