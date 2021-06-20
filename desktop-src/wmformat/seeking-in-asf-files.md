---
title: Búsqueda en archivos ASF (Windows Media Format SDK 11)
description: Obtenga información sobre cómo el lector de ASF de WM puede realizar búsquedas temporales muy precisas en contenido basado en Windows Media que tiene un índice temporal en Windows Media Format SDK 11.
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Media Format SDK, buscar en archivos ASF
- Windows Media Format SDK,DirectShow
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- Formato de sistemas avanzados (ASF), buscar
- ASF (formato de sistemas avanzados), buscar
- DirectShow, buscar en archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807631861cdc820457360058f22fca380fca29ea
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409888"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>Búsqueda en archivos ASF (Windows Media Format SDK 11)

El [lector DE ASF](wm-asf-reader-filter.md)de WM, a través de su interfaz **IMediaSeeking,** puede realizar búsquedas temporales muy precisas en contenido basado en Windows Media que tiene un índice temporal. (Todo el contenido indexado por fotogramas también contiene un índice temporal). Las búsquedas precisas de fotogramas garantizadas no se admiten directamente en el lector DE ASF de WM, pero hay una manera de hacerlo si necesita esta funcionalidad. En primer lugar, use el SDK de Windows Media Format directamente para crear una instancia del objeto de lector sincrónico, abrir el archivo, obtener la marca de tiempo asociada a un marco especificado y, a continuación, usar la interfaz **IMediaSeeking** de DirectShow para buscar a esa hora. La interfaz **IVideoFrameStep** de DirectShow no admite la búsqueda precisa de fotogramas del contenido basado en Windows Media. El ejemplo DSSeekFm del SDK de Windows Media Format muestra cómo realizar búsquedas precisas de fotogramas mediante el lector DE ASF de WM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Filtro de lector asf de WM**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




