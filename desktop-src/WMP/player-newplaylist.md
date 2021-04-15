---
title: Player. reproducción (método)
description: El método reproducción crea un nuevo objeto de lista de reproducción.
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- método reproducción de Windows Media Player
- método reproducción Windows Media Player, clase Player
- Clase Player Media Player Windows, método reproducción
topic_type:
- apiref
api_name:
- Player.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa65ae4b453fe919116a33c5ee86b14ba353f681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708251"
---
# <a name="playernewplaylist-method"></a><span data-ttu-id="58e5a-106">Player. reproducción (método)</span><span class="sxs-lookup"><span data-stu-id="58e5a-106">Player.newPlaylist method</span></span>

<span data-ttu-id="58e5a-107">El método **reproducción** crea un nuevo objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="58e5a-107">The **newPlaylist** method creates a new **Playlist** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="58e5a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58e5a-108">Syntax</span></span>


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="58e5a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58e5a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58e5a-110">*nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="58e5a-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e5a-111">**Cadena** que contiene el nombre de la nueva lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="58e5a-111">**String** containing the name of the new playlist.</span></span>

</dd> <dt>

<span data-ttu-id="58e5a-112">*Dirección URL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58e5a-112">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e5a-113">**Cadena** que contiene la dirección URL de la lista de reproducción del metarchivo de Windows Media para crear el objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="58e5a-113">**String** containing the URL of the Windows Media metafile playlist to create the **Playlist** object with.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58e5a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58e5a-114">Return value</span></span>

<span data-ttu-id="58e5a-115">Este método devuelve un objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="58e5a-115">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="58e5a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58e5a-116">Remarks</span></span>

<span data-ttu-id="58e5a-117">Si el parámetro de *dirección URL* se establece en null o en "" (cadena vacía), se creará un objeto de **lista de reproducción** vacío.</span><span class="sxs-lookup"><span data-stu-id="58e5a-117">If the *URL* parameter is set to null or "" (empty string), an empty **Playlist** object will be created.</span></span> <span data-ttu-id="58e5a-118">Si el parámetro *Name* se establece en "", se utiliza el nombre del metarchivo.</span><span class="sxs-lookup"><span data-stu-id="58e5a-118">If the *name* parameter is set to "", the name in the metafile is used.</span></span>

<span data-ttu-id="58e5a-119">La nueva lista de reproducción creada con este método no se agrega a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="58e5a-119">The new playlist created with this method is not added to the library.</span></span> <span data-ttu-id="58e5a-120">Para agregar una nueva lista de reproducción a la biblioteca, use *PlaylistCollection*. **importPlaylist** o *PlaylistCollection*. **reproducción**.</span><span class="sxs-lookup"><span data-stu-id="58e5a-120">To add a new playlist to the library, use *PlaylistCollection*.**importPlaylist** or *PlaylistCollection*.**newPlaylist**.</span></span> <span data-ttu-id="58e5a-121">Los espacios iniciales o finales del nombre de la lista de reproducción se quitan automáticamente cuando se agregan a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="58e5a-121">Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.</span></span>

<span data-ttu-id="58e5a-122">Dado que la biblioteca permite varias listas de reproducción con el mismo nombre, es posible que desee comprobar la presencia de una lista de reproducción con un nombre determinado antes de agregar una nueva.</span><span class="sxs-lookup"><span data-stu-id="58e5a-122">Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e5a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58e5a-123">Requirements</span></span>



| <span data-ttu-id="58e5a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="58e5a-124">Requirement</span></span> | <span data-ttu-id="58e5a-125">Value</span><span class="sxs-lookup"><span data-stu-id="58e5a-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58e5a-126">Versión</span><span class="sxs-lookup"><span data-stu-id="58e5a-126">Version</span></span><br/> | <span data-ttu-id="58e5a-127">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="58e5a-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="58e5a-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="58e5a-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="58e5a-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58e5a-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e5a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="58e5a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e5a-131">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="58e5a-131">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="58e5a-132">**PlaylistCollection.importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="58e5a-132">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="58e5a-133">**PlaylistCollection. reproducción**</span><span class="sxs-lookup"><span data-stu-id="58e5a-133">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="58e5a-134">**Metaarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="58e5a-134">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 





