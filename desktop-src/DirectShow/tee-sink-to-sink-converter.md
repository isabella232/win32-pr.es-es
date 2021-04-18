---
description: Convertidor Tee/Sink-to-Sink
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: Convertidor Tee/Sink-to-Sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf85e3eb58f601273ff352a3878d352ca0f0d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678257"
---
# <a name="teesink-to-sink-converter"></a>Convertidor Tee/Sink-to-Sink

El convertidor Tee/Sink-to-Sink es un filtro basado en KsProxy y en modo kernel. Se usa en gráficos de filtro de televisión de vídeo analógico donde se representan o capturan datos de VBI. El filtro se conecta ascendente al filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) y proporciona un medio eficaz para duplicar secuencias de datos en modo kernel sin las transiciones costosas entre el modo kernel y el usuario. Proporciona cada bloque de datos recibido a todos los pin de salida, y el códec de bajada es responsable de buscar los datos de VBI específicos que se van a descodificar.

El convertidor Tee/Sink-to-Sink aparece en la categoría de filtro "dispositivos de transmisión por secuencias WDM y divisora" ( \_ KSCATEGORY \_ ).

Dado que se trata de un filtro en modo kernel, las aplicaciones no pueden crearlo directamente mediante [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). En su lugar, use el [enumerador de dispositivos del sistema](system-device-enumerator.md). Para obtener más información, vea [crear filtros de Kernel-Mode](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 
