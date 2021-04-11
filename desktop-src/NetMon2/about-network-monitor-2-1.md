---
description: Monitor de red es un componente de Microsoft Systems Management Server (SMS) que se usa para detectar y solucionar problemas en LAN, WAN y vínculos serie que ejecutan el servidor de acceso remoto (RAS) de Microsoft.
ms.assetid: bd273439-daa2-4263-8f12-28ec988beea0
title: Acerca de Monitor de red 2,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447f4763e0c73dc0dcac4cf719a0bad4b61f073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082618"
---
# <a name="about-network-monitor-21"></a>Acerca de Monitor de red 2,1

Monitor de red es un componente de Microsoft Systems Management Server (SMS) que se usa para detectar y solucionar problemas en LAN, WAN y vínculos serie que ejecutan el servidor de acceso remoto (RAS) de Microsoft. Monitor de red proporciona análisis de datos de red posteriores a la captura.

En el análisis posterior a la captura, el tráfico de red se guarda en un archivo de captura de propiedad, de modo que los datos capturados se puedan analizar más adelante. En este caso, el análisis puede tener la forma de los [*analizadores*](p.md) de protocolo que eligen tipos de tramas de red específicos y muestran los datos de fotogramas en la interfaz de usuario de monitor de red. o el análisis puede ser en forma de [*expertos*](e.md) que examinan los datos de red y muestran un informe (los expertos también pueden manipular los datos de red).

Monitor de red proporciona los siguientes tipos de funcionalidad:

-   Captura datos de red en modo en tiempo real o retrasado.
-   Proporciona funciones de filtrado al capturar datos.
-   Utiliza expertos y analizadores para el análisis detallado posterior a la captura.

Para obtener más información acerca de las características de Monitor de red, consulte:

-   [Arquitectura de expertos y del analizador](expert-and-parser-architecture.md)
-   [Expertos](experts.md)
-   [Analizadores](parsers.md)
-   [Proveedores de paquetes de red](network-packet-providers.md)
-   [Blobs Monitor de red](network-monitor-blobs.md)
-   [Página referencia de eventos](event-reference-page.md)
-   [Filtros de captura](capture-filters.md)

**Windows Vista:** Monitor de red 2,1 y versiones anteriores no se admiten en esta plataforma.

 

 



