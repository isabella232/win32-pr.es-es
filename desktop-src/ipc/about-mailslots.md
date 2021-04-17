---
description: Un buzón de correo es un pseudofile que reside en la memoria y utiliza funciones de archivo estándar para tener acceso a él.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: Acerca de los procesadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd83fc0d952577efdb149d4c7f25fffbab9784f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669963"
---
# <a name="about-mailslots"></a>Acerca de los procesadores

Un buzón de correo es un pseudofile que reside en la memoria y utiliza funciones de archivo estándar para tener acceso a él. Los datos de un mensaje de buzón de correo pueden estar en cualquier formato, pero no pueden ser mayores de 424 bytes cuando se envían entre equipos. A diferencia de los archivos de disco, los buzones de archivos son temporales. Cuando se cierran todos los identificadores de un buzón de correo, el buzón de correo y todos los datos que contiene se eliminan.

Un *servidor de buzón de correo* es un proceso que crea y posee un buzón de correo. Cuando el servidor crea un buzón de correo, recibe un identificador de buzón de correo. Este identificador se debe utilizar cuando un proceso Lee los mensajes del buzón de correo. Solo el proceso que crea un buzón de correo o que ha obtenido el identificador de otro mecanismo (como la herencia) puede leer desde el buzón de correo. Todos los procesadores de curso son locales para el proceso que los crea. Un proceso no puede crear un buzón remoto.

Un *cliente de buzón de correo* es un proceso que escribe un mensaje en un buzón de correo. Cualquier proceso que tenga el nombre de un buzón de correo puede colocar un mensaje allí. Los mensajes nuevos siguen los mensajes existentes en el buzón de correo.

Los procesadores de mensajes pueden difundir mensajes dentro de un dominio. Si cada uno de los procesos de un dominio crea un buzón de correo con el mismo nombre, los procesos participantes reciben todos los mensajes que se dirigen a ese buzón de correo y se envían al dominio. Dado que un proceso puede controlar un identificador de buzón de correo de servidor y el identificador de cliente recuperados cuando se abre el buzón de correo para una operación de escritura, las aplicaciones pueden implementar fácilmente una sencilla característica de paso de mensajes dentro de un dominio.

Para enviar mensajes de más de 424 bytes entre equipos, utilice [canalizaciones con nombre](named-pipes.md) o [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) en su lugar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Nombres de buzón de correo](mailslot-names.md)
</dt> <dt>

[Operaciones de buzón de correo](mailslot-operations.md)
</dt> </dl>

 

 
