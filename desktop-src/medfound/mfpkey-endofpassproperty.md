---
description: Especifica el final de una fase de codificación.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: Propiedad MFPKEY_ENDOFPASS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a38e03867e11cde944bf902ae52f98cda7b8313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908781"
---
# <a name="mfpkey_endofpass-property"></a><span data-ttu-id="c33e3-103">\_Propiedad ENDOFPASS de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="c33e3-103">MFPKEY\_ENDOFPASS Property</span></span>

<span data-ttu-id="c33e3-104">Especifica el final de una fase de codificación.</span><span class="sxs-lookup"><span data-stu-id="c33e3-104">Specifies the end of an encoding pass.</span></span>

## <a name="data-type"></a><span data-ttu-id="c33e3-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c33e3-105">Data Type</span></span>

<span data-ttu-id="c33e3-106">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="c33e3-106">**VT\_BOOL**</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c33e3-107">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c33e3-107">Constant for IPropertyBag</span></span>

<span data-ttu-id="c33e3-108">g \_ wszWMVCEndOfPass</span><span class="sxs-lookup"><span data-stu-id="c33e3-108">g\_wszWMVCEndOfPass</span></span>

## <a name="data-type-for-ipropertybag"></a><span data-ttu-id="c33e3-109">Tipo de datos de IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c33e3-109">Data Type for IPropertyBag</span></span>

<span data-ttu-id="c33e3-110">No se requiere ningún tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c33e3-110">No data type is required.</span></span> <span data-ttu-id="c33e3-111">Para establecer esta propiedad, pase una **variante** no inicializada.</span><span class="sxs-lookup"><span data-stu-id="c33e3-111">To set this property, pass an uninitialized **VARIANT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c33e3-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c33e3-112">Remarks</span></span>

<span data-ttu-id="c33e3-113">Esta propiedad no es una propiedad normal porque tiene el mismo efecto sin tener en cuenta si el valor es VARIANT \_ true o Variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="c33e3-113">This property is not a normal property because it has the same effect regardless of whether the value is VARIANT\_TRUE or VARIANT\_FALSE.</span></span> <span data-ttu-id="c33e3-114">Debe establecer esta propiedad después de procesar los últimos ejemplos de entrada para un paso de preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="c33e3-114">You must set this property after you process the last input samples for a preprocessing pass.</span></span> <span data-ttu-id="c33e3-115">Si va a realizar varias fases, debe establecer esta propiedad al final de cada paso de preprocesamiento (en la actualidad ninguno de los códecs admite más de una).</span><span class="sxs-lookup"><span data-stu-id="c33e3-115">If you are performing multiple passes, you must set this property at the end of each preprocessing pass (at present none of the codecs supports more than one).</span></span> <span data-ttu-id="c33e3-116">Si no establece esta propiedad, el códec asumirá que sigue pasando ejemplos para el preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="c33e3-116">If you do not set this property, the codec will assume that you are still passing samples for preprocessing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c33e3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c33e3-117">Requirements</span></span>



| <span data-ttu-id="c33e3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c33e3-118">Requirement</span></span> | <span data-ttu-id="c33e3-119">Value</span><span class="sxs-lookup"><span data-stu-id="c33e3-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c33e3-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c33e3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c33e3-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c33e3-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c33e3-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c33e3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c33e3-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c33e3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c33e3-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c33e3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c33e3-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c33e3-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c33e3-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c33e3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c33e3-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c33e3-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




