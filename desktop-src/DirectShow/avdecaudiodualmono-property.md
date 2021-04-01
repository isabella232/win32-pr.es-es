---
description: Especifica si el audio de 2 canales se codifica como estéreo o dual mono.
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Propiedad AVDecAudioDualMono (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 107adb00eb68cbb9ec19331b0c0f3f9db916a306
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906771"
---
# <a name="avdecaudiodualmono-property"></a><span data-ttu-id="50526-103">Propiedad AVDecAudioDualMono</span><span class="sxs-lookup"><span data-stu-id="50526-103">AVDecAudioDualMono property</span></span>

<span data-ttu-id="50526-104">Especifica si el audio de 2 canales se codifica como estéreo o dual mono.</span><span class="sxs-lookup"><span data-stu-id="50526-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="50526-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="50526-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="50526-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="50526-106">Data type</span></span>

<span data-ttu-id="50526-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="50526-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="50526-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="50526-108">Property GUID</span></span>

<span data-ttu-id="50526-109">**CODECAPI \_ AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="50526-109">**CODECAPI\_AVDecAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="50526-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="50526-110">Property value</span></span>

<span data-ttu-id="50526-111">El valor de esta propiedad es un miembro de la enumeración [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) .</span><span class="sxs-lookup"><span data-stu-id="50526-111">The value of this property is a member of the [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="50526-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50526-112">Remarks</span></span>

<span data-ttu-id="50526-113">Esta propiedad solo se aplica cuando el flujo de bits de entrada del descodificador contiene audio de dos canales.</span><span class="sxs-lookup"><span data-stu-id="50526-113">This property applies only when the decoder's input bit stream contains two-channel audio.</span></span> <span data-ttu-id="50526-114">Una secuencia de audio de dos canales podría estar codificada como estéreo o como dual mono.</span><span class="sxs-lookup"><span data-stu-id="50526-114">A two-channel audio stream might be encoded as stereo or as dual mono.</span></span> <span data-ttu-id="50526-115">Si el audio es dual mono, puede establecer la propiedad [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) para configurar el modo en que el descodificador reproduce el audio.</span><span class="sxs-lookup"><span data-stu-id="50526-115">If the audio is dual mono, you can set the [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) property to configure how the decoder reproduces the audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="50526-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50526-116">Requirements</span></span>



| <span data-ttu-id="50526-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="50526-117">Requirement</span></span> | <span data-ttu-id="50526-118">Value</span><span class="sxs-lookup"><span data-stu-id="50526-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50526-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50526-119">Minimum supported client</span></span><br/> | <span data-ttu-id="50526-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="50526-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="50526-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50526-121">Minimum supported server</span></span><br/> | <span data-ttu-id="50526-122">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="50526-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="50526-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50526-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="50526-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="50526-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50526-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="50526-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50526-126">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="50526-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="50526-127">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="50526-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




