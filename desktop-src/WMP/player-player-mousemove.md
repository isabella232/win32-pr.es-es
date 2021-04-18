---
title: Evento Player. MouseMove
description: El evento MouseMove se produce cuando se mueve el puntero del mouse. | Evento Player. MouseMove
ms.assetid: 026928a3-25a6-4e67-837a-df71c05e49ee
keywords:
- Media Player de eventos de MouseMove en Windows
- Evento MouseMove Windows Media Player, clase Player
- Clase de reproductor Windows Media Player, evento MouseMove
topic_type:
- apiref
api_name:
- Player.MouseMove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a536609ba5e3095fed9826b071084491a81b385f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708664"
---
# <a name="playermousemove-event"></a><span data-ttu-id="27002-107">Evento Player. MouseMove</span><span class="sxs-lookup"><span data-stu-id="27002-107">Player.MouseMove event</span></span>

<span data-ttu-id="27002-108">El evento **MouseMove** se produce cuando se mueve el puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="27002-108">The **MouseMove** event occurs when the mouse pointer is moved.</span></span>

## <a name="syntax"></a><span data-ttu-id="27002-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27002-109">Syntax</span></span>


```JScript
Player.MouseMove(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="27002-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27002-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27002-111">*Nbotón*</span><span class="sxs-lookup"><span data-stu-id="27002-111">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="27002-112">**Número** (**int**) que especifica un campo de bits con bits correspondientes al botón izquierdo (bit 0), botón derecho (bit 1) y botón central (bit 2).</span><span class="sxs-lookup"><span data-stu-id="27002-112">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="27002-113">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="27002-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="27002-114">Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunos, todos o ninguno de los botones.</span><span class="sxs-lookup"><span data-stu-id="27002-114">Some, all, or none of the bits can be set, indicating that some, all, or none of the buttons are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="27002-115">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="27002-115">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="27002-116">**Número** (**int**) que especifica un campo de bits con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla Ctrl (bit 1) y la tecla Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="27002-116">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="27002-117">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="27002-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="27002-118">El argumento Shift indica el estado de estas claves.</span><span class="sxs-lookup"><span data-stu-id="27002-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="27002-119">Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.</span><span class="sxs-lookup"><span data-stu-id="27002-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="27002-120">*Efectos*</span><span class="sxs-lookup"><span data-stu-id="27002-120">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="27002-121">**Número** (**largo**) que especifica la coordenada x del puntero del mouse en relación con la esquina superior izquierda del control.</span><span class="sxs-lookup"><span data-stu-id="27002-121">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="27002-122">*fY*</span><span class="sxs-lookup"><span data-stu-id="27002-122">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="27002-123">**Número** (**largo**) que especifica la coordenada y del puntero del mouse en relación con la esquina superior izquierda del control.</span><span class="sxs-lookup"><span data-stu-id="27002-123">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27002-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27002-124">Return value</span></span>

<span data-ttu-id="27002-125">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="27002-125">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="27002-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27002-126">Remarks</span></span>

<span data-ttu-id="27002-127">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="27002-127">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="27002-128">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="27002-128">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="27002-129">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="27002-129">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="27002-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27002-130">Requirements</span></span>



| <span data-ttu-id="27002-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="27002-131">Requirement</span></span> | <span data-ttu-id="27002-132">Value</span><span class="sxs-lookup"><span data-stu-id="27002-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="27002-133">Versión</span><span class="sxs-lookup"><span data-stu-id="27002-133">Version</span></span><br/> | <span data-ttu-id="27002-134">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="27002-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="27002-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="27002-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="27002-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27002-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27002-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="27002-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27002-138">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="27002-138">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





