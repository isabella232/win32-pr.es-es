---
title: MediaCollection. getByGenre, método
description: El método getByGenre recupera una lista de reproducción de los elementos multimedia con el género especificado.
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- método getByGenre de Windows Media Player
- método getByGenre de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getByGenre
topic_type:
- apiref
api_name:
- MediaCollection.getByGenre
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73cd7fe9bb3efa9115e2ba5d01b6d12c89898d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690299"
---
# <a name="mediacollectiongetbygenre-method"></a><span data-ttu-id="67dc1-106">MediaCollection. getByGenre, método</span><span class="sxs-lookup"><span data-stu-id="67dc1-106">MediaCollection.getByGenre method</span></span>

<span data-ttu-id="67dc1-107">El método **getByGenre** recupera una lista de reproducción de los elementos multimedia con el género especificado.</span><span class="sxs-lookup"><span data-stu-id="67dc1-107">The **getByGenre** method retrieves a playlist of the media items with the specified genre.</span></span>

## <a name="syntax"></a><span data-ttu-id="67dc1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67dc1-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a><span data-ttu-id="67dc1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67dc1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67dc1-110">*género* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="67dc1-110">*genre* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67dc1-111">**Cadena** que contiene el nombre del género.</span><span class="sxs-lookup"><span data-stu-id="67dc1-111">**String** containing the name of the genre.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67dc1-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67dc1-112">Return value</span></span>

<span data-ttu-id="67dc1-113">Este método devuelve un objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="67dc1-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="67dc1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67dc1-114">Remarks</span></span>

<span data-ttu-id="67dc1-115">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="67dc1-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="67dc1-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="67dc1-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="67dc1-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="67dc1-117">Examples</span></span>

<span data-ttu-id="67dc1-118">En el siguiente ejemplo de JScript se usa *MediaCollection*. **getByGenre** para recuperar una lista de reproducción de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="67dc1-118">The following JScript example uses *MediaCollection*.**getByGenre** to retrieve a playlist of media items.</span></span> <span data-ttu-id="67dc1-119">La lista de reproducción contiene elementos con el género especificado por el usuario en un elemento de entrada de texto HTML denominado GetGenre.</span><span class="sxs-lookup"><span data-stu-id="67dc1-119">The playlist contains items with the genre specified by the user in an HTML TEXT input element named GetGenre.</span></span> <span data-ttu-id="67dc1-120">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="67dc1-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play 
the media items. -->
<INPUT TYPE = "BUTTON"  
       NAME = "PlayGenre"  
       ID = "PlayGenre"  
       VALUE = "Play Genre"

onClick = "
    /* Retrieve the genre text from the user. */
    var genre = GetGenre.value;

    /* Create the playlist using getByGenre. */
    var pl = Player.mediaCollection.getByGenre(genre);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the digital media item in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="67dc1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67dc1-121">Requirements</span></span>



| <span data-ttu-id="67dc1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="67dc1-122">Requirement</span></span> | <span data-ttu-id="67dc1-123">Value</span><span class="sxs-lookup"><span data-stu-id="67dc1-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67dc1-124">Versión</span><span class="sxs-lookup"><span data-stu-id="67dc1-124">Version</span></span><br/> | <span data-ttu-id="67dc1-125">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="67dc1-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="67dc1-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67dc1-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="67dc1-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67dc1-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67dc1-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="67dc1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67dc1-129">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="67dc1-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="67dc1-130">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="67dc1-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="67dc1-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="67dc1-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="67dc1-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="67dc1-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





