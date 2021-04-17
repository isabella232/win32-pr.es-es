---
title: Controls. currentItem
description: La propiedad currentItem especifica o recupera el elemento multimedia actual.
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- Controls. currentItem Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentItem
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81658665cb6f31acd327f5050a733a2fc3c70371
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699932"
---
# <a name="controlscurrentitem"></a><span data-ttu-id="49d13-104">Controls. currentItem</span><span class="sxs-lookup"><span data-stu-id="49d13-104">Controls.currentItem</span></span>

<span data-ttu-id="49d13-105">La propiedad **CurrentItem** especifica o recupera el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="49d13-105">The **currentItem** property specifies or retrieves the current media item.</span></span>

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a><span data-ttu-id="49d13-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="49d13-106">Possible Values</span></span>

<span data-ttu-id="49d13-107">Esta propiedad es un objeto **multimedia** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="49d13-107">This property is a read/write **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="49d13-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49d13-108">Remarks</span></span>

<span data-ttu-id="49d13-109">Este método solo funciona con elementos del *reproductor*. **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="49d13-109">This method works only with items in *Player*.**currentPlaylist**.</span></span> <span data-ttu-id="49d13-110">No se admite la llamada a **CurrentItem** con una referencia a un elemento multimedia guardado.</span><span class="sxs-lookup"><span data-stu-id="49d13-110">Calling **currentItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="49d13-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="49d13-111">Examples</span></span>

<span data-ttu-id="49d13-112">En el siguiente ejemplo de JScript se usa **CurrentItem** para establecer el elemento multimedia actual del control Player en el valor seleccionado en un elemento Select de HTML.</span><span class="sxs-lookup"><span data-stu-id="49d13-112">The following JScript example uses **currentItem** to set the player control current media item to the selected value in an HTML SELECT element.</span></span> <span data-ttu-id="49d13-113">La lista de reproducción actual se especificó por primera vez mediante *PlaylistCollection*. **getByName**.</span><span class="sxs-lookup"><span data-stu-id="49d13-113">The current playlist was first specified by using *PlaylistCollection*.**getByName**.</span></span> <span data-ttu-id="49d13-114">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="49d13-114">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = playItem  NAME = "playItem"  LANGUAGE = "JScript"

    /* Specify the current item when the selected list value changes. */
    onChange = "Player.controls.currentItem = Player.currentPlaylist.item(playItem.value);">

    /* Fill the SELECT element list with three items that match
       the songs in the playlist. */
    <OPTION VALUE = 0 >Laure
    <OPTION VALUE = 1 >Jeanne
    <OPTION VALUE = 2 >House
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="49d13-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49d13-115">Requirements</span></span>



| <span data-ttu-id="49d13-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="49d13-116">Requirement</span></span> | <span data-ttu-id="49d13-117">Value</span><span class="sxs-lookup"><span data-stu-id="49d13-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="49d13-118">Versión</span><span class="sxs-lookup"><span data-stu-id="49d13-118">Version</span></span><br/> | <span data-ttu-id="49d13-119">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="49d13-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="49d13-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49d13-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="49d13-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49d13-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49d13-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="49d13-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49d13-123">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="49d13-123">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="49d13-124">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="49d13-124">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="49d13-125">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="49d13-125">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





