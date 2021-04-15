---
title: Método playlist. appendItem
description: El método appendItem agrega un elemento multimedia al final de la lista de reproducción.
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- método appendItem de Windows Media Player
- método appendItem Windows Media Player, clase playlist
- Clase PlayList Windows Media Player, método appendItem
topic_type:
- apiref
api_name:
- Playlist.appendItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 828799d5b6e71e7ff0e7be4c1e55714f6343be51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708781"
---
# <a name="playlistappenditem-method"></a><span data-ttu-id="23027-106">Método playlist. appendItem</span><span class="sxs-lookup"><span data-stu-id="23027-106">Playlist.appendItem method</span></span>

<span data-ttu-id="23027-107">El método **appendItem** agrega un elemento multimedia al final de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="23027-107">The **appendItem** method adds a media item to the end of the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="23027-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23027-108">Syntax</span></span>


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="23027-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23027-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23027-110">*elemento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="23027-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23027-111">Objeto **multimedia** que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="23027-111">**Media** object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23027-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23027-112">Return value</span></span>

<span data-ttu-id="23027-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="23027-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23027-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23027-114">Remarks</span></span>

<span data-ttu-id="23027-115">Para usar este método, se necesita acceso completo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="23027-115">To use this method, full access to the library is required.</span></span> <span data-ttu-id="23027-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="23027-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="23027-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="23027-117">Examples</span></span>

<span data-ttu-id="23027-118">En el siguiente ejemplo de JScript se usa la *lista de reproducción*. **appendItem** para agregar el elemento multimedia actual a la lista de reproducción denominada "ThreeList".</span><span class="sxs-lookup"><span data-stu-id="23027-118">The following JScript example uses *Playlist*.**appendItem** to add the current media item to the playlist named "ThreeList".</span></span> <span data-ttu-id="23027-119">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="23027-119">The **Player** object was created with ID="Player".</span></span>


```JScript
// Get the current media item.
var currMedia = Player.currentMedia;

// Get the playlist object by name.
var plThreeList = Player.playlistCollection.getByName("ThreeList").item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);

```



## <a name="requirements"></a><span data-ttu-id="23027-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23027-120">Requirements</span></span>



| <span data-ttu-id="23027-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="23027-121">Requirement</span></span> | <span data-ttu-id="23027-122">Value</span><span class="sxs-lookup"><span data-stu-id="23027-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23027-123">Versión</span><span class="sxs-lookup"><span data-stu-id="23027-123">Version</span></span><br/> | <span data-ttu-id="23027-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="23027-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="23027-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23027-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="23027-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23027-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23027-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="23027-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23027-128">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="23027-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="23027-129">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="23027-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="23027-130">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="23027-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





