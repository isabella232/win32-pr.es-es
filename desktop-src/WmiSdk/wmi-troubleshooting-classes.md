---
description: WMI proporciona un conjunto de clases de solución de problemas que los scripts y las aplicaciones pueden utilizar para obtener información sobre el estado interno de WMI durante las operaciones básicas de WMI y de proveedor.
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: Clases de solución de problemas de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b3972ba59c80a1495916ab24a72f6e93bef8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003009"
---
# <a name="wmi-troubleshooting-classes"></a>Clases de solución de problemas de WMI

WMI proporciona un conjunto de clases de solución de problemas que los scripts y las aplicaciones pueden utilizar para obtener información sobre el estado interno de WMI durante las operaciones básicas de WMI y de proveedor. Para obtener más información acerca de la solución de problemas de WMI, consulte solución de problemas de [WMI](wmi-troubleshooting.md) y [clases de solución de problemas](provider-configuration-and-troubleshooting-classes.md).

WMI tiene varias clases básicas de solución de problemas para las operaciones básicas y de proveedor de WMI:

-   [**\_Contadores de msft WmiProvider \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    Solo se encuentra una de estas clases en cada sistema del equipo. Proporciona recuentos de diferentes tipos de operaciones de proveedor en ese sistema.

-   [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    Las clases de solución de problemas de eventos derivan de [**msft \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent). Las consultas de esta clase devuelven instancias de clases de eventos como [**msft \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) o [**msft \_ WmiProvider \_ CreateInstanceEnumAsyncEvent \_ post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).

    En la lista siguiente se proporcionan vínculos a distintas categorías de clases de eventos derivadas de [**msft \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):

    -   [Clases de solución de problemas de eventos de proveedor](provider-event-troubleshooting-classes.md)
    -   [Clases de solución de problemas de ConsumerProvider](consumerprovider-troubleshooting-classes.md)
    -   [Clases de solución de problemas de eventos del servicio WMI](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Recibir un evento de WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
