---
title: Player. currentMedia
description: La propiedad currentMedia especifica o recupera el objeto multimedia actual.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- Media Player de Windows Player. currentMedia
topic_type:
- apiref
api_name:
- Player.currentMedia
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea90b7be72bcb10a8ec0d3c49116f3effceb9a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699697"
---
# <a name="playercurrentmedia"></a><span data-ttu-id="44ed2-104">Player. currentMedia</span><span class="sxs-lookup"><span data-stu-id="44ed2-104">Player.currentMedia</span></span>

<span data-ttu-id="44ed2-105">La propiedad **currentMedia** especifica o recupera el objeto multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="44ed2-105">The **currentMedia** property specifies or retrieves the current Media object.</span></span>

## <a name="syntax"></a><span data-ttu-id="44ed2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44ed2-106">Syntax</span></span>

<span data-ttu-id="44ed2-107">*reproductor* . **currentMedia**</span><span class="sxs-lookup"><span data-stu-id="44ed2-107">*player* .**currentMedia**</span></span>

## <a name="possible-values"></a><span data-ttu-id="44ed2-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="44ed2-108">Possible Values</span></span>

<span data-ttu-id="44ed2-109">Esta propiedad es un objeto multimedia de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="44ed2-109">This property is a read/write Media object.</span></span>

## <a name="remarks"></a><span data-ttu-id="44ed2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44ed2-110">Remarks</span></span>

<span data-ttu-id="44ed2-111">Es si se trata de la *configuración*. la propiedad **autoStart** es true, la reproducción se inicia automáticamente cada vez que se establece **currentMedia**.</span><span class="sxs-lookup"><span data-stu-id="44ed2-111">If the *Settings*.**autoStart** property is true, playback begins automatically whenever you set **currentMedia**.</span></span>

<span data-ttu-id="44ed2-112">Esta propiedad toma un objeto multimedia, que se puede adquirir mediante la *lista de reproducción*. **elemento**.</span><span class="sxs-lookup"><span data-stu-id="44ed2-112">This property takes a Media object, which can be acquired by using *Playlist*.**item**.</span></span> <span data-ttu-id="44ed2-113">Para cargar un elemento **multimedia** con un nombre de archivo, establezca la propiedad URL o use **newMedia**.</span><span class="sxs-lookup"><span data-stu-id="44ed2-113">To load a **Media** item using a file name, set the URL property or use **newMedia**.</span></span>

## <a name="examples"></a><span data-ttu-id="44ed2-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="44ed2-114">Examples</span></span>

<span data-ttu-id="44ed2-115">En el siguiente ejemplo de JScript se recupera el primer elemento multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="44ed2-115">The following JScript example retrieves the first media item in the library.</span></span> <span data-ttu-id="44ed2-116">A continuación, usa **currentMedia** para convertir el elemento multimedia recuperado en el elemento multimedia actual y, después, para mostrar el nombre del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="44ed2-116">It then uses **currentMedia** to make the retrieved media item the current media item, and then to display the name of the current media item.</span></span> <span data-ttu-id="44ed2-117">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="44ed2-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first media item from the library.
var firstMedia = Player.mediaCollection.getAll().item(0);

// Make the retrieved media item the current media item.
Player.currentMedia = firstMedia;

// Display the name of the current media item.
document.write("Found first media item. Name = " + Player.currentMedia.name);
```



## <a name="requirements"></a><span data-ttu-id="44ed2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44ed2-118">Requirements</span></span>



| <span data-ttu-id="44ed2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="44ed2-119">Requirement</span></span> | <span data-ttu-id="44ed2-120">Value</span><span class="sxs-lookup"><span data-stu-id="44ed2-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44ed2-121">Versión</span><span class="sxs-lookup"><span data-stu-id="44ed2-121">Version</span></span><br/> | <span data-ttu-id="44ed2-122">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="44ed2-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="44ed2-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44ed2-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="44ed2-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44ed2-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44ed2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="44ed2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ed2-126">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="44ed2-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="44ed2-127">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="44ed2-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="44ed2-128">**Player. newMedia**</span><span class="sxs-lookup"><span data-stu-id="44ed2-128">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="44ed2-129">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="44ed2-129">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="44ed2-130">**Configuración. Inicio automático**</span><span class="sxs-lookup"><span data-stu-id="44ed2-130">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 





