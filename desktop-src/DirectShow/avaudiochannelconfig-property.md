---
description: Obtiene la configuración de los altavoces para los canales de audio en el flujo de bits de audio.
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: Propiedad AVAudioChannelConfig (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ee1bc7897d92f7efa1b6d351d2f73c32867529
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079952"
---
# <a name="avaudiochannelconfig-property"></a><span data-ttu-id="f1f49-103">Propiedad AVAudioChannelConfig</span><span class="sxs-lookup"><span data-stu-id="f1f49-103">AVAudioChannelConfig property</span></span>

<span data-ttu-id="f1f49-104">Obtiene la configuración de los altavoces para los canales de audio en el flujo de bits de audio.</span><span class="sxs-lookup"><span data-stu-id="f1f49-104">Gets the speaker configuration for the audio channels in the audio bit stream.</span></span>

<span data-ttu-id="f1f49-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f1f49-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="f1f49-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f1f49-106">Data type</span></span>

<span data-ttu-id="f1f49-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="f1f49-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f1f49-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="f1f49-108">Property GUID</span></span>

<span data-ttu-id="f1f49-109">**CODECAPI \_ AVAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="f1f49-109">**CODECAPI\_AVAudioChannelConfig**</span></span>

## <a name="property-value"></a><span data-ttu-id="f1f49-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f1f49-110">Property value</span></span>

<span data-ttu-id="f1f49-111">El valor de esta propiedad es una operación OR bit a bit de los miembros de la enumeración [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) .</span><span class="sxs-lookup"><span data-stu-id="f1f49-111">The value of this property is a bitwise OR of members of the [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1f49-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1f49-112">Remarks</span></span>

<span data-ttu-id="f1f49-113">El número de canales incluye el canal de efecto de baja frecuencia (LFE), si está presente.</span><span class="sxs-lookup"><span data-stu-id="f1f49-113">The number of channels includes the low frequency effect (LFE) channel, if present.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1f49-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1f49-114">Requirements</span></span>



| <span data-ttu-id="f1f49-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1f49-115">Requirement</span></span> | <span data-ttu-id="f1f49-116">Value</span><span class="sxs-lookup"><span data-stu-id="f1f49-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f49-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1f49-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f1f49-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="f1f49-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f1f49-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1f49-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f1f49-120">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="f1f49-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f1f49-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1f49-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1f49-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1f49-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1f49-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1f49-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1f49-124">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="f1f49-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="f1f49-125">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="f1f49-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




