---
title: Evento Player. OpenStateChange
description: El evento OpenStateChange se produce cuando cambia el valor de la propiedad openState. | Evento Player. OpenStateChange
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Media Player OpenStateChange de eventos de Windows
- Evento OpenStateChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento OpenStateChange
topic_type:
- apiref
api_name:
- Player.OpenStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020a25a811623b9f7d7dd8f316c470cada6a142b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708661"
---
# <a name="playeropenstatechange-event"></a><span data-ttu-id="1e720-107">Evento Player. OpenStateChange</span><span class="sxs-lookup"><span data-stu-id="1e720-107">Player.OpenStateChange event</span></span>

<span data-ttu-id="1e720-108">El evento **OpenStateChange** se produce cuando cambia el valor de la propiedad **openState** .</span><span class="sxs-lookup"><span data-stu-id="1e720-108">The **OpenStateChange** event occurs when the **openState** property changes value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e720-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e720-109">Syntax</span></span>


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a><span data-ttu-id="1e720-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e720-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e720-111">*NewState*</span><span class="sxs-lookup"><span data-stu-id="1e720-111">*NewState*</span></span> 
</dt> <dd>

<span data-ttu-id="1e720-112">**Número** (**largo**) que especifica el nuevo estado abierto.</span><span class="sxs-lookup"><span data-stu-id="1e720-112">**Number** (**long**) specifying the new open state.</span></span> <span data-ttu-id="1e720-113">Consulte [openState](player-openstate.md) para obtener una tabla de valores.</span><span class="sxs-lookup"><span data-stu-id="1e720-113">See [openState](player-openstate.md) for a table of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e720-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e720-114">Return value</span></span>

<span data-ttu-id="1e720-115">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="1e720-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e720-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e720-116">Remarks</span></span>

<span data-ttu-id="1e720-117">Windows Media Player puede pasar por varios Estados abiertos mientras trata de abrir un archivo de red, como localizar el servidor, conectarse al servidor y, por último, abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="1e720-117">Windows Media Player can go through several open states while it attempts to open a network file, such as locating the server, connecting to the server, and finally opening the file.</span></span> <span data-ttu-id="1e720-118">Este evento se desencadenará cada vez que cambie el estado abierto.</span><span class="sxs-lookup"><span data-stu-id="1e720-118">This event will be fired each time the open state changes.</span></span>

<span data-ttu-id="1e720-119">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="1e720-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="1e720-120">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1e720-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="1e720-121">No se garantiza que los Estados Media Player de Windows se produzcan en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="1e720-121">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="1e720-122">Además, no todos los Estados se producen necesariamente durante una secuencia de eventos.</span><span class="sxs-lookup"><span data-stu-id="1e720-122">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="1e720-123">No debe escribir código que se base en el orden de los Estados.</span><span class="sxs-lookup"><span data-stu-id="1e720-123">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e720-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e720-124">Requirements</span></span>



| <span data-ttu-id="1e720-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e720-125">Requirement</span></span> | <span data-ttu-id="1e720-126">Value</span><span class="sxs-lookup"><span data-stu-id="1e720-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e720-127">Versión</span><span class="sxs-lookup"><span data-stu-id="1e720-127">Version</span></span><br/> | <span data-ttu-id="1e720-128">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="1e720-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1e720-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e720-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="1e720-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e720-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e720-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e720-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e720-132">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="1e720-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="1e720-133">**Player. openState**</span><span class="sxs-lookup"><span data-stu-id="1e720-133">**Player.openState**</span></span>](player-openstate.md)
</dt> </dl>

 

 





