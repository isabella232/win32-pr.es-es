---
title: Player. DoubleClick (evento)
description: El evento DoubleClick se produce cuando el usuario hace doble clic en un botón del mouse.
ms.assetid: e2055cff-e4b0-49e3-a93a-7084789b6842
keywords:
- DoubleClick Media Player de eventos de Windows
- DoubleClick Event Windows Media Player, clase Player
- Clase Player Media Player Windows, evento DoubleClick
topic_type:
- apiref
api_name:
- Player.DoubleClick
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3670bfbf3b72fad64f8fb515f5151920b34f52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708965"
---
# <a name="playerdoubleclick-event"></a><span data-ttu-id="788bc-106">Player. DoubleClick (evento)</span><span class="sxs-lookup"><span data-stu-id="788bc-106">Player.DoubleClick event</span></span>

<span data-ttu-id="788bc-107">El evento **DoubleClick** se produce cuando el usuario hace doble clic en un botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="788bc-107">The **DoubleClick** event occurs when the user double-clicks a mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="788bc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="788bc-108">Syntax</span></span>


```JScript
Player.DoubleClick(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="788bc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="788bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="788bc-110">*Nbotón*</span><span class="sxs-lookup"><span data-stu-id="788bc-110">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="788bc-111">**Número** (**int**) que especifica un campo de bits con bits correspondientes al botón izquierdo (bit 0), botón derecho (bit 1) y botón central (bit 2).</span><span class="sxs-lookup"><span data-stu-id="788bc-111">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="788bc-112">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="788bc-112">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="788bc-113">Solo se establece uno de los bits, que indica el botón que causó el evento.</span><span class="sxs-lookup"><span data-stu-id="788bc-113">Only one of the bits is set, indicating the button that caused the event.</span></span>

</dd> <dt>

<span data-ttu-id="788bc-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="788bc-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="788bc-115">**Número** (**int**) que especifica un campo de bits con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla Ctrl (bit 1) y la tecla Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="788bc-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="788bc-116">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="788bc-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="788bc-117">El argumento Shift indica el estado de estas claves.</span><span class="sxs-lookup"><span data-stu-id="788bc-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="788bc-118">Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.</span><span class="sxs-lookup"><span data-stu-id="788bc-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="788bc-119">*Efectos*</span><span class="sxs-lookup"><span data-stu-id="788bc-119">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="788bc-120">**Número** (**largo**) que especifica la coordenada x del puntero del mouse en relación con la esquina superior izquierda del control.</span><span class="sxs-lookup"><span data-stu-id="788bc-120">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="788bc-121">*fY*</span><span class="sxs-lookup"><span data-stu-id="788bc-121">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="788bc-122">**Número** (**largo**) que especifica la coordenada y del puntero del mouse en relación con la esquina superior izquierda del control.</span><span class="sxs-lookup"><span data-stu-id="788bc-122">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="788bc-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="788bc-123">Return value</span></span>

<span data-ttu-id="788bc-124">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="788bc-124">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="788bc-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="788bc-125">Remarks</span></span>

<span data-ttu-id="788bc-126">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="788bc-126">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="788bc-127">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="788bc-127">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="788bc-128">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="788bc-128">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="788bc-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="788bc-129">Requirements</span></span>



| <span data-ttu-id="788bc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="788bc-130">Requirement</span></span> | <span data-ttu-id="788bc-131">Value</span><span class="sxs-lookup"><span data-stu-id="788bc-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="788bc-132">Versión</span><span class="sxs-lookup"><span data-stu-id="788bc-132">Version</span></span><br/> | <span data-ttu-id="788bc-133">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="788bc-133">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="788bc-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="788bc-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="788bc-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="788bc-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="788bc-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="788bc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="788bc-137">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="788bc-137">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





