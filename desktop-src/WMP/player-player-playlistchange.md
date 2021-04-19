---
title: Evento Player. PlaylistChange
description: El evento PlaylistChange se produce cuando cambia una lista de reproducción. | Evento Player. PlaylistChange
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Media Player PlaylistChange de eventos de Windows
- Evento PlaylistChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento PlaylistChange
topic_type:
- apiref
api_name:
- Player.PlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d371818e8166b536543246eeecf0090509e62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708660"
---
# <a name="playerplaylistchange-event"></a><span data-ttu-id="be790-107">Evento Player. PlaylistChange</span><span class="sxs-lookup"><span data-stu-id="be790-107">Player.PlaylistChange event</span></span>

<span data-ttu-id="be790-108">El evento **PlaylistChange** se produce cuando cambia una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="be790-108">The **PlaylistChange** event occurs when a playlist changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="be790-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be790-109">Syntax</span></span>


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a><span data-ttu-id="be790-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be790-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be790-111">*Lista de reproducción*</span><span class="sxs-lookup"><span data-stu-id="be790-111">*Playlist*</span></span> 
</dt> <dd>

<span data-ttu-id="be790-112">Objeto de **lista de reproducción** que cambió.</span><span class="sxs-lookup"><span data-stu-id="be790-112">**Playlist** object which changed.</span></span>

</dd> <dt>

<span data-ttu-id="be790-113">*change*</span><span class="sxs-lookup"><span data-stu-id="be790-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="be790-114">**Número** (**largo**) que indica el tipo de cambio que se produjo en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="be790-114">**Number** (**long**) indicating the type of change that occurred to the playlist.</span></span> <span data-ttu-id="be790-115">Contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="be790-115">Contains one of the following values.</span></span>



| <span data-ttu-id="be790-116">número</span><span class="sxs-lookup"><span data-stu-id="be790-116">Number</span></span> | <span data-ttu-id="be790-117">NOMBRE</span><span class="sxs-lookup"><span data-stu-id="be790-117">Name</span></span>          |
|--------|---------------|
| <span data-ttu-id="be790-118">0</span><span class="sxs-lookup"><span data-stu-id="be790-118">0</span></span>      | <span data-ttu-id="be790-119">Unknown</span><span class="sxs-lookup"><span data-stu-id="be790-119">Unknown</span></span>       |
| <span data-ttu-id="be790-120">1</span><span class="sxs-lookup"><span data-stu-id="be790-120">1</span></span>      | <span data-ttu-id="be790-121">Borrar</span><span class="sxs-lookup"><span data-stu-id="be790-121">Clear</span></span>         |
| <span data-ttu-id="be790-122">2</span><span class="sxs-lookup"><span data-stu-id="be790-122">2</span></span>      | <span data-ttu-id="be790-123">InfoChange</span><span class="sxs-lookup"><span data-stu-id="be790-123">InfoChange</span></span>    |
| <span data-ttu-id="be790-124">3</span><span class="sxs-lookup"><span data-stu-id="be790-124">3</span></span>      | <span data-ttu-id="be790-125">Move</span><span class="sxs-lookup"><span data-stu-id="be790-125">Move</span></span>          |
| <span data-ttu-id="be790-126">4</span><span class="sxs-lookup"><span data-stu-id="be790-126">4</span></span>      | <span data-ttu-id="be790-127">Eliminar</span><span class="sxs-lookup"><span data-stu-id="be790-127">Delete</span></span>        |
| <span data-ttu-id="be790-128">5</span><span class="sxs-lookup"><span data-stu-id="be790-128">5</span></span>      | <span data-ttu-id="be790-129">Insertar</span><span class="sxs-lookup"><span data-stu-id="be790-129">Insert</span></span>        |
| <span data-ttu-id="be790-130">6</span><span class="sxs-lookup"><span data-stu-id="be790-130">6</span></span>      | <span data-ttu-id="be790-131">Append</span><span class="sxs-lookup"><span data-stu-id="be790-131">Append</span></span>        |
| <span data-ttu-id="be790-132">7</span><span class="sxs-lookup"><span data-stu-id="be790-132">7</span></span>      | <span data-ttu-id="be790-133">No compatible</span><span class="sxs-lookup"><span data-stu-id="be790-133">Not supported</span></span> |
| <span data-ttu-id="be790-134">8</span><span class="sxs-lookup"><span data-stu-id="be790-134">8</span></span>      | <span data-ttu-id="be790-135">NameChange (</span><span class="sxs-lookup"><span data-stu-id="be790-135">NameChange</span></span>    |
| <span data-ttu-id="be790-136">9</span><span class="sxs-lookup"><span data-stu-id="be790-136">9</span></span>      | <span data-ttu-id="be790-137">No compatible</span><span class="sxs-lookup"><span data-stu-id="be790-137">Not supported</span></span> |
| <span data-ttu-id="be790-138">10</span><span class="sxs-lookup"><span data-stu-id="be790-138">10</span></span>     | <span data-ttu-id="be790-139">Sort</span><span class="sxs-lookup"><span data-stu-id="be790-139">Sort</span></span>          |



 

<span data-ttu-id="be790-140">La constante de enumeración de estilo C se puede derivar prefijando el valor de nombre con "wmplc".</span><span class="sxs-lookup"><span data-stu-id="be790-140">The C-style enumeration constant can be derived by prefixing the name value with "wmplc".</span></span> <span data-ttu-id="be790-141">Por ejemplo, la constante para el estado de movimiento es **wmplcMove**.</span><span class="sxs-lookup"><span data-stu-id="be790-141">For example, the constant for the Move state is **wmplcMove**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be790-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be790-142">Return value</span></span>

<span data-ttu-id="be790-143">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="be790-143">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be790-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be790-144">Remarks</span></span>

<span data-ttu-id="be790-145">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="be790-145">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="be790-146">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="be790-146">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="be790-147">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="be790-147">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="be790-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be790-148">Requirements</span></span>



| <span data-ttu-id="be790-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="be790-149">Requirement</span></span> | <span data-ttu-id="be790-150">Value</span><span class="sxs-lookup"><span data-stu-id="be790-150">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be790-151">Versión</span><span class="sxs-lookup"><span data-stu-id="be790-151">Version</span></span><br/> | <span data-ttu-id="be790-152">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="be790-152">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="be790-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="be790-153">DLL</span></span><br/>     | <dl> <span data-ttu-id="be790-154"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be790-154"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be790-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="be790-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be790-156">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="be790-156">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





