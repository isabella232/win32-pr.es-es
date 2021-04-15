---
title: Playlist. Item (método)
description: El método Item recupera el elemento multimedia en el índice especificado.
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- método de elemento Media Player de Windows
- método de elemento Windows Media Player, clase playlist
- Clase PlayList Windows Media Player, método Item
topic_type:
- apiref
api_name:
- Playlist.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c69386871aeec33dbc36a066ce3f75e80d7514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709216"
---
# <a name="playlistitem-method"></a><span data-ttu-id="96be9-106">Playlist. Item (método)</span><span class="sxs-lookup"><span data-stu-id="96be9-106">Playlist.item method</span></span>

<span data-ttu-id="96be9-107">El método **Item** recupera el elemento multimedia en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="96be9-107">The **item** method retrieves the media item at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="96be9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96be9-108">Syntax</span></span>


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="96be9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96be9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96be9-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="96be9-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96be9-111">**Número** (**largo**) que contiene el índice del elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="96be9-111">**Number** (**long**) containing the index of the item to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96be9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96be9-112">Return value</span></span>

<span data-ttu-id="96be9-113">Este método devuelve un objeto **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="96be9-113">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="96be9-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96be9-114">Remarks</span></span>

<span data-ttu-id="96be9-115">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="96be9-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="96be9-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="96be9-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="96be9-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="96be9-117">Examples</span></span>

<span data-ttu-id="96be9-118">En el siguiente ejemplo de JScript se usa la *lista de reproducción*. **elemento** para recuperar un elemento multimedia de la lista de reproducción actual en función de la selección del usuario.</span><span class="sxs-lookup"><span data-stu-id="96be9-118">The following JScript example uses *Playlist*.**item** to retrieve a media item from the current playlist based on a user selection.</span></span> <span data-ttu-id="96be9-119">Se ha creado un elemento SELECT de HTML con el nombre "weblist" y se ha rellenado con los títulos de la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="96be9-119">An HTML SELECT element was created with name "weblist", and filled with the titles from the current playlist.</span></span> <span data-ttu-id="96be9-120">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="96be9-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the value of the selected item in the list box
// using the selectedIndex property.
var index = weblist.selectedIndex;

// Store the corresponding digital media object from the current playlist.
var listItem = Player.currentPlaylist.item(index);

// Set the URL using the listItem variable.
Player.URL = listItem.sourceURL;

```



## <a name="requirements"></a><span data-ttu-id="96be9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96be9-121">Requirements</span></span>



| <span data-ttu-id="96be9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="96be9-122">Requirement</span></span> | <span data-ttu-id="96be9-123">Value</span><span class="sxs-lookup"><span data-stu-id="96be9-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96be9-124">Versión</span><span class="sxs-lookup"><span data-stu-id="96be9-124">Version</span></span><br/> | <span data-ttu-id="96be9-125">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="96be9-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="96be9-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="96be9-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="96be9-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96be9-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96be9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="96be9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96be9-129">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="96be9-129">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="96be9-130">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="96be9-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="96be9-131">**Lista de reproducción. insertItem**</span><span class="sxs-lookup"><span data-stu-id="96be9-131">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="96be9-132">**Lista de reproducción. removeItem**</span><span class="sxs-lookup"><span data-stu-id="96be9-132">**Playlist.removeItem**</span></span>](playlist-removeitem.md)
</dt> <dt>

[<span data-ttu-id="96be9-133">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="96be9-133">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="96be9-134">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="96be9-134">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





