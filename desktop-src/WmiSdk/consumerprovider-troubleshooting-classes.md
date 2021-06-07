---
description: En la tabla siguiente se enumeran las clases de eventos de solución de problemas generadas por las operaciones del proveedor de consumidores de eventos.
ms.assetid: dd685a41-8eae-4977-ab94-902dd8dddcc9
ms.tgt_platform: multiple
title: Clases de solución de problemas de ConsumerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740b8c0eb1884181fa84efe26e0611dda4b1712f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443616"
---
# <a name="consumerprovider-troubleshooting-classes"></a>Clases de solución de problemas de ConsumerProvider

En la tabla siguiente se enumeran las clases de eventos de solución de problemas generadas por las [*operaciones del proveedor de consumidores de*](gloss-e.md) eventos.

Puede suscribirse a la clase base abstracta [**MSFT \_ ProviderEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) notifications para obtener todos los eventos siguientes.



| Evento                                                                                                | Descripción                                                                                |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**MSFT \_ WmiProviderEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiproviderevent)                               | Clase primaria para todos los eventos del proveedor de consumidores.                                  |
| [**MSFT \_ WmiConsumerProviderLoaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderloaded)             | Define la activación correcta del objeto COM del proveedor de consumidores de eventos.    |
| [**MSFT \_ WmiConsumerProviderUnloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderunloaded)         | Define la desactivación correcta del objeto COM del proveedor de consumidores de eventos.  |
| [**MSFT \_ WmiConsumerProviderSinkLoaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkloaded)     | Define la activación correcta del objeto receptor del proveedor de consumidores de eventos.   |
| [**MSFT \_ WmiConsumerProviderSinkUnloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkunloaded) | Define la desactivación correcta del objeto receptor del proveedor de consumidores de eventos. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

Solución de problemas de WMI
</dt> <dt>

[Recepción de un evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
