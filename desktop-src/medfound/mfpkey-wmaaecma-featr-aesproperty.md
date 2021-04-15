---
description: Especifica el número de veces que el DSP de captura de voz realiza la supresión del eco acústico (AES) en la señal residual.
ms.assetid: 409b40f8-38eb-49f7-be30-348ab5cdd33a
title: Propiedad MFPKEY_WMAAECMA_FEATR_AES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5da7505a259a51ca8456f3caffa153790649320
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648247"
---
# <a name="mfpkey_wmaaecma_featr_aes-property"></a><span data-ttu-id="77018-103">\_Propiedad AES de MFPKEY WMAAECMA \_ feat \_</span><span class="sxs-lookup"><span data-stu-id="77018-103">MFPKEY\_WMAAECMA\_FEATR\_AES Property</span></span>

<span data-ttu-id="77018-104">Especifica el número de veces que el DSP de captura de voz realiza la supresión del eco acústico (AES) en la señal residual.</span><span class="sxs-lookup"><span data-stu-id="77018-104">Specifies how many times the Voice Capture DSP performs acoustic echo suppression (AES) on the residual signal.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="77018-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="77018-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="77018-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="77018-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="77018-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="77018-107">Data Type</span></span>

<span data-ttu-id="77018-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="77018-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="77018-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="77018-109">Default Value</span></span>

<span data-ttu-id="77018-110">0</span><span class="sxs-lookup"><span data-stu-id="77018-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="77018-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="77018-111">Applies To</span></span>

-   [<span data-ttu-id="77018-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="77018-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="77018-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77018-113">Remarks</span></span>

<span data-ttu-id="77018-114">La captura de voz DSP puede realizar AES en la señal residual después de la cancelación del eco.</span><span class="sxs-lookup"><span data-stu-id="77018-114">The Voice Capture DSP can perform AES on the residual signal after echo cancellation.</span></span> <span data-ttu-id="77018-115">Esta propiedad puede tener el valor 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="77018-115">This property can have the value 0, 1, or 2.</span></span> <span data-ttu-id="77018-116">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="77018-116">The default value is 0.</span></span> <span data-ttu-id="77018-117">Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="77018-117">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="77018-118">El DSP usa esta propiedad solo cuando el procesamiento de AEC está habilitado.</span><span class="sxs-lookup"><span data-stu-id="77018-118">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="77018-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77018-119">Requirements</span></span>



| <span data-ttu-id="77018-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="77018-120">Requirement</span></span> | <span data-ttu-id="77018-121">Value</span><span class="sxs-lookup"><span data-stu-id="77018-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77018-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77018-122">Minimum supported client</span></span><br/> | <span data-ttu-id="77018-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="77018-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="77018-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77018-124">Minimum supported server</span></span><br/> | <span data-ttu-id="77018-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="77018-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77018-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77018-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="77018-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="77018-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77018-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="77018-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77018-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="77018-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="77018-130">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="77018-130">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
