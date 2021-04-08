---
description: Se produce cuando el usuario presiona una tecla mientras el control InkEdit tiene el foco.
ms.assetid: 14b05b72-ae5d-416a-8ea5-9d9716c0967f
title: Evento InkEdit. KeyDown (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cee260d4c902534b9b234e0e30d0b60645c579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002886"
---
# <a name="inkeditkeydown-event"></a><span data-ttu-id="53a28-103">Evento InkEdit. KeyDown</span><span class="sxs-lookup"><span data-stu-id="53a28-103">InkEdit.KeyDown event</span></span>

<span data-ttu-id="53a28-104">Se produce cuando el usuario presiona una tecla mientras el control [InkEdit](inkedit-control-reference.md) tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="53a28-104">Occurs when the user presses a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a28-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53a28-105">Syntax</span></span>


```C++
HRESULT KeyDown(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="53a28-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53a28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53a28-107">*pKey*</span><span class="sxs-lookup"><span data-stu-id="53a28-107">*pKey*</span></span> 
</dt> <dd>

<span data-ttu-id="53a28-108">Código de tecla virtual de la tecla presionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="53a28-108">The virtual-key code of the key pressed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="53a28-109">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="53a28-109">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="53a28-110">Miembro de la enumeración [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) , que indica qué teclas modificadoras están presionadas en el momento del evento.</span><span class="sxs-lookup"><span data-stu-id="53a28-110">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration, that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="53a28-111">Value</span><span class="sxs-lookup"><span data-stu-id="53a28-111">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="53a28-112">Significado</span><span class="sxs-lookup"><span data-stu-id="53a28-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="53a28-113"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="53a28-113"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="53a28-114">Especifica que la tecla Mayús se utilizó como modificador.</span><span class="sxs-lookup"><span data-stu-id="53a28-114">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="53a28-115"><dt>**IKM \_ Control** de</dt></span><span class="sxs-lookup"><span data-stu-id="53a28-115"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="53a28-116">Especifica que la tecla CTRL se utilizó como modificador.</span><span class="sxs-lookup"><span data-stu-id="53a28-116">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="53a28-117"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="53a28-117"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="53a28-118">Especifica que la tecla ALT se ha utilizado como modificador.</span><span class="sxs-lookup"><span data-stu-id="53a28-118">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53a28-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53a28-119">Return value</span></span>

<span data-ttu-id="53a28-120">Si este evento se realiza correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="53a28-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53a28-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="53a28-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="53a28-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53a28-122">Remarks</span></span>

<span data-ttu-id="53a28-123">Este método de evento se define en la interfaz **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="53a28-123">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="53a28-124">La interfaz **\_ IInkEditEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IeeKeyDown.</span><span class="sxs-lookup"><span data-stu-id="53a28-124">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="53a28-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53a28-125">Requirements</span></span>



| <span data-ttu-id="53a28-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="53a28-126">Requirement</span></span> | <span data-ttu-id="53a28-127">Value</span><span class="sxs-lookup"><span data-stu-id="53a28-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53a28-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53a28-128">Minimum supported client</span></span><br/> | <span data-ttu-id="53a28-129">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="53a28-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="53a28-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53a28-130">Minimum supported server</span></span><br/> | <span data-ttu-id="53a28-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="53a28-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="53a28-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53a28-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="53a28-133"><dt>Autodibujado. h (también requiere la intermano \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="53a28-133"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="53a28-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53a28-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="53a28-135"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53a28-135"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="53a28-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="53a28-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a28-137">InkEdit</span><span class="sxs-lookup"><span data-stu-id="53a28-137">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="53a28-138">**Enumeración InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="53a28-138">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="53a28-139">[**Control InkEdit de eventos KeyPress \[\]**](inkedit-keypress.md)</span><span class="sxs-lookup"><span data-stu-id="53a28-139">[**KeyPress Event \[InkEdit Control\]**](inkedit-keypress.md)</span></span>
</dt> <dt>

<span data-ttu-id="53a28-140">[**Control InkEdit de evento KeyUp \[\]**](inkedit-keyup.md)</span><span class="sxs-lookup"><span data-stu-id="53a28-140">[**KeyUp Event \[InkEdit Control\]**](inkedit-keyup.md)</span></span>
</dt> </dl>

 

