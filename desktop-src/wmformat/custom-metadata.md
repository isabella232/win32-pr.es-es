---
title: Metadatos personalizados
description: Metadatos personalizados
ms.assetid: 86132163-da56-416a-9539-874d18972932
keywords:
- SDK de Windows Media Format, metadatos personalizados
- Advanced Systems Format (ASF), metadatos personalizados
- ASF (formato de sistemas avanzados), metadatos personalizados
- SDK de Windows Media Format, interfaz IWMHeaderInfo3
- Advanced Systems Format (ASF), IWMHeaderInfo3 (interfaz)
- ASF (formato de sistemas avanzados), interfaz IWMHeaderInfo3
- metadatos, personalizar
- IWMHeaderInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a795ab184e5bd6120278f61c0d3654679fd79c28
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "103789166"
---
# <a name="custom-metadata"></a><span data-ttu-id="95110-111">Metadatos personalizados</span><span class="sxs-lookup"><span data-stu-id="95110-111">Custom Metadata</span></span>

<span data-ttu-id="95110-112">Además de los muchos atributos admitidos que se proporcionan con el SDK de Windows Media Format, puede crear atributos de metadatos para sus propias especificaciones.</span><span class="sxs-lookup"><span data-stu-id="95110-112">In addition to the many supported attributes provided with the Windows Media Format SDK, you can create metadata attributes to your own specifications.</span></span> <span data-ttu-id="95110-113">Al crear atributos de metadatos personalizados, debe utilizar una Convención de nomenclatura fácilmente identificable para evitar posibles conflictos con los atributos creados por otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="95110-113">When creating custom metadata attributes, you should use an easily identifiable naming convention to avoid possible conflict with attributes created by others.</span></span>

<span data-ttu-id="95110-114">Se recomienda usar los métodos de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) para crear los metadatos debido a la flexibilidad agregada que proporcionan a través de los métodos de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span><span class="sxs-lookup"><span data-stu-id="95110-114">It is recommended that you use the methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) to create your metadata because of the added flexibility they provide over the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span></span>

## <a name="related-topics"></a><span data-ttu-id="95110-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95110-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95110-116">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="95110-116">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="95110-117">**Características de metadatos**</span><span class="sxs-lookup"><span data-stu-id="95110-117">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="95110-118">**Trabajar con metadatos**</span><span class="sxs-lookup"><span data-stu-id="95110-118">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




