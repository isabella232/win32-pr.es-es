---
title: CDROM. Playlist
description: La propiedad de lista de reproducción recupera un objeto de lista de reproducción que representa las pistas del CD que se encuentran actualmente en la unidad de CD o en las entradas de título de nivel de raíz de DVD.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- CDROM. Playlist Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom.playlist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdb50daa169c6f6eb0690de376abd4433ffe130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695936"
---
# <a name="cdromplaylist"></a><span data-ttu-id="5ae8f-104">CDROM. Playlist</span><span class="sxs-lookup"><span data-stu-id="5ae8f-104">Cdrom.playlist</span></span>

<span data-ttu-id="5ae8f-105">La propiedad de **lista de reproducción** recupera un objeto de **lista de reproducción** que representa las pistas del CD que se encuentran actualmente en la unidad de CD o en las entradas de título de nivel de raíz de DVD.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-105">The **playlist** property retrieves a **Playlist** object representing the tracks on the CD currently in the CD drive or the root-level title entries for DVD.</span></span>

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a><span data-ttu-id="5ae8f-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="5ae8f-106">Possible Values</span></span>

<span data-ttu-id="5ae8f-107">Esta propiedad es un objeto de **lista de reproducción** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-107">This property is a read-only **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ae8f-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ae8f-108">Remarks</span></span>

<span data-ttu-id="5ae8f-109">Normalmente, los DVDs se organizan en títulos.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-109">Typically, DVDs are organized into titles.</span></span> <span data-ttu-id="5ae8f-110">Cada título contiene uno o varios capítulos.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-110">Each title contains one or more chapters.</span></span> <span data-ttu-id="5ae8f-111">Cada DVD se crea de forma diferente, por lo que la forma de usar títulos y capítulos depende del autor del contenido.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-111">Each DVD is authored differently, so how titles and chapters are used is up to the content author.</span></span>

<span data-ttu-id="5ae8f-112">En el caso de DVD, este método recupera una lista de reproducción que contiene como primer elemento un objeto **multimedia** que representa el DVD.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-112">For DVD, this method retrieves a playlist that contains as the first item a **Media** object that represents the DVD media.</span></span> <span data-ttu-id="5ae8f-113">Reproducir el elemento hace que el DVD se reproduzca desde el principio si es el primer juego después de insertar un DVD nuevo o reanudar la reproducción si el DVD es el mismo que el último DVD visualizado.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-113">Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed.</span></span> <span data-ttu-id="5ae8f-114">Al establecer este elemento como el actual durante la reproducción, el DVD se reproduce desde el principio.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-114">Setting this item as the current one during playback results in the DVD playing from the beginning.</span></span>

<span data-ttu-id="5ae8f-115">Los elementos adicionales (objetos **multimedia** ) de la lista de reproducción son títulos de DVD que se representan mediante listas de reproducción anidadas.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-115">Additional items (**Media** objects) in the playlist are DVD titles that are represented by nested playlists.</span></span> <span data-ttu-id="5ae8f-116">Al especificar *controles*. **CurrentItem** es igual a uno de estos elementos de lista de reproducción anidados, Windows Media Player establece automáticamente la lista de reproducción anidada como *reproductor*. **currentPlaylist** después del inicio de la reproducción del capítulo.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-116">When you specify *Controls*.**currentItem** to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as *Player*.**currentPlaylist** after chapter playback begins.</span></span> <span data-ttu-id="5ae8f-117">A continuación, puede usar las propiedades, los métodos y los eventos del objeto **currentPlaylist** para trabajar con capítulos de DVD, que también son elementos de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-117">You can then use the **currentPlaylist** object properties, methods, and events to work with DVD chapters, which are also playlist items.</span></span>

<span data-ttu-id="5ae8f-118">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-118">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="5ae8f-119">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5ae8f-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="5ae8f-120">**Windows Media Player 10 Mobile:** Esta propiedad no se admite.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-120">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="5ae8f-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5ae8f-121">Examples</span></span>

<span data-ttu-id="5ae8f-122">En el ejemplo siguiente se usa *CDROM*. **lista de reproducción** para rellenar un elemento de texto HTML, denominado mi texto, con los títulos del CD de audio actualmente en la primera unidad de CD.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-122">The following example uses *Cdrom*.**playlist** to fill an HTML text element, named myText, with the titles of the audio CD currently in the first CD drive.</span></span> <span data-ttu-id="5ae8f-123">Use *CdromCollection*. **recuento** para determinar el número de unidades de CD disponibles.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-123">Use *CdromCollection*.**count** to determine the number of available CD drives.</span></span> <span data-ttu-id="5ae8f-124">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5ae8f-124">The **Player** object was created with ID = "Player".</span></span>


```
// Store the CD playlist object.
var pl = Player.cdromCollection.Item(0).Playlist;

// Iterate through the CD track list.
for(var i = 0; i < pl.count; i++){

   // Print each CD track name.
   myText.value += pl.Item(i).name + "\n"; 
}
```



## <a name="requirements"></a><span data-ttu-id="5ae8f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ae8f-125">Requirements</span></span>



| <span data-ttu-id="5ae8f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ae8f-126">Requirement</span></span> | <span data-ttu-id="5ae8f-127">Value</span><span class="sxs-lookup"><span data-stu-id="5ae8f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae8f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ae8f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5ae8f-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5ae8f-129">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5ae8f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ae8f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5ae8f-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ae8f-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5ae8f-132">Versión</span><span class="sxs-lookup"><span data-stu-id="5ae8f-132">Version</span></span><br/>                  | <span data-ttu-id="5ae8f-133">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-133">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5ae8f-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ae8f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ae8f-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ae8f-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ae8f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ae8f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ae8f-137">**CDROM (objeto)**</span><span class="sxs-lookup"><span data-stu-id="5ae8f-137">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="5ae8f-138">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5ae8f-138">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5ae8f-139">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5ae8f-139">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





