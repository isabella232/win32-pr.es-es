---
title: Player. currentPlaylist
description: La propiedad currentPlaylist especifica o recupera el objeto de lista de reproducción actual.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- Media Player de Windows Player. currentPlaylist
topic_type:
- apiref
api_name:
- Player.currentPlaylist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceae33a201086d268942e47496874678ec13f459
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700018"
---
# <a name="playercurrentplaylist"></a><span data-ttu-id="98677-104">Player. currentPlaylist</span><span class="sxs-lookup"><span data-stu-id="98677-104">Player.currentPlaylist</span></span>

<span data-ttu-id="98677-105">La propiedad currentPlaylist especifica o recupera el objeto de **lista de reproducción** actual.</span><span class="sxs-lookup"><span data-stu-id="98677-105">The currentPlaylist property specifies or retrieves the current **Playlist** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="98677-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98677-106">Syntax</span></span>

<span data-ttu-id="98677-107">*reproductor* . **currentPlaylist**</span><span class="sxs-lookup"><span data-stu-id="98677-107">*player* .**currentPlaylist**</span></span>

## <a name="possible-values"></a><span data-ttu-id="98677-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="98677-108">Possible Values</span></span>

<span data-ttu-id="98677-109">Esta propiedad es un objeto de **lista de reproducción** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="98677-109">This property is a read/write **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="98677-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98677-110">Remarks</span></span>

<span data-ttu-id="98677-111">Es si se trata de la *configuración*. la propiedad **autoStart** es true, la reproducción se inicia automáticamente cada vez que se establece **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="98677-111">If the *Settings*.**autoStart** property is true, playback begins automatically whenever you set **currentPlaylist**.</span></span>

<span data-ttu-id="98677-112">Esta propiedad toma un objeto de lista de reproducción, que se puede adquirir de varias maneras, por ejemplo, mediante una llamada a *PlaylistArray*. **elemento** o *PlaylistCollection*. **reproducción**.</span><span class="sxs-lookup"><span data-stu-id="98677-112">This property takes a Playlist object, which can be acquired in several ways, such as by calling *PlaylistArray*.**item** or *PlaylistCollection*.**newPlaylist**.</span></span> <span data-ttu-id="98677-113">Para cargar un elemento de **lista de reproducción** con un nombre de archivo, establezca la propiedad URL o use *Player*. **reproducción**.</span><span class="sxs-lookup"><span data-stu-id="98677-113">To load a **Playlist** item using a file name, set the URL property or use *Player*.**newPlaylist**.</span></span>

## <a name="examples"></a><span data-ttu-id="98677-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="98677-114">Examples</span></span>

<span data-ttu-id="98677-115">En el siguiente ejemplo de JScript se recupera la primera lista de reproducción de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="98677-115">The following JScript example retrieves the first playlist in the library.</span></span> <span data-ttu-id="98677-116">A continuación, usa **currentPlaylist** para que la lista de reproducción recuperada sea la lista de reproducción actual y, a continuación, muestre el nombre de la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="98677-116">It then uses **currentPlaylist** to make the retrieved playlist the current playlist, and then to display the name of the current playlist.</span></span> <span data-ttu-id="98677-117">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="98677-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
```



## <a name="requirements"></a><span data-ttu-id="98677-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98677-118">Requirements</span></span>



| <span data-ttu-id="98677-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="98677-119">Requirement</span></span> | <span data-ttu-id="98677-120">Value</span><span class="sxs-lookup"><span data-stu-id="98677-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="98677-121">Versión</span><span class="sxs-lookup"><span data-stu-id="98677-121">Version</span></span><br/> | <span data-ttu-id="98677-122">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="98677-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="98677-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="98677-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="98677-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98677-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98677-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="98677-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98677-126">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="98677-126">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="98677-127">**Player. reproducción**</span><span class="sxs-lookup"><span data-stu-id="98677-127">**Player.newPlaylist**</span></span>](player-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="98677-128">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="98677-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="98677-129">**PlaylistArray. Item**</span><span class="sxs-lookup"><span data-stu-id="98677-129">**PlaylistArray.item**</span></span>](playlistarray-item.md)
</dt> <dt>

[<span data-ttu-id="98677-130">**PlaylistCollection. reproducción**</span><span class="sxs-lookup"><span data-stu-id="98677-130">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="98677-131">**Configuración. Inicio automático**</span><span class="sxs-lookup"><span data-stu-id="98677-131">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 





