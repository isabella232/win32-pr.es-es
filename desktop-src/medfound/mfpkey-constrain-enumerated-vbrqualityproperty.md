---
description: Especifica si los modos enumerados por el codificador se Limeted a aquellos que cumplen un requisito de calidad proporcionado por \_ MFPKEY \_ VBRQUALITY deseado.
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: Propiedad MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700367"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a><span data-ttu-id="54241-103">\_ \_ Propiedad VBRQUALITY enumerada MFPKEY restringida \_</span><span class="sxs-lookup"><span data-stu-id="54241-103">MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY Property</span></span>

<span data-ttu-id="54241-104">Especifica si los modos enumerados por el codificador se Limeted a aquellos que cumplen un requisito de calidad proporcionado [**por \_ MFPKEY \_ VBRQUALITY deseado**](mfpkey-desired-vbrqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="54241-104">Specifies whether modes enumerated by the encoder are limeted to those that meet a quality requirement given by [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="54241-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="54241-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="54241-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="54241-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="54241-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="54241-107">Data Type</span></span>

<span data-ttu-id="54241-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="54241-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="54241-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="54241-109">Default Value</span></span>

<span data-ttu-id="54241-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="54241-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="54241-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54241-111">Remarks</span></span>

<span data-ttu-id="54241-112">Para enumerar los modos VBR que cumplen un requisito de calidad determinado, establezca las siguientes propiedades del codificador.</span><span class="sxs-lookup"><span data-stu-id="54241-112">To enumerate VBR modes that meet a certain quality requirement, set the following encoder properties.</span></span>

-   <span data-ttu-id="54241-113">Establezca [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="54241-113">Set [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="54241-114">Establezca **MFPKEY \_ restricción de \_ \_ VBRQUALITY enumerada** en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="54241-114">Set **MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY** to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="54241-115">Establezca [**MFPKEY \_ deseado \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) en la calidad deseada.</span><span class="sxs-lookup"><span data-stu-id="54241-115">Set [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) to the desired quality.</span></span> <span data-ttu-id="54241-116">En el caso de los modos sin pérdida, establezca la calidad deseada en 100.</span><span class="sxs-lookup"><span data-stu-id="54241-116">For Lossless modes, set the desired quality to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="54241-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54241-117">Requirements</span></span>



| <span data-ttu-id="54241-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="54241-118">Requirement</span></span> | <span data-ttu-id="54241-119">Value</span><span class="sxs-lookup"><span data-stu-id="54241-119">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54241-120">Remoto</span><span class="sxs-lookup"><span data-stu-id="54241-120">Client</span></span><br/> | <span data-ttu-id="54241-121">Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="54241-121">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="54241-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54241-122">Header</span></span><br/> | <dl> <span data-ttu-id="54241-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="54241-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54241-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="54241-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54241-125">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="54241-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
