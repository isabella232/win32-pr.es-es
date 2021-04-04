---
description: Especifica la complejidad del algoritmo de codificación.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: Propiedad MFPKEY_ENCCOMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f50e7966a05affe8ae75869b670cf75f088b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908782"
---
# <a name="mfpkey_enccomplexity-property"></a><span data-ttu-id="0e65d-103">\_Propiedad ENCCOMPLEXITY de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="0e65d-103">MFPKEY\_ENCCOMPLEXITY Property</span></span>

<span data-ttu-id="0e65d-104">Especifica la complejidad del algoritmo de codificación.</span><span class="sxs-lookup"><span data-stu-id="0e65d-104">Specifies the complexity of the encoding algorithm.</span></span> <span data-ttu-id="0e65d-105">El valor es un entero comprendido entre 0 y 100, donde 0 especifica el algoritmo menos complejo y 100 especifica el algoritmo más complejo.</span><span class="sxs-lookup"><span data-stu-id="0e65d-105">The value is an integer between 0 and 100, where 0 specifies the least complex algorithm, and 100 specifies the most complex algorithm.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0e65d-106">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0e65d-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="0e65d-107">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="0e65d-107">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="0e65d-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0e65d-108">Data Type</span></span>

<span data-ttu-id="0e65d-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="0e65d-109">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="0e65d-110">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0e65d-110">Default Value</span></span>

<span data-ttu-id="0e65d-111">100 para Windows Media Audio 10 y Windows Media Audio 10 Professional</span><span class="sxs-lookup"><span data-stu-id="0e65d-111">100 for Windows Media Audio 10 and Windows Media Audio 10 Professional</span></span>

<span data-ttu-id="0e65d-112">100 para la versión de Windows Vista de Windows Media Audio 10 Lossless</span><span class="sxs-lookup"><span data-stu-id="0e65d-112">100 for the Windows Vista release of Windows Media Audio 10 Lossless</span></span>

<span data-ttu-id="0e65d-113">0 para Windows 7 Release Windows Media Audio 10 Lossless</span><span class="sxs-lookup"><span data-stu-id="0e65d-113">0 for the Windows 7 release Windows Media Audio 10 Lossless</span></span>

## <a name="remarks"></a><span data-ttu-id="0e65d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e65d-114">Remarks</span></span>

<span data-ttu-id="0e65d-115">Si la [**propiedad \_ CONSTRAINECOMPLEXITY de MFPKEY**](mfpkey-constrainenccomplexityproperty.md) tiene un valor de **Variant \_ true**, el codificador ajusta la complejidad de su algoritmo según el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0e65d-115">If the [**MFPKEY\_CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) property has a value of **VARIANT\_TRUE**, the encoder adjusts the complexity of its algorithm according to the value of this property.</span></span>

<span data-ttu-id="0e65d-116">En el caso del codificador Windows Media Audio 10 y el codificador Windows Media Audio 10 Professional, si el valor de esta propiedad es 100, el codificador coloca una gran demanda en la CPU y genera la salida de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="0e65d-116">For the Windows Media Audio 10 encoder and the Windows Media Audio 10 Professional encoder, if the value of this property is 100, the encoder places a high demand on the CPU and produces the highest quality output.</span></span> <span data-ttu-id="0e65d-117">A medida que se reduce el valor de esta propiedad, se reduce la demanda de la CPU, pero también se reduce la calidad de la salida.</span><span class="sxs-lookup"><span data-stu-id="0e65d-117">As the value of this property decreases, the demand on the CPU decreases, but the quality of the output also decreases.</span></span>

<span data-ttu-id="0e65d-118">En el caso del codificador de Windows Media Audio 10 sin pérdida de código, si el valor de esta propiedad es 0, el codificador pone una demanda baja en la CPU.</span><span class="sxs-lookup"><span data-stu-id="0e65d-118">For the Windows Media Audio 10 Lossless encoder, if the value of this property is 0, the encoder places a low demand on the CPU.</span></span> <span data-ttu-id="0e65d-119">A medida que aumenta el valor de esta propiedad, aumenta la demanda de la CPU y el tamaño de la salida del codificador se reduce ligeramente.</span><span class="sxs-lookup"><span data-stu-id="0e65d-119">As the value of this property increases, the demand on the CPU increases, and the size of the encoder output decreases slightly.</span></span> <span data-ttu-id="0e65d-120">La salida es sin pérdida, independientemente del valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0e65d-120">The output is lossless regardless of the value of this property.</span></span>

<span data-ttu-id="0e65d-121">Si deja esta propiedad en su valor predeterminado de **Variant \_ false**, el codificador utiliza su algoritmo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0e65d-121">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder uses its default algorithm.</span></span> <span data-ttu-id="0e65d-122">El algoritmo predeterminado depende del codificador que esté usando y de la versión de Windows que se esté ejecutando.</span><span class="sxs-lookup"><span data-stu-id="0e65d-122">The default algorithm depends on which encoder you are using and which version of Windows is running.</span></span> <span data-ttu-id="0e65d-123">En la tabla siguiente se describe el comportamiento predeterminado de las distintas combinaciones.</span><span class="sxs-lookup"><span data-stu-id="0e65d-123">The following table describes the default behavior for the different combinations.</span></span>



| <span data-ttu-id="0e65d-124">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0e65d-124">Operating system</span></span> | <span data-ttu-id="0e65d-125">Comportamiento predeterminado</span><span class="sxs-lookup"><span data-stu-id="0e65d-125">Default behavior</span></span>                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e65d-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e65d-126">Windows Vista</span></span>    | <span data-ttu-id="0e65d-127">Los codificadores Windows Media Audio 10, Windows Media Audio 10 Professional y Windows Media Audio 10 sin pérdida utilizan el algoritmo más complejo de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0e65d-127">The Windows Media Audio 10, Windows Media Audio 10 Professional, and Windows Media Audio 10 Lossless encoders all use the most complex algorithm by default.</span></span>                                                    |
| <span data-ttu-id="0e65d-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e65d-128">Windows 7</span></span>        | <span data-ttu-id="0e65d-129">Los codificadores Windows Media Audio 10 y Windows Media Audio 10 Professional usan el algoritmo más complejo de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0e65d-129">The Windows Media Audio 10 and Windows Media Audio 10 Professional encoders use the most complex algorithm by default.</span></span> <span data-ttu-id="0e65d-130">De forma predeterminada, el codificador sin pérdida de Windows Media Audio 10 usa el algoritmo menos complejo.</span><span class="sxs-lookup"><span data-stu-id="0e65d-130">The Windows Media Audio 10 Lossless encoder uses the least complex algorithm by default.</span></span> |



 

<span data-ttu-id="0e65d-131">Si la [**propiedad \_ CONSTRAINECOMPLEXITY de MFPKEY**](mfpkey-constrainenccomplexityproperty.md) tiene un valor de **Variant \_ false**, el codificador omite esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0e65d-131">If the [**MFPKEY\_CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) property has a value of **VARIANT\_FALSE**, the encoder ignores this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e65d-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e65d-132">Requirements</span></span>



| <span data-ttu-id="0e65d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e65d-133">Requirement</span></span> | <span data-ttu-id="0e65d-134">Value</span><span class="sxs-lookup"><span data-stu-id="0e65d-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e65d-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e65d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0e65d-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0e65d-136">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0e65d-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e65d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0e65d-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e65d-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e65d-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e65d-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e65d-140"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e65d-140"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e65d-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e65d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e65d-142">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e65d-142">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
