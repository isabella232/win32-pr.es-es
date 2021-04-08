---
description: Especifica la velocidad de bits promedio, en bits por segundo, para un codificador que está configurado para usar la codificación VBR de tamaño medio.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: Propiedad MFPKEY_DYN_VBR_RAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8103d36db5a9e946449231943e076c26258eec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001634"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a><span data-ttu-id="8f33a-103">\_Propiedad RAVG de MFPKEY DIN \_ VBR \_</span><span class="sxs-lookup"><span data-stu-id="8f33a-103">MFPKEY\_DYN\_VBR\_RAVG Property</span></span>

<span data-ttu-id="8f33a-104">Especifica la velocidad de bits promedio, en bits por segundo, para un codificador que está configurado para usar la codificación VBR de tamaño medio.</span><span class="sxs-lookup"><span data-stu-id="8f33a-104">Specifies the average bit rate, in bits per second, for an encoder that is configured to use average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8f33a-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="8f33a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="8f33a-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="8f33a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="8f33a-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8f33a-107">Data Type</span></span>

<span data-ttu-id="8f33a-108">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="8f33a-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="8f33a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f33a-109">Remarks</span></span>

<span data-ttu-id="8f33a-110">Si las propiedades [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) y [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) están establecidas en **Variant \_ true**, el codificador usa la codificación VBR de media controlable.</span><span class="sxs-lookup"><span data-stu-id="8f33a-110">If the [**MFPKEY\_AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) and [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) properties are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="8f33a-111">En ese caso, el codificador se configura a sí mismo según el valor de esta propiedad y la propiedad [**BAVG de MFPKEY \_ DYN \_ VBR \_**](mfpkey-dyn-vbr-bavgproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="8f33a-111">In that case, the encoder configures itself according to the value of this property and the [**MFPKEY\_DYN\_VBR\_BAVG**](mfpkey-dyn-vbr-bavgproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f33a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f33a-112">Requirements</span></span>



| <span data-ttu-id="8f33a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f33a-113">Requirement</span></span> | <span data-ttu-id="8f33a-114">Value</span><span class="sxs-lookup"><span data-stu-id="8f33a-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f33a-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f33a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8f33a-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8f33a-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8f33a-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f33a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8f33a-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f33a-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8f33a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f33a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f33a-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f33a-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f33a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f33a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f33a-122">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8f33a-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
