---
description: Especifica si el codificador debe usar un tamaño de marco preferido dado en número de muestras por fotograma.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: Propiedad MFPKEY_REQUESTING_A_FRAMESIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3355e84318ba4ad7995ac5ad0f002f4d70767b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700400"
---
# <a name="mfpkey_requesting_a_framesize-property"></a><span data-ttu-id="7695a-103">MFPKEY \_ solicitar \_ una \_ propiedad de trama</span><span class="sxs-lookup"><span data-stu-id="7695a-103">MFPKEY\_REQUESTING\_A\_FRAMESIZE Property</span></span>

<span data-ttu-id="7695a-104">Especifica si el codificador debe usar un tamaño de marco preferido dado en número de muestras por fotograma.</span><span class="sxs-lookup"><span data-stu-id="7695a-104">Specifies whether the encoder should use a preferred frame size given in number of samples per frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7695a-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7695a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7695a-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="7695a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="7695a-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7695a-107">Data Type</span></span>

<span data-ttu-id="7695a-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="7695a-108">**VT\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="7695a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7695a-109">Remarks</span></span>

<span data-ttu-id="7695a-110">Para especificar un tamaño de marco preferido, establezca las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="7695a-110">To specifiy a preferred frame size, set the following properties.</span></span>

-   <span data-ttu-id="7695a-111">Establezca **MFPKEY para \_ solicitar \_ una \_ trama** a Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="7695a-111">Set **MFPKEY\_REQUESTING\_A\_FRAMESIZE** to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="7695a-112">Establezca [**MFPKEY \_ preferido \_ tramas**](mfpkey-preferred-framesizeproperty.md) en el número de muestras que desee en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="7695a-112">Set [**MFPKEY\_PREFERRED\_FRAMESIZE**](mfpkey-preferred-framesizeproperty.md) to the number of samples you want in each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="7695a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7695a-113">Requirements</span></span>



| <span data-ttu-id="7695a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7695a-114">Requirement</span></span> | <span data-ttu-id="7695a-115">Value</span><span class="sxs-lookup"><span data-stu-id="7695a-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7695a-116">Remoto</span><span class="sxs-lookup"><span data-stu-id="7695a-116">Client</span></span><br/> | <span data-ttu-id="7695a-117">Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="7695a-117">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="7695a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7695a-118">Header</span></span><br/> | <dl> <span data-ttu-id="7695a-119"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7695a-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7695a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7695a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7695a-121">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7695a-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
