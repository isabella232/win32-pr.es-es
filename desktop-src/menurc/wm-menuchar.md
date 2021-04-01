---
title: Mensaje de WM_MENUCHAR (Winuser. h)
description: Se envía cuando un menú está activo y el usuario presiona una tecla que no se corresponde con ninguna tecla de método abreviado o tecla de aceleración. Este mensaje se envía a la ventana que posee el menú.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_MENUCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a278e4a1b4333631741a6a542318a8a55e40b512
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804022"
---
# <a name="wm_menuchar-message"></a><span data-ttu-id="c8b91-105">Mensaje de MENUCHAR de WM \_</span><span class="sxs-lookup"><span data-stu-id="c8b91-105">WM\_MENUCHAR message</span></span>

<span data-ttu-id="c8b91-106">Se envía cuando un menú está activo y el usuario presiona una tecla que no se corresponde con ninguna tecla de método abreviado o tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="c8b91-106">Sent when a menu is active and the user presses a key that does not correspond to any mnemonic or accelerator key.</span></span> <span data-ttu-id="c8b91-107">Este mensaje se envía a la ventana que posee el menú.</span><span class="sxs-lookup"><span data-stu-id="c8b91-107">This message is sent to the window that owns the menu.</span></span>


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a><span data-ttu-id="c8b91-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8b91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8b91-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8b91-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8b91-110">La palabra de orden inferior especifica el código de carácter correspondiente a la tecla que el usuario presionó.</span><span class="sxs-lookup"><span data-stu-id="c8b91-110">The low-order word specifies the character code that corresponds to the key the user pressed.</span></span>

<span data-ttu-id="c8b91-111">La palabra de orden superior especifica el tipo de menú activo.</span><span class="sxs-lookup"><span data-stu-id="c8b91-111">The high-order word specifies the active menu type.</span></span> <span data-ttu-id="c8b91-112">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c8b91-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c8b91-113">Valor</span><span class="sxs-lookup"><span data-stu-id="c8b91-113">Value</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="c8b91-114">Significado</span><span class="sxs-lookup"><span data-stu-id="c8b91-114">Meaning</span></span>                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="c8b91-115"><dt>**MF \_**</dt> <dt>0x00000010L</dt> emergente</span><span class="sxs-lookup"><span data-stu-id="c8b91-115"><dt>**MF\_POPUP**</dt> <dt>0x00000010L</dt></span></span> </dl>       | <span data-ttu-id="c8b91-116">Menú desplegable, submenú o menú contextual.</span><span class="sxs-lookup"><span data-stu-id="c8b91-116">A drop-down menu, submenu, or shortcut menu.</span></span><br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <span data-ttu-id="c8b91-117"><dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt></span><span class="sxs-lookup"><span data-stu-id="c8b91-117"><dt>**MF\_SYSMENU**</dt> <dt>0x00002000L</dt></span></span> </dl> | <span data-ttu-id="c8b91-118">El menú ventana.</span><span class="sxs-lookup"><span data-stu-id="c8b91-118">The window menu.</span></span><br/>                             |



 

</dd> <dt>

<span data-ttu-id="c8b91-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8b91-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8b91-120">Identificador del menú activo.</span><span class="sxs-lookup"><span data-stu-id="c8b91-120">A handle to the active menu.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8b91-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8b91-121">Return value</span></span>

<span data-ttu-id="c8b91-122">Una aplicación que procesa este mensaje debe devolver uno de los valores siguientes en la palabra de orden superior del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="c8b91-122">An application that processes this message should return one of the following values in the high-order word of the return value.</span></span>



| <span data-ttu-id="c8b91-123">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8b91-123">Return code/value</span></span>                                                                                                                                  | <span data-ttu-id="c8b91-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8b91-124">Description</span></span>                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8b91-125"><dt>**MNC \_ CERRAR**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c8b91-125"><dt>**MNC\_CLOSE**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="c8b91-126">Informa al sistema de que debe cerrar el menú activo.</span><span class="sxs-lookup"><span data-stu-id="c8b91-126">Informs the system that it should close the active menu.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="c8b91-127"><dt>**MNC \_ EJECUTAR**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c8b91-127"><dt>**MNC\_EXECUTE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="c8b91-128">Informa al sistema de que debe elegir el elemento especificado en la palabra de orden inferior del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="c8b91-128">Informs the system that it should choose the item specified in the low-order word of the return value.</span></span> <span data-ttu-id="c8b91-129">La ventana propietaria recibe un mensaje de [**\_ comando de WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="c8b91-129">The owner window receives a [**WM\_COMMAND**](wm-command.md) message.</span></span><br/> |
| <dl> <span data-ttu-id="c8b91-130"><dt>**MNC \_ OMITIr**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8b91-130"><dt>**MNC\_IGNORE**</dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="c8b91-131">Informa al sistema de que debe descartar el carácter que el usuario presionó y crear un pitido corto en el altavoz del sistema.</span><span class="sxs-lookup"><span data-stu-id="c8b91-131">Informs the system that it should discard the character the user pressed and create a short beep on the system speaker.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="c8b91-132"><dt>**MNC \_ Seleccione**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c8b91-132"><dt>**MNC\_SELECT**</dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="c8b91-133">Informa al sistema de que debe seleccionar el elemento especificado en la palabra de orden inferior del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="c8b91-133">Informs the system that it should select the item specified in the low-order word of the return value.</span></span> <br/>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="c8b91-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8b91-134">Remarks</span></span>

<span data-ttu-id="c8b91-135">La palabra de orden inferior se omite si la palabra de orden superior contiene 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="c8b91-135">The low-order word is ignored if the high-order word contains 0 or 1.</span></span>

<span data-ttu-id="c8b91-136">Una aplicación debe procesar este mensaje cuando se utiliza un acelerador para seleccionar un elemento de menú que muestra un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="c8b91-136">An application should process this message when an accelerator is used to select a menu item that displays a bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8b91-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8b91-137">Requirements</span></span>



| <span data-ttu-id="c8b91-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8b91-138">Requirement</span></span> | <span data-ttu-id="c8b91-139">Value</span><span class="sxs-lookup"><span data-stu-id="c8b91-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b91-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8b91-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b91-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c8b91-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c8b91-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8b91-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b91-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c8b91-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8b91-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8b91-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8b91-145"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8b91-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8b91-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8b91-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8b91-147">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c8b91-147">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="c8b91-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c8b91-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c8b91-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c8b91-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c8b91-150">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c8b91-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c8b91-151">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="c8b91-151">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

