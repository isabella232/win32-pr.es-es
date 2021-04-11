---
description: Ajusta el matiz.
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: Propiedad MFPKEY_COLOR_HUE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ddf0109090bfb56102560dc06a853c970e7ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156097"
---
# <a name="mfpkey_color_hue-property"></a><span data-ttu-id="2676d-103">\_Propiedad matiz de color MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="2676d-103">MFPKEY\_COLOR\_HUE Property</span></span>

<span data-ttu-id="2676d-104">Ajusta el matiz.</span><span class="sxs-lookup"><span data-stu-id="2676d-104">Adjusts the hue.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2676d-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2676d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2676d-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="2676d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="2676d-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2676d-107">Data Type</span></span>

<span data-ttu-id="2676d-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2676d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="2676d-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2676d-109">Default Value</span></span>

<span data-ttu-id="2676d-110">0</span><span class="sxs-lookup"><span data-stu-id="2676d-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="2676d-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="2676d-111">Applies To</span></span>

-   [<span data-ttu-id="2676d-112">DSP de transformación de control de color</span><span class="sxs-lookup"><span data-stu-id="2676d-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="2676d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2676d-113">Remarks</span></span>

<span data-ttu-id="2676d-114">El ajuste de matiz se realiza mediante la combinación de los valores CB y CR.</span><span class="sxs-lookup"><span data-stu-id="2676d-114">Hue adjustment is performed by mixing the Cb and Cr values.</span></span> <span data-ttu-id="2676d-115">(Si CB y CR están trazados en un espacio de 2 dimensiones, el ajuste de matiz se realiza girando alrededor del origen).</span><span class="sxs-lookup"><span data-stu-id="2676d-115">(If Cb and Cr are plotted in a 2-dimensional space, hue adjustment is performed by rotating around the origin.)</span></span>

<span data-ttu-id="2676d-116">Esta propiedad tiene un intervalo de-127 a 127.</span><span class="sxs-lookup"><span data-stu-id="2676d-116">This property has a range of -127 to 127.</span></span> <span data-ttu-id="2676d-117">Cero indica que no hay ningún cambio en el matiz.</span><span class="sxs-lookup"><span data-stu-id="2676d-117">Zero indicates no change in hue.</span></span>

## <a name="requirements"></a><span data-ttu-id="2676d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2676d-118">Requirements</span></span>



| <span data-ttu-id="2676d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2676d-119">Requirement</span></span> | <span data-ttu-id="2676d-120">Value</span><span class="sxs-lookup"><span data-stu-id="2676d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2676d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2676d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2676d-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2676d-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2676d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2676d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2676d-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2676d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2676d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2676d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2676d-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2676d-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2676d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2676d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2676d-128">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2676d-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
