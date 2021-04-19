---
title: Controls. playItem (método)
description: El método playItem reproduce el elemento multimedia especificado. | Controls. playItem (método)
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- método playItem de Windows Media Player
- método playItem Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método playItem
topic_type:
- apiref
api_name:
- Controls.playItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9096e378a328f43147a0a94d97034c8e566b611
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700145"
---
# <a name="controlsplayitem-method"></a><span data-ttu-id="c52be-107">Controls. playItem (método)</span><span class="sxs-lookup"><span data-stu-id="c52be-107">Controls.playItem method</span></span>

<span data-ttu-id="c52be-108">El método **playItem** reproduce el elemento multimedia especificado.</span><span class="sxs-lookup"><span data-stu-id="c52be-108">The **playItem** method plays the specified media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c52be-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c52be-109">Syntax</span></span>


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a><span data-ttu-id="c52be-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c52be-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c52be-111">*theMediaItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c52be-111">*theMediaItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c52be-112">Objeto **multimedia** que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="c52be-112">**Media** object to be played.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c52be-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c52be-113">Return value</span></span>

<span data-ttu-id="c52be-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c52be-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c52be-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c52be-115">Remarks</span></span>

<span data-ttu-id="c52be-116">El elemento multimedia se cargará y reproducirá automáticamente, independientemente del valor de la *configuración*. propiedad **autoStart** .</span><span class="sxs-lookup"><span data-stu-id="c52be-116">The media item will be loaded and played automatically, regardless of the value of the *Settings*.**autoStart** property.</span></span> <span data-ttu-id="c52be-117">Para cargar un elemento sin reproducirlo automáticamente, establezca la *configuración*. Inicie **automáticamente** en false y asigne un valor a *Player*. **URL**, después del cual se puede llamar a **Play** para empezar a reproducir el elemento.</span><span class="sxs-lookup"><span data-stu-id="c52be-117">To load an item without playing it automatically, set *Settings*.**autoStart** to false and assign a value to *Player*.**URL**, after which **play** can be called to start playing the item.</span></span>

<span data-ttu-id="c52be-118">Nota</span><span class="sxs-lookup"><span data-stu-id="c52be-118">Note</span></span>

<span data-ttu-id="c52be-119">**playItem** solo funciona con elementos de *currentPlaylist*.</span><span class="sxs-lookup"><span data-stu-id="c52be-119">**playItem** works only with items in *currentPlaylist*.</span></span> <span data-ttu-id="c52be-120">No se admite la llamada a **playItem** con una referencia a un elemento multimedia guardado.</span><span class="sxs-lookup"><span data-stu-id="c52be-120">Calling **playItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="c52be-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c52be-121">Examples</span></span>

<span data-ttu-id="c52be-122">En el siguiente ejemplo de JScript se usa **playItem** para reproducir un elemento multimedia de la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="c52be-122">The following JScript example uses **playItem** to play a media item from the current playlist.</span></span> <span data-ttu-id="c52be-123">El elemento que se va a reproducir se elige en función de su posición en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c52be-123">The item to play is chosen based upon its position in the playlist.</span></span> <span data-ttu-id="c52be-124">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c52be-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
var index = 3

// Retrieve the media item at the fourth position in the current playlist.
var media = Player.currentPlaylist.item(index);

// Play the media item.
Player.controls.playItem(media);

```



## <a name="requirements"></a><span data-ttu-id="c52be-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c52be-125">Requirements</span></span>



| <span data-ttu-id="c52be-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c52be-126">Requirement</span></span> | <span data-ttu-id="c52be-127">Value</span><span class="sxs-lookup"><span data-stu-id="c52be-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c52be-128">Versión</span><span class="sxs-lookup"><span data-stu-id="c52be-128">Version</span></span><br/> | <span data-ttu-id="c52be-129">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="c52be-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c52be-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c52be-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="c52be-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c52be-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c52be-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c52be-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c52be-133">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="c52be-133">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="c52be-134">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="c52be-134">**Playlist.item**</span></span>](playlist-item.md)
</dt> </dl>

 

 





