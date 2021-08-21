---
description: WMI proporciona un conjunto de clases de solución de problemas que los scripts y las aplicaciones pueden usar para obtener información sobre el estado interno de WMI durante las operaciones básicas y de proveedor de WMI.
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: Clases de solución de problemas de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d3c5f1d40cd5da9e61ff289fc0b137ec7613ec8156fb0acc4f225e793a8407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049863"
---
# <a name="wmi-troubleshooting-classes"></a>Clases de solución de problemas de WMI

WMI proporciona un conjunto de clases de solución de problemas que los scripts y las aplicaciones pueden usar para obtener información sobre el estado interno de WMI durante las operaciones básicas y de proveedor de WMI. Para obtener más información sobre la solución de problemas de [WMI,](wmi-troubleshooting.md) vea Solución de problemas de WMI y [Configuración del proveedor y Clases de solución de problemas](provider-configuration-and-troubleshooting-classes.md).

WMI tiene varias clases básicas de solución de problemas para las operaciones básicas de núcleo y proveedor de WMI:

-   [**Contadores \_ wmiProvider de MSFT \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    Solo se encuentra una de estas clases en cada sistema informático. Proporciona recuentos de diversas operaciones de proveedor en ese sistema.

-   [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    Las clases de solución de problemas de eventos derivan [**de MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent). Las consultas de esta clase devuelven instancias de clases de eventos como [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) o [**MSFT \_ WmiProvider \_ CreateInstanceEnumAsyncEvent \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).

    En la lista siguiente se proporcionan vínculos a diferentes categorías de clases de eventos derivadas de [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):

    -   [Clases de solución de problemas de eventos de proveedor](provider-event-troubleshooting-classes.md)
    -   [Clases de solución de problemas de ConsumerProvider](consumerprovider-troubleshooting-classes.md)
    -   [Clases de solución de problemas de eventos del servicio WMI](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Recepción de un evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
