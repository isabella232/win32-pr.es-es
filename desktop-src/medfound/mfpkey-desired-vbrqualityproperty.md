---
description: Especifica el nivel de calidad deseado para la codificación de velocidad de bits variable (VBR) (1-pass) de la calidad de las secuencias de audio.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: Propiedad MFPKEY_DESIRED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa0f2cf86db076fa211f9c850db15de730a3a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648309"
---
# <a name="mfpkey_desired_vbrquality-property"></a><span data-ttu-id="19d67-103">MFPKEY \_ \_ propiedad VBRQUALITY deseada</span><span class="sxs-lookup"><span data-stu-id="19d67-103">MFPKEY\_DESIRED\_VBRQUALITY Property</span></span>

<span data-ttu-id="19d67-104">Especifica el nivel de calidad deseado para la codificación de velocidad de bits variable (VBR) (1-pass) de la calidad de las secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="19d67-104">Specifies the desired quality level for quality based (1-pass) variable-bit-rate (VBR) encoding of audio streams.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="19d67-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="19d67-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="19d67-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="19d67-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="19d67-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="19d67-107">Data Type</span></span>

<span data-ttu-id="19d67-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="19d67-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="19d67-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="19d67-109">Default Value</span></span>

<span data-ttu-id="19d67-110">0</span><span class="sxs-lookup"><span data-stu-id="19d67-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="19d67-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19d67-111">Remarks</span></span>

<span data-ttu-id="19d67-112">Este valor puede estar comprendido entre 0 y 100, donde 100 es la calidad máxima.</span><span class="sxs-lookup"><span data-stu-id="19d67-112">This value can be from 0 to 100, where 100 is maximum quality.</span></span> <span data-ttu-id="19d67-113">Un valor de 0 indica que no se va a usar el método de codificación VBR basado en la calidad.</span><span class="sxs-lookup"><span data-stu-id="19d67-113">A value of 0 indicates that the quality-based VBR encoding method is not to be used.</span></span>

<span data-ttu-id="19d67-114">Para enumerar los modos VBR que cumplen un requisito de calidad determinado, establezca las siguientes propiedades del codificador.</span><span class="sxs-lookup"><span data-stu-id="19d67-114">To enumerate VBR modes that meet a certain quality requirement, set the following encoder properties.</span></span>

-   <span data-ttu-id="19d67-115">Establezca [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="19d67-115">Set [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="19d67-116">Establezca [**MFPKEY \_ restricción de \_ \_ VBRQUALITY enumerada**](mfpkey-constrain-enumerated-vbrqualityproperty.md) en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="19d67-116">Set [**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="19d67-117">Establezca **MFPKEY \_ deseado \_ VBRQUALITY** en la calidad deseada.</span><span class="sxs-lookup"><span data-stu-id="19d67-117">Set **MFPKEY\_DESIRED\_VBRQUALITY** to the desired quality.</span></span> <span data-ttu-id="19d67-118">En el caso de los modos sin pérdida, establezca la calidad deseada en 100.</span><span class="sxs-lookup"><span data-stu-id="19d67-118">For Lossless modes, set the desired quality to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="19d67-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19d67-119">Requirements</span></span>



| <span data-ttu-id="19d67-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="19d67-120">Requirement</span></span> | <span data-ttu-id="19d67-121">Value</span><span class="sxs-lookup"><span data-stu-id="19d67-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19d67-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19d67-122">Minimum supported client</span></span><br/> | <span data-ttu-id="19d67-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="19d67-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="19d67-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19d67-124">Minimum supported server</span></span><br/> | <span data-ttu-id="19d67-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="19d67-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="19d67-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19d67-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="19d67-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="19d67-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19d67-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="19d67-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19d67-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="19d67-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
