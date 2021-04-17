---
description: Escribir filtros de captura
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Escribir filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1a64de2b56dbc0728432307036fc46387f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687717"
---
# <a name="writing-capture-filters"></a>Escribir filtros de captura

No se recomienda escribir un filtro de captura de audio o vídeo para DirectShow. En su lugar, DirectShow proporciona compatibilidad automática para dispositivos de captura de audio y vídeo, mediante filtros de contenedor y el [enumerador de dispositivos de sistema](system-device-enumerator.md). Para obtener más información acerca de la implementación de un controlador de dispositivo, consulte la documentación del kit de controladores de Windows (WDK).

Esta sección está destinada únicamente a los desarrolladores que necesitan capturar algún tipo de datos personalizados desde un dispositivo de hardware inusual.

Este artículo contiene las siguientes secciones:

-   [Requisitos de PIN para los filtros de captura](pin-requirements-for-capture-filters.md)
-   [Implementación de un PIN de versión preliminar (opcional)](implementing-a-preview-pin--optional.md)
-   [Generar datos en un filtro de captura](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



