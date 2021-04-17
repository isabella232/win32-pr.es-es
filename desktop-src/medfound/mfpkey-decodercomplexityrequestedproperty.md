---
description: Especifica la plantilla de conformidad del dispositivo que desea usar para la codificación de vídeo.
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: Propiedad MFPKEY_DECODERCOMPLEXITYREQUESTED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e017361d7e8267d33ecb2cfdbce2a6e79758fac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696950"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a><span data-ttu-id="fedb5-103">\_Propiedad DECODERCOMPLEXITYREQUESTED de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="fedb5-103">MFPKEY\_DECODERCOMPLEXITYREQUESTED Property</span></span>

<span data-ttu-id="fedb5-104">Especifica la plantilla de conformidad del dispositivo que desea usar para la codificación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fedb5-104">Specifies the device conformance template that you want to use for video encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="fedb5-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fedb5-105">Data Type</span></span>

<span data-ttu-id="fedb5-106">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="fedb5-106">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="fedb5-107">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="fedb5-107">Default Value</span></span>

<span data-ttu-id="fedb5-108">1</span><span class="sxs-lookup"><span data-stu-id="fedb5-108">1</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="fedb5-109">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="fedb5-109">Constant for IPropertyBag</span></span>

<span data-ttu-id="fedb5-110">g \_ wszWMVCDecoderComplexityRequested</span><span class="sxs-lookup"><span data-stu-id="fedb5-110">g\_wszWMVCDecoderComplexityRequested</span></span>

## <a name="data-type-for-ipropertybag"></a><span data-ttu-id="fedb5-111">Tipo de datos de IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="fedb5-111">Data Type for IPropertyBag</span></span>

<span data-ttu-id="fedb5-112">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="fedb5-112">VT\_BSTR</span></span>

## <a name="default-value-for-ipropertybag"></a><span data-ttu-id="fedb5-113">Valor predeterminado de IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="fedb5-113">Default Value for IPropertyBag</span></span>

<span data-ttu-id="fedb5-114">MP</span><span class="sxs-lookup"><span data-stu-id="fedb5-114">"MP"</span></span>

## <a name="remarks"></a><span data-ttu-id="fedb5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fedb5-115">Remarks</span></span>

<span data-ttu-id="fedb5-116">El códec intentará codificar el contenido mediante la plantilla de conformidad del dispositivo especificada por este valor.</span><span class="sxs-lookup"><span data-stu-id="fedb5-116">The codec will attempt to encode the content using the device conformance template specified by this value.</span></span> <span data-ttu-id="fedb5-117">La plantilla real a la que se ajusta el contenido codificado se puede recuperar de la propiedad [MFPKEY \_ DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) después de la codificación.</span><span class="sxs-lookup"><span data-stu-id="fedb5-117">The actual template to which the encoded content conforms can be retrieved from the [MFPKEY\_DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) property after encoding.</span></span>

<span data-ttu-id="fedb5-118">Esta propiedad debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fedb5-118">This property must be one of the following values.</span></span>



| <span data-ttu-id="fedb5-119">Valor de IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="fedb5-119">Value for IPropertyStore</span></span> | <span data-ttu-id="fedb5-120">Valor de IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="fedb5-120">Value for IPropertyBag</span></span> | <span data-ttu-id="fedb5-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="fedb5-121">Description</span></span>         |
|--------------------------|------------------------|---------------------|
| <span data-ttu-id="fedb5-122">0</span><span class="sxs-lookup"><span data-stu-id="fedb5-122">0</span></span>                        | <span data-ttu-id="fedb5-123">DAÑADO</span><span class="sxs-lookup"><span data-stu-id="fedb5-123">"SP"</span></span>                   | <span data-ttu-id="fedb5-124">Perfil simple</span><span class="sxs-lookup"><span data-stu-id="fedb5-124">simple profile</span></span>      |
| <span data-ttu-id="fedb5-125">1</span><span class="sxs-lookup"><span data-stu-id="fedb5-125">1</span></span>                        | <span data-ttu-id="fedb5-126">MP</span><span class="sxs-lookup"><span data-stu-id="fedb5-126">"MP"</span></span>                   | <span data-ttu-id="fedb5-127">Perfil principal</span><span class="sxs-lookup"><span data-stu-id="fedb5-127">main profile</span></span>        |
| <span data-ttu-id="fedb5-128">2</span><span class="sxs-lookup"><span data-stu-id="fedb5-128">2</span></span>                        | <span data-ttu-id="fedb5-129">CP</span><span class="sxs-lookup"><span data-stu-id="fedb5-129">"CP"</span></span>                   | <span data-ttu-id="fedb5-130">ya no se admite</span><span class="sxs-lookup"><span data-stu-id="fedb5-130">no longer supported</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="fedb5-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fedb5-131">Requirements</span></span>



| <span data-ttu-id="fedb5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="fedb5-132">Requirement</span></span> | <span data-ttu-id="fedb5-133">Value</span><span class="sxs-lookup"><span data-stu-id="fedb5-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fedb5-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fedb5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fedb5-135">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fedb5-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fedb5-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fedb5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fedb5-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fedb5-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fedb5-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fedb5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="fedb5-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fedb5-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fedb5-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="fedb5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fedb5-141">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fedb5-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




