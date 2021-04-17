---
title: Evento Player. CurrentPlaylistChange
description: El evento CurrentPlaylistChange se produce cuando hay algún cambio en la lista de reproducción actual. | Evento Player. CurrentPlaylistChange
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- Media Player CurrentPlaylistChange de eventos de Windows
- Evento CurrentPlaylistChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento CurrentPlaylistChange
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4722db224285587198e3ddb021022ec5d8f2cea6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708646"
---
# <a name="playercurrentplaylistchange-event"></a><span data-ttu-id="99579-107">Evento Player. CurrentPlaylistChange</span><span class="sxs-lookup"><span data-stu-id="99579-107">Player.CurrentPlaylistChange event</span></span>

<span data-ttu-id="99579-108">El evento **CurrentPlaylistChange** se produce cuando hay algún cambio en la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="99579-108">The **CurrentPlaylistChange** event occurs when something changes within the current playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="99579-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99579-109">Syntax</span></span>


```JScript
Player.CurrentPlaylistChange(
  change
)
```



## <a name="parameters"></a><span data-ttu-id="99579-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99579-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99579-111">*change*</span><span class="sxs-lookup"><span data-stu-id="99579-111">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="99579-112">**Número** (**largo**) que indica el tipo de cambio que se ha producido en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="99579-112">**Number** (**long**) indicating what type of change occurred to the playlist.</span></span> <span data-ttu-id="99579-113">Vea el *reproductor*. Evento **PlaylistChange** para una tabla de valores posibles.</span><span class="sxs-lookup"><span data-stu-id="99579-113">See the *Player*.**PlaylistChange** event for a table of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99579-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99579-114">Return value</span></span>

<span data-ttu-id="99579-115">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="99579-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99579-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99579-116">Remarks</span></span>

<span data-ttu-id="99579-117">Este evento no se produce cuando una lista de reproducción distinta se convierte en la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="99579-117">This event does not occur when a different playlist becomes the current playlist.</span></span> <span data-ttu-id="99579-118">Solo se produce cuando se produce un cambio en la lista de reproducción actual, como un elemento multimedia que se anexa a la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="99579-118">It only occurs when a change happens within the current playlist, such as a media item being appended to the playlist.</span></span>

<span data-ttu-id="99579-119">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="99579-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="99579-120">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="99579-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="examples"></a><span data-ttu-id="99579-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="99579-121">Examples</span></span>

<span data-ttu-id="99579-122">En el siguiente ejemplo de JScript se actualiza el texto de un elemento HTML DIV, denominado PlItems, para mostrar los nombres de los elementos multimedia de la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="99579-122">The following JScript example updates the text in an HTML DIV element, named PlItems, to display the names of the media items in the current playlist.</span></span> <span data-ttu-id="99579-123">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="99579-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for current playlist change. -->
<SCRIPT FOR = "Player" EVENT = "currentPlaylistChange(change)">
   switch (change){
      // Only update for move, delete, insert, and append events.
      case 3, 4, 5, 6:

         // Clear the contents of the DIV.
         PlItems.innerHTML = "";

         // Loop through the playlist and display each item name.
         for (var i = 0; i < Player.currentPlaylist.count; i++){
            PlItems.innerHTML += Player.currentPlaylist.item(i).name;
            PlItems.innerHTML += "<br>";
         }
         break;
      
      default:
   } 
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="99579-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99579-124">Requirements</span></span>



| <span data-ttu-id="99579-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="99579-125">Requirement</span></span> | <span data-ttu-id="99579-126">Value</span><span class="sxs-lookup"><span data-stu-id="99579-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="99579-127">Versión</span><span class="sxs-lookup"><span data-stu-id="99579-127">Version</span></span><br/> | <span data-ttu-id="99579-128">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="99579-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="99579-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="99579-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="99579-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99579-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99579-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="99579-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99579-132">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="99579-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="99579-133">**Player. currentPlaylist**</span><span class="sxs-lookup"><span data-stu-id="99579-133">**Player.currentPlaylist**</span></span>](player-currentplaylist.md)
</dt> <dt>

[<span data-ttu-id="99579-134">**Player. PlaylistChange**</span><span class="sxs-lookup"><span data-stu-id="99579-134">**Player.PlaylistChange**</span></span>](player-player-playlistchange.md)
</dt> </dl>

 

 





