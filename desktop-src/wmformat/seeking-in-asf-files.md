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
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a><span data-ttu-id="83023-110">Búsqueda en archivos ASF (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="83023-110">Seeking in ASF Files (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="83023-111">El [lector DE ASF](wm-asf-reader-filter.md)de WM, a través de su interfaz **IMediaSeeking,** puede realizar búsquedas temporales muy precisas en contenido basado en Windows Media que tiene un índice temporal.</span><span class="sxs-lookup"><span data-stu-id="83023-111">The [WM ASF Reader](wm-asf-reader-filter.md), through its **IMediaSeeking** interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="83023-112">(Todo el contenido indexado por fotogramas también contiene un índice temporal). Las búsquedas precisas de fotogramas garantizadas no se admiten directamente en el lector DE ASF de WM, pero hay una manera de hacerlo si necesita esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="83023-112">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="83023-113">En primer lugar, use el SDK de Windows Media Format directamente para crear una instancia del objeto de lector sincrónico, abrir el archivo, obtener la marca de tiempo asociada a un marco especificado y, a continuación, usar la interfaz **IMediaSeeking** de DirectShow para buscar a esa hora.</span><span class="sxs-lookup"><span data-stu-id="83023-113">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="83023-114">La interfaz **IVideoFrameStep** de DirectShow no admite la búsqueda precisa de fotogramas del contenido basado en Windows Media.</span><span class="sxs-lookup"><span data-stu-id="83023-114">The DirectShow **IVideoFrameStep** interface does not support frame-accurate seeking of Windows Media–based content.</span></span> <span data-ttu-id="83023-115">El ejemplo DSSeekFm del SDK de Windows Media Format muestra cómo realizar búsquedas precisas de fotogramas mediante el lector DE ASF de WM.</span><span class="sxs-lookup"><span data-stu-id="83023-115">The DSSeekFm sample in the Windows Media Format SDK demonstrates how to perform frame-accurate seeking using the WM ASF Reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83023-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83023-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83023-117">**Filtro de lector asf de WM**</span><span class="sxs-lookup"><span data-stu-id="83023-117">**WM ASF Reader Filter**</span></span>](wm-asf-reader-filter.md)
</dt> </dl>

 

 




