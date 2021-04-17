---
title: Playlist. removeItem (método)
description: El método removeItem quita el elemento especificado de la lista de reproducción.
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- método removeItem Media Player Windows
- método removeItem Windows Media Player, clase playlist
- Clase PlayList Windows Media Player, método removeItem
topic_type:
- apiref
api_name:
- Playlist.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de03333e2373744f9e9197be8ed8582997c557d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708808"
---
# <a name="playlistremoveitem-method"></a><span data-ttu-id="16b00-106">Playlist. removeItem (método)</span><span class="sxs-lookup"><span data-stu-id="16b00-106">Playlist.removeItem method</span></span>

<span data-ttu-id="16b00-107">El método **RemoveItem** quita el elemento especificado de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="16b00-107">The **removeItem** method removes the specified item from the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b00-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16b00-108">Syntax</span></span>


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="16b00-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16b00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16b00-110">*elemento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="16b00-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b00-111">Objeto **multimedia** que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="16b00-111">**Media** object to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16b00-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16b00-112">Return value</span></span>

<span data-ttu-id="16b00-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="16b00-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16b00-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16b00-114">Remarks</span></span>

<span data-ttu-id="16b00-115">Si el elemento que se quita es la pista actual (*jugador*.**currentMedia**), se detiene la reproducción y el siguiente elemento de la lista de reproducción se convierte en el actual.</span><span class="sxs-lookup"><span data-stu-id="16b00-115">If the item removed is the currently playing track (*Player*.**currentMedia**), playback stops and the next item in the playlist becomes the current one.</span></span> <span data-ttu-id="16b00-116">Si no hay ningún elemento siguiente, se usa el elemento anterior o si no hay otros elementos y, a continuación, el *jugador*. **currentMedia** se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="16b00-116">If there is no next item, the previous item is used, or if there are no other items, then *Player*.**currentMedia** is set to **NULL**.</span></span>

<span data-ttu-id="16b00-117">Para usar este método, se necesita acceso completo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="16b00-117">To use this method, full access to the library is required.</span></span> <span data-ttu-id="16b00-118">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="16b00-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16b00-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16b00-119">Requirements</span></span>



| <span data-ttu-id="16b00-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="16b00-120">Requirement</span></span> | <span data-ttu-id="16b00-121">Value</span><span class="sxs-lookup"><span data-stu-id="16b00-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16b00-122">Versión</span><span class="sxs-lookup"><span data-stu-id="16b00-122">Version</span></span><br/> | <span data-ttu-id="16b00-123">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="16b00-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="16b00-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="16b00-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="16b00-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16b00-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16b00-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="16b00-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16b00-127">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="16b00-127">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="16b00-128">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="16b00-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="16b00-129">**Lista de reproducción. insertItem**</span><span class="sxs-lookup"><span data-stu-id="16b00-129">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="16b00-130">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="16b00-130">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="16b00-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="16b00-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="16b00-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="16b00-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





