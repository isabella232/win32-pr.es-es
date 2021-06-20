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
# <a name="seeking-in-asf-files-directshow"></a><span data-ttu-id="76b2e-103">Búsqueda en archivos ASF (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="76b2e-103">Seeking in ASF Files (DirectShow)</span></span>

<span data-ttu-id="76b2e-104">El [lector DE ASF](wm-asf-reader-filter.md)de WM, a través de su interfaz [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) puede realizar búsquedas temporales muy precisas en contenido basado en Windows Media que tiene un índice temporal.</span><span class="sxs-lookup"><span data-stu-id="76b2e-104">The [WM ASF Reader](wm-asf-reader-filter.md), through its [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="76b2e-105">(Todo el contenido indexado por fotogramas también contiene un índice temporal). Las búsquedas precisas de fotogramas garantizadas no se admiten directamente en el lector DE ASF de WM, pero hay una manera de hacerlo si necesita esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="76b2e-105">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="76b2e-106">En primer lugar, use el SDK de Windows Media Format directamente para crear una instancia del objeto de lector sincrónico, abrir el archivo, obtener la marca de tiempo asociada a un marco especificado y, a continuación, usar la interfaz **IMediaSeeking** de DirectShow para buscar a esa hora.</span><span class="sxs-lookup"><span data-stu-id="76b2e-106">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="76b2e-107">La [**interfaz IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) no admite la búsqueda precisa de fotogramas del contenido basado en Windows Media.</span><span class="sxs-lookup"><span data-stu-id="76b2e-107">The [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface does not support frame-accurate seeking of Windows Media–based content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76b2e-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76b2e-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76b2e-109">Lectura de archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="76b2e-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



