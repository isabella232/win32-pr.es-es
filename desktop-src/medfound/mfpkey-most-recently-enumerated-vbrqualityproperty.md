---
description: Especifica el nivel de calidad VBR del tipo de salida enumerado más recientemente.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: Propiedad MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd3b5f3aae6dc5347672cf6697c3431163dcbd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650163"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a><span data-ttu-id="164ed-103">\_ \_ \_ Propiedad VBRQUALITY enumerada más reciente de MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="164ed-103">MFPKEY\_MOST\_RECENT\_ENUMERATED\_VBRQUALITY Property</span></span>

<span data-ttu-id="164ed-104">Especifica el nivel de calidad VBR del tipo de salida enumerado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="164ed-104">Specifies the VBR quality level of the most recently enumerated output type.</span></span> <span data-ttu-id="164ed-105">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="164ed-105">Read-only.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="164ed-106">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="164ed-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="164ed-107">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="164ed-107">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="164ed-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="164ed-108">Data Type</span></span>

<span data-ttu-id="164ed-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="164ed-109">**VT\_UI4**</span></span>

## <a name="remarks"></a><span data-ttu-id="164ed-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="164ed-110">Remarks</span></span>

<span data-ttu-id="164ed-111">Cuando el codificador actúa como una transformación de Media Foundation (MFT) y enumera un tipo de salida en una llamada a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), puede consultar la MFT de la propiedad **\_ \_ \_ \_ VBRQUALITY enumerada más recientemente de MFPKEY** .</span><span class="sxs-lookup"><span data-stu-id="164ed-111">When the encoder is acting as an Media Foundation Transform (MFT) and it enumerates an output type on a call to [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), you can query the MFT for the **MFPKEY\_MOST\_RECENTLY\_ENUMERATED\_VBRQUALITY** property.</span></span> <span data-ttu-id="164ed-112">El valor devuelto indica la calidad VBR del tipo de medio de salida devuelto más recientemente.</span><span class="sxs-lookup"><span data-stu-id="164ed-112">The value returned indicates the VBR quality of the most recently returned output media type.</span></span> <span data-ttu-id="164ed-113">Después, puede usar ese valor para establecer la [**propiedad \_ \_ VBRQUALITY deseada de MFPKEY**](mfpkey-desired-vbrqualityproperty.md) del codificador.</span><span class="sxs-lookup"><span data-stu-id="164ed-113">Then you can use that value to set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property of the encoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="164ed-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="164ed-114">Requirements</span></span>



| <span data-ttu-id="164ed-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="164ed-115">Requirement</span></span> | <span data-ttu-id="164ed-116">Value</span><span class="sxs-lookup"><span data-stu-id="164ed-116">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="164ed-117">Remoto</span><span class="sxs-lookup"><span data-stu-id="164ed-117">Client</span></span><br/> | <span data-ttu-id="164ed-118">Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="164ed-118">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="164ed-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="164ed-119">Header</span></span><br/> | <dl> <span data-ttu-id="164ed-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="164ed-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="164ed-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="164ed-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="164ed-122">**MFPKEY \_ VBRENABLED**</span><span class="sxs-lookup"><span data-stu-id="164ed-122">**MFPKEY\_VBRENABLED**</span></span>](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[<span data-ttu-id="164ed-123">**MFPKEY \_ restricción de \_ VBRQUALITY enumerada \_**</span><span class="sxs-lookup"><span data-stu-id="164ed-123">**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**</span></span>](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="164ed-124">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="164ed-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
