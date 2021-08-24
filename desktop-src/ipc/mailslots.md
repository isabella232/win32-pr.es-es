---
description: Un mailslot es un mecanismo para las comunicaciones uní las comunicaciones entre procesos (IPC). Las aplicaciones pueden almacenar mensajes en un mailslot. El propietario del mailslot puede recuperar los mensajes almacenados allí.
ms.assetid: e23894ca-edc7-49e6-bcc4-c82f357ecedf
title: Mailslots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72a4bc50c2cb563894ce9b7c616f9ae86cd9ae6e4abb966c78475c504c75f54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716835"
---
# <a name="mailslots"></a>Mailslots

Un *mailslot* es un mecanismo para las comunicaciones uní las comunicaciones entre procesos (IPC). Las aplicaciones pueden almacenar mensajes en un mailslot. El propietario del mailslot puede recuperar los mensajes almacenados allí. Normalmente, estos mensajes se envían a través de una red a un equipo especificado o a todos los equipos de un dominio especificado. Un *dominio* es un grupo de estaciones de trabajo y servidores que comparten un nombre de grupo.

-   [Acerca de Mailslots](about-mailslots.md)
-   [Uso de Mailslots](using-mailslots.md)
-   [Referencia de Mailslot](mailslot-reference.md)

Puede optar por usar [canalizaciones con](named-pipes.md) nombre [o sockets Windows en](/windows/desktop/WinSock/windows-sockets-start-page-2) lugar de mailslots para las comunicaciones entre procesos. Las canalizaciones con nombre son una manera sencilla de que dos procesos interc ambos intercambios de mensajes. Los mailslots, por otro lado, son una manera sencilla de que un proceso difunda mensajes a varios procesos. Una consideración importante es que mailslots difunde mensajes mediante datagramas. Un *datagrama* es un pequeño paquete de información que la red envía a lo largo de la conexión. Al igual que una difusión de radio o televisión, un datagrama no ofrece ninguna confirmación de recepción. no hay ninguna manera de garantizar que se ha recibido un datagrama. Al igual que las montañas, los edificios grandes o las señales que interfieren pueden hacer que se pierda una señal de radio o televisión, hay cosas que pueden impedir que un datagrama llegue a un destino determinado. Las canalizaciones con nombre son como llamadas telefónicas: solo se habla con una parte, pero sabe que se recibe el mensaje.

 

 
