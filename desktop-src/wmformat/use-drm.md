---
title: Use_DRM
description: El \_ atributo use DRM indica al objeto de escritor que aplique la protección de DRM versión 1 al archivo actual.
ms.assetid: ad959e4a-faf7-4b61-9988-6878afcf3a90
keywords:
- Use_DRM formato de Windows Media
topic_type:
- apiref
api_name:
- Use_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fcb010855ac4660792a7c579556001d5d7c4c96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104532974"
---
# <a name="use_drm"></a><span data-ttu-id="9c8bb-104">Usar \_ DRM</span><span class="sxs-lookup"><span data-stu-id="9c8bb-104">Use\_DRM</span></span>

<span data-ttu-id="9c8bb-105">El atributo **use \_ DRM** indica al objeto de escritor que aplique la protección de DRM versión 1 al archivo actual.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-105">The **Use\_DRM** attribute instructs the writer object to apply DRM version 1 protection to the current file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="9c8bb-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="9c8bb-106">Global Constant</span></span>

<span data-ttu-id="9c8bb-107">g \_ wszWMUse \_ DRM</span><span class="sxs-lookup"><span data-stu-id="9c8bb-107">g\_wszWMUse\_DRM</span></span>

## <a name="data-type"></a><span data-ttu-id="9c8bb-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9c8bb-108">Data Type</span></span>

<span data-ttu-id="9c8bb-109">**tipo de WMT \_ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="9c8bb-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="9c8bb-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c8bb-110">Remarks</span></span>

<span data-ttu-id="9c8bb-111">Use [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) para establecer esta propiedad en **true** al crear el contenido de la versión 1 de DRM.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-111">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property to **TRUE** when creating DRM version 1 content.</span></span> <span data-ttu-id="9c8bb-112">No se puede obtener acceso a esta propiedad desde el objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-112">This property is not accessible from the reader object.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c8bb-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c8bb-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c8bb-114">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="9c8bb-114">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




