---
title: PlaylistCollection. getByName, método
description: El método getByName recupera un objeto PlaylistArray que contiene listas de reproducción con el nombre especificado, si existe alguno.
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- método getByName de Windows Media Player
- método getByName de Windows Media Player, clase PlaylistCollection
- Clase PlaylistCollection Windows Media Player, método getByName
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7954df8e0ccc487df77ea31b3a26dce9eea6d2e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718883"
---
# <a name="playlistcollectiongetbyname-method"></a><span data-ttu-id="e0a21-106">PlaylistCollection. getByName, método</span><span class="sxs-lookup"><span data-stu-id="e0a21-106">PlaylistCollection.getByName method</span></span>

<span data-ttu-id="e0a21-107">El método **getByName** recupera un objeto **PlaylistArray** que contiene listas de reproducción con el nombre especificado, si existe alguno.</span><span class="sxs-lookup"><span data-stu-id="e0a21-107">The **getByName** method retrieves a **PlaylistArray** object containing playlists with the specified name, if any exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0a21-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0a21-108">Syntax</span></span>


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="e0a21-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0a21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0a21-110">*nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e0a21-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0a21-111">**Cadena** que contiene el nombre de las listas de reproducción que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="e0a21-111">**String** containing the name of the playlists to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0a21-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0a21-112">Return value</span></span>

<span data-ttu-id="e0a21-113">Este método devuelve un objeto **PlaylistArray** .</span><span class="sxs-lookup"><span data-stu-id="e0a21-113">This method returns a **PlaylistArray** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0a21-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0a21-114">Remarks</span></span>

<span data-ttu-id="e0a21-115">Use *PlaylistArray*. **recuento** para determinar si existe una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e0a21-115">Use *PlaylistArray*.**count** to determine whether a playlist exists.</span></span> <span data-ttu-id="e0a21-116">Si **Count** es cero, no existe ninguna lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e0a21-116">If **count** is zero, a playlist does not exist.</span></span>

<span data-ttu-id="e0a21-117">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e0a21-117">To use this method, read access to the library is required.</span></span> <span data-ttu-id="e0a21-118">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e0a21-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e0a21-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e0a21-119">Examples</span></span>

<span data-ttu-id="e0a21-120">En el siguiente ejemplo de JScript se usa *playlistCollection*. **getByName** para comprobar el objeto **playlistCollection** para una lista de reproducción denominada "ThreeList".</span><span class="sxs-lookup"><span data-stu-id="e0a21-120">The following JScript example uses *playlistCollection*.**getByName** to check the **playlistCollection** object for a playlist named "ThreeList".</span></span> <span data-ttu-id="e0a21-121">Si existe la lista de reproducción "Threelist", **getByName** establece "Threelist" como la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="e0a21-121">If the "Threelist" playlist exists, **getByName** sets "ThreeList" as the current playlist.</span></span> <span data-ttu-id="e0a21-122">El objeto **Player** se creó con el identificador = "Player".</span><span class="sxs-lookup"><span data-stu-id="e0a21-122">The **Player** object was created with the ID = "Player".</span></span>


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a><span data-ttu-id="e0a21-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0a21-123">Requirements</span></span>



| <span data-ttu-id="e0a21-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0a21-124">Requirement</span></span> | <span data-ttu-id="e0a21-125">Value</span><span class="sxs-lookup"><span data-stu-id="e0a21-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0a21-126">Versión</span><span class="sxs-lookup"><span data-stu-id="e0a21-126">Version</span></span><br/> | <span data-ttu-id="e0a21-127">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e0a21-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e0a21-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e0a21-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="e0a21-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0a21-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0a21-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0a21-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0a21-131">**Objeto PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="e0a21-131">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="e0a21-132">**PlaylistArray. Count**</span><span class="sxs-lookup"><span data-stu-id="e0a21-132">**PlaylistArray.count**</span></span>](playlistarray-count.md)
</dt> <dt>

[<span data-ttu-id="e0a21-133">**Objeto PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="e0a21-133">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="e0a21-134">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e0a21-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e0a21-135">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e0a21-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





