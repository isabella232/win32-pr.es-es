---
title: Evento Player. PlaylistCollectionPlaylistAdded
description: El evento PlaylistCollectionPlaylistAdded se produce cuando se agrega una lista de reproducción a la colección de listas de reproducción. | Evento Player. PlaylistCollectionPlaylistAdded
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- Media Player PlaylistCollectionPlaylistAdded de eventos de Windows
- Evento PlaylistCollectionPlaylistAdded de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento PlaylistCollectionPlaylistAdded
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a229aff95d29ae93433dab538521d88c50c1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708952"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a><span data-ttu-id="723d2-107">Evento Player. PlaylistCollectionPlaylistAdded</span><span class="sxs-lookup"><span data-stu-id="723d2-107">Player.PlaylistCollectionPlaylistAdded event</span></span>

<span data-ttu-id="723d2-108">El evento **PlaylistCollectionPlaylistAdded** se produce cuando se agrega una lista de reproducción a la colección de listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="723d2-108">The **PlaylistCollectionPlaylistAdded** event occurs when a playlist is added to the playlist collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="723d2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="723d2-109">Syntax</span></span>


```JScript
Player.PlaylistCollectionPlaylistAdded(
  bstrPlaylistName
)
```



## <a name="parameters"></a><span data-ttu-id="723d2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="723d2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="723d2-111">*bstrPlaylistName*</span><span class="sxs-lookup"><span data-stu-id="723d2-111">*bstrPlaylistName*</span></span> 
</dt> <dd>

<span data-ttu-id="723d2-112">**Cadena** que especifica el nombre de la lista de reproducción que se ha agregado.</span><span class="sxs-lookup"><span data-stu-id="723d2-112">**String** specifying the name of the playlist that was added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="723d2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="723d2-113">Return value</span></span>

<span data-ttu-id="723d2-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="723d2-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="723d2-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="723d2-115">Remarks</span></span>

<span data-ttu-id="723d2-116">El nombre de la lista de reproducción que se ha agregado se puede usar para recuperar el objeto de **lista de reproducción** correspondiente mediante *PlaylistCollection*. método **getByName** .</span><span class="sxs-lookup"><span data-stu-id="723d2-116">The name of the playlist that was added can be used to retrieve the corresponding **Playlist** object using the *PlaylistCollection*.**getByName** method.</span></span>

<span data-ttu-id="723d2-117">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="723d2-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="723d2-118">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="723d2-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="723d2-119">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="723d2-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="723d2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="723d2-120">Requirements</span></span>



| <span data-ttu-id="723d2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="723d2-121">Requirement</span></span> | <span data-ttu-id="723d2-122">Value</span><span class="sxs-lookup"><span data-stu-id="723d2-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="723d2-123">Versión</span><span class="sxs-lookup"><span data-stu-id="723d2-123">Version</span></span><br/> | <span data-ttu-id="723d2-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="723d2-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="723d2-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="723d2-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="723d2-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="723d2-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="723d2-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="723d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="723d2-128">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="723d2-128">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="723d2-129">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="723d2-129">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





