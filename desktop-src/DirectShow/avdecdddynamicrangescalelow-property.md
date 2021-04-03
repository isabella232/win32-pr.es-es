---
description: Especifica el aumento de bajo nivel cuando el descodificador realiza el control de intervalo dinámico en una secuencia de audio Dolby AC-3.
ms.assetid: d723c825-f2f1-4ba0-a667-8285009764fd
title: Propiedad AVDecDDDynamicRangeScaleLow (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b68b1d4376d9ba15859be943ded23458fe16d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080054"
---
# <a name="avdecdddynamicrangescalelow-property"></a><span data-ttu-id="10760-103">Propiedad AVDecDDDynamicRangeScaleLow</span><span class="sxs-lookup"><span data-stu-id="10760-103">AVDecDDDynamicRangeScaleLow property</span></span>

<span data-ttu-id="10760-104">Especifica el aumento de bajo nivel cuando el descodificador realiza el control de intervalo dinámico en una secuencia de audio Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="10760-104">Specifies the low-level boost when the decoder performs dynamic range control on a Dolby AC-3 audio stream.</span></span>

<span data-ttu-id="10760-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="10760-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="10760-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="10760-106">Data type</span></span>

<span data-ttu-id="10760-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="10760-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="10760-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="10760-108">Property GUID</span></span>

<span data-ttu-id="10760-109">**CODECAPI \_ AVDecDDDynamicRangeScaleLow**</span><span class="sxs-lookup"><span data-stu-id="10760-109">**CODECAPI\_AVDecDDDynamicRangeScaleLow**</span></span>

## <a name="property-value"></a><span data-ttu-id="10760-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="10760-110">Property value</span></span>

<span data-ttu-id="10760-111">El valor de esta propiedad tiene el siguiente intervalo.</span><span class="sxs-lookup"><span data-stu-id="10760-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="10760-112">Value</span><span class="sxs-lookup"><span data-stu-id="10760-112">Value</span></span> | <span data-ttu-id="10760-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="10760-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="10760-114">0</span><span class="sxs-lookup"><span data-stu-id="10760-114">0</span></span>     | <span data-ttu-id="10760-115">Sin compresión de intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="10760-115">No dynamic range compression.</span></span> <span data-ttu-id="10760-116">Conserva el intervalo dinámico completo.</span><span class="sxs-lookup"><span data-stu-id="10760-116">Preserve the full dynamic range.</span></span> |
| <span data-ttu-id="10760-117">100</span><span class="sxs-lookup"><span data-stu-id="10760-117">100</span></span>   | <span data-ttu-id="10760-118">Aplique la compresión de intervalo dinámico completa.</span><span class="sxs-lookup"><span data-stu-id="10760-118">Apply full dynamic range compression.</span></span>                          |



 

## <a name="remarks"></a><span data-ttu-id="10760-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10760-119">Remarks</span></span>

<span data-ttu-id="10760-120">Esta propiedad solo se aplica cuando el valor de la propiedad [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) es eAVDecDDOperationalMode \_ line.</span><span class="sxs-lookup"><span data-stu-id="10760-120">This property applies only when the value of the [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) property is eAVDecDDOperationalMode\_LINE.</span></span>

## <a name="requirements"></a><span data-ttu-id="10760-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10760-121">Requirements</span></span>



| <span data-ttu-id="10760-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="10760-122">Requirement</span></span> | <span data-ttu-id="10760-123">Value</span><span class="sxs-lookup"><span data-stu-id="10760-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10760-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10760-124">Minimum supported client</span></span><br/> | <span data-ttu-id="10760-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="10760-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="10760-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10760-126">Minimum supported server</span></span><br/> | <span data-ttu-id="10760-127">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="10760-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="10760-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10760-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="10760-129"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="10760-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10760-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="10760-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10760-131">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="10760-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="10760-132">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="10760-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




