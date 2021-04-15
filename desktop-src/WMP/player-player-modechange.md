---
title: Evento Player. ModeChange
description: El evento ModeChange se produce cuando se cambia un modo de Media Player de Windows. | Evento Player. ModeChange
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Media Player ModeChange de eventos de Windows
- Evento ModeChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento ModeChange
topic_type:
- apiref
api_name:
- Player.ModeChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb202672c7fce6705b8e86889c0ca44d7004a19e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708271"
---
# <a name="playermodechange-event"></a><span data-ttu-id="8513e-107">Evento Player. ModeChange</span><span class="sxs-lookup"><span data-stu-id="8513e-107">Player.ModeChange event</span></span>

<span data-ttu-id="8513e-108">El evento **ModeChange** se produce cuando se cambia un modo de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="8513e-108">The **ModeChange** event occurs when a mode of Windows Media Player is changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8513e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8513e-109">Syntax</span></span>


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a><span data-ttu-id="8513e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8513e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8513e-111">*ModeName*</span><span class="sxs-lookup"><span data-stu-id="8513e-111">*ModeName*</span></span> 
</dt> <dd>

<span data-ttu-id="8513e-112">**Cadena** que indica el modo que se cambió.</span><span class="sxs-lookup"><span data-stu-id="8513e-112">**String** indicating the mode that was changed.</span></span> <span data-ttu-id="8513e-113">Contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8513e-113">Contains one of the following values.</span></span>



| <span data-ttu-id="8513e-114">Value</span><span class="sxs-lookup"><span data-stu-id="8513e-114">Value</span></span>   | <span data-ttu-id="8513e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8513e-115">Description</span></span>                                         |
|---------|-----------------------------------------------------|
| <span data-ttu-id="8513e-116">shuffle</span><span class="sxs-lookup"><span data-stu-id="8513e-116">shuffle</span></span> | <span data-ttu-id="8513e-117">Las pistas se reproducen en orden aleatorio.</span><span class="sxs-lookup"><span data-stu-id="8513e-117">Tracks are played in random order.</span></span>                  |
| <span data-ttu-id="8513e-118">bucle</span><span class="sxs-lookup"><span data-stu-id="8513e-118">loop</span></span>    | <span data-ttu-id="8513e-119">Toda la secuencia de pistas se reproduce varias veces.</span><span class="sxs-lookup"><span data-stu-id="8513e-119">The entire sequence of tracks is played repeatedly.</span></span> |



 

</dd> <dt>

<span data-ttu-id="8513e-120">*Nuevovalor*</span><span class="sxs-lookup"><span data-stu-id="8513e-120">*NewValue*</span></span> 
</dt> <dd>

<span data-ttu-id="8513e-121">**Valor booleano** que indica el nuevo estado del modo especificado.</span><span class="sxs-lookup"><span data-stu-id="8513e-121">**Boolean** indicating the new state of the specified mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8513e-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8513e-122">Return value</span></span>

<span data-ttu-id="8513e-123">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="8513e-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8513e-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8513e-124">Remarks</span></span>

<span data-ttu-id="8513e-125">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="8513e-125">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="8513e-126">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8513e-126">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="8513e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8513e-127">Requirements</span></span>



| <span data-ttu-id="8513e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8513e-128">Requirement</span></span> | <span data-ttu-id="8513e-129">Value</span><span class="sxs-lookup"><span data-stu-id="8513e-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8513e-130">Versión</span><span class="sxs-lookup"><span data-stu-id="8513e-130">Version</span></span><br/> | <span data-ttu-id="8513e-131">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="8513e-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8513e-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8513e-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="8513e-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8513e-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8513e-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="8513e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8513e-135">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="8513e-135">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="8513e-136">**Settings. getMode**</span><span class="sxs-lookup"><span data-stu-id="8513e-136">**Settings.getMode**</span></span>](settings-getmode.md)
</dt> <dt>

[<span data-ttu-id="8513e-137">**Settings. setMode**</span><span class="sxs-lookup"><span data-stu-id="8513e-137">**Settings.setMode**</span></span>](settings-setmode.md)
</dt> </dl>

 

 





