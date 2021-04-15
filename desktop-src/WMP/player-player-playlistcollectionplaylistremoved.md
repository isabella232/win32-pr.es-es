---
title: Evento Player. PlaylistCollectionPlaylistRemoved
description: El evento PlaylistCollectionPlaylistRemoved se produce cuando se quita una lista de reproducción de la colección de listas de reproducción. | Evento Player. PlaylistCollectionPlaylistRemoved
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- Media Player PlaylistCollectionPlaylistRemoved de eventos de Windows
- Evento PlaylistCollectionPlaylistRemoved de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento PlaylistCollectionPlaylistRemoved
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a449a7b00516f4fee613722d1cc126eb74227948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709225"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a><span data-ttu-id="e1d04-107">Evento Player. PlaylistCollectionPlaylistRemoved</span><span class="sxs-lookup"><span data-stu-id="e1d04-107">Player.PlaylistCollectionPlaylistRemoved event</span></span>

<span data-ttu-id="e1d04-108">El evento **PlaylistCollectionPlaylistRemoved** se produce cuando se quita una lista de reproducción de la colección de listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e1d04-108">The **PlaylistCollectionPlaylistRemoved** event occurs when a playlist is removed from the playlist collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d04-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1d04-109">Syntax</span></span>


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a><span data-ttu-id="e1d04-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1d04-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1d04-111">*bstrPlaylistName*</span><span class="sxs-lookup"><span data-stu-id="e1d04-111">*bstrPlaylistName*</span></span> 
</dt> <dd>

<span data-ttu-id="e1d04-112">**Cadena** que especifica el nombre de la lista de reproducción que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="e1d04-112">**String** specifying the name of the playlist that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1d04-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1d04-113">Return value</span></span>

<span data-ttu-id="e1d04-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="e1d04-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1d04-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1d04-115">Remarks</span></span>

<span data-ttu-id="e1d04-116">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="e1d04-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="e1d04-117">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e1d04-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="e1d04-118">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="e1d04-118">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1d04-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1d04-119">Requirements</span></span>



| <span data-ttu-id="e1d04-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1d04-120">Requirement</span></span> | <span data-ttu-id="e1d04-121">Value</span><span class="sxs-lookup"><span data-stu-id="e1d04-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d04-122">Versión</span><span class="sxs-lookup"><span data-stu-id="e1d04-122">Version</span></span><br/> | <span data-ttu-id="e1d04-123">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e1d04-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e1d04-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e1d04-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1d04-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1d04-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1d04-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1d04-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d04-127">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="e1d04-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="e1d04-128">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="e1d04-128">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





