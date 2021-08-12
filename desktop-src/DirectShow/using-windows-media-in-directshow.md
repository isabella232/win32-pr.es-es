---
description: Uso Windows multimedia en DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Uso Windows multimedia en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fea308943d4be732c75e774d3e0c3cb09ac7c6609a8399d2e6eca4666d99e6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651091"
---
# <a name="using-windows-media-in-directshow"></a>Uso Windows multimedia en DirectShow

En esta sección se describe cómo usar DirectShow para reproducir y escribir archivos de formato de sistemas avanzados (ASF). Los archivos ASF normalmente contienen contenido de audio y vídeo codificado mediante los códecs Windows media audio y vídeo. Sin embargo, ASF puede contener cualquier tipo de datos.

Los siguientes filtros DirectShow admiten la lectura y escritura de archivos ASF:

-   [Filtro del lector DE ASF de WM](wm-asf-reader-filter.md). Lee archivos ASF.
-   [Filtro de escritor de ASF de WM](wm-asf-writer-filter.md). Archivos ASF de Wrties.
-   [DMO filtro contenedor .](dmo-wrapper-filter.md) Encapsula el codificador Windows multimedia y las DDO descodificadores.

### <a name="versions"></a>Versiones

Los filtros Lector de ASF de WM y Escritor de ASF de WM se empaquetan en el archivo DLL denominado qasf.dll y los filtros se denominan colectivamente "componentes qasf". Estos filtros son contenedores para el SDK Windows Media Format. El archivo DLL (qasf.dll) se publicó por primera vez en el SDK de DirectX, pero más adelante se actualizó en el SDK Windows Media Format. Este es el historial de versiones de los filtros QASF:

-   DirectShow 8.1 admite Windows SDK de formato multimedia versión 7.0.
-   DirectShow 9.0 admite Windows SDK de formato multimedia versión 7.1.
-   Windows XP Service Pack 2 admite Windows SDK de Formato multimedia 9.
-   Windows Vista admite Windows SDK de Formato multimedia 11.
-   Windows El SDK de Formato multimedia 9 y versiones posteriores contienen las versiones correspondientes de QASF.

Para obtener la versión más reciente de QASF, descargue siempre la versión más reciente Windows SDK de formato multimedia.

### <a name="legacy-windows-media-source-filter"></a>Filtro de origen Windows multimedia heredado

En Windows XP Service Pack 1 y versiones anteriores, el filtro de origen predeterminado para los archivos ASF (extensiones de archivo .asf, .wmv y .wma) es el filtro de origen multimedia obsoleto [Windows](windows-media-source-filter.md). Este comportamiento se ha mantenido para garantizar la compatibilidad con versiones anteriores con las aplicaciones que usaban Reproductor de Windows Media 6.4. Las nuevas aplicaciones deben usar las versiones más recientes de QASF, que hacen que el lector de ASF wm filtre el filtro predeterminado para reproducir archivos ASF.

Para obtener más información sobre Windows conjunto multimedia de kits de desarrollo de software, consulte la sección [Audio y vídeo](../audio-and-video.md) de la biblioteca MDSN.

Ese artículo contiene los siguientes temas:

-   [Leer archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
-   [Creación de archivos ASF en DirectShow](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DirectShow](using-directshow.md)
</dt> </dl>

 

 
