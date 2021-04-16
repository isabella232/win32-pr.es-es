---
title: Método media. isMemberOf
description: El método isMemberOf devuelve un valor que indica si el elemento multimedia es un miembro de la lista de reproducción especificada.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- método isMemberOf de Windows Media Player
- método isMemberOf Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método isMemberOf
topic_type:
- apiref
api_name:
- Media.isMemberOf
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41555bd5910ddb3151468a458c5becbf247ea484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699363"
---
# <a name="mediaismemberof-method"></a><span data-ttu-id="90f5b-106">Método media. isMemberOf</span><span class="sxs-lookup"><span data-stu-id="90f5b-106">Media.isMemberOf method</span></span>

<span data-ttu-id="90f5b-107">El método **isMemberOf** devuelve un valor que indica si el elemento multimedia es un miembro de la lista de reproducción especificada.</span><span class="sxs-lookup"><span data-stu-id="90f5b-107">The **isMemberOf** method returns a value indicating whether the media item is a member of the specified playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="90f5b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90f5b-108">Syntax</span></span>


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="90f5b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90f5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90f5b-110">*lista de reproducción* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90f5b-110">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90f5b-111">Objeto de **lista de reproducción** que puede contener el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="90f5b-111">**Playlist** object that might contain the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90f5b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90f5b-112">Return value</span></span>

<span data-ttu-id="90f5b-113">Este método devuelve un **valor booleano**.</span><span class="sxs-lookup"><span data-stu-id="90f5b-113">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="90f5b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90f5b-114">Remarks</span></span>

<span data-ttu-id="90f5b-115">Este método no puede comprobar las listas de reproducción recuperadas a través del objeto **MediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="90f5b-115">This method is cannot check playlists retrieved through the **MediaCollection** object.</span></span> <span data-ttu-id="90f5b-116">Para probar si un elemento multimedia es miembro de una lista de reproducción con nombre determinada, recupere la lista de reproducción con el *reproductor*. *playlistCollection*. **getByName**(*nombre*). **elemento**(0).</span><span class="sxs-lookup"><span data-stu-id="90f5b-116">To test whether a media item is a member of a particular named playlist, retrieve the playlist with *player*.*playlistCollection*.**getByName**(*name*).**item**(0).</span></span> <span data-ttu-id="90f5b-117">Este método también se puede utilizar con listas de reproducción de CD y listas de reproducción de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="90f5b-117">This method can also be used with CD playlists and metafile playlists.</span></span>

<span data-ttu-id="90f5b-118">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="90f5b-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="90f5b-119">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="90f5b-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="90f5b-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="90f5b-120">Examples</span></span>

<span data-ttu-id="90f5b-121">En el siguiente ejemplo de JScript se utiliza el *medio*. **isMemberOf** para comprobar si el elemento multimedia actual es un miembro de la lista de reproducción denominada lista de reproducción de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="90f5b-121">The following JScript example uses *Media*.**isMemberOf** to test whether the current media item is a member of the playlist named Sample Playlist.</span></span> <span data-ttu-id="90f5b-122">Si no es así, el elemento multimedia actual se anexa a la lista de reproducción de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="90f5b-122">If it is not, the current media item is appended to the sample playlist.</span></span> <span data-ttu-id="90f5b-123">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="90f5b-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the playlist object named Sample Playlist.
var sPlaylist = Player.playlistcollection.getbyname("Sample Playlist").item(0);

// Test whether the current media item is a member of Sample Playlist.
 var answer = ((Player.currentMedia.isMemberOf(sPlaylist))?"Yes":"No");

// If the current media item is not a member of Sample Playlist,
// append the current media item to the playlist.
if (answer == "No"){
   sPlaylist.appendItem(Player.currentMedia);
}

```



## <a name="requirements"></a><span data-ttu-id="90f5b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90f5b-124">Requirements</span></span>



| <span data-ttu-id="90f5b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="90f5b-125">Requirement</span></span> | <span data-ttu-id="90f5b-126">Value</span><span class="sxs-lookup"><span data-stu-id="90f5b-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="90f5b-127">Versión</span><span class="sxs-lookup"><span data-stu-id="90f5b-127">Version</span></span><br/> | <span data-ttu-id="90f5b-128">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="90f5b-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="90f5b-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="90f5b-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="90f5b-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90f5b-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90f5b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="90f5b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90f5b-132">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="90f5b-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="90f5b-133">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="90f5b-133">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="90f5b-134">**Objeto PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="90f5b-134">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="90f5b-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="90f5b-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="90f5b-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="90f5b-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





