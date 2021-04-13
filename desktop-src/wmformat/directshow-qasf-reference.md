---
title: Referencia de QASF de DirectShow
description: Referencia de QASF de DirectShow
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- SDK de Windows Media Format, QASF
- Windows Media Format SDK, DirectShow
- DirectShow, referencia de QASF
- Filtros de QASF, referencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c509030f676b83a84f67590a242aea623656a514
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421033"
---
# <a name="directshow-qasf-reference"></a><span data-ttu-id="02385-107">Referencia de QASF de DirectShow</span><span class="sxs-lookup"><span data-stu-id="02385-107">DirectShow QASF Reference</span></span>

<span data-ttu-id="02385-108">Esta sección contiene referencias de programación para los siguientes filtros, interfaces y enumeraciones de QASF de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="02385-108">This section contains programming references for the following DirectShow QASF filters, interfaces and enumerations.</span></span> <span data-ttu-id="02385-109">La documentación del SDK de DirectShow contiene materiales de referencia y de programación para interfaces genéricas adicionales expuestas por estos filtros, como **IBaseFilter** y **IPin**, y para versiones anteriores de los componentes de qasf.</span><span class="sxs-lookup"><span data-stu-id="02385-109">The DirectShow SDK documentation contains reference and programming guide materials for additional generic interfaces exposed by these filters, such as **IBaseFilter** and **IPin**, and for earlier versions of the QASF components.</span></span>

<span data-ttu-id="02385-110">Para obtener una explicación del nombre de QASF, consulte [acerca de DirectShow](about-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="02385-110">For an explanation of the QASF name, see [About DirectShow](about-directshow.md).</span></span>

<span data-ttu-id="02385-111">Los siguientes filtros se incluyen con los componentes de QASF de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="02385-111">The following filters are included with the DirectShow QASF components.</span></span>



| <span data-ttu-id="02385-112">Filter</span><span class="sxs-lookup"><span data-stu-id="02385-112">Filter</span></span>                                           | <span data-ttu-id="02385-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="02385-113">Description</span></span>                                                      |
|--------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="02385-114">Filtro de lector ASF de WM</span><span class="sxs-lookup"><span data-stu-id="02385-114">WM ASF Reader Filter</span></span>](wm-asf-reader-filter.md) | <span data-ttu-id="02385-115">Lee y analiza archivos ASF locales o remotos.</span><span class="sxs-lookup"><span data-stu-id="02385-115">Reads and parses local or remote ASF files.</span></span>                      |
| [<span data-ttu-id="02385-116">Filtro de escritor ASF de WM</span><span class="sxs-lookup"><span data-stu-id="02385-116">WM ASF Writer Filter</span></span>](wm-asf-writer-filter.md) | <span data-ttu-id="02385-117">Crea archivos ASF a partir de flujos de entrada comprimidos o sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="02385-117">Creates ASF files from compressed or uncompressed input streams.</span></span> |



 

<span data-ttu-id="02385-118">Las siguientes interfaces se definen para su uso con los componentes de QASF de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="02385-118">The following interfaces are defined for use with the DirectShow QASF components.</span></span>



| <span data-ttu-id="02385-119">Interfaz</span><span class="sxs-lookup"><span data-stu-id="02385-119">Interface</span></span>                                                  | <span data-ttu-id="02385-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="02385-120">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02385-121">**IAMWMBufferPass**</span><span class="sxs-lookup"><span data-stu-id="02385-121">**IAMWMBufferPass**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)                 | <span data-ttu-id="02385-122">Proporciona un método que permite que las aplicaciones se registren para las devoluciones de llamada desde los pines de entrada del [escritor ASF de WM](wm-asf-writer-filter.md) o los clavijas de salida del filtro de [lector ASF de WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="02385-122">Provides a method that enables applications to register for callbacks from the input pins of the [WM ASF Writer](wm-asf-writer-filter.md) or the output pins of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="02385-123">Se usa en la indización y al agregar extensiones de unidad de datos.</span><span class="sxs-lookup"><span data-stu-id="02385-123">Used in indexing and when adding data unit extensions.</span></span> |
| [<span data-ttu-id="02385-124">**IAMWMBufferPassCallback**</span><span class="sxs-lookup"><span data-stu-id="02385-124">**IAMWMBufferPassCallback**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) | <span data-ttu-id="02385-125">Implementado por aplicaciones y llamado por los filtros.</span><span class="sxs-lookup"><span data-stu-id="02385-125">Implemented by applications and called by the filters.</span></span> <span data-ttu-id="02385-126">Las aplicaciones usan el método One en esta interfaz para obtener información sobre los ejemplos individuales de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="02385-126">Applications use the one method on this interface to obtain information about individual samples in the stream.</span></span> <span data-ttu-id="02385-127">Se usa en la indización y al agregar extensiones de unidad de datos.</span><span class="sxs-lookup"><span data-stu-id="02385-127">Used in indexing and when adding data unit extensions.</span></span>                                                 |
| <span data-ttu-id="02385-128">[**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="02385-128">[**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>               | <span data-ttu-id="02385-129">Implementado en el escritor ASF de WM.</span><span class="sxs-lookup"><span data-stu-id="02385-129">Implemented on the WM ASF Writer.</span></span> <span data-ttu-id="02385-130">Lo usan las aplicaciones para especificar los perfiles y los parámetros de indización para el archivo.</span><span class="sxs-lookup"><span data-stu-id="02385-130">Used by applications to specify profiles and indexing parameters for the file.</span></span>                                                                                                                                                              |
| <span data-ttu-id="02385-131">[**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="02385-131">[**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>             | <span data-ttu-id="02385-132">Proporciona funciones de configuración adicionales en el escritor ASF de WM.</span><span class="sxs-lookup"><span data-stu-id="02385-132">Provides additional configuration functions on the WM ASF Writer.</span></span>                                                                                                                                                                                                             |



 

<span data-ttu-id="02385-133">La enumeración, la estructura y los eventos siguientes se definen para su uso con los componentes de QASF de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="02385-133">The following enumeration, structure, and events are defined for use with the DirectShow QASF components.</span></span>



| <span data-ttu-id="02385-134">Enumeración</span><span class="sxs-lookup"><span data-stu-id="02385-134">Enumeration</span></span>                                                               | <span data-ttu-id="02385-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="02385-135">Description</span></span>                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02385-136">[\_\_parámetro ASFWRITERCONFIG \_ AM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="02385-136">[\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))</span></span> | <span data-ttu-id="02385-137">Define los parámetros de configuración de filtro utilizados en los métodos [**IConfigAsfWriter2:: GetParam**](iconfigasfwriter2-getparam.md) y [**SetParam**](iconfigasfwriter2-setparam.md) .</span><span class="sxs-lookup"><span data-stu-id="02385-137">Defines filter configuration parameters used in the [**IConfigAsfWriter2::GetParam**](iconfigasfwriter2-getparam.md) and [**SetParam**](iconfigasfwriter2-setparam.md) methods.</span></span> |



 



| <span data-ttu-id="02385-138">Estructura</span><span class="sxs-lookup"><span data-stu-id="02385-138">Structure</span></span>                                         | <span data-ttu-id="02385-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="02385-139">Description</span></span>                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02385-140">**\_datos de \_ evento \_ WMT de AM**</span><span class="sxs-lookup"><span data-stu-id="02385-140">**AM\_WMT\_EVENT\_DATA**</span></span>](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | <span data-ttu-id="02385-141">Contiene información relativa a un evento [**de \_ Estado de WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) y el código de estado asociado devuelto por el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="02385-141">Contains information pertaining to a [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) event and the associated status code returned by the Windows Media Format SDK.</span></span> |



 



| <span data-ttu-id="02385-142">Evento</span><span class="sxs-lookup"><span data-stu-id="02385-142">Event</span></span>                                           | <span data-ttu-id="02385-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="02385-143">Description</span></span>                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02385-144">\_evento WMT de EC \_</span><span class="sxs-lookup"><span data-stu-id="02385-144">EC\_WMT\_EVENT</span></span>](ec-wmt-event.md)              | <span data-ttu-id="02385-145">Evento reenviado desde el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="02385-145">Event forwarded from the Windows Media Format SDK.</span></span>                                                              |
| [<span data-ttu-id="02385-146">\_evento de \_ Índice \_ WMT de EC</span><span class="sxs-lookup"><span data-stu-id="02385-146">EC\_WMT\_INDEX\_EVENT</span></span>](ec-wmt-index-event.md) | <span data-ttu-id="02385-147">Se envía cuando una aplicación utiliza el [escritor ASF de WM](wm-asf-writer-filter.md) para indizar Windows Media Video archivos.</span><span class="sxs-lookup"><span data-stu-id="02385-147">Sent when an application uses the [WM ASF Writer](wm-asf-writer-filter.md) to index Windows Media Video files.</span></span> |



 

 

 