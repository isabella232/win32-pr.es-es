---
description: Convertidor de tee/sink-to-sink
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: Convertidor de tee/sink-to-sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b1639572dc4809df4b326fabeac613bbb1b38b9392b32e1c1f54f717a0f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050015"
---
# <a name="teesink-to-sink-converter"></a>Convertidor de tee/sink-to-sink

El convertidor de receptor a receptor es un filtro basado en KsProxy en modo kernel. Se usa en gráficos de filtros de televisión de vídeo análogo en los que se representan o capturan datos de VBI. El filtro está conectado en sentido ascendente al filtro de captura de vídeo [de WDM](wdm-video-capture-filter.md) y proporciona un medio eficaz para duplicar flujos de datos en modo kernel sin las costosas transiciones entre el modo kernel y el modo de usuario. Entrega cada bloque de datos recibido a todos los pines de salida y el códec de bajada es responsable de buscar los datos de VBI específicos que se descodifican.

El convertidor de tee/sink-to-sink aparece en la categoría de filtro "WDM Streaming Tee/Splitter Devices" (AM \_ KSCATEGORY \_ SPLITTER).

Dado que se trata de un filtro en modo kernel, las aplicaciones no pueden crearlo directamente mediante [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). En su lugar, use [el enumerador de dispositivos del sistema](system-device-enumerator.md). Para obtener más información, vea [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 
