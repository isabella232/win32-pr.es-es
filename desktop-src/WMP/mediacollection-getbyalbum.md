---
title: MediaCollection. getByAlbum, método
description: El método GetByAlbum recupera una lista de reproducción que contiene los elementos multimedia del álbum especificado.
ms.assetid: e7e72f0e-e0ae-4bbd-a8b7-966f0fc50059
keywords:
- método getByAlbum de Windows Media Player
- método getByAlbum de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getByAlbum
topic_type:
- apiref
api_name:
- MediaCollection.getByAlbum
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d94cdfa880288893e9659b73b01bc754ac59bbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690637"
---
# <a name="mediacollectiongetbyalbum-method"></a><span data-ttu-id="234c8-106">MediaCollection. getByAlbum, método</span><span class="sxs-lookup"><span data-stu-id="234c8-106">MediaCollection.getByAlbum method</span></span>

<span data-ttu-id="234c8-107">El método **GetByAlbum** recupera una lista de reproducción que contiene los elementos multimedia del álbum especificado.</span><span class="sxs-lookup"><span data-stu-id="234c8-107">The **GetByAlbum** method retrieves a playlist containing the media items from the specified album.</span></span>

## <a name="syntax"></a><span data-ttu-id="234c8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="234c8-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAlbum(
  album
)
```



## <a name="parameters"></a><span data-ttu-id="234c8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="234c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="234c8-110">*álbum* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="234c8-110">*album* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="234c8-111">**Cadena** que contiene el nombre del álbum.</span><span class="sxs-lookup"><span data-stu-id="234c8-111">**String** containing the name of the album.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="234c8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="234c8-112">Return value</span></span>

<span data-ttu-id="234c8-113">Este método devuelve un objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="234c8-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="234c8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="234c8-114">Remarks</span></span>

<span data-ttu-id="234c8-115">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="234c8-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="234c8-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="234c8-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="234c8-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="234c8-117">Examples</span></span>

<span data-ttu-id="234c8-118">En el ejemplo siguiente se usa *MediaCollection*. **getByAlbum** para recuperar una lista de reproducción de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="234c8-118">The following example uses *MediaCollection*.**getByAlbum** to retrieve a playlist of media items.</span></span> <span data-ttu-id="234c8-119">La lista de reproducción contiene elementos con el álbum especificado por el usuario en un elemento de entrada de texto HTML denominado GetAlbum.</span><span class="sxs-lookup"><span data-stu-id="234c8-119">The playlist contains items with the album specified by the user in an HTML TEXT input element named GetAlbum.</span></span> <span data-ttu-id="234c8-120">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="234c8-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and 
then play the digital media items. -->
<INPUT TYPE = "BUTTON"
       NAME = "PlayAlbum" 
       ID = "PlayAlbum"  
       VALUE = "Play Album"

onClick = "
    /* Retrieve the album title text from the user. */
    var album = GetAlbum.value;

    /* Create the playlist using getByAlbum. */
    var pl = Player.mediaCollection.getByAlbum(album);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="234c8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="234c8-121">Requirements</span></span>



| <span data-ttu-id="234c8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="234c8-122">Requirement</span></span> | <span data-ttu-id="234c8-123">Value</span><span class="sxs-lookup"><span data-stu-id="234c8-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="234c8-124">Versión</span><span class="sxs-lookup"><span data-stu-id="234c8-124">Version</span></span><br/> | <span data-ttu-id="234c8-125">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="234c8-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="234c8-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="234c8-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="234c8-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="234c8-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="234c8-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="234c8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="234c8-129">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="234c8-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="234c8-130">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="234c8-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="234c8-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="234c8-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="234c8-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="234c8-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





