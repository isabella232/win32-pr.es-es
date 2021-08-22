---
description: Uso de NSPStartup y NSPCleanup para la inicialización y limpieza del proveedor de espacios de nombres en Windows Sockets (Winsock) SPI.
ms.assetid: c9f55845-190d-440f-8b27-1be9585137e2
title: Inicialización y limpieza del proveedor de espacios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4007533bb1456268ee3a1110da4681a7041a56ed80c0d9a522790c8a0c9a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612985"
---
# <a name="namespace-provider-initialization-and-cleanup"></a>Inicialización y limpieza del proveedor de espacios de nombres

-   [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)
-   [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)

Como es el caso del SPI de transporte, un proveedor de espacios de nombres se inicializa con una llamada a [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) y finaliza con una llamada final a [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup). Las llamadas a la función de inicio pueden estar anidadas, pero coincidirán con las llamadas correspondientes a la función cleanup. Un proveedor debe emplear el recuento de referencias para determinar cuándo se ha producido la llamada final a **NSPCleanup.**

 

 



