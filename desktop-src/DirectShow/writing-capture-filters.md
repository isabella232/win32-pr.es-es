---
description: Escribir filtros de captura
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Escribir filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa4807f381dc925a68fa3c60e45d5c8c5c444653230f366895b370e97aaccb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049095"
---
# <a name="writing-capture-filters"></a>Escribir filtros de captura

No se recomienda escribir un filtro de captura de audio DirectShow vídeo. En su lugar, DirectShow compatibilidad automática con dispositivos de captura de audio y vídeo, mediante filtros contenedor y [el enumerador de dispositivos del sistema](system-device-enumerator.md). Para obtener más información sobre cómo implementar un controlador de dispositivo, consulte la documentación Windows Driver Kit (WDK).

Esta sección está pensada solo para desarrolladores que necesitan capturar algún tipo de datos personalizados desde un dispositivo de hardware inusual.

Este artículo contiene las siguientes secciones:

-   [Requisitos de anclar para filtros de captura](pin-requirements-for-capture-filters.md)
-   [Implementar un pin de vista previa (opcional)](implementing-a-preview-pin--optional.md)
-   [Generar datos en un filtro de captura](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



