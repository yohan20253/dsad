local Players = game:GetService("Players")

-- IDs das Gamepasses que você deseja simular (esses são exemplos genéricos)
local fakeGamepasses = {
	["Premium"] = true,
	["VIP"] = true,
	["UnicornPack"] = true,
	["HorsePack"] = true,
	["VehiclePack"] = true,
	["WeaponsPack"] = true,
	["MusicPlayer"] = true,
	["FlyingAbility"] = true,
	["AdminPack"] = true,
}

Players.PlayerAdded:Connect(function(player)
	-- Simula que o jogador possui todas as gamepasses listadas
	player:SetAttribute("HasAllGamepasses", true)

	for gamepassName, _ in pairs(fakeGamepasses) do
		player:SetAttribute("HasGamepass_" .. gamepassName, true)
	end
end)
# dsad
