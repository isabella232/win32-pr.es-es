---
title: MediaCollection. getAll, método
description: El método getAll recupera una lista de reproducción que contiene todos los elementos multimedia de la biblioteca.
ms.assetid: c22532ee-5714-4762-966f-7dc6543384f4
keywords:
- getAll (método) de Windows Media Player
- getAll (método) Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getAll
topic_type:
- apiref
api_name:
- MediaCollection.getAll
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1681cd533be4084123cb80cdcc199ab5e1ce2981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690640"
---
# <a name="mediacollectiongetall-method"></a><span data-ttu-id="0fbe4-106">MediaCollection. getAll, método</span><span class="sxs-lookup"><span data-stu-id="0fbe4-106">MediaCollection.getAll method</span></span>

<span data-ttu-id="0fbe4-107">El método **getAll** recupera una lista de reproducción que contiene todos los elementos multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0fbe4-107">The **getAll** method retrieves a playlist containing all media items in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fbe4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0fbe4-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getAll()
```



## <a name="parameters"></a><span data-ttu-id="0fbe4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fbe4-109">Parameters</span></span>

<span data-ttu-id="0fbe4-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0fbe4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0fbe4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0fbe4-111">Return value</span></span>

<span data-ttu-id="0fbe4-112">Este método devuelve un objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="0fbe4-112">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fbe4-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fbe4-113">Remarks</span></span>

<span data-ttu-id="0fbe4-114">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0fbe4-114">To use this method, read access to the library is required.</span></span> <span data-ttu-id="0fbe4-115">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0fbe4-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0fbe4-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0fbe4-116">Examples</span></span>

<span data-ttu-id="0fbe4-117">En el siguiente ejemplo de JScript se usa *MediaCollection*. **getAll** para reproducir elementos multimedia aleatoriamente desde la colección de medios.</span><span class="sxs-lookup"><span data-stu-id="0fbe4-117">The following JScript example uses *MediaCollection*.**getAll** to play media items randomly from the media collection.</span></span> <span data-ttu-id="0fbe4-118">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="0fbe4-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the count of all media items in the media collection.
var count = Player.mediaCollection.getAll().count;

// Generate a random number using the media count.
var rand = Math.random() * count;

// Round down the random number to the nearest integer.
rand = Math.floor(rand);

// Make the random media item the current media item.
Player.currentMedia = Player.mediaCollection.getAll().item(rand);

// Play the media item.
// Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="0fbe4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fbe4-119">Requirements</span></span>



| <span data-ttu-id="0fbe4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fbe4-120">Requirement</span></span> | <span data-ttu-id="0fbe4-121">Value</span><span class="sxs-lookup"><span data-stu-id="0fbe4-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0fbe4-122">Versión</span><span class="sxs-lookup"><span data-stu-id="0fbe4-122">Version</span></span><br/> | <span data-ttu-id="0fbe4-123">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="0fbe4-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0fbe4-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0fbe4-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="0fbe4-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fbe4-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fbe4-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fbe4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fbe4-127">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="0fbe4-127">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="0fbe4-128">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="0fbe4-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="0fbe4-129">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0fbe4-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="0fbe4-130">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0fbe4-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





