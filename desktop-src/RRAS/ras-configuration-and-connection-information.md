---
title: Información de conexión y configuración de RAS
description: Las aplicaciones que se ejecutan en Windows NT 4,0 y versiones posteriores, y Windows 95, pueden usar la función RasEnumConnections para obtener información acerca de las conexiones existentes en el equipo local.
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- Configuración y conexión, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c4e768f4686a24857a75212e40f2e64bc91109
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676149"
---
# <a name="ras-configuration-and-connection-information"></a>Información de conexión y configuración de RAS

Las aplicaciones que se ejecutan en Windows NT 4,0 y versiones posteriores, y Windows 95, pueden usar la función [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) para obtener información acerca de las conexiones existentes en el equipo local. La información de cada conexión incluye un identificador de conexión y el nombre de la entrada de la libreta de teléfonos utilizada para establecer la conexión. Puede usar el identificador de conexión en una llamada a la función [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para obtener el estado actual de la conexión.

Windows NT Server 4,0 y versiones posteriores proporcionan dos funciones nuevas para recuperar información de RAS. Windows 95does no admite estas funciones.

La función [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) devuelve el nombre y el tipo de los dispositivos compatibles con ras que están configurados en el equipo local.

La función [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) especifica un objeto de evento que el sistema señala cuando se crea o finaliza una conexión RAS.

 

 




