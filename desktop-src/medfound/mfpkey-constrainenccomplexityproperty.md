---
description: Especifica si la complejidad del algoritmo de codificación de audio está restringida.
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: Propiedad MFPKEY_CONSTRAINENCOMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696955"
---
# <a name="mfpkey_constrainencomplexity-property"></a><span data-ttu-id="81377-103">\_Propiedad CONSTRAINENCOMPLEXITY de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="81377-103">MFPKEY\_CONSTRAINENCOMPLEXITY Property</span></span>

<span data-ttu-id="81377-104">Especifica si la complejidad del algoritmo de codificación de audio está restringida.</span><span class="sxs-lookup"><span data-stu-id="81377-104">Specifies whether the complexity of the audio encoding algorithm is constrained.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="81377-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="81377-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="81377-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="81377-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="81377-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="81377-107">Data Type</span></span>

<span data-ttu-id="81377-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="81377-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="81377-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="81377-109">Default Value</span></span>

<span data-ttu-id="81377-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="81377-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="81377-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81377-111">Remarks</span></span>

<span data-ttu-id="81377-112">Si deja esta propiedad en su valor predeterminado de **Variant \_ false**, el codificador de audio utiliza su algoritmo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="81377-112">If you leave this property at its default value of **VARIANT\_FALSE**, the audio encoder uses its default algorithm.</span></span> <span data-ttu-id="81377-113">El algoritmo predeterminado depende del tipo de salida y de la versión de Windows que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="81377-113">The default algorithm depends on the output type and which version of Windows is running.</span></span> <span data-ttu-id="81377-114">En la tabla siguiente se describe el comportamiento predeterminado de las distintas combinaciones.</span><span class="sxs-lookup"><span data-stu-id="81377-114">The following table describes the default behavior for the different combinations.</span></span>



| <span data-ttu-id="81377-115">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="81377-115">Operating system</span></span> | <span data-ttu-id="81377-116">Comportamiento predeterminado</span><span class="sxs-lookup"><span data-stu-id="81377-116">Default behavior</span></span>                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81377-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81377-117">Windows Vista</span></span>    | <span data-ttu-id="81377-118">En todos los tipos de salida, el codificador de audio usa el algoritmo más complejo de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="81377-118">For all output types, the audio encoder uses the most complex algorithm by default.</span></span>                                                                                                                 |
| <span data-ttu-id="81377-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="81377-119">Windows 7</span></span>        | <span data-ttu-id="81377-120">En el caso de los tipos de salida Standard y Professional, el codificador de audio usa el algoritmo más complejo de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="81377-120">For Standard and Professional output types, the audio encoder uses the most complex algorithm by default.</span></span> <span data-ttu-id="81377-121">En el caso de los tipos de salida sin pérdida, el codificador de audio usa el algoritmo menos complejo de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="81377-121">For Lossless output types, the audio encoder uses the least complex algorithm by default.</span></span> |



 

<span data-ttu-id="81377-122">Si establece esta propiedad en **Variant \_ true**, también debe especificar un valor de complejidad estableciendo la propiedad [**MFPKEY \_ ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="81377-122">If you set this property to **VARIANT\_TRUE**, you must also specify a complexity value by setting the [**MFPKEY\_ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="81377-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81377-123">Requirements</span></span>



| <span data-ttu-id="81377-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="81377-124">Requirement</span></span> | <span data-ttu-id="81377-125">Value</span><span class="sxs-lookup"><span data-stu-id="81377-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81377-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81377-126">Minimum supported client</span></span><br/> | <span data-ttu-id="81377-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="81377-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="81377-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81377-128">Minimum supported server</span></span><br/> | <span data-ttu-id="81377-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="81377-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="81377-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81377-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="81377-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="81377-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81377-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="81377-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81377-133">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="81377-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
