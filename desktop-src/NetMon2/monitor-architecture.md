---
description: En la siguiente ilustración se muestra la relación entre los monitores y otros componentes de la arquitectura de Monitor de red.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Arquitectura de monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c1a36ef19933d888f27079d8d94ddba16bde79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104549919"
---
# <a name="monitor-architecture"></a>Arquitectura de monitor

En la siguiente ilustración se muestra la relación entre los [*monitores*](m.md) y otros componentes de la arquitectura de monitor de red.

![relación entre monitores y otros componentes de monitor de red](images/nmarch2.png)

El tráfico de red se recopila (como fotogramas individuales) del controlador NDIS. A continuación, el controlador de Monitor de red (Nmnt.sys) enruta los fotogramas a un proveedor de paquetes de red (NPP), que a su vez captura los datos en modo en tiempo real. NPP es una colección de interfaces COM que se utiliza para capturar datos. En este caso, la interfaz [**IRTC**](irtc.md) se utiliza para realizar una captura en tiempo real.

> [!Note]  
> El NPP se utiliza para las capturas retrasadas y en tiempo real. En el caso de las capturas retrasadas usadas por expertos y analizadores, se usa la interfaz [**IDelaydC**](idelaydc.md) .

 

A continuación, el monitor examina los datos capturados en modo en tiempo real, detectando condiciones de red específicas y generando eventos según sea necesario.

Las aplicaciones de supervisión usan otros tres componentes: la herramienta supervisar control, el servicio de control de supervisión (MCSVC) y el Visor de eventos:

-   La herramienta supervisar control se utiliza para administrar las aplicaciones de supervisión. Esto incluye la configuración y ejecución de todas las aplicaciones de supervisión.
-   El servicio de control de supervisión (MCSVC) desencadena eventos, proporciona un vínculo de comunicaciones a WMI para la visualización de eventos y coordina el procesamiento de las operaciones de supervisión.
-   El Visor de eventos muestra los eventos desencadenados por el servicio de control de supervisión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMonitor**](imonitor.md)
</dt> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> </dl>

 

 



