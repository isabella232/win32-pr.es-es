---
title: Buscar en archivos ASF (Windows SDK de formato multimedia 11)
description: Obtenga información sobre cómo el lector de ASF wm puede realizar búsquedas temporales muy precisas en contenido basado en Windows Media que tiene un índice temporal en el SDK de Windows Media Format 11.
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows SDK de formato multimedia, buscar en archivos ASF
- Windows SDK de formato multimedia, DirectShow
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Formato de sistemas avanzados (ASF), buscar
- ASF (formato de sistemas avanzados), buscar
- DirectShow, buscar en archivos de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6730f1535c9601cfd0697e374ddfa35b05250ed49fc4b575fa3458b69e389285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845900"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>Buscar en archivos ASF (Windows SDK de formato multimedia 11)

El [lector DE ASF](wm-asf-reader-filter.md)de WM, a través de su interfaz **IMediaSeeking,** puede realizar búsquedas temporales muy precisas en Windows contenido basado en medios que tiene un índice temporal. (Todo el contenido indexado por fotogramas también contiene un índice temporal). Las búsquedas con precisión de fotogramas garantizadas no se admiten directamente en el lector de ASF de WM, pero hay una manera de hacerlo si necesita esta funcionalidad. En primer lugar, use el SDK de formato multimedia de Windows directamente para crear una instancia del objeto de lector sincrónico, abrir el archivo, obtener la marca de tiempo asociada a un marco especificado y, a continuación, usar la interfaz **IMediaSeeking** de DirectShow para buscar a esa hora. La DirectShow **IVideoFrameStep** no admite búsquedas precisas de fotogramas Windows contenido basado en multimedia. El ejemplo DSSeekFm del SDK Windows Media Format muestra cómo realizar búsquedas precisas de fotogramas mediante el lector DE ASF de WM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Filtro de lector DE ASF de WM**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




