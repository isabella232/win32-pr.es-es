---
title: Buscar en archivos ASF (Windows Media Format 11 SDK)
description: Buscar en archivos ASF
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- SDK de Windows Media Format, buscar en archivos ASF
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), buscar
- ASF (formato de sistemas avanzados), búsqueda
- DirectShow, buscar en archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18389ded80f0202564cba0ce6384b5ff02d26fdd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078697"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a><span data-ttu-id="b0dc1-110">Buscar en archivos ASF (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="b0dc1-110">Seeking in ASF Files (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="b0dc1-111">El [lector ASF de WM](wm-asf-reader-filter.md), a través de su interfaz **IMediaSeeking** , puede realizar búsquedas temporales muy precisas en el contenido basado en Windows Media que tiene un índice temporal.</span><span class="sxs-lookup"><span data-stu-id="b0dc1-111">The [WM ASF Reader](wm-asf-reader-filter.md), through its **IMediaSeeking** interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="b0dc1-112">(Todo el contenido indizado de Marcos también contiene un índice temporal). La búsqueda con precisión de fotogramas garantizada no se admite directamente en el lector ASF de WM, pero hay una manera de hacerlo si necesita esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="b0dc1-112">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="b0dc1-113">En primer lugar, use el SDK de Windows Media Format directamente para crear una instancia del objeto lector sincrónico, abra el archivo, obtenga la marca de tiempo asociada a un marco especificado y, a continuación, use la interfaz **IMediaSeeking** de DirectShow para buscar en ese momento.</span><span class="sxs-lookup"><span data-stu-id="b0dc1-113">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="b0dc1-114">La interfaz **IVideoFrameStep** de DirectShow no admite la búsqueda de contenido basado en Windows Media con precisión de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="b0dc1-114">The DirectShow **IVideoFrameStep** interface does not support frame-accurate seeking of Windows Media–based content.</span></span> <span data-ttu-id="b0dc1-115">En el ejemplo DSSeekFm del SDK de Windows Media Format se muestra cómo realizar búsquedas con precisión de fotogramas mediante el lector ASF de WM.</span><span class="sxs-lookup"><span data-stu-id="b0dc1-115">The DSSeekFm sample in the Windows Media Format SDK demonstrates how to perform frame-accurate seeking using the WM ASF Reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0dc1-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b0dc1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0dc1-117">**Filtro de lector ASF de WM**</span><span class="sxs-lookup"><span data-stu-id="b0dc1-117">**WM ASF Reader Filter**</span></span>](wm-asf-reader-filter.md)
</dt> </dl>

 

 




