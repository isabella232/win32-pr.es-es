---
title: Evento Player. CurrentItemChange
description: El evento CurrentItemChange se produce cuando cambia Controls. currentItem.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- Media Player CurrentItemChange de eventos de Windows
- Evento CurrentItemChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento CurrentItemChange
topic_type:
- apiref
api_name:
- Player.CurrentItemChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c425184bf4b338177ec892ed5362c085dd8cb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709227"
---
# <a name="playercurrentitemchange-event"></a><span data-ttu-id="8ea40-106">Evento Player. CurrentItemChange</span><span class="sxs-lookup"><span data-stu-id="8ea40-106">Player.CurrentItemChange event</span></span>

<span data-ttu-id="8ea40-107">El evento **CurrentItemChange** se produce cuando hay *controles*. **CurrentItem** cambia.</span><span class="sxs-lookup"><span data-stu-id="8ea40-107">The **CurrentItemChange** event occurs when *Controls*.**currentItem** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea40-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ea40-108">Syntax</span></span>


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a><span data-ttu-id="8ea40-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ea40-109">Parameters</span></span>

<span data-ttu-id="8ea40-110">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8ea40-110">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8ea40-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ea40-111">Return value</span></span>

<span data-ttu-id="8ea40-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="8ea40-112">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="8ea40-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8ea40-113">Examples</span></span>

<span data-ttu-id="8ea40-114">En el siguiente ejemplo de JScript se muestra un controlador de eventos para el *reproductor*. evento **currentItemChange** .</span><span class="sxs-lookup"><span data-stu-id="8ea40-114">The following JScript example demonstrates an event handler for the *Player*.**currentItemChange** event.</span></span> <span data-ttu-id="8ea40-115">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="8ea40-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML text box to display the media item name. -->
<INPUT TYPE="TEXT" NAME="MEDIA">

<!-- Create an event handler. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = currentItemChange()>

   // Display the name of the new media item.
   MEDIA.value = Player.currentMedia.name;

</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="8ea40-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ea40-116">Requirements</span></span>



| <span data-ttu-id="8ea40-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ea40-117">Requirement</span></span> | <span data-ttu-id="8ea40-118">Value</span><span class="sxs-lookup"><span data-stu-id="8ea40-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea40-119">Versión</span><span class="sxs-lookup"><span data-stu-id="8ea40-119">Version</span></span><br/> | <span data-ttu-id="8ea40-120">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="8ea40-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8ea40-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ea40-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="8ea40-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ea40-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ea40-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ea40-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea40-124">**Controls. currentItem**</span><span class="sxs-lookup"><span data-stu-id="8ea40-124">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="8ea40-125">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="8ea40-125">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





