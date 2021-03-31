---
title: Ver atributos de archivos protegidos
description: Ver atributos de archivos protegidos
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- SDK de Windows Media Format, ver atributos de archivos protegidos
- SDK de Windows Media Format, atributos de archivos protegidos
- SDK de Windows Media Format, archivos protegidos
- Advanced Systems Format (ASF), ver atributos de archivos protegidos
- ASF (formato de sistemas avanzados), ver atributos de archivos protegidos
- Advanced Systems Format (ASF), atributos de archivos protegidos
- ASF (formato de sistemas avanzados), atributos de archivos protegidos
- Advanced Systems Format (ASF), archivos protegidos
- ASF (formato de sistemas avanzados), archivos protegidos
- Administración de derechos digitales (DRM), ver atributos de archivos protegidos
- DRM (administración de derechos digitales), ver atributos de archivos protegidos
- Administración de derechos digitales (DRM), atributos de archivos protegidos
- DRM (administración de derechos digitales), atributos de archivos protegidos
- Administración de derechos digitales (DRM), archivos protegidos
- DRM (administración de derechos digitales), archivos protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642e9f580c3dffa1d3785985d548a5f971cfc218
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788686"
---
# <a name="viewing-attributes-of-protected-files"></a><span data-ttu-id="8a3f5-118">Ver atributos de archivos protegidos</span><span class="sxs-lookup"><span data-stu-id="8a3f5-118">Viewing Attributes of Protected Files</span></span>

<span data-ttu-id="8a3f5-119">En algunos escenarios, puede que necesite recuperar determinados atributos DRM en un archivo sin tener acceso realmente al contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="8a3f5-119">In some scenarios, you may need to retrieve certain DRM attributes in a file without actually accessing the contents of the file.</span></span> <span data-ttu-id="8a3f5-120">Esta funcionalidad es útil, por ejemplo, en aplicaciones que procesan lotes de archivos de maneras diferentes en función de la información del encabezado de archivo.</span><span class="sxs-lookup"><span data-stu-id="8a3f5-120">This capability is useful, for example, in applications that process batches of files in different ways based on information in the file header.</span></span> <span data-ttu-id="8a3f5-121">En versiones anteriores del SDK de Windows Media Format, las aplicaciones tenían que vincularse a la biblioteca estática de DRM para poder abrir cualquier archivo protegido.</span><span class="sxs-lookup"><span data-stu-id="8a3f5-121">In previous versions of the Windows Media Format SDK, applications were required to link to the DRM static library in order to open any protected file.</span></span> <span data-ttu-id="8a3f5-122">Las aplicaciones que no tienen la biblioteca DRM pueden utilizar la interfaz [**IWMDRMEditor:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) en el objeto editor de metadatos para examinar determinados atributos DRM.</span><span class="sxs-lookup"><span data-stu-id="8a3f5-122">Applications that do not have the DRM library can use the [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) interface on the metadata editor object to examine certain DRM attributes.</span></span>

> [!Note]  
> <span data-ttu-id="8a3f5-123">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="8a3f5-123">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8a3f5-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a3f5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a3f5-125">**Lista de atributos de DRM**</span><span class="sxs-lookup"><span data-stu-id="8a3f5-125">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="8a3f5-126">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="8a3f5-126">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="8a3f5-127">**Interfaz IWMDRMEditor**</span><span class="sxs-lookup"><span data-stu-id="8a3f5-127">**IWMDRMEditor Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




