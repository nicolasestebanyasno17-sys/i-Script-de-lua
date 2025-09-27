-- Tabla de keys válidas
local validKeys = {
    ["542d6626f0d52f4ca1e3112b288dc5c1"] = true, -- Puedes agregar más keys aquí
}

-- Comando para ingresar la key
RegisterCommand("verificar", function(source, args, rawCommand)
    local key = args[1]
    if not key then
        TriggerClientEvent('chat:addMessage', source, {
            args = { 'Sistema', 'Usa: /verificar TU_KEY' }
        })
        return
    end

    if validKeys[key] then
        -- Si la key es válida, da el link a Google (o a donde quieras)
        TriggerClientEvent('chat:addMessage', source, {
            args = { 'Sistema', 'Key válida! Ve a este link: https://www.google.com/' }
        })
        -- Después de 10 segundos, da el link de tu server
        Citizen.SetTimeout(10000, function()
            TriggerClientEvent('chat:addMessage', source, {
                args = { 'Sistema', 'Ahora puedes entrar a tu servidor: fivem://tuip:tuport' }
            })
        end)
    else
        -- Si la key es inválida
        TriggerClientEvent('chat:addMessage', source, {
            args = { 'Sistema', 'Key inválida! Solicita tu key en Discord.' }
        })
    end
end, false)
