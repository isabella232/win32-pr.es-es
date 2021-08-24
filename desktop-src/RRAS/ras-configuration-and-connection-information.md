---
title: Información de configuración e conexión de RAS
description: Las aplicaciones que se ejecutan en Windows NT 4.0 y versiones posteriores, y Windows 95, pueden usar la función RasEnumConnections para obtener información sobre las conexiones existentes en el equipo local.
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- Configuración y conexión, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af528af93318247b7f88a50dc1db240670d17bcc48e11a7d683bfccd9054d671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673435"
---
# <a name="ras-configuration-and-connection-information"></a>Información de configuración e conexión de RAS

Las aplicaciones que se ejecutan en Windows NT 4.0 y versiones posteriores, y Windows 95, pueden usar la función [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) para obtener información sobre las conexiones existentes en el equipo local. La información de cada conexión incluye un identificador de conexión y el nombre de la entrada de la libreta de teléfonos utilizada para establecer la conexión. Puede usar el identificador de conexión en una llamada a la función [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para obtener el estado actual de la conexión.

Windows NT Server 4.0 y versiones posteriores proporcionan dos nuevas funciones para recuperar información ras. Windows 95 no admite estas funciones.

La [**función RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) devuelve el nombre y el tipo de los dispositivos compatibles con RAS configurados en el equipo local.

La [**función RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) especifica un objeto de evento que el sistema señala cuando se crea o finaliza una conexión RAS.

 

 




