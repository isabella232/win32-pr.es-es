---
description: Buscar en archivos ASF
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Buscar en archivos ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e957fbdf7ed7df1a9cb38b14e39d384b15ab25b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537119"
---
# <a name="seeking-in-asf-files-directshow"></a><span data-ttu-id="5fb77-103">Buscar en archivos ASF (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="5fb77-103">Seeking in ASF Files (DirectShow)</span></span>

<span data-ttu-id="5fb77-104">El [lector ASF de WM](wm-asf-reader-filter.md), a través de su interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , puede realizar búsquedas temporales muy precisas en el contenido basado en Windows Media que tiene un índice temporal.</span><span class="sxs-lookup"><span data-stu-id="5fb77-104">The [WM ASF Reader](wm-asf-reader-filter.md), through its [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="5fb77-105">(Todo el contenido indizado de Marcos también contiene un índice temporal). La búsqueda con precisión de fotogramas garantizada no se admite directamente en el lector ASF de WM, pero hay una manera de hacerlo si necesita esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="5fb77-105">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="5fb77-106">En primer lugar, use el SDK de Windows Media Format directamente para crear una instancia del objeto lector sincrónico, abra el archivo, obtenga la marca de tiempo asociada a un marco especificado y, a continuación, use la interfaz **IMediaSeeking** de DirectShow para buscar en ese momento.</span><span class="sxs-lookup"><span data-stu-id="5fb77-106">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="5fb77-107">La interfaz [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) no admite la búsqueda de contenido basado en Windows Media con precisión de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="5fb77-107">The [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface does not support frame-accurate seeking of Windows Media–based content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fb77-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5fb77-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fb77-109">Leer archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="5fb77-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



