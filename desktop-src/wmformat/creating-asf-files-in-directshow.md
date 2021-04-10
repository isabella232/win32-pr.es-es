---
title: Crear archivos ASF en DirectShow (Windows Media Format 11 SDK)
description: Crear archivos ASF en DirectShow
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- SDK de Windows Media Format, crear archivos ASF en DirectShow
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), crear en DirectShow
- ASF (formato de sistemas avanzados), crear en DirectShow
- DirectShow, crear archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe4a6a37a508e5d7c713ae4cf38d771d075cefa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149785"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="bf7ce-110">Crear archivos ASF en DirectShow (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="bf7ce-110">Creating ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="bf7ce-111">Puede usar DirectShow para crear archivos ASF directamente desde orígenes de captura, como videocámaras DV, o para transcodificar otros archivos en el formato de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bf7ce-111">You can use DirectShow to create ASF files directly from capture sources such as DV camcorders or to transcode other files into Windows Media Format.</span></span> <span data-ttu-id="bf7ce-112">En cualquier escenario, las aplicaciones crean gráficos de filtro que incluyen el filtro de [escritor ASF de WM](wm-asf-writer-filter.md) como representador.</span><span class="sxs-lookup"><span data-stu-id="bf7ce-112">In either scenario, applications create filter graphs that include the [WM ASF Writer](wm-asf-writer-filter.md) filter as the renderer.</span></span>

<span data-ttu-id="bf7ce-113">El escritor ASF de WM proporciona un contenedor parcial para el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="bf7ce-113">The WM ASF Writer provides a partial wrapper for the Windows Media Format SDK.</span></span> <span data-ttu-id="bf7ce-114">Las aplicaciones pueden usar la interfaz [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) del filtro para pasar un perfil del sistema (versiones 4, 7 u 8), o bien usar el SDK de Windows Media Format directamente para crear un perfil personalizado y pasarlo al filtro.</span><span class="sxs-lookup"><span data-stu-id="bf7ce-114">Applications can use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface of the filter to pass in a system profile (versions 4, 7, or 8), or use the Windows Media Format SDK directly to create a custom profile to pass to the filter.</span></span> <span data-ttu-id="bf7ce-115">Para agregar metadatos y otra información de encabezado, la aplicación usa la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , que se puede obtener del filtro.</span><span class="sxs-lookup"><span data-stu-id="bf7ce-115">To add metadata and other header information, the application uses the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which can be obtained from the filter.</span></span> <span data-ttu-id="bf7ce-116">Una vez configurados el perfil y los metadatos, la aplicación puede simplemente ejecutar el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="bf7ce-116">After the profile and metadata have been configured, the application can simply run the filter graph.</span></span> <span data-ttu-id="bf7ce-117">Internamente, el filtro usa el SDK de Windows Media Format para escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="bf7ce-117">Internally, the filter uses the Windows Media Format SDK to write the file.</span></span> <span data-ttu-id="bf7ce-118">El filtro controla todos los detalles de la sincronización de audio y vídeo, que de otro modo sería responsabilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bf7ce-118">The filter handles all the audio-video synchronization details, which would otherwise be the responsibility of the application.</span></span>

<span data-ttu-id="bf7ce-119">Este proceso se explica con más detalle en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="bf7ce-119">This process is explained in more detail in the following sections.</span></span>



| <span data-ttu-id="bf7ce-120">Sección</span><span class="sxs-lookup"><span data-stu-id="bf7ce-120">Section</span></span>                                                                                                           | <span data-ttu-id="bf7ce-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf7ce-121">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf7ce-122">Configuración del escritor ASF de WM (QASF)</span><span class="sxs-lookup"><span data-stu-id="bf7ce-122">Configuring the WM ASF Writer (QASF)</span></span>](configuring-the-wm-asf-writer--qasf.md)                                   | <span data-ttu-id="bf7ce-123">Describe cómo configurar el filtro del escritor ASF de WM.</span><span class="sxs-lookup"><span data-stu-id="bf7ce-123">Describes how to configure the WM ASF Writer filter.</span></span>                                   |
| [<span data-ttu-id="bf7ce-124">Generar gráficos de filtro para escribir archivos ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="bf7ce-124">Building Filter Graphs to Write ASF Files (QASF)</span></span>](building-filter-graphs-to-write-asf-files--qasf.md)           | <span data-ttu-id="bf7ce-125">Describe cómo crear gráficos de captura y de transcodificación de archivos.</span><span class="sxs-lookup"><span data-stu-id="bf7ce-125">Describes how to create file-transcoding and capture graphs.</span></span>                           |
| [<span data-ttu-id="bf7ce-126">Configuración de perfiles y otras propiedades de archivo (QASF)</span><span class="sxs-lookup"><span data-stu-id="bf7ce-126">Configuring Profiles and Other File Properties (QASF)</span></span>](configuring-profiles-and-other-file-properties--qasf.md) | <span data-ttu-id="bf7ce-127">Describe cómo realizar diversas tareas de configuración de archivos ASF mediante el escritor ASF de WM.</span><span class="sxs-lookup"><span data-stu-id="bf7ce-127">Describes how to perform various ASF file-configuration tasks using the WM ASF Writer.</span></span> |



 

 

 
