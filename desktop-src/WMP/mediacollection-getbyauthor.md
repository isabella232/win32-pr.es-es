---
title: MediaCollection. getByAuthor, método
description: El método getByAuthor recupera una lista de reproducción de los elementos multimedia por el autor especificado.
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- método getByAuthor de Windows Media Player
- método getByAuthor de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getByAuthor
topic_type:
- apiref
api_name:
- MediaCollection.getByAuthor
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eae0928250e37e76bf3a39f38b43bef8a5691c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708215"
---
# <a name="mediacollectiongetbyauthor-method"></a><span data-ttu-id="b30cc-106">MediaCollection. getByAuthor, método</span><span class="sxs-lookup"><span data-stu-id="b30cc-106">MediaCollection.getByAuthor method</span></span>

<span data-ttu-id="b30cc-107">El método **getByAuthor** recupera una lista de reproducción de los elementos multimedia por el autor especificado.</span><span class="sxs-lookup"><span data-stu-id="b30cc-107">The **getByAuthor** method retrieves a playlist of the media items by the specified author.</span></span>

## <a name="syntax"></a><span data-ttu-id="b30cc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b30cc-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a><span data-ttu-id="b30cc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b30cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b30cc-110">*autor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b30cc-110">*author* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b30cc-111">**Cadena** que contiene el nombre del autor.</span><span class="sxs-lookup"><span data-stu-id="b30cc-111">**String** containing the name of the author.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b30cc-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b30cc-112">Return value</span></span>

<span data-ttu-id="b30cc-113">Este método devuelve un objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="b30cc-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b30cc-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b30cc-114">Remarks</span></span>

<span data-ttu-id="b30cc-115">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b30cc-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="b30cc-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b30cc-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b30cc-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b30cc-117">Examples</span></span>

<span data-ttu-id="b30cc-118">En el siguiente ejemplo de JScript se usa *MediaCollection*. **getByAuthor** para recuperar una lista de reproducción de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="b30cc-118">The following JScript example uses *MediaCollection*.**getByAuthor** to retrieve a playlist of media items.</span></span> <span data-ttu-id="b30cc-119">La lista de reproducción contiene elementos que coinciden con el autor especificado por el usuario en un elemento de entrada de texto HTML denominado GetAuthor.</span><span class="sxs-lookup"><span data-stu-id="b30cc-119">The playlist contains items matching the author specified by the user in an HTML TEXT input element named GetAuthor.</span></span> <span data-ttu-id="b30cc-120">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="b30cc-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play the media items. -->
<INPUT TYPE = "BUTTON"  NAME = "PlayAuthor"  
       ID = "PlayAuthor"  
       VALUE = "Play Author"

onClick = "
    /* Retrieve the author name text from the user. */
    var author = GetAuthor.value;

    /* Create the playlist by using getByAuthor. */
    var pl = Player.mediaCollection.getByAuthor(Author);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media items in the new playlist. */
               Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="b30cc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b30cc-121">Requirements</span></span>



| <span data-ttu-id="b30cc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b30cc-122">Requirement</span></span> | <span data-ttu-id="b30cc-123">Value</span><span class="sxs-lookup"><span data-stu-id="b30cc-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b30cc-124">Versión</span><span class="sxs-lookup"><span data-stu-id="b30cc-124">Version</span></span><br/> | <span data-ttu-id="b30cc-125">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b30cc-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b30cc-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b30cc-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="b30cc-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b30cc-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b30cc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b30cc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b30cc-129">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="b30cc-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="b30cc-130">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="b30cc-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="b30cc-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b30cc-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b30cc-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b30cc-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





