---
title: Network. maxBandwidth
description: La propiedad maxBandwidth especifica o recupera el ancho de banda máximo permitido.
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- Red. maxBandwidth Windows Media Player
topic_type:
- apiref
api_name:
- Network.maxBandwidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbe8283c4cc756a4f88fad1240df3a757b53a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649494"
---
# <a name="networkmaxbandwidth"></a><span data-ttu-id="1085f-104">Network. maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="1085f-104">Network.maxBandwidth</span></span>

<span data-ttu-id="1085f-105">La propiedad **maxBandwidth** especifica o recupera el ancho de banda máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="1085f-105">The **maxBandwidth** property specifies or retrieves the maximum allowed bandwidth.</span></span>

## <a name="syntax"></a><span data-ttu-id="1085f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1085f-106">Syntax</span></span>

<span data-ttu-id="1085f-107">*reproductor*. *red*. **maxBandwidth**</span><span class="sxs-lookup"><span data-stu-id="1085f-107">*player*.*network*.**maxBandwidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="1085f-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="1085f-108">Possible Values</span></span>

<span data-ttu-id="1085f-109">Esta propiedad es un **número** de lectura y escritura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="1085f-109">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="1085f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1085f-110">Remarks</span></span>

<span data-ttu-id="1085f-111">Esta propiedad no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1085f-111">This property has no default value.</span></span> <span data-ttu-id="1085f-112">Se puede especificar su valor mientras se reproduce Windows Media Player, pero el cambio no surtirá efecto hasta que se libere el elemento multimedia actual abriendo otro o llamando al *reproductor*. **cierre**.</span><span class="sxs-lookup"><span data-stu-id="1085f-112">Its value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling *Player*.**close**.</span></span> <span data-ttu-id="1085f-113">Windows Media Player intenta lograr el ancho de banda más alto posible.</span><span class="sxs-lookup"><span data-stu-id="1085f-113">Windows Media Player attempts to achieve the highest bandwidth possible.</span></span> <span data-ttu-id="1085f-114">Solo en el caso del valor que se está configurando, se producirá cualquier reducción del ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="1085f-114">Only in the case of the value being set will any bandwidth reduction occur.</span></span>

<span data-ttu-id="1085f-115">Esta configuración es útil para reducir la cantidad de ancho de banda que se usa, especialmente en el caso de una secuencia de velocidad de bits múltiple (MBR).</span><span class="sxs-lookup"><span data-stu-id="1085f-115">This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream.</span></span> <span data-ttu-id="1085f-116">Una secuencia MBR contiene varias secuencias con velocidades de bits diferentes.</span><span class="sxs-lookup"><span data-stu-id="1085f-116">An MBR stream contains multiple streams with different bit rates.</span></span> <span data-ttu-id="1085f-117">En algunos casos, puede ser conveniente usar una secuencia con una velocidad de bits menor que la que requiere el cliente.</span><span class="sxs-lookup"><span data-stu-id="1085f-117">In some cases, it may be desirable to use a stream with a lower bit rate than the client requires.</span></span> <span data-ttu-id="1085f-118">En este caso, si se establece la propiedad **maxBandwidth** , se seleccionará una secuencia de velocidad de bits inferior.</span><span class="sxs-lookup"><span data-stu-id="1085f-118">In this case, setting the **maxBandwidth** property will select a lower bit-rate stream.</span></span>

<span data-ttu-id="1085f-119">Por ejemplo, una secuencia MBR podría incluir secuencias codificadas a 20 kilobits por segundo (kbps), 37 Kbps y 200 Kbps.</span><span class="sxs-lookup"><span data-stu-id="1085f-119">For example, an MBR stream could include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps.</span></span> <span data-ttu-id="1085f-120">Si se establece la propiedad **maxBandwidth** en 50.000 (50 Kbps), se seleccionará la secuencia de 37 kbps en lugar de la secuencia de 200 Kbps.</span><span class="sxs-lookup"><span data-stu-id="1085f-120">Setting the **maxBandwidth** property to 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="1085f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1085f-121">Requirements</span></span>



| <span data-ttu-id="1085f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1085f-122">Requirement</span></span> | <span data-ttu-id="1085f-123">Value</span><span class="sxs-lookup"><span data-stu-id="1085f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1085f-124">Versión</span><span class="sxs-lookup"><span data-stu-id="1085f-124">Version</span></span><br/> | <span data-ttu-id="1085f-125">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="1085f-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1085f-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1085f-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="1085f-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1085f-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1085f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="1085f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1085f-129">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="1085f-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="1085f-130">**Player. Close**</span><span class="sxs-lookup"><span data-stu-id="1085f-130">**Player.close**</span></span>](player-close.md)
</dt> </dl>

 

 





