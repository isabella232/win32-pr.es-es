---
description: El \_32.dll Ws2 (y los protocolos en capas) llamará a WSPCleanup una vez para cada invocación de WSPStartup.
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: Limpieza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc294183f964d00ae9ebb1d74b90b346c2ce8fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696399"
---
# <a name="cleanup"></a>Limpieza

El \_32.dll Ws2 (y los protocolos en capas) llamará a [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) una vez para cada invocación de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). En cada invocación, **WSPCleanup** debe disminuir un contador de referencia por proceso y, cuando el contador llega a cero, el proveedor de servicios debe prepararse para descargarse de la memoria. El primer orden de negocio es finalizar la transmisión de los datos no enviados en los sockets configurados para un cierre estable. A partir de ese momento, se liberarán todos los recursos retenidos por el proveedor. El proveedor de servicios debe dejarse en un estado en el que se pueda reinicializar inmediatamente mediante una llamada a **WSPStartup**.

 

 
