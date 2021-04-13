---
title: Crear archivos protegidos
description: Crear archivos protegidos
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- SDK de Windows Media Format, crear archivos protegidos
- SDK de Windows Media Format, archivos protegidos
- Advanced Systems Format (ASF), crear archivos protegidos
- ASF (formato de sistemas avanzados), crear archivos protegidos
- Advanced Systems Format (ASF), archivos protegidos
- ASF (formato de sistemas avanzados), archivos protegidos
- Advanced Systems Format (ASF), WMStubDRM. lib
- ASF (formato de sistemas avanzados), WMStubDRM. lib
- WMStubDRM. lib, crear archivos protegidos
- WMStubDRM. lib, archivos protegidos
- Administración de derechos digitales (DRM), WMStubDRM. lib
- DRM (administración de derechos digitales), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a14d96da924bdb2a307bc804514a1ec3de083
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358682"
---
# <a name="creating-protected-files"></a><span data-ttu-id="8822d-115">Crear archivos protegidos</span><span class="sxs-lookup"><span data-stu-id="8822d-115">Creating Protected Files</span></span>

<span data-ttu-id="8822d-116">Para crear archivos de medios digitales protegidos mediante DRM versión 1 o DRM y versiones posteriores, vincule al archivo WMStubDRM. lib que obtuvo de Microsoft y cree el objeto de escritor.</span><span class="sxs-lookup"><span data-stu-id="8822d-116">To create protected digital media files using either DRM version 1 or DRM versions 7 and later, link to the WMStubDRM.lib file that you obtained from Microsoft, and create the writer object.</span></span> <span data-ttu-id="8822d-117">Para la protección de la versión 1, use la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) para establecer los atributos DRM que desea aplicar.</span><span class="sxs-lookup"><span data-stu-id="8822d-117">For version 1 protection, use the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface to set the DRM attributes you want to apply.</span></span> <span data-ttu-id="8822d-118">Para las versiones 7 y posteriores, use los métodos de la interfaz [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) .</span><span class="sxs-lookup"><span data-stu-id="8822d-118">For versions 7 and later, use the [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) interface methods.</span></span>

<span data-ttu-id="8822d-119">En los temas siguientes se describe en detalle cómo proteger los archivos.</span><span class="sxs-lookup"><span data-stu-id="8822d-119">The following topics describe in detail how to protect files.</span></span>

-   [<span data-ttu-id="8822d-120">Protección de archivos con DRM versión 1</span><span class="sxs-lookup"><span data-stu-id="8822d-120">Protecting Files with DRM Version 1</span></span>](protecting-files-with-drm-version-1.md)
-   [<span data-ttu-id="8822d-121">Protección de archivos con DRM versión 7 o posterior</span><span class="sxs-lookup"><span data-stu-id="8822d-121">Protecting Files with DRM Version 7 or Later</span></span>](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> <span data-ttu-id="8822d-122">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="8822d-122">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8822d-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8822d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8822d-124">**Lista de atributos de DRM**</span><span class="sxs-lookup"><span data-stu-id="8822d-124">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="8822d-125">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="8822d-125">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="8822d-126">**Versiones de DRM**</span><span class="sxs-lookup"><span data-stu-id="8822d-126">**DRM Versions**</span></span>](drm-versions.md)
</dt> <dt>

[<span data-ttu-id="8822d-127">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="8822d-127">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="8822d-128">**Obtención de la biblioteca DRM necesaria**</span><span class="sxs-lookup"><span data-stu-id="8822d-128">**Obtaining the Required DRM Library**</span></span>](obtaining-the-required-drm-library.md)
</dt> <dt>

[<span data-ttu-id="8822d-129">**Leer archivos protegidos**</span><span class="sxs-lookup"><span data-stu-id="8822d-129">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




