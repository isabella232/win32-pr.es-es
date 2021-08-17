---
description: Obtenga información sobre cómo el lector de ASF wm puede realizar búsquedas temporales muy precisas en Windows contenido basado en medios que tiene un índice temporal en DirectShow.
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Buscar en archivos ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1bea9749b80b15072efe29a749bd7312de865514ce597f1ec1584dca5cf139c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951954"
---
# <a name="seeking-in-asf-files-directshow"></a>Buscar en archivos ASF (DirectShow)

El [lector DE ASF](wm-asf-reader-filter.md)de WM, a través de su interfaz [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) puede realizar búsquedas temporales muy precisas en Windows contenido basado en medios que tiene un índice temporal. (Todo el contenido indexado por fotogramas también contiene un índice temporal). Las búsquedas con precisión de fotogramas garantizadas no se admiten directamente en el lector de ASF de WM, pero hay una manera de hacerlo si necesita esta funcionalidad. En primer lugar, use el SDK de formato multimedia de Windows directamente para crear una instancia del objeto de lector sincrónico, abrir el archivo, obtener la marca de tiempo asociada a un marco especificado y, a continuación, usar la interfaz **IMediaSeeking** de DirectShow para buscar a esa hora. La [**interfaz IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) no admite búsquedas precisas de fotogramas Windows contenido basado en multimedia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lectura de archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



