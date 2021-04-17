---
description: Especifica el número preferido de muestras por fotograma.
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: Propiedad MFPKEY_PREFERRED_FRAMESIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe04ad37c6cd684e3179cbd16328346fd6f11dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700289"
---
# <a name="mfpkey_preferred_framesize-property"></a><span data-ttu-id="c661a-103">MFPKEY \_ propiedad de trama preferida \_</span><span class="sxs-lookup"><span data-stu-id="c661a-103">MFPKEY\_PREFERRED\_FRAMESIZE Property</span></span>

<span data-ttu-id="c661a-104">Especifica el número preferido de muestras por fotograma.</span><span class="sxs-lookup"><span data-stu-id="c661a-104">Specifies the preferred number of samples per frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c661a-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c661a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c661a-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="c661a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="c661a-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c661a-107">Data Type</span></span>

<span data-ttu-id="c661a-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="c661a-108">**VT\_UI4**</span></span>

## <a name="remarks"></a><span data-ttu-id="c661a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c661a-109">Remarks</span></span>

<span data-ttu-id="c661a-110">Para especificar un tamaño de marco preferido, establezca las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="c661a-110">To specifiy a preferred frame size, set the following properties.</span></span>

-   <span data-ttu-id="c661a-111">Establezca [**MFPKEY para \_ solicitar \_ una \_ trama**](mfpkey-requesting-a-framesizeproperty.md) a **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="c661a-111">Set [**MFPKEY\_REQUESTING\_A\_FRAMESIZE**](mfpkey-requesting-a-framesizeproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="c661a-112">Establezca **MFPKEY \_ preferido \_ tramas** en el número de muestras que desee en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="c661a-112">Set **MFPKEY\_PREFERRED\_FRAMESIZE** to the number of samples you want in each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="c661a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c661a-113">Requirements</span></span>



| <span data-ttu-id="c661a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c661a-114">Requirement</span></span> | <span data-ttu-id="c661a-115">Value</span><span class="sxs-lookup"><span data-stu-id="c661a-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c661a-116">Remoto</span><span class="sxs-lookup"><span data-stu-id="c661a-116">Client</span></span><br/> | <span data-ttu-id="c661a-117">Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="c661a-117">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="c661a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c661a-118">Header</span></span><br/> | <dl> <span data-ttu-id="c661a-119"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c661a-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c661a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="c661a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c661a-121">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c661a-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
