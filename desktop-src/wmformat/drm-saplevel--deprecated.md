---
title: DRM_SAPLEVEL (desusado)
description: Especifica el nivel de la ruta de acceso de audio seguro (SAP) admitido por la aplicación.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (en desuso) formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43711c6c394761f599271809419a46311265d8b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649467"
---
# <a name="drm_saplevel-deprecated"></a><span data-ttu-id="c25c4-104">DRM \_ SAPLEVEL (desusado)</span><span class="sxs-lookup"><span data-stu-id="c25c4-104">DRM\_SAPLEVEL (deprecated)</span></span>

<span data-ttu-id="c25c4-105">\[**DRM \_ SAPLEVEL** ya no está disponible para su uso a partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c25c4-105">\[**DRM\_SAPLEVEL** is no longer available for use as of Windows Vista.</span></span> <span data-ttu-id="c25c4-106">En su lugar, use el audio de modo de usuario protegido (PUMA) en la biblioteca de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c25c4-106">Instead, use Protected User Mode Audio (PUMA) in the Media Foundation library.</span></span> <span data-ttu-id="c25c4-107">\]</span><span class="sxs-lookup"><span data-stu-id="c25c4-107">\]</span></span>

<span data-ttu-id="c25c4-108">La **propiedad \_ SAPLEVEL de DRM** especifica el nivel de la ruta de acceso de audio seguro (SAP) admitido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c25c4-108">The **DRM\_SAPLEVEL** property specifies the secure audio path (SAP) level supported by your application.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c25c4-109">Constante global</span><span class="sxs-lookup"><span data-stu-id="c25c4-109">Global Constant</span></span>

<span data-ttu-id="c25c4-110">g \_ wszWMDRM \_ SAPLEVEL</span><span class="sxs-lookup"><span data-stu-id="c25c4-110">g\_wszWMDRM\_SAPLEVEL</span></span>

## <a name="data-type"></a><span data-ttu-id="c25c4-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c25c4-111">Data Type</span></span>

<span data-ttu-id="c25c4-112">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="c25c4-112">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="c25c4-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c25c4-113">Remarks</span></span>

<span data-ttu-id="c25c4-114">Se trata de una propiedad de solo escritura que se establece mediante una llamada a [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="c25c4-114">This is a write-only property that is set by calling [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty).</span></span> <span data-ttu-id="c25c4-115">El valor es una representación de cadena de caracteres anchos del nivel de SAP, como L "200".</span><span class="sxs-lookup"><span data-stu-id="c25c4-115">The value is a wide-character string representation of the SAP level, such as L"200".</span></span> <span data-ttu-id="c25c4-116">Los valores admitidos actualmente son 200 y 300.</span><span class="sxs-lookup"><span data-stu-id="c25c4-116">Current supported values are 200 and 300.</span></span>

## <a name="requirements"></a><span data-ttu-id="c25c4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c25c4-117">Requirements</span></span>



| <span data-ttu-id="c25c4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c25c4-118">Requirement</span></span> | <span data-ttu-id="c25c4-119">Value</span><span class="sxs-lookup"><span data-stu-id="c25c4-119">Value</span></span> |
|----------------------------------|--------------------------------|
| <span data-ttu-id="c25c4-120">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c25c4-120">End of client support</span></span><br/> | <span data-ttu-id="c25c4-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c25c4-121">Windows XP</span></span><br/>          |
| <span data-ttu-id="c25c4-122">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="c25c4-122">End of server support</span></span><br/> | <span data-ttu-id="c25c4-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c25c4-123">Windows Server 2003</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c25c4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c25c4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c25c4-125">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="c25c4-125">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 





