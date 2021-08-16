---
description: Un mailslot es un pseudoarchivo que reside en memoria y se usan funciones de archivo estándar para acceder a él.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: Acerca de Mailslots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d009b2e667e5feebedeb4b842fc3f6e1630b39069e717ce08f5d0441ebe25aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756523"
---
# <a name="about-mailslots"></a>Acerca de Mailslots

Un mailslot es un pseudoarchivo que reside en memoria y se usan funciones de archivo estándar para acceder a él. Los datos de un mensaje mailslot pueden tener cualquier formato, pero no pueden tener más de 424 bytes cuando se envían entre equipos. A diferencia de los archivos de disco, los mailslots son temporales. Cuando se cierran todos los identificadores de un mailslot, se eliminan el mailslot y todos los datos que contiene.

Un *servidor mailslot* es un proceso que crea y posee un mailslot. Cuando el servidor crea un mailslot, recibe un identificador mailslot. Este identificador debe usarse cuando un proceso lee mensajes del mailslot. Solo el proceso que crea un mailslot o que ha obtenido el identificador mediante algún otro mecanismo (como la herencia) puede leer del mailslot. Todos los mailslots son locales para el proceso que los crea. Un proceso no puede crear un mailslot remoto.

Un *cliente mailslot* es un proceso que escribe un mensaje en un mailslot. Cualquier proceso que tenga el nombre de un mailslot puede colocar un mensaje allí. Los mensajes nuevos siguen los mensajes existentes en mailslot.

Mailslots puede difundir mensajes dentro de un dominio. Si varios procesos de un dominio crean un mailslot con el mismo nombre, los procesos participantes reciben cada mensaje que se dirige a ese mailslot y se envía al dominio. Dado que un proceso puede controlar un identificador mailslot de servidor y el identificador de cliente recuperado cuando se abre mailslot para una operación de escritura, las aplicaciones pueden implementar fácilmente una sencilla instalación de paso de mensajes dentro de un dominio.

Para enviar mensajes de más de 424 bytes entre equipos, [use](named-pipes.md) canalizaciones con nombre [o sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) Windows en su lugar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Nombres mailslot](mailslot-names.md)
</dt> <dt>

[Operaciones mailslot](mailslot-operations.md)
</dt> </dl>

 

 
