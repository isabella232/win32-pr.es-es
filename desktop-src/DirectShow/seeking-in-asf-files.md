---
description: Obtenga información sobre cómo el lector de ASF de WM puede realizar búsquedas temporales muy precisas en contenido basado en Windows Media que tiene un índice temporal en DirectShow.
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Búsqueda en archivos ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ffc570536463b86a88e1f26be338bd748c790c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405588"
---
# <a name="seeking-in-asf-files-directshow"></a>Búsqueda en archivos ASF (DirectShow)

El [lector DE ASF](wm-asf-reader-filter.md)de WM, a través de su interfaz [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) puede realizar búsquedas temporales muy precisas en contenido basado en Windows Media que tiene un índice temporal. (Todo el contenido indexado por fotogramas también contiene un índice temporal). Las búsquedas precisas de fotogramas garantizadas no se admiten directamente en el lector DE ASF de WM, pero hay una manera de hacerlo si necesita esta funcionalidad. En primer lugar, use el SDK de Windows Media Format directamente para crear una instancia del objeto de lector sincrónico, abrir el archivo, obtener la marca de tiempo asociada a un marco especificado y, a continuación, usar la interfaz **IMediaSeeking** de DirectShow para buscar a esa hora. La [**interfaz IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) no admite la búsqueda precisa de fotogramas del contenido basado en Windows Media.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lectura de archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



