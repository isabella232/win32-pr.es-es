---
title: Player. openPlayer (método)
description: El método openPlayer abre Windows Media Player mediante la dirección URL especificada. | Player. openPlayer (método)
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- método openPlayer de Windows Media Player
- método openPlayer Windows Media Player, clase Player
- Clase Player Media Player Windows, método openPlayer
topic_type:
- apiref
api_name:
- Player.openPlayer
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3378df48f961f1aa5e3fccec72e79b7f1c26ff08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708766"
---
# <a name="playeropenplayer-method"></a><span data-ttu-id="437d2-107">Player. openPlayer (método)</span><span class="sxs-lookup"><span data-stu-id="437d2-107">Player.openPlayer method</span></span>

<span data-ttu-id="437d2-108">El método **openPlayer** abre Windows Media Player mediante la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="437d2-108">The **openPlayer** method opens Windows Media Player using the specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="437d2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="437d2-109">Syntax</span></span>


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="437d2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="437d2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="437d2-111">*Dirección URL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="437d2-111">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="437d2-112">**Cadena** que representa la dirección URL del elemento multimedia que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="437d2-112">**String** representing the URL of the media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="437d2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="437d2-113">Return value</span></span>

<span data-ttu-id="437d2-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="437d2-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="437d2-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="437d2-115">Remarks</span></span>

<span data-ttu-id="437d2-116">Este método inicia Windows Media Player con la dirección URL especificada como elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="437d2-116">This method launches Windows Media Player with the specified URL set as the current media item.</span></span> <span data-ttu-id="437d2-117">Si el reproductor se cerró previamente en modo de máscara, se abrirá con la última máscara elegida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="437d2-117">If the Player was previously closed in skin mode it will open using the skin last chosen by the user.</span></span> <span data-ttu-id="437d2-118">De lo contrario, el reproductor se abre en modo completo.</span><span class="sxs-lookup"><span data-stu-id="437d2-118">Otherwise, the Player opens in full mode.</span></span>

<span data-ttu-id="437d2-119">Si se llama a este método desde un control PlayerActiveX de Windows Media incrustado en modo remoto, su comportamiento es idéntico al de *PlayerApplication*. método **switchToPlayerApplication** .</span><span class="sxs-lookup"><span data-stu-id="437d2-119">If this method is called from a Windows Media PlayerActiveX control embedded in remote mode, its behavior is identical to the *PlayerApplication*.**switchToPlayerApplication** method.</span></span>

<span data-ttu-id="437d2-120">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="437d2-120">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="437d2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="437d2-121">Requirements</span></span>



| <span data-ttu-id="437d2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="437d2-122">Requirement</span></span> | <span data-ttu-id="437d2-123">Value</span><span class="sxs-lookup"><span data-stu-id="437d2-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="437d2-124">Versión</span><span class="sxs-lookup"><span data-stu-id="437d2-124">Version</span></span><br/> | <span data-ttu-id="437d2-125">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="437d2-125">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="437d2-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="437d2-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="437d2-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="437d2-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="437d2-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="437d2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="437d2-129">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="437d2-129">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="437d2-130">**PlayerApplication.switchToPlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="437d2-130">**PlayerApplication.switchToPlayerApplication**</span></span>](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





