---
description: En la ilustración siguiente se muestra la relación entre los monitores y otros componentes de la Monitor de red arquitectura.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Arquitectura de supervisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9cd0a099fc1474255b36f1f04d28899b25a527fee19ba1d29434b4692615ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677135"
---
# <a name="monitor-architecture"></a>Arquitectura de supervisión

En la ilustración siguiente se muestra la relación entre [*los monitores*](m.md) y otros componentes de Monitor de red arquitectura.

![relación entre monitores y otros componentes del monitor de red](images/nmarch2.png)

El tráfico de red se recopila (como fotogramas individuales) del controlador NDIS. El controlador Monitor de red (Nmnt.sys) enruta los fotogramas a un proveedor de paquetes de red (NPP), que a su vez captura los datos en modo en tiempo real. El NPP es una colección de interfaces COM que se usan para capturar datos. En este caso, la [**interfaz IRTC**](irtc.md) se usa para realizar una captura en tiempo real.

> [!Note]  
> El NPP se usa para las capturas retrasadas y en tiempo real. Para las capturas diferida usadas por expertos y analizadores, se usa la [**interfaz IDelaydC.**](idelaydc.md)

 

A continuación, el monitor examina los datos capturados en modo en tiempo real, detectando condiciones de red específicas y generando eventos según sea necesario.

Las aplicaciones de supervisión usan otros tres componentes: Monitor Control Tool, Monitor Control Service (MCSVC) y Visor de eventos:

-   Monitor Control Tool se usa para administrar las aplicaciones de supervisión. Esto incluye la configuración y ejecución de todas las aplicaciones de supervisión.
-   El Servicio de control de supervisión (MCSVC) establece eventos, proporciona un vínculo de comunicaciones a WMI para la visualización de eventos y coordina el procesamiento de las operaciones de supervisión.
-   El Visor de eventos muestra los eventos desencadenados por el Servicio de control de supervisión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMonitor**](imonitor.md)
</dt> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> </dl>

 

 



