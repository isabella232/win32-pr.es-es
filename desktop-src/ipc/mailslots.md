---
description: Un buzón de correo es un mecanismo para las comunicaciones entre procesos (IPC) unidireccionales. Las aplicaciones pueden almacenar mensajes en un buzón de correo. El propietario del buzón de correo puede recuperar los mensajes que se almacenan allí.
ms.assetid: e23894ca-edc7-49e6-bcc4-c82f357ecedf
title: Buzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6886e8d6f08206c6104db22c050aa6bb9859f96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716805"
---
# <a name="mailslots"></a>Buzo

Un *buzón de correo* es un mecanismo para las comunicaciones entre procesos (IPC) unidireccionales. Las aplicaciones pueden almacenar mensajes en un buzón de correo. El propietario del buzón de correo puede recuperar los mensajes que se almacenan allí. Normalmente, estos mensajes se envían a través de una red a un equipo especificado o a todos los equipos de un dominio especificado. Un *dominio* es un grupo de estaciones de trabajo y servidores que comparten un nombre de grupo.

-   [Acerca de los procesadores](about-mailslots.md)
-   [Uso de buzones de](using-mailslots.md)
-   [Referencia de buzón de correo](mailslot-reference.md)

Puede optar por usar [canalizaciones con nombre](named-pipes.md) o [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) en lugar de a través de buzones para las comunicaciones entre procesos. Las canalizaciones con nombre son una manera sencilla de que dos procesos intercambien mensajes. Los procesadores de mensajes, por otro lado, son una manera sencilla de que un proceso difunda mensajes a varios procesos. Una consideración importante es que los procesadores difunden mensajes mediante datagramas. Un *datagrama* es un pequeño paquete de información que la red envía a lo largo de la conexión. Al igual que una difusión de radio o televisión, un datagrama no ofrece ninguna confirmación de recepción; no hay ninguna manera de garantizar que se ha recibido un datagrama. Del mismo modo que las montañas, los edificios grandes o las señales que interfieren pueden provocar la pérdida de una señal de radio o televisión, hay cosas que pueden impedir que un datagrama llegue a un destino determinado. Las canalizaciones con nombre son similares a las llamadas telefónicas: solo se comunica con una entidad, pero sabe que el mensaje se está recibiendo.

 

 
