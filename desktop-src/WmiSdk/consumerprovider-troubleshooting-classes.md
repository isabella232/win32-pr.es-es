---
description: En la tabla siguiente se enumeran las clases de eventos de solución de problemas generados por las operaciones del proveedor de consumidor de eventos.
ms.assetid: dd685a41-8eae-4977-ab94-902dd8dddcc9
ms.tgt_platform: multiple
title: Clases de solución de problemas de ConsumerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 536c23fb35ca6a4d2146cf87782768c51f37a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716563"
---
# <a name="consumerprovider-troubleshooting-classes"></a>Clases de solución de problemas de ConsumerProvider

En la tabla siguiente se enumeran las clases de eventos de solución de problemas generados por las operaciones del [*proveedor de consumidor de eventos*](gloss-e.md) .

Puede suscribirse a las notificaciones de la clase base abstracta [**msft \_ ProviderEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) para obtener todos los eventos siguientes.



|                                                                                                 |                                                                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**MSFT \_ WmiProviderEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiproviderevent)                               | Clase primaria para todos los eventos de proveedor de consumidor.                                  |
| [**MSFT \_ WmiConsumerProviderLoaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderloaded)             | Define la activación correcta del objeto COM del proveedor del consumidor de eventos.    |
| [**MSFT \_ WmiConsumerProviderUnloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderunloaded)         | Define la desactivación correcta del objeto COM del proveedor del consumidor de eventos.  |
| [**MSFT \_ WmiConsumerProviderSinkLoaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkloaded)     | Define la activación correcta del objeto de receptor de proveedor de consumidor de eventos.   |
| [**MSFT \_ WmiConsumerProviderSinkUnloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkunloaded) | Define la desactivación correcta del objeto de receptor de proveedor de consumidor de eventos. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

Solución de problemas de WMI
</dt> <dt>

[Recibir un evento de WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
