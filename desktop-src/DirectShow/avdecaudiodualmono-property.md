---
description: 'Propiedad AVDecAudioDualMono: especifica si el audio de 2 canales se codifica como estéreo o mono dual.'
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Propiedad AVDecAudioDualMono (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc84e19d41840b358e3e79576152dbc8527e2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096573"
---
# <a name="avdecaudiodualmono-property"></a><span data-ttu-id="2fb67-103">AvDecAudioDualMono, propiedad</span><span class="sxs-lookup"><span data-stu-id="2fb67-103">AVDecAudioDualMono property</span></span>

<span data-ttu-id="2fb67-104">Especifica si el audio de 2 canales se codifica como estéreo o mono dual.</span><span class="sxs-lookup"><span data-stu-id="2fb67-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="2fb67-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2fb67-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="2fb67-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2fb67-106">Data type</span></span>

<span data-ttu-id="2fb67-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="2fb67-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2fb67-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fb67-108">Property GUID</span></span>

<span data-ttu-id="2fb67-109">**CODECAPI \_ AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="2fb67-109">**CODECAPI\_AVDecAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="2fb67-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fb67-110">Property value</span></span>

<span data-ttu-id="2fb67-111">El valor de esta propiedad es un miembro de la [**enumeración eAVDecAudioDualMono.**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)</span><span class="sxs-lookup"><span data-stu-id="2fb67-111">The value of this property is a member of the [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fb67-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2fb67-112">Remarks</span></span>

<span data-ttu-id="2fb67-113">Esta propiedad solo se aplica cuando la secuencia de bits de entrada del descodificador contiene audio de dos canales.</span><span class="sxs-lookup"><span data-stu-id="2fb67-113">This property applies only when the decoder's input bit stream contains two-channel audio.</span></span> <span data-ttu-id="2fb67-114">Una secuencia de audio de dos canales se puede codificar como estéreo o como mono dual.</span><span class="sxs-lookup"><span data-stu-id="2fb67-114">A two-channel audio stream might be encoded as stereo or as dual mono.</span></span> <span data-ttu-id="2fb67-115">Si el audio es mono dual, puede establecer la propiedad [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) para configurar cómo reproduce el audio el descodificador.</span><span class="sxs-lookup"><span data-stu-id="2fb67-115">If the audio is dual mono, you can set the [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) property to configure how the decoder reproduces the audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fb67-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fb67-116">Requirements</span></span>



| <span data-ttu-id="2fb67-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fb67-117">Requirement</span></span> | <span data-ttu-id="2fb67-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2fb67-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb67-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fb67-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2fb67-120">Aplicaciones de escritorio para \[ UWP de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="2fb67-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2fb67-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fb67-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2fb67-122">Aplicaciones de escritorio de Windows 2000 Server \[ \| para UWP\]</span><span class="sxs-lookup"><span data-stu-id="2fb67-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2fb67-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fb67-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fb67-124"><dt>Codecapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fb67-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2fb67-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fb67-126">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="2fb67-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="2fb67-127">**ICodecAPI (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="2fb67-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




