---
description: Especifica si el codificador básico utiliza el &\# 0034; Más&\# 0034; característica.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: Propiedad MFPKEY_ENHANCED_WMA (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1c7ddc0e7bfb6d62d51e535f10b257eac6f2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650192"
---
# <a name="mfpkey_enhanced_wma-property"></a><span data-ttu-id="8a9d1-103">MFPKEY \_ \_ propiedad WMA mejorada</span><span class="sxs-lookup"><span data-stu-id="8a9d1-103">MFPKEY\_ENHANCED\_WMA Property</span></span>

<span data-ttu-id="8a9d1-104">Especifica si el codificador básico usa la característica "Plus".</span><span class="sxs-lookup"><span data-stu-id="8a9d1-104">Specifies whether the core encoder uses the "Plus" feature.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8a9d1-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="8a9d1-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="8a9d1-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="8a9d1-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="8a9d1-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8a9d1-107">Data Type</span></span>

<span data-ttu-id="8a9d1-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="8a9d1-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="8a9d1-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8a9d1-109">Default Value</span></span>

<span data-ttu-id="8a9d1-110">0</span><span class="sxs-lookup"><span data-stu-id="8a9d1-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="8a9d1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a9d1-111">Remarks</span></span>

<span data-ttu-id="8a9d1-112">Esta propiedad solo está disponible para Windows Media Audio sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="8a9d1-112">This property is available only for Windows Media Audio Lossless.</span></span>

<span data-ttu-id="8a9d1-113">Si deja esta propiedad en su valor predeterminado de 0, o si se establece en 1, el codificador principal decide si se debe usar la parte "más".</span><span class="sxs-lookup"><span data-stu-id="8a9d1-113">If you leave this property at its default value of 0, or if you set it to 1, the core encoder decides whether the "Plus" portion should be used.</span></span> <span data-ttu-id="8a9d1-114">Si establece esta propiedad en 2, el codificador básico no utiliza la característica "Plus".</span><span class="sxs-lookup"><span data-stu-id="8a9d1-114">If you set this property to 2, the core encoder does not use the "Plus" feature.</span></span>

<span data-ttu-id="8a9d1-115">Esta propiedad modifica los tipos de medios enumerados, por lo que si se establece, debe hacerlo antes de establecer el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="8a9d1-115">This property alters the enumerated media types, so if you set it, you must do so before you set the output type.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a9d1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a9d1-116">Requirements</span></span>



| <span data-ttu-id="8a9d1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a9d1-117">Requirement</span></span> | <span data-ttu-id="8a9d1-118">Value</span><span class="sxs-lookup"><span data-stu-id="8a9d1-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a9d1-119">Remoto</span><span class="sxs-lookup"><span data-stu-id="8a9d1-119">Client</span></span><br/> | <span data-ttu-id="8a9d1-120">Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="8a9d1-120">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="8a9d1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a9d1-121">Header</span></span><br/> | <dl> <span data-ttu-id="8a9d1-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a9d1-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a9d1-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a9d1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a9d1-124">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8a9d1-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
