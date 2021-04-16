---
description: Usar Windows Media en DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Usar Windows Media en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104424127"
---
# <a name="using-windows-media-in-directshow"></a>Usar Windows Media en DirectShow

En esta sección se describe cómo usar DirectShow para reproducir y escribir archivos Advanced Systems Format (ASF). Los archivos ASF suelen contener contenido de audio y vídeo codificado mediante los códecs de vídeo y Windows Media Audio. Sin embargo, ASF puede contener cualquier tipo de datos.

Los filtros DirectShow siguientes admiten la lectura y escritura de archivos ASF:

-   [Filtro de lector ASF de WM](wm-asf-reader-filter.md). Lee archivos ASF.
-   [Filtro del escritor ASF de WM](wm-asf-writer-filter.md). Archivos ASF de Wrties.
-   [Filtro de contenedor de DMO](dmo-wrapper-filter.md). Incluye el codificador y descodificador de Windows Media DMOs.

### <a name="versions"></a>Versiones

Los filtros del lector ASF de WM y del escritor ASF de WM se empaquetan en el archivo DLL denominado qasf.dll y los filtros se denominan colectivamente "componentes QASF". Estos filtros son contenedores del SDK de Windows Media Format. El archivo DLL (qasf.dll) se publicó por primera vez en el SDK de DirectX, pero se actualizó posteriormente en el SDK de Windows Media Format. Este es el historial de versiones de los filtros de QASF:

-   DirectShow 8,1 es compatible con Windows Media Format SDK versión 7,0.
-   DirectShow 9,0 es compatible con Windows Media Format SDK versión 7,1.
-   Windows XP Service Pack 2 es compatible con Windows Media Format 9 SDK.
-   Windows Vista es compatible con Windows Media Format 11 SDK.
-   Windows Media Format 9 SDK y versiones posteriores contienen las versiones correspondientes de QASF.

Para obtener la versión más reciente de QASF, Descargue siempre el SDK de Windows Media Format más reciente.

### <a name="legacy-windows-media-source-filter"></a>Filtro de origen de Windows Media heredado

En Windows XP Service Pack 1 y versiones anteriores, el filtro de origen predeterminado para los archivos ASF (extensiones de archivo. ASF,. WMV y. WMA) es el filtro de origen obsoleto de [Windows Media](windows-media-source-filter.md). Este comportamiento se mantuvo para garantizar la compatibilidad con versiones anteriores de las aplicaciones que usaban Windows Media Player 6,4. Las nuevas aplicaciones deben usar las versiones más recientes de QASF, que hacen que el lector ASF de WM filtre el filtro predeterminado para reproducir archivos ASF.

Para obtener más información sobre el conjunto de aplicaciones de Windows Media de kits de desarrollo de software, consulte la sección [audio y vídeo](../audio-and-video.md) de la biblioteca MDSN.

Ese artículo contiene los siguientes temas:

-   [Leer archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
-   [Crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar DirectShow](using-directshow.md)
</dt> </dl>

 

 
