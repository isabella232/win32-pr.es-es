---
description: Uso de Windows multimedia en DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Uso de Windows multimedia en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160106"
---
# <a name="using-windows-media-in-directshow"></a>Uso de Windows multimedia en DirectShow

En esta sección se describe cómo usar DirectShow reproducir y escribir archivos de formato de sistemas avanzados (ASF). Los archivos ASF normalmente contienen contenido de audio y vídeo codificado mediante los códecs Windows media audio y vídeo. Sin embargo, ASF puede contener cualquier tipo de datos.

Los siguientes filtros DirectShow admiten la lectura y escritura de archivos ASF:

-   [Filtro de lector DE ASF de WM.](wm-asf-reader-filter.md) Lee archivos ASF.
-   [Filtro wm asf writer](wm-asf-writer-filter.md). Archivos ASF de wrties.
-   [DMO filtro contenedor .](dmo-wrapper-filter.md) Encapsula el codificador Windows multimedia y el descodificador.

### <a name="versions"></a>Versiones

Los filtros wm asf reader y WM ASF Writer se empaquetan en el archivo DLL denominado qasf.dll y los filtros se denominan colectivamente "componentes QASF". Estos filtros son contenedores para el SDK Windows Media Format. El archivo DLL (qasf.dll) se publicó por primera vez en el SDK de DirectX, pero más adelante se actualizó en el SDK Windows Media Format. Este es el historial de versiones de los filtros QASF:

-   DirectShow 8.1 admite Windows SDK de formato multimedia versión 7.0.
-   DirectShow 9.0 admite Windows SDK de formato multimedia versión 7.1.
-   Windows XP Service Pack 2 admite Windows SDK de Formato multimedia 9.
-   Windows Vista admite Windows SDK de Formato multimedia 11.
-   Windows El SDK de Formato multimedia 9 y versiones posteriores contienen las versiones correspondientes de QASF.

Para obtener la versión más reciente de QASF, descargue siempre la versión más reciente Windows SDK de formato multimedia.

### <a name="legacy-windows-media-source-filter"></a>Filtro de origen Windows multimedia heredado

En Windows XP Service Pack 1 y versiones anteriores, el filtro de origen predeterminado para los archivos ASF (extensiones de archivo .asf, .wmv y .wma) es el filtro de origen de Windows multimedia [obsoleto.](windows-media-source-filter.md) Este comportamiento se ha mantenido para garantizar la compatibilidad con versiones anteriores con las aplicaciones que usaban Reproductor de Windows Media 6.4. Las nuevas aplicaciones deben usar las versiones más recientes de QASF, que hacen que el lector de ASF wm filtre el filtro predeterminado para reproducir archivos ASF.

Para obtener más información sobre el conjunto Windows multimedia de kits de desarrollo de software, consulte la sección [Audio y vídeo](../audio-and-video.md) de la biblioteca MDSN.

Ese artículo contiene los siguientes temas:

-   [Lectura de archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
-   [Crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DirectShow](using-directshow.md)
</dt> </dl>

 

 
