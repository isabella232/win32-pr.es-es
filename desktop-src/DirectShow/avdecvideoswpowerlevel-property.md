---
description: Especifica el nivel de ahorro de energía de un descodificador de vídeo.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: Propiedad AVDecVideoSWPowerLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1196c45cf038085856b1d63a5cd3a1c7dc350d0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666131"
---
# <a name="avdecvideoswpowerlevel-property"></a><span data-ttu-id="29500-103">Propiedad AVDecVideoSWPowerLevel</span><span class="sxs-lookup"><span data-stu-id="29500-103">AVDecVideoSWPowerLevel property</span></span>

<span data-ttu-id="29500-104">Especifica el nivel de ahorro de energía de un descodificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="29500-104">Specifies the power-saving level of a video decoder.</span></span>

<span data-ttu-id="29500-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="29500-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="29500-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="29500-106">Data type</span></span>

<span data-ttu-id="29500-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="29500-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="29500-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="29500-108">Property GUID</span></span>

<span data-ttu-id="29500-109">**CODECAPI \_ AVDecVideoSWPowerLevel**</span><span class="sxs-lookup"><span data-stu-id="29500-109">**CODECAPI\_AVDecVideoSWPowerLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="29500-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="29500-110">Property value</span></span>

<span data-ttu-id="29500-111">El intervalo de valores posibles es \[ 0.. 100 \] , ambos inclusive, con el significado siguiente.</span><span class="sxs-lookup"><span data-stu-id="29500-111">The range of possible values is \[0..100\], inclusive, with the following meaning.</span></span>



| <span data-ttu-id="29500-112">Value</span><span class="sxs-lookup"><span data-stu-id="29500-112">Value</span></span> | <span data-ttu-id="29500-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="29500-113">Description</span></span>                 |
|-------|-----------------------------|
| <span data-ttu-id="29500-114">0</span><span class="sxs-lookup"><span data-stu-id="29500-114">0</span></span>     | <span data-ttu-id="29500-115">Optimizar para la duración de la batería.</span><span class="sxs-lookup"><span data-stu-id="29500-115">Optimize for battery life.</span></span>  |
| <span data-ttu-id="29500-116">100</span><span class="sxs-lookup"><span data-stu-id="29500-116">100</span></span>   | <span data-ttu-id="29500-117">Optimice la calidad del vídeo.</span><span class="sxs-lookup"><span data-stu-id="29500-117">Optimize for video quality.</span></span> |



 

<span data-ttu-id="29500-118">La enumeración [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) define algunas constantes específicas dentro de este intervalo.</span><span class="sxs-lookup"><span data-stu-id="29500-118">The [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) enumeration defines some specific constants within this range.</span></span>

## <a name="remarks"></a><span data-ttu-id="29500-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29500-119">Remarks</span></span>

<span data-ttu-id="29500-120">Puede establecer esta propiedad durante la reproducción para cambiar el nivel de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="29500-120">You can set this property during playback to change the pwoer-saving level.</span></span>

## <a name="requirements"></a><span data-ttu-id="29500-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29500-121">Requirements</span></span>



| <span data-ttu-id="29500-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="29500-122">Requirement</span></span> | <span data-ttu-id="29500-123">Value</span><span class="sxs-lookup"><span data-stu-id="29500-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29500-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29500-124">Minimum supported client</span></span><br/> | <span data-ttu-id="29500-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="29500-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="29500-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29500-126">Minimum supported server</span></span><br/> | <span data-ttu-id="29500-127">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="29500-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="29500-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29500-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="29500-129"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="29500-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29500-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="29500-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29500-131">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="29500-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="29500-132">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="29500-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




