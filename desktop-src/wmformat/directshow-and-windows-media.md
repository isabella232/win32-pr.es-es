---
title: DirectShow y Windows Media
description: DirectShow y Windows Media
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- DirectShow, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779752"
---
# <a name="directshow-and-windows-media"></a><span data-ttu-id="94614-107">DirectShow y Windows Media</span><span class="sxs-lookup"><span data-stu-id="94614-107">DirectShow and Windows Media</span></span>

<span data-ttu-id="94614-108">Como alternativa al uso exclusivo del SDK de Windows Media Format, las aplicaciones también pueden leer y escribir contenido basado en Windows Media mediante la arquitectura de streaming de Microsoft® DirectShow®, tal y como se describe en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="94614-108">As an alternative to using the Windows Media Format SDK exclusively, applications can also read and write Windows Media-based content by using the Microsoft® DirectShow® streaming architecture, as described in the following sections.</span></span>



| <span data-ttu-id="94614-109">Sección</span><span class="sxs-lookup"><span data-stu-id="94614-109">Section</span></span>                                                                                   | <span data-ttu-id="94614-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="94614-110">Description</span></span>                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94614-111">Acerca de DirectShow</span><span class="sxs-lookup"><span data-stu-id="94614-111">About DirectShow</span></span>](about-directshow.md)                                                  | <span data-ttu-id="94614-112">Describe DirectShow en términos generales y indica dónde obtener más información.</span><span class="sxs-lookup"><span data-stu-id="94614-112">Describes DirectShow in general terms and tells where to get more information about it.</span></span>                                                     |
| [<span data-ttu-id="94614-113">¿Por qué usar DirectShow?</span><span class="sxs-lookup"><span data-stu-id="94614-113">Why Use DirectShow?</span></span>](why-use-directshow.md)                                             | <span data-ttu-id="94614-114">Describe cómo DirectShow simplifica ciertas tareas en la creación y reproducción de contenido basado en Windows Media.</span><span class="sxs-lookup"><span data-stu-id="94614-114">Describes how DirectShow simplifies certain tasks in the creation and playback of Windows Media–based content.</span></span>                              |
| [<span data-ttu-id="94614-115">Leer archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="94614-115">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)                    | <span data-ttu-id="94614-116">Describe cómo reproducir archivos ASF con DirectShow.</span><span class="sxs-lookup"><span data-stu-id="94614-116">Describes how to play ASF files using DirectShow.</span></span>                                                                                           |
| [<span data-ttu-id="94614-117">Crear archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="94614-117">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)                  | <span data-ttu-id="94614-118">Describe cómo crear archivos ASF con DirectShow.</span><span class="sxs-lookup"><span data-stu-id="94614-118">Describes how to create ASF files using DirectShow.</span></span>                                                                                         |
| [<span data-ttu-id="94614-119">\_Notificación de eventos de estado de WMT en DirectShow</span><span class="sxs-lookup"><span data-stu-id="94614-119">WMT\_STATUS Event Notification in DirectShow</span></span>](wmt-status-notification-in-directshow.md) | <span data-ttu-id="94614-120">Describe qué eventos de **\_ Estado de WMT** se administran mediante los filtros ASF Reader y ASF Writer, y cómo las aplicaciones pueden recibir esos eventos.</span><span class="sxs-lookup"><span data-stu-id="94614-120">Describes which **WMT\_STATUS** events are handled by the ASF Reader and ASF Writer filters, and how applications can receive those events.</span></span> |
| [<span data-ttu-id="94614-121">Compatibilidad con DRM en DirectShow</span><span class="sxs-lookup"><span data-stu-id="94614-121">DRM Support in DirectShow</span></span>](drm-support-in-directshow.md)                                | <span data-ttu-id="94614-122">Describe cómo leer y escribir archivos protegidos con DRM mediante DirectShow.</span><span class="sxs-lookup"><span data-stu-id="94614-122">Describes how to read and write DRM-protected files through DirectShow.</span></span>                                                                     |
| [<span data-ttu-id="94614-123">Referencia de QASF de DirectShow</span><span class="sxs-lookup"><span data-stu-id="94614-123">DirectShow QASF Reference</span></span>](directshow-qasf-reference.md)                                | <span data-ttu-id="94614-124">Contiene la documentación de referencia de los componentes de DirectShow que admiten Windows Media.</span><span class="sxs-lookup"><span data-stu-id="94614-124">Contains the reference documentation for the DirectShow components that support Windows Media.</span></span>                                              |



 

<span data-ttu-id="94614-125">Tres aplicaciones de ejemplo del SDK ilustran el uso de DirectShow: DSCopy, DSPlay y DSSeekFM.</span><span class="sxs-lookup"><span data-stu-id="94614-125">Three sample applications in the SDK illustrate the use of DirectShow: DSCopy, DSPlay, and DSSeekFM.</span></span> <span data-ttu-id="94614-126">Para obtener más información, vea [aplicaciones de ejemplo](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="94614-126">For more information, see [Sample Applications](sample-applications.md).</span></span>

> [!Note]  
> <span data-ttu-id="94614-127">Las aplicaciones que usan los componentes de QASF incluidos en este SDK requieren que se instale el tiempo de ejecución del SDK de Microsoft DirectX® 8,1 o posterior en los sistemas Windows® 2000, Windows 98 y Windows 95.</span><span class="sxs-lookup"><span data-stu-id="94614-127">Applications that use the QASF components included in this SDK require the Microsoft DirectX® 8.1 or later SDK runtime to be installed on Windows® 2000, Windows 98, and Windows 95 systems.</span></span> <span data-ttu-id="94614-128">En concreto, este tiempo de ejecución es necesario para el filtro de contenedor de DMO que hospeda los códecs de Windows Media en un gráfico de filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="94614-128">Specifically, this runtime is required by the DMO Wrapper filter which hosts the Windows Media codecs in a DirectShow filter graph.</span></span>

 

 

 




