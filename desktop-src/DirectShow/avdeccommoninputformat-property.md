---
description: Especifica el formato de entrada actual para el descodificador.
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: Propiedad AVDecCommonInputFormat (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7432d2a48727ec144d4206d4a11bfe65ce2c5d2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495466"
---
# <a name="avdeccommoninputformat-property"></a><span data-ttu-id="824ea-103">Propiedad AVDecCommonInputFormat</span><span class="sxs-lookup"><span data-stu-id="824ea-103">AVDecCommonInputFormat property</span></span>

<span data-ttu-id="824ea-104">Especifica el formato de entrada actual para el descodificador.</span><span class="sxs-lookup"><span data-stu-id="824ea-104">Specifies the current input format for the decoder.</span></span>

<span data-ttu-id="824ea-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="824ea-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="824ea-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="824ea-106">Data type</span></span>

<span data-ttu-id="824ea-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="824ea-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="824ea-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="824ea-108">Property GUID</span></span>

<span data-ttu-id="824ea-109">**CODECAPI \_ AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="824ea-109">**CODECAPI\_AVDecCommonInputFormat**</span></span>

## <a name="property-value"></a><span data-ttu-id="824ea-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="824ea-110">Property value</span></span>

<span data-ttu-id="824ea-111">El valor de esta propiedad es un **BSTR** que contiene la representación de cadena de un GUID.</span><span class="sxs-lookup"><span data-stu-id="824ea-111">The value of this property is a **BSTR** that contains the string representation of a GUID.</span></span> <span data-ttu-id="824ea-112">Se definen los siguientes GUID.</span><span class="sxs-lookup"><span data-stu-id="824ea-112">The following GUIDs are defined.</span></span>



| <span data-ttu-id="824ea-113">**GUID**</span><span class="sxs-lookup"><span data-stu-id="824ea-113">**GUID**</span></span>                                            | <span data-ttu-id="824ea-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="824ea-114">Description</span></span>                                    |
|-----------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="824ea-115">**CODECAPI \_ GUID \_ AVDecAudioInputAAC**</span><span class="sxs-lookup"><span data-stu-id="824ea-115">**CODECAPI\_GUID\_AVDecAudioInputAAC**</span></span>              | <span data-ttu-id="824ea-116">Codificación de audio avanzada (AAC)</span><span class="sxs-lookup"><span data-stu-id="824ea-116">Advanced Audio Coding (AAC)</span></span>                    |
| <span data-ttu-id="824ea-117">**CODECAPI \_ GUID \_ AVDecAudioInputDolbyDigitalPlus**</span><span class="sxs-lookup"><span data-stu-id="824ea-117">**CODECAPI\_GUID\_AVDecAudioInputDolbyDigitalPlus**</span></span> | <span data-ttu-id="824ea-118">Audio Dolby Digital Plus</span><span class="sxs-lookup"><span data-stu-id="824ea-118">Dolby Digital Plus audio</span></span>                       |
| <span data-ttu-id="824ea-119">**CODECAPI \_ GUID \_ AVDecAudioInputDolby**</span><span class="sxs-lookup"><span data-stu-id="824ea-119">**CODECAPI\_GUID\_AVDecAudioInputDolby**</span></span>            | <span data-ttu-id="824ea-120">Audio Dolby</span><span class="sxs-lookup"><span data-stu-id="824ea-120">Dolby audio</span></span>                                    |
| <span data-ttu-id="824ea-121">**CODECAPI \_ GUID \_ AVDecAudioInputDTS**</span><span class="sxs-lookup"><span data-stu-id="824ea-121">**CODECAPI\_GUID\_AVDecAudioInputDTS**</span></span>              | <span data-ttu-id="824ea-122">Audio DTS</span><span class="sxs-lookup"><span data-stu-id="824ea-122">DTS audio</span></span>                                      |
| <span data-ttu-id="824ea-123">**CODECAPI \_ GUID \_ AVDecAudioInputHEAAC**</span><span class="sxs-lookup"><span data-stu-id="824ea-123">**CODECAPI\_GUID\_AVDecAudioInputHEAAC**</span></span>            | <span data-ttu-id="824ea-124">High-Efficiency codificación de audio avanzada (HE-AAC)</span><span class="sxs-lookup"><span data-stu-id="824ea-124">High-Efficiency Advanced Audio Coding (HE-AAC)</span></span> |
| <span data-ttu-id="824ea-125">**CODECAPI \_ GUID \_ AVDecAudioInputMPEG**</span><span class="sxs-lookup"><span data-stu-id="824ea-125">**CODECAPI\_GUID\_AVDecAudioInputMPEG**</span></span>             | <span data-ttu-id="824ea-126">Audio MPEG</span><span class="sxs-lookup"><span data-stu-id="824ea-126">MPEG audio</span></span>                                     |
| <span data-ttu-id="824ea-127">**CODECAPI \_ GUID \_ AVDecAudioInputPCM**</span><span class="sxs-lookup"><span data-stu-id="824ea-127">**CODECAPI\_GUID\_AVDecAudioInputPCM**</span></span>              | <span data-ttu-id="824ea-128">Audio PCM</span><span class="sxs-lookup"><span data-stu-id="824ea-128">PCM audio</span></span>                                      |
| <span data-ttu-id="824ea-129">**CODECAPI \_ GUID \_ AVDecAudioInputWMA**</span><span class="sxs-lookup"><span data-stu-id="824ea-129">**CODECAPI\_GUID\_AVDecAudioInputWMA**</span></span>              | <span data-ttu-id="824ea-130">Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="824ea-130">Windows Media Audio</span></span>                            |
| <span data-ttu-id="824ea-131">**CODECAPI \_ GUID \_ AVDecAudioInputWMAPro**</span><span class="sxs-lookup"><span data-stu-id="824ea-131">**CODECAPI\_GUID\_AVDecAudioInputWMAPro**</span></span>           | <span data-ttu-id="824ea-132">Windows Media Audio 9 Professional (WMA Pro)</span><span class="sxs-lookup"><span data-stu-id="824ea-132">Windows Media Audio 9 Professional (WMA Pro)</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="824ea-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="824ea-133">Requirements</span></span>



| <span data-ttu-id="824ea-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="824ea-134">Requirement</span></span> | <span data-ttu-id="824ea-135">Value</span><span class="sxs-lookup"><span data-stu-id="824ea-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="824ea-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="824ea-136">Minimum supported client</span></span><br/> | <span data-ttu-id="824ea-137">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="824ea-137">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="824ea-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="824ea-138">Minimum supported server</span></span><br/> | <span data-ttu-id="824ea-139">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="824ea-139">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="824ea-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="824ea-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="824ea-141"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="824ea-141"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="824ea-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="824ea-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="824ea-143">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="824ea-143">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="824ea-144">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="824ea-144">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




