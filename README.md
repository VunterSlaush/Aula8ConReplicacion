# Aula8ConReplicacion
Pizarra con replicacion de audio y trazos / lineas 


#Requerimientos para su uso

1.- Servidor de nodeJS corriendo en el puerto 1234 
    si se desea cambiar el puerto, en la clase Servidor de la app cambien la constante PUERTO
    
2.- Estas Lineas de Codigo en el codigo de su servidor

    client.on('send_audio', function(data)
    {
        client.broadcast.emit('get_audio', data);
        console.log('recibiendo audio');
    });
    client.on("pintar", function(data)
    {
        client.broadcast.emit("pintar",data);
        console.log(data);
    });

    client.on("borrar todo", function()
    {
        client.broadcast.emit("borrar todo");
        console.log("Borrar todo");
    });
