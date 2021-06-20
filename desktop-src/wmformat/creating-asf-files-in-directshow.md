---
title: Creación de archivos ASF en DirectShow (Windows Media Format SDK 11)
description: Obtenga información sobre cómo crear archivos ASF en DirectShow mediante el SDK Windows Media Format 11. ASF es un formato de contenedor que puede contener cualquier tipo de datos.
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK, creación de archivos ASF en DirectShow
- Windows Media Format SDK,DirectShow
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- Formato de sistemas avanzados (ASF), crear en DirectShow
- ASF (formato de sistemas avanzados), crear en DirectShow
- DirectShow, crear archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e06b6deb6dc9f07115f8143309d32dcf4a58a0f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406188"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="908cd-111">Creación de archivos ASF en DirectShow (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="908cd-111">Creating ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="908cd-112">Puede usar DirectShow para crear archivos ASF directamente desde orígenes de captura, como cámaras de vídeo DV, o para transcodificar otros archivos en Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="908cd-112">You can use DirectShow to create ASF files directly from capture sources such as DV camcorders or to transcode other files into Windows Media Format.</span></span> <span data-ttu-id="908cd-113">En cualquier escenario, las aplicaciones crean gráficos de filtro que incluyen el filtro [WM ASF Writer](wm-asf-writer-filter.md) como representador.</span><span class="sxs-lookup"><span data-stu-id="908cd-113">In either scenario, applications create filter graphs that include the [WM ASF Writer](wm-asf-writer-filter.md) filter as the renderer.</span></span>

<span data-ttu-id="908cd-114">WM ASF Writer proporciona un contenedor parcial para el SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="908cd-114">The WM ASF Writer provides a partial wrapper for the Windows Media Format SDK.</span></span> <span data-ttu-id="908cd-115">Las aplicaciones pueden usar la interfaz [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) del filtro para pasar un perfil del sistema (versiones 4, 7 o 8) o usar el SDK de Windows Media Format directamente para crear un perfil personalizado para pasar al filtro.</span><span class="sxs-lookup"><span data-stu-id="908cd-115">Applications can use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface of the filter to pass in a system profile (versions 4, 7, or 8), or use the Windows Media Format SDK directly to create a custom profile to pass to the filter.</span></span> <span data-ttu-id="908cd-116">Para agregar metadatos y otra información de encabezado, la aplicación usa la [**interfaz IWMHeaderInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) que se puede obtener del filtro.</span><span class="sxs-lookup"><span data-stu-id="908cd-116">To add metadata and other header information, the application uses the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which can be obtained from the filter.</span></span> <span data-ttu-id="908cd-117">Una vez configurados el perfil y los metadatos, la aplicación puede ejecutar simplemente el gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="908cd-117">After the profile and metadata have been configured, the application can simply run the filter graph.</span></span> <span data-ttu-id="908cd-118">Internamente, el filtro usa Windows Media Format SDK para escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="908cd-118">Internally, the filter uses the Windows Media Format SDK to write the file.</span></span> <span data-ttu-id="908cd-119">El filtro controla todos los detalles de sincronización de audio y vídeo, que de lo contrario serían responsabilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="908cd-119">The filter handles all the audio-video synchronization details, which would otherwise be the responsibility of the application.</span></span>

<span data-ttu-id="908cd-120">Este proceso se explica con más detalle en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="908cd-120">This process is explained in more detail in the following sections.</span></span>



| <span data-ttu-id="908cd-121">Sección</span><span class="sxs-lookup"><span data-stu-id="908cd-121">Section</span></span>                                                                                                           | <span data-ttu-id="908cd-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="908cd-122">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="908cd-123">Configuración de WM ASF Writer (QASF)</span><span class="sxs-lookup"><span data-stu-id="908cd-123">Configuring the WM ASF Writer (QASF)</span></span>](configuring-the-wm-asf-writer--qasf.md)                                   | <span data-ttu-id="908cd-124">Describe cómo configurar el filtro WM ASF Writer.</span><span class="sxs-lookup"><span data-stu-id="908cd-124">Describes how to configure the WM ASF Writer filter.</span></span>                                   |
| [<span data-ttu-id="908cd-125">Creación de gráficos de filtro para escribir archivos ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="908cd-125">Building Filter Graphs to Write ASF Files (QASF)</span></span>](building-filter-graphs-to-write-asf-files--qasf.md)           | <span data-ttu-id="908cd-126">Describe cómo crear gráficos de captura y transcodificación de archivos.</span><span class="sxs-lookup"><span data-stu-id="908cd-126">Describes how to create file-transcoding and capture graphs.</span></span>                           |
| [<span data-ttu-id="908cd-127">Configuración de perfiles y otras propiedades de archivo (QASF)</span><span class="sxs-lookup"><span data-stu-id="908cd-127">Configuring Profiles and Other File Properties (QASF)</span></span>](configuring-profiles-and-other-file-properties--qasf.md) | <span data-ttu-id="908cd-128">Describe cómo realizar varias tareas de configuración de archivos de ASF mediante WM ASF Writer.</span><span class="sxs-lookup"><span data-stu-id="908cd-128">Describes how to perform various ASF file-configuration tasks using the WM ASF Writer.</span></span> |



 

 

 
