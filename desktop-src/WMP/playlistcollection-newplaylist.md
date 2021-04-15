---
title: PlaylistCollection. reproducción, método
description: El método reproducción crea una nueva lista de reproducción en la biblioteca.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- método reproducción de Windows Media Player
- método reproducción de Windows Media Player, clase PlaylistCollection
- Clase PlaylistCollection Windows Media Player, método reproducción
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d94c25a8dfe6f1eb7c4dac40dd644433a5f0d7e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709085"
---
# <a name="playlistcollectionnewplaylist-method"></a><span data-ttu-id="417b2-106">PlaylistCollection. reproducción, método</span><span class="sxs-lookup"><span data-stu-id="417b2-106">PlaylistCollection.newPlaylist method</span></span>

<span data-ttu-id="417b2-107">El método **reproducción** crea una nueva lista de reproducción en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="417b2-107">The **newPlaylist** method creates a new playlist in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="417b2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="417b2-108">Syntax</span></span>


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="417b2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="417b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="417b2-110">*nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="417b2-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="417b2-111">**Cadena** que contiene el nombre de la lista de reproducción que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="417b2-111">**String** containing the name of the playlist to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="417b2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="417b2-112">Return value</span></span>

<span data-ttu-id="417b2-113">Este método devuelve un objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="417b2-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="417b2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="417b2-114">Remarks</span></span>

<span data-ttu-id="417b2-115">Este método crea una lista de reproducción vacía en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="417b2-115">This method creates an empty playlist in the library.</span></span> <span data-ttu-id="417b2-116">Para rellenar la lista de reproducción con elementos multimedia, use la *lista de reproducción*. **appendItem** o *lista de reproducción*. **insertItem**.</span><span class="sxs-lookup"><span data-stu-id="417b2-116">To fill the playlist with media items, use *Playlist*.**appendItem** or *Playlist*.**insertItem**.</span></span>

<span data-ttu-id="417b2-117">En la biblioteca se permiten varias listas de reproducción con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="417b2-117">Multiple playlists having the same name are permitted in the library.</span></span> <span data-ttu-id="417b2-118">Para evitar la creación de un nombre de lista de reproducción duplicado con este método, use **getByName** y *PlaylistArray*. **recuento** para determinar si ya existe una lista de reproducción con un nombre determinado.</span><span class="sxs-lookup"><span data-stu-id="417b2-118">To avoid creating a duplicate playlist name with this method, use **getByName** and *PlaylistArray*.**count** to determine whether a playlist with a particular name already exists.</span></span>

<span data-ttu-id="417b2-119">Los espacios iniciales y finales no se permiten en los nombres de las listas de reproducción y se quitan automáticamente del valor especificado para el parámetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="417b2-119">Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the *name* parameter.</span></span>

<span data-ttu-id="417b2-120">Para usar este método, se necesita acceso completo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="417b2-120">To use this method, full access to the library is required.</span></span> <span data-ttu-id="417b2-121">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="417b2-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="417b2-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="417b2-122">Examples</span></span>

<span data-ttu-id="417b2-123">En el siguiente ejemplo de JScript se crea una nueva lista de reproducción vacía denominada "ThreeList".</span><span class="sxs-lookup"><span data-stu-id="417b2-123">The following JScript example creates a new empty playlist called "ThreeList".</span></span> <span data-ttu-id="417b2-124">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="417b2-124">The **Player** object was created with ID="Player".</span></span>


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a><span data-ttu-id="417b2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="417b2-125">Requirements</span></span>



| <span data-ttu-id="417b2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="417b2-126">Requirement</span></span> | <span data-ttu-id="417b2-127">Value</span><span class="sxs-lookup"><span data-stu-id="417b2-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="417b2-128">Versión</span><span class="sxs-lookup"><span data-stu-id="417b2-128">Version</span></span><br/> | <span data-ttu-id="417b2-129">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="417b2-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="417b2-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="417b2-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="417b2-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="417b2-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="417b2-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="417b2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="417b2-133">**MediaCollection. Add**</span><span class="sxs-lookup"><span data-stu-id="417b2-133">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="417b2-134">**Lista de reproducción. appendItem**</span><span class="sxs-lookup"><span data-stu-id="417b2-134">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="417b2-135">**Lista de reproducción. insertItem**</span><span class="sxs-lookup"><span data-stu-id="417b2-135">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="417b2-136">**PlaylistArray. Count**</span><span class="sxs-lookup"><span data-stu-id="417b2-136">**PlaylistArray.count**</span></span>](playlistarray-count.md)
</dt> <dt>

[<span data-ttu-id="417b2-137">**Objeto PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="417b2-137">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="417b2-138">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="417b2-138">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> <dt>

[<span data-ttu-id="417b2-139">**PlaylistCollection.importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="417b2-139">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="417b2-140">**PlaylistCollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="417b2-140">**PlaylistCollection.remove**</span></span>](playlistcollection-remove.md)
</dt> <dt>

[<span data-ttu-id="417b2-141">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="417b2-141">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="417b2-142">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="417b2-142">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





