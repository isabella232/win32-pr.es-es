---
title: Evento Player. click
description: El evento click se produce cuando el usuario hace clic en un botón del mouse.
ms.assetid: c2d5fab9-9b53-4d0c-a001-8cbf4430e713
keywords:
- Haga clic en ventanas de eventos Media Player
- Haga clic en Windows Event Media Player, clase Player
- Clase de reproductor Windows Media Player, haga clic en evento
topic_type:
- apiref
api_name:
- Player.Click
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8389460d59018b221749719d32edbaa89943808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708881"
---
# <a name="playerclick-event"></a><span data-ttu-id="a62d0-106">Evento Player. click</span><span class="sxs-lookup"><span data-stu-id="a62d0-106">Player.Click event</span></span>

<span data-ttu-id="a62d0-107">El evento **click** se produce cuando el usuario hace clic en un botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="a62d0-107">The **Click** event occurs when the user clicks a mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="a62d0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a62d0-108">Syntax</span></span>


```JScript
Player.Click(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="a62d0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a62d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a62d0-110">*Nbotón*</span><span class="sxs-lookup"><span data-stu-id="a62d0-110">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="a62d0-111">**Número** (**int**) que especifica un campo de bits con bits correspondientes al botón izquierdo (bit 0), botón derecho (bit 1) y botón central (bit 2).</span><span class="sxs-lookup"><span data-stu-id="a62d0-111">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="a62d0-112">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a62d0-112">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="a62d0-113">Solo se establece uno de los bits, que indica el botón que causó el evento.</span><span class="sxs-lookup"><span data-stu-id="a62d0-113">Only one of the bits is set, indicating the button that caused the event.</span></span>

</dd> <dt>

<span data-ttu-id="a62d0-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="a62d0-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="a62d0-115">**Número** (**int**) que especifica un campo de bits con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla Ctrl (bit 1) y la tecla Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="a62d0-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="a62d0-116">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a62d0-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="a62d0-117">El argumento Shift indica el estado de estas claves.</span><span class="sxs-lookup"><span data-stu-id="a62d0-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="a62d0-118">Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.</span><span class="sxs-lookup"><span data-stu-id="a62d0-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="a62d0-119">*Efectos*</span><span class="sxs-lookup"><span data-stu-id="a62d0-119">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="a62d0-120">**Número** (**largo**) que especifica la coordenada x del puntero del mouse en relación con la esquina superior izquierda del control.</span><span class="sxs-lookup"><span data-stu-id="a62d0-120">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="a62d0-121">*fY*</span><span class="sxs-lookup"><span data-stu-id="a62d0-121">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="a62d0-122">**Número** (**largo**) que especifica la coordenada y del puntero del mouse en relación con la esquina superior izquierda del control.</span><span class="sxs-lookup"><span data-stu-id="a62d0-122">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a62d0-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a62d0-123">Return value</span></span>

<span data-ttu-id="a62d0-124">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="a62d0-124">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a62d0-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a62d0-125">Remarks</span></span>

<span data-ttu-id="a62d0-126">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="a62d0-126">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="a62d0-127">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a62d0-127">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="a62d0-128">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="a62d0-128">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="a62d0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a62d0-129">Requirements</span></span>



| <span data-ttu-id="a62d0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a62d0-130">Requirement</span></span> | <span data-ttu-id="a62d0-131">Value</span><span class="sxs-lookup"><span data-stu-id="a62d0-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a62d0-132">Versión</span><span class="sxs-lookup"><span data-stu-id="a62d0-132">Version</span></span><br/> | <span data-ttu-id="a62d0-133">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="a62d0-133">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="a62d0-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a62d0-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="a62d0-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a62d0-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a62d0-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a62d0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a62d0-137">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="a62d0-137">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





