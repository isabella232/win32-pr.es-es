---
title: Evento Player. KeyUp
description: El evento KeyUp se produce cuando se suelta una tecla. | Evento Player. KeyUp
ms.assetid: 8b624374-403f-4d41-8481-5e94cee70861
keywords:
- Media Player de eventos KeyUp de Windows
- Evento KeyUp Windows Media Player, clase Player
- Clase de reproductor Windows Media Player, evento KeyUp
topic_type:
- apiref
api_name:
- Player.KeyUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06e9b77871e9f62d46bdfa223bfa40b87feaf06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690185"
---
# <a name="playerkeyup-event"></a><span data-ttu-id="4060e-107">Evento Player. KeyUp</span><span class="sxs-lookup"><span data-stu-id="4060e-107">Player.KeyUp event</span></span>

<span data-ttu-id="4060e-108">El evento **KeyUp** se produce cuando se suelta una tecla.</span><span class="sxs-lookup"><span data-stu-id="4060e-108">The **KeyUp** event occurs when a key is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="4060e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4060e-109">Syntax</span></span>


```JScript
Player.KeyUp(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a><span data-ttu-id="4060e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4060e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4060e-111">*nKeyCode*</span><span class="sxs-lookup"><span data-stu-id="4060e-111">*nKeyCode*</span></span> 
</dt> <dd>

<span data-ttu-id="4060e-112">**Número** (**int**) que especifica qué tecla física se presiona.</span><span class="sxs-lookup"><span data-stu-id="4060e-112">**Number** (**int**) specifying which physical key is pressed.</span></span> <span data-ttu-id="4060e-113">Para ver los valores posibles, consulte el [evento Player. KeyDown](player-player-keydown.md).</span><span class="sxs-lookup"><span data-stu-id="4060e-113">For possible values, see [Player.KeyDown Event](player-player-keydown.md).</span></span>

</dd> <dt>

<span data-ttu-id="4060e-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="4060e-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="4060e-115">**Número** (**int**) que especifica un campo de bits con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla Ctrl (bit 1) y la tecla Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="4060e-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="4060e-116">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4060e-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="4060e-117">El argumento Shift indica el estado de estas claves.</span><span class="sxs-lookup"><span data-stu-id="4060e-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="4060e-118">Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.</span><span class="sxs-lookup"><span data-stu-id="4060e-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4060e-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4060e-119">Return value</span></span>

<span data-ttu-id="4060e-120">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="4060e-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4060e-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4060e-121">Remarks</span></span>

<span data-ttu-id="4060e-122">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="4060e-122">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="4060e-123">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4060e-123">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="4060e-124">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="4060e-124">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="4060e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4060e-125">Requirements</span></span>



| <span data-ttu-id="4060e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4060e-126">Requirement</span></span> | <span data-ttu-id="4060e-127">Value</span><span class="sxs-lookup"><span data-stu-id="4060e-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4060e-128">Versión</span><span class="sxs-lookup"><span data-stu-id="4060e-128">Version</span></span><br/> | <span data-ttu-id="4060e-129">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="4060e-129">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="4060e-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4060e-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="4060e-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4060e-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4060e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4060e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4060e-133">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="4060e-133">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





