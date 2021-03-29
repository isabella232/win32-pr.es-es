---
title: Mensaje de WM_MEASUREITEM (Winuser. h)
description: Se envía a la ventana propietaria de un cuadro combinado, un cuadro de lista, un control de vista de lista o un elemento de menú cuando se crea el control o el menú.
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- WM_MEASUREITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_MEASUREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e14cc0c39e1d319fb9190f8ad7d51ea25f821c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905396"
---
# <a name="wm_measureitem-message"></a><span data-ttu-id="88da4-104">Mensaje de MEASUREITEM de WM \_</span><span class="sxs-lookup"><span data-stu-id="88da4-104">WM\_MEASUREITEM message</span></span>

<span data-ttu-id="88da4-105">Se envía a la ventana propietaria de un cuadro combinado, un cuadro de lista, un control de vista de lista o un elemento de menú cuando se crea el control o el menú.</span><span class="sxs-lookup"><span data-stu-id="88da4-105">Sent to the owner window of a combo box, list box, list-view control, or menu item when the control or menu is created.</span></span>

<span data-ttu-id="88da4-106">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="88da4-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="88da4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88da4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88da4-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="88da4-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88da4-109">Contiene el valor del miembro **CtlID** de la estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) señalada por el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="88da4-109">Contains the value of the **CtlID** member of the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lParam* parameter.</span></span> <span data-ttu-id="88da4-110">Este valor identifica el control que envió el mensaje de **\_ MEASUREITEM de WM** .</span><span class="sxs-lookup"><span data-stu-id="88da4-110">This value identifies the control that sent the **WM\_MEASUREITEM** message.</span></span> <span data-ttu-id="88da4-111">Si el valor es cero, un menú envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="88da4-111">If the value is zero, the message was sent by a menu.</span></span> <span data-ttu-id="88da4-112">Si el valor es distinto de cero, el mensaje se envió mediante un cuadro combinado o un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="88da4-112">If the value is nonzero, the message was sent by a combo box or by a list box.</span></span> <span data-ttu-id="88da4-113">Si el valor es distinto de cero y el valor del miembro **itemID** de **measureitemstruct (** al que apunta *lParam* es (uint) 1, el mensaje se envió mediante un campo de edición combinado.</span><span class="sxs-lookup"><span data-stu-id="88da4-113">If the value is nonzero, and the value of the **itemID** member of the **MEASUREITEMSTRUCT** pointed to by *lParam* is (UINT)  1, the message was sent by a combo edit field.</span></span>

</dd> <dt>

<span data-ttu-id="88da4-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88da4-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88da4-115">Puntero a una estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que contiene las dimensiones del elemento de menú o control dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="88da4-115">Pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that contains the dimensions of the owner-drawn control or menu item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88da4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88da4-116">Return value</span></span>

<span data-ttu-id="88da4-117">Si una aplicación procesa este mensaje, debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="88da4-117">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="88da4-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88da4-118">Remarks</span></span>

<span data-ttu-id="88da4-119">Cuando la ventana propietaria recibe el mensaje de **\_ MEASUREITEM de WM** , el propietario rellena la estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) señalada por el parámetro *lParam* del mensaje y devuelve; esto informa al sistema de las dimensiones del control.</span><span class="sxs-lookup"><span data-stu-id="88da4-119">When the owner window receives the **WM\_MEASUREITEM** message, the owner fills in the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lParam* parameter of the message and returns; this informs the system of the dimensions of the control.</span></span> <span data-ttu-id="88da4-120">Si se crea un cuadro de lista o un cuadro combinado con el estilo [**lb \_ OwnerDrawVariable**](list-box-styles.md) o [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) , este mensaje se envía al propietario de cada elemento del control; de lo contrario, este mensaje se envía una vez.</span><span class="sxs-lookup"><span data-stu-id="88da4-120">If a list box or combo box is created with the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) or [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style, this message is sent to the owner for each item in the control; otherwise, this message is sent once.</span></span>

<span data-ttu-id="88da4-121">El sistema envía el mensaje de **WM \_ MEASUREITEM** a la ventana propietaria de cuadros combinados y cuadros de lista creados con el estilo OWNERDRAWFIXED antes de enviar el mensaje de [**\_ INITDIALOG de WM**](/windows/desktop/dlgbox/wm-initdialog) .</span><span class="sxs-lookup"><span data-stu-id="88da4-121">The system sends the **WM\_MEASUREITEM** message to the owner window of combo boxes and list boxes created with the OWNERDRAWFIXED style before sending the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message.</span></span> <span data-ttu-id="88da4-122">Como resultado, cuando el propietario recibe este mensaje, el sistema no ha determinado aún el alto y el ancho de la fuente utilizada en el control. las llamadas de función y los cálculos que requieren estos valores deben aparecer en la función Main de la aplicación o biblioteca.</span><span class="sxs-lookup"><span data-stu-id="88da4-122">As a result, when the owner receives this message, the system has not yet determined the height and width of the font used in the control; function calls and calculations requiring these values should occur in the main function of the application or library.</span></span>

## <a name="requirements"></a><span data-ttu-id="88da4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88da4-123">Requirements</span></span>



| <span data-ttu-id="88da4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="88da4-124">Requirement</span></span> | <span data-ttu-id="88da4-125">Value</span><span class="sxs-lookup"><span data-stu-id="88da4-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88da4-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88da4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="88da4-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="88da4-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="88da4-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88da4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="88da4-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="88da4-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="88da4-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88da4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="88da4-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88da4-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88da4-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="88da4-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="88da4-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="88da4-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="88da4-134">**MEASUREITEMSTRUCT (**</span><span class="sxs-lookup"><span data-stu-id="88da4-134">**MEASUREITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

<span data-ttu-id="88da4-135">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="88da4-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="88da4-136">**INITDIALOG de WM \_**</span><span class="sxs-lookup"><span data-stu-id="88da4-136">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 

