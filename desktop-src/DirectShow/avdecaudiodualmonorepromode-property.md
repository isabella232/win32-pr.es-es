---
description: Especifica cómo el descodificador Reproduce audio mono dual.
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: Propiedad AVDecAudioDualMonoReproMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71ebe7e003b2dc4b6eebc30901525ffb918a9a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806463"
---
# <a name="avdecaudiodualmonorepromode-property"></a><span data-ttu-id="a8d6f-103">Propiedad AVDecAudioDualMonoReproMode</span><span class="sxs-lookup"><span data-stu-id="a8d6f-103">AVDecAudioDualMonoReproMode property</span></span>

<span data-ttu-id="a8d6f-104">Especifica cómo el descodificador Reproduce audio mono dual.</span><span class="sxs-lookup"><span data-stu-id="a8d6f-104">Specifies how the decoder reproduces dual mono audio.</span></span>

<span data-ttu-id="a8d6f-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a8d6f-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a8d6f-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a8d6f-106">Data type</span></span>

<span data-ttu-id="a8d6f-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a8d6f-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a8d6f-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="a8d6f-108">Property GUID</span></span>

<span data-ttu-id="a8d6f-109">**CODECAPI \_ AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="a8d6f-109">**CODECAPI\_AVDecAudioDualMonoReproMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="a8d6f-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a8d6f-110">Property value</span></span>

<span data-ttu-id="a8d6f-111">El valor de esta propiedad es un miembro de la enumeración [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) .</span><span class="sxs-lookup"><span data-stu-id="a8d6f-111">The value of this property is a member of the [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8d6f-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8d6f-112">Remarks</span></span>

<span data-ttu-id="a8d6f-113">Estas propiedades solo se aplican cuando el flujo de bits de entrada del descodificador contiene audio mono dual.</span><span class="sxs-lookup"><span data-stu-id="a8d6f-113">This properties applies only when the decoder's input bit stream contains dual mono audio.</span></span> <span data-ttu-id="a8d6f-114">Para probar esta condición, obtenga el valor de la propiedad [AVDecAudioDualMono](avdecaudiodualmono-property.md) .</span><span class="sxs-lookup"><span data-stu-id="a8d6f-114">To test this condition, get the value of the [AVDecAudioDualMono](avdecaudiodualmono-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8d6f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8d6f-115">Requirements</span></span>



| <span data-ttu-id="a8d6f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8d6f-116">Requirement</span></span> | <span data-ttu-id="a8d6f-117">Value</span><span class="sxs-lookup"><span data-stu-id="a8d6f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d6f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8d6f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a8d6f-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="a8d6f-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a8d6f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8d6f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a8d6f-121">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="a8d6f-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a8d6f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8d6f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8d6f-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8d6f-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8d6f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8d6f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8d6f-125">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="a8d6f-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a8d6f-126">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a8d6f-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




