---
title: Mensaje de WM_DRAWITEM (Winuser. h)
description: Se envía a la ventana primaria de un botón dibujado por el propietario, un cuadro combinado, un cuadro de lista o un menú cuando ha cambiado un aspecto visual del botón, el cuadro combinado, el cuadro de lista o el menú.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- WM_DRAWITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bd6465a560a0590ed9f5b483afae4c0d72d637
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802173"
---
# <a name="wm_drawitem-message"></a><span data-ttu-id="2fe74-104">Mensaje de la DRAWITEM de WM \_</span><span class="sxs-lookup"><span data-stu-id="2fe74-104">WM\_DRAWITEM message</span></span>

<span data-ttu-id="2fe74-105">Se envía a la ventana primaria de un botón dibujado por el propietario, un cuadro combinado, un cuadro de lista o un menú cuando ha cambiado un aspecto visual del botón, el cuadro combinado, el cuadro de lista o el menú.</span><span class="sxs-lookup"><span data-stu-id="2fe74-105">Sent to the parent window of an owner-drawn button, combo box, list box, or menu when a visual aspect of the button, combo box, list box, or menu has changed.</span></span>

<span data-ttu-id="2fe74-106">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2fe74-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2fe74-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fe74-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fe74-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2fe74-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fe74-109">Especifica el identificador del control que envió el mensaje de **la \_ DRAWITEM de WM** .</span><span class="sxs-lookup"><span data-stu-id="2fe74-109">Specifies the identifier of the control that sent the **WM\_DRAWITEM** message.</span></span> <span data-ttu-id="2fe74-110">Si el mensaje se envió mediante un menú, este parámetro es cero.</span><span class="sxs-lookup"><span data-stu-id="2fe74-110">If the message was sent by a menu, this parameter is zero.</span></span>

</dd> <dt>

<span data-ttu-id="2fe74-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2fe74-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fe74-112">Puntero a una estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contiene información sobre el elemento que se va a dibujar y el tipo de dibujo necesario.</span><span class="sxs-lookup"><span data-stu-id="2fe74-112">Pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure containing information about the item to be drawn and the type of drawing required.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fe74-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fe74-113">Return value</span></span>

<span data-ttu-id="2fe74-114">Si una aplicación procesa este mensaje, debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="2fe74-114">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fe74-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fe74-115">Remarks</span></span>

<span data-ttu-id="2fe74-116">De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dibuja el rectángulo de foco para un elemento de cuadro de lista dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="2fe74-116">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function draws the focus rectangle for an owner-drawn list box item.</span></span>

<span data-ttu-id="2fe74-117">El miembro *del itemaction* de la estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) especifica la operación de dibujo que una aplicación debe realizar.</span><span class="sxs-lookup"><span data-stu-id="2fe74-117">The *itemAction* member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure specifies the drawing operation that an application should perform.</span></span>

<span data-ttu-id="2fe74-118">Antes de volver a procesar este mensaje, una aplicación debe asegurarse de que el contexto de dispositivo identificado por el miembro *HDC* de la estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) está en el estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2fe74-118">Before returning from processing this message, an application should ensure that the device context identified by the *hDC* member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure is in the default state.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fe74-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fe74-119">Requirements</span></span>



| <span data-ttu-id="2fe74-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fe74-120">Requirement</span></span> | <span data-ttu-id="2fe74-121">Value</span><span class="sxs-lookup"><span data-stu-id="2fe74-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fe74-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fe74-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2fe74-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2fe74-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2fe74-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fe74-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2fe74-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2fe74-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2fe74-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fe74-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fe74-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2fe74-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fe74-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fe74-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="2fe74-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2fe74-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2fe74-130">**DRAWITEMSTRUCT (**</span><span class="sxs-lookup"><span data-stu-id="2fe74-130">**DRAWITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

<span data-ttu-id="2fe74-131">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="2fe74-131">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2fe74-132">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="2fe74-132">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

