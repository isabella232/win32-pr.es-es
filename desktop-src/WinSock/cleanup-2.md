---
description: El32.dll Ws2 (y protocolos por capas) llamará a WSPCleanup una vez por cada \_ invocación de WSPStartup.
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: Limpieza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aefac8f58b7d6eed0380b7aa0e7759ff07e5af2a2762cde7d8e9bab445ca1fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741443"
---
# <a name="cleanup"></a>Limpieza

El32.dll Ws2 (y protocolos por capas) llamará a \_ [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) una vez por cada invocación de [**WSPStartup.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) En cada invocación, **WSPCleanup** debe disminuir un contador de referencia por proceso y, cuando el contador alcanza cero, el proveedor de servicios debe prepararse para descargarse de la memoria. El primer orden de la empresa es terminar de transmitir los datos no enviados en sockets configurados para un cierre correcto. A partir de ese momento, se liberarán todos y cada uno de los recursos que tenga el proveedor. El proveedor de servicios debe quedar en un estado en el que se pueda reinicializar inmediatamente mediante una llamada a **WSPStartup**.

 

 
