---
title: Player. PositionChange (evento)
description: El evento PositionChange se produce cuando se ha cambiado la posición actual del elemento multimedia.
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- Media Player de eventos de PositionChange en Windows
- Evento PositionChange Windows Media Player, clase Player
- Clase de reproductor Windows Media Player, evento PositionChange
topic_type:
- apiref
api_name:
- Player.PositionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ab7f64d6f5c4a081b8a81a14e3fcb353e1478e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708830"
---
# <a name="playerpositionchange-event"></a><span data-ttu-id="42dcb-106">Player. PositionChange (evento)</span><span class="sxs-lookup"><span data-stu-id="42dcb-106">Player.PositionChange event</span></span>

<span data-ttu-id="42dcb-107">El evento **PositionChange** se produce cuando se ha cambiado la posición actual del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="42dcb-107">The **PositionChange** event occurs when the current position of the media item has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="42dcb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42dcb-108">Syntax</span></span>


```JScript
Player.PositionChange(
  oldPosition,
  newPosition
)
```



## <a name="parameters"></a><span data-ttu-id="42dcb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42dcb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42dcb-110">*oldPosition*</span><span class="sxs-lookup"><span data-stu-id="42dcb-110">*oldPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="42dcb-111">Número (**Double**) que especifica la posición anterior.</span><span class="sxs-lookup"><span data-stu-id="42dcb-111">Number (**double**) specifying the old position.</span></span>

</dd> <dt>

<span data-ttu-id="42dcb-112">*newPosition*</span><span class="sxs-lookup"><span data-stu-id="42dcb-112">*newPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="42dcb-113">**Número** (**Double**) que especifica la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="42dcb-113">**Number** (**double**) specifying the new position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42dcb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42dcb-114">Return value</span></span>

<span data-ttu-id="42dcb-115">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="42dcb-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42dcb-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42dcb-116">Remarks</span></span>

<span data-ttu-id="42dcb-117">Este evento no se genera rutinariamente durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="42dcb-117">This event is not raised routinely during playback.</span></span> <span data-ttu-id="42dcb-118">Solo se produce cuando algo cambia activamente la posición actual del elemento multimedia de reproducción, como el usuario que mueve el identificador de búsqueda o el código que especifica un valor para *los controles*. **currentPosition**.</span><span class="sxs-lookup"><span data-stu-id="42dcb-118">It only occurs when something actively changes the current position of the playing media item, such as the user moving the seek handle or code specifying a value for *Controls*.**currentPosition**.</span></span>

<span data-ttu-id="42dcb-119">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="42dcb-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="42dcb-120">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="42dcb-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="42dcb-121">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="42dcb-121">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="42dcb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42dcb-122">Requirements</span></span>



| <span data-ttu-id="42dcb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="42dcb-123">Requirement</span></span> | <span data-ttu-id="42dcb-124">Value</span><span class="sxs-lookup"><span data-stu-id="42dcb-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42dcb-125">Versión</span><span class="sxs-lookup"><span data-stu-id="42dcb-125">Version</span></span><br/> | <span data-ttu-id="42dcb-126">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="42dcb-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="42dcb-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42dcb-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="42dcb-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42dcb-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42dcb-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="42dcb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42dcb-130">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="42dcb-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





