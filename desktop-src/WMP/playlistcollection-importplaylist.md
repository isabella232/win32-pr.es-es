---
title: PlaylistCollection. importPlaylist, método
description: El método importPlaylist agrega una lista de reproducción estática a la biblioteca. | PlaylistCollection. importPlaylist, método
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- método importPlaylist de Windows Media Player
- método importPlaylist de Windows Media Player, clase PlaylistCollection
- Clase PlaylistCollection Windows Media Player, método importPlaylist
topic_type:
- apiref
api_name:
- PlaylistCollection.importPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736e9afa17f571428fada48660726b606268796a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718816"
---
# <a name="playlistcollectionimportplaylist-method"></a><span data-ttu-id="cda4e-107">PlaylistCollection. importPlaylist, método</span><span class="sxs-lookup"><span data-stu-id="cda4e-107">PlaylistCollection.importPlaylist method</span></span>

<span data-ttu-id="cda4e-108">El método **importPlaylist** agrega una lista de reproducción estática a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="cda4e-108">The **importPlaylist** method adds a static playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda4e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cda4e-109">Syntax</span></span>


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="cda4e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cda4e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cda4e-111">*lista de reproducción* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cda4e-111">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cda4e-112">Objeto de **lista de reproducción** que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="cda4e-112">**Playlist** object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cda4e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cda4e-113">Return value</span></span>

<span data-ttu-id="cda4e-114">Este método devuelve el objeto de la **lista de reproducción** que se agregó.</span><span class="sxs-lookup"><span data-stu-id="cda4e-114">This method returns the **Playlist** object that was added.</span></span>

## <a name="remarks"></a><span data-ttu-id="cda4e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cda4e-115">Remarks</span></span>

<span data-ttu-id="cda4e-116">Las listas de reproducción que no contienen elementos multimedia no se pueden agregar a la biblioteca mediante este método.</span><span class="sxs-lookup"><span data-stu-id="cda4e-116">Playlists that do not contain any media items cannot be added to the library by using this method.</span></span> <span data-ttu-id="cda4e-117">Para crear una lista de reproducción vacía en la biblioteca, use el método **reproducción** .</span><span class="sxs-lookup"><span data-stu-id="cda4e-117">To create an empty playlist in the library, use the **newPlaylist** method.</span></span> <span data-ttu-id="cda4e-118">A continuación, puede rellenar la lista de reproducción resultante con elementos multimedia mediante la *lista de reproducción*. **appendItem** o *lista de reproducción*. **insertItem**.</span><span class="sxs-lookup"><span data-stu-id="cda4e-118">You can then fill the resulting playlist with media items by using *Playlist*.**appendItem** or *Playlist*.**insertItem**.</span></span>

<span data-ttu-id="cda4e-119">Si pasa este método a una lista de reproducción automática, la consulta se ejecuta una vez y el resultado se agrega a la biblioteca como una lista de reproducción estática.</span><span class="sxs-lookup"><span data-stu-id="cda4e-119">If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist.</span></span> <span data-ttu-id="cda4e-120">Para agregar una lista de reproducción automática a la biblioteca y conservar su comportamiento automático, use *MediaCollection*. **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="cda4e-120">To add an auto playlist to the library and preserve its automatic behavior, use *MediaCollection*.**add**.</span></span> <span data-ttu-id="cda4e-121">Para obtener más información, vea [listas de reproducción estáticas y automáticas](static-and-auto-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="cda4e-121">For more information, see [Static and Auto Playlists](static-and-auto-playlists.md).</span></span>

<span data-ttu-id="cda4e-122">Para usar este método, se necesita acceso completo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="cda4e-122">To use this method, full access to the library is required.</span></span> <span data-ttu-id="cda4e-123">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="cda4e-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cda4e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cda4e-124">Requirements</span></span>



| <span data-ttu-id="cda4e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cda4e-125">Requirement</span></span> | <span data-ttu-id="cda4e-126">Value</span><span class="sxs-lookup"><span data-stu-id="cda4e-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cda4e-127">Versión</span><span class="sxs-lookup"><span data-stu-id="cda4e-127">Version</span></span><br/> | <span data-ttu-id="cda4e-128">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="cda4e-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="cda4e-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cda4e-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="cda4e-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cda4e-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cda4e-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="cda4e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda4e-132">**Administrar listas de reproducción**</span><span class="sxs-lookup"><span data-stu-id="cda4e-132">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="cda4e-133">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="cda4e-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="cda4e-134">**MediaCollection. Add**</span><span class="sxs-lookup"><span data-stu-id="cda4e-134">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="cda4e-135">**Lista de reproducción. appendItem**</span><span class="sxs-lookup"><span data-stu-id="cda4e-135">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="cda4e-136">**Lista de reproducción. insertItem**</span><span class="sxs-lookup"><span data-stu-id="cda4e-136">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="cda4e-137">**Objeto PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="cda4e-137">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="cda4e-138">**PlaylistCollection. reproducción**</span><span class="sxs-lookup"><span data-stu-id="cda4e-138">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="cda4e-139">**PlaylistCollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="cda4e-139">**PlaylistCollection.remove**</span></span>](playlistcollection-remove.md)
</dt> <dt>

[<span data-ttu-id="cda4e-140">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="cda4e-140">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="cda4e-141">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="cda4e-141">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





