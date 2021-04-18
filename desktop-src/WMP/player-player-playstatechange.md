---
title: Evento Player. PlayStateChange
description: El evento PlayStateChange se produce cuando hay un cambio en la propiedad playState.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Media Player PlayStateChange de eventos de Windows
- Evento PlayStateChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento PlayStateChange
topic_type:
- apiref
api_name:
- Player.PlayStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e621d8698a5379b0d39a55db141fc0012f6ef969
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708293"
---
# <a name="playerplaystatechange-event"></a><span data-ttu-id="969ef-106">Evento Player. PlayStateChange</span><span class="sxs-lookup"><span data-stu-id="969ef-106">Player.PlayStateChange event</span></span>

<span data-ttu-id="969ef-107">El evento **PlayStateChange** se produce cuando hay un cambio en la propiedad **playState** .</span><span class="sxs-lookup"><span data-stu-id="969ef-107">The **PlayStateChange** event occurs when there is a change in the **playState** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="969ef-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="969ef-108">Syntax</span></span>


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a><span data-ttu-id="969ef-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="969ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="969ef-110">*NewState*</span><span class="sxs-lookup"><span data-stu-id="969ef-110">*NewState*</span></span> 
</dt> <dd>

<span data-ttu-id="969ef-111">Número (**Long**) que especifica el nuevo **playState**.</span><span class="sxs-lookup"><span data-stu-id="969ef-111">Number (**long**) which specifies the new **playState**.</span></span> <span data-ttu-id="969ef-112">Consulte [playState](player-playstate.md) para obtener una tabla de valores posibles.</span><span class="sxs-lookup"><span data-stu-id="969ef-112">See [playState](player-playstate.md) for a table of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="969ef-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="969ef-113">Return value</span></span>

<span data-ttu-id="969ef-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="969ef-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="969ef-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="969ef-115">Remarks</span></span>

<span data-ttu-id="969ef-116">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="969ef-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="969ef-117">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="969ef-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="969ef-118">No se garantiza que los Estados Media Player de Windows se produzcan en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="969ef-118">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="969ef-119">Además, no todos los Estados se producen necesariamente durante una secuencia de eventos.</span><span class="sxs-lookup"><span data-stu-id="969ef-119">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="969ef-120">No debe escribir código que se base en el orden de los Estados.</span><span class="sxs-lookup"><span data-stu-id="969ef-120">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="969ef-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="969ef-121">Examples</span></span>

<span data-ttu-id="969ef-122">En el ejemplo siguiente se muestra un controlador de eventos para el *reproductor*. evento **playStateChange** .</span><span class="sxs-lookup"><span data-stu-id="969ef-122">The following example demonstrates an event handler for the *Player*.**playStateChange** event.</span></span> <span data-ttu-id="969ef-123">Un elemento de texto HTML, denominado "mi texto", muestra el nuevo estado de reproducción.</span><span class="sxs-lookup"><span data-stu-id="969ef-123">An HTML text element, named "myText", displays the new play state.</span></span> <span data-ttu-id="969ef-124">El objeto Player se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="969ef-124">The player object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = playStateChange(NewState)>

// Test for the player current state, display a message for each.
switch (NewState){
    case 1:
        myText.value = "Stopped";
        break;

    case 2:
        myText.value = "Paused";
        break;

    case 3:
        myText.value = "Playing";
        break;

    // Other cases go here.

    default:
        myText.value = "";
}
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="969ef-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="969ef-125">Requirements</span></span>



| <span data-ttu-id="969ef-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="969ef-126">Requirement</span></span> | <span data-ttu-id="969ef-127">Value</span><span class="sxs-lookup"><span data-stu-id="969ef-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="969ef-128">Versión</span><span class="sxs-lookup"><span data-stu-id="969ef-128">Version</span></span><br/> | <span data-ttu-id="969ef-129">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="969ef-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="969ef-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="969ef-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="969ef-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="969ef-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="969ef-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="969ef-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="969ef-133">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="969ef-133">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="969ef-134">**Player. playState**</span><span class="sxs-lookup"><span data-stu-id="969ef-134">**Player.playState**</span></span>](player-playstate.md)
</dt> </dl>

 

 





