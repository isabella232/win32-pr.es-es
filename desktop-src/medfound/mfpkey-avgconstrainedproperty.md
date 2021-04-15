---
description: Especifica si el codificador utiliza la codificación VBR de promedio controlable.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: Propiedad MFPKEY_AVGCONSTRAINED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0623fb4a73e3721f9079f2a1e5e330ecb466a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696340"
---
# <a name="mfpkey_avgconstrained-property"></a><span data-ttu-id="d1380-103">\_Propiedad AVGCONSTRAINED de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="d1380-103">MFPKEY\_AVGCONSTRAINED Property</span></span>

<span data-ttu-id="d1380-104">Especifica si el codificador utiliza la codificación VBR de promedio controlable.</span><span class="sxs-lookup"><span data-stu-id="d1380-104">Specifies whether the encoder uses average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d1380-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d1380-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d1380-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="d1380-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="d1380-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d1380-107">Data Type</span></span>

<span data-ttu-id="d1380-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="d1380-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="d1380-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="d1380-109">Default Value</span></span>

<span data-ttu-id="d1380-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="d1380-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="d1380-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1380-111">Remarks</span></span>

<span data-ttu-id="d1380-112">Si esta propiedad y la [**propiedad \_ VBRENABLED de MFPKEY**](mfpkey-vbrenabledproperty.md) están establecidas en **Variant \_ true**, el codificador usa la codificación VBR de promedio controlable.</span><span class="sxs-lookup"><span data-stu-id="d1380-112">If this property and the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="d1380-113">En ese caso, el codificador se configura a sí mismo según los valores de [**MFPKEY \_ DYN \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) y [**MFPKEY \_ DYN \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md).</span><span class="sxs-lookup"><span data-stu-id="d1380-113">In that case, the encoder configures itself according to the values of [**MFPKEY\_DYN\_VBR\_BAVG**](mfpkey-dyn-vbr-bavgproperty.md) and [**MFPKEY\_DYN\_VBR\_RAVG**](mfpkey-dyn-vbr-ravgproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1380-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1380-114">Requirements</span></span>



| <span data-ttu-id="d1380-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1380-115">Requirement</span></span> | <span data-ttu-id="d1380-116">Value</span><span class="sxs-lookup"><span data-stu-id="d1380-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1380-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1380-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d1380-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d1380-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d1380-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1380-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d1380-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1380-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d1380-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1380-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1380-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1380-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1380-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1380-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1380-124">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d1380-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
