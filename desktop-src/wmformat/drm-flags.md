---
title: DRM_Flags
description: La \_ propiedad marcas DRM se usa solo con contenido de la versión 1 de DRM para especificar los derechos que se incluirán en la licencia local.
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f2f8eb2baa401f1bc8519da5ca555a1fe428ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994943"
---
# <a name="drm_flags"></a><span data-ttu-id="7b703-104">\_Marcas DRM</span><span class="sxs-lookup"><span data-stu-id="7b703-104">DRM\_Flags</span></span>

<span data-ttu-id="7b703-105">La **propiedad \_ marcas DRM** se usa solo con contenido de la versión 1 de DRM para especificar los derechos que se incluirán en la licencia local.</span><span class="sxs-lookup"><span data-stu-id="7b703-105">The **DRM\_Flags** property is used with DRM version 1 content only to specify the rights that will be contained in the local license.</span></span> <span data-ttu-id="7b703-106">Los derechos se especifican con valores definidos por el tipo de enumeración de **\_ derechos WMT** .</span><span class="sxs-lookup"><span data-stu-id="7b703-106">Rights are specified with values defined by the **WMT\_RIGHTS** enumeration type.</span></span> <span data-ttu-id="7b703-107">Se puede seleccionar más de un valor combinándolos con el operador bit a bit **or** .</span><span class="sxs-lookup"><span data-stu-id="7b703-107">More than one value can be selected by combining them with the bitwise **OR** operator.</span></span>

## <a name="global-constant"></a><span data-ttu-id="7b703-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="7b703-108">Global Constant</span></span>

<span data-ttu-id="7b703-109">g \_ marcas de wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="7b703-109">g\_wszWMDRM\_Flags</span></span>

## <a name="data-type"></a><span data-ttu-id="7b703-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7b703-110">Data Type</span></span>

<span data-ttu-id="7b703-111">**tipo de WMT \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7b703-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="7b703-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b703-112">Remarks</span></span>

<span data-ttu-id="7b703-113">Al tener acceso a la interfaz **IWMHeaderInfo3** del objeto escritor, puede Agregar o cambiar este valor.</span><span class="sxs-lookup"><span data-stu-id="7b703-113">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="7b703-114">En otros objetos (editor de metadatos, lector y lector sincrónico), este valor es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7b703-114">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span> <span data-ttu-id="7b703-115">Use [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) para establecer esta propiedad al crear el contenido de la versión 1 de DRM.</span><span class="sxs-lookup"><span data-stu-id="7b703-115">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property when creating DRM version 1 content.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b703-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b703-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b703-117">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="7b703-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




