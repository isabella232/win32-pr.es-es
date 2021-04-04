---
title: Leer metadatos en la reproducción
description: Leer metadatos en la reproducción
ms.assetid: 48d37a9e-5e22-4298-abc4-b69998906dcb
keywords:
- SDK de Windows Media Format, leer metadatos
- SDK de Windows Media Format, lectores asincrónicos
- SDK de Windows Media Format, lectores sincrónicos
- Advanced Systems Format (ASF), leer metadatos
- ASF (formato de sistemas avanzados), leer metadatos
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- lectores asincrónicos, leer metadatos
- lectores sincrónicos, leer metadatos
- metadatos, leer en la reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a2515dd62092d02a45b0261fe2b501e0833a31
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077434"
---
# <a name="reading-metadata-at-playback"></a><span data-ttu-id="b484e-115">Leer metadatos en la reproducción</span><span class="sxs-lookup"><span data-stu-id="b484e-115">Reading Metadata at Playback</span></span>

<span data-ttu-id="b484e-116">Tanto el objeto lector asincrónico como el objeto lector sincrónico pueden leer los metadatos desde el encabezado de un archivo ASF cargado.</span><span class="sxs-lookup"><span data-stu-id="b484e-116">Both the asynchronous reader object and the synchronous reader object can read the metadata from the header of a loaded ASF file.</span></span> <span data-ttu-id="b484e-117">Al leer archivos, los atributos de metadatos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b484e-117">When reading files, the metadata attributes are all read-only.</span></span> <span data-ttu-id="b484e-118">Ambos objetos de lector se pueden consultar para las interfaces [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) y [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) .</span><span class="sxs-lookup"><span data-stu-id="b484e-118">Both reader objects can be queried for the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) and [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) interfaces.</span></span>

<span data-ttu-id="b484e-119">Para obtener más información sobre el acceso a los metadatos, vea [trabajar con metadatos](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="b484e-119">For more information about accessing metadata, see [Working with Metadata](working-with-metadata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b484e-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b484e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b484e-121">**Leer archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="b484e-121">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




