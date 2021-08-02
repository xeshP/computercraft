params = {...}
local modem = peripheral.wrap("right")
datacount = 0
list = {}

if params[1] == nil then
    for slot = 1, 16 do
    turtle.select(slot)
    data = turtle.getItemDetail()
    icount = turtle.getItemCount()
    if data then
        datacount = (datacount + 1)
        dats = "[i]"..slot.."|"..data.name.."|"..icount
        table.insert(list, dats)
        end
    end
    modem.transmit(1337, 1336, datacount)
    for row = 1, #list do
        print(list[row])
        modem.transmit(1337, 1336, list[row])
        end    
else
    numb = tonumber (params[1])
    turtle.select(numb)
    data = turtle.getItemDetail()
    icount = turtle.getItemCount()
    if data then
        datacount = (datacount + 1)
        dats = "[i]"..numb.."|"..data.name.."|"..icount
        print(dats)
        modem.transmit(1337, 1336, datacount)
        modem.transmit(1337, 1336, dats)
        else
            modem.transmit(1337, 1336, "0")
        end
    end
    
