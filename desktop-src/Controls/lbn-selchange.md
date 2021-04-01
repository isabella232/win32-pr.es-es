---
title: Código de notificación de LBN_SELCHANGE (Winuser. h)
description: Notifica a la aplicación que la selección de un cuadro de lista ha cambiado como resultado de los datos proporcionados por el usuario. La ventana primaria del cuadro de lista recibe este código de notificación a través del mensaje de comando de WM \_ .
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- LBN_SELCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e029d1753a0fa74f39a59a459d6ede45811a40fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802329"
---
# <a name="lbn_selchange-notification-code"></a><span data-ttu-id="1fec8-105">Código de notificación de SELCHANGE de LBN \_</span><span class="sxs-lookup"><span data-stu-id="1fec8-105">LBN\_SELCHANGE notification code</span></span>

<span data-ttu-id="1fec8-106">Notifica a la aplicación que la selección de un cuadro de lista ha cambiado como resultado de los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="1fec8-106">Notifies the application that the selection in a list box has changed as a result of user input.</span></span> <span data-ttu-id="1fec8-107">La ventana primaria del cuadro de lista recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="1fec8-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1fec8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fec8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fec8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1fec8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fec8-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="1fec8-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="1fec8-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="1fec8-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="1fec8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1fec8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fec8-113">Identificador del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="1fec8-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fec8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fec8-114">Remarks</span></span>

<span data-ttu-id="1fec8-115">Este código de notificación solo se envía mediante un cuadro de lista que tiene el estilo de [**\_ notificación lb**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1fec8-115">This notification code is sent only by a list box that has the [**LBS\_NOTIFY**](list-box-styles.md) style.</span></span>

<span data-ttu-id="1fec8-116">Este código de notificación no se envía si el mensaje [**lb \_ SETSEL**](lb-setsel.md), [**lb \_ SETCURSEL**](lb-setcursel.md), [**lb \_ SELECTSTRING**](lb-selectstring.md), [**lb \_ SELITEMRANGE**](lb-selitemrange.md) o [**lb \_ SELITEMRANGEEX**](lb-selitemrangeex.md) cambia la selección.</span><span class="sxs-lookup"><span data-stu-id="1fec8-116">This notification code is not sent if the [**LB\_SETSEL**](lb-setsel.md), [**LB\_SETCURSEL**](lb-setcursel.md), [**LB\_SELECTSTRING**](lb-selectstring.md), [**LB\_SELITEMRANGE**](lb-selitemrange.md) or [**LB\_SELITEMRANGEEX**](lb-selitemrangeex.md) message changes the selection.</span></span>

<span data-ttu-id="1fec8-117">En el caso de un cuadro de lista de selección múltiple, \_ se envía el código de notificación LBN SELCHANGE cuando el usuario presiona una tecla de dirección, incluso si la selección no cambia.</span><span class="sxs-lookup"><span data-stu-id="1fec8-117">For a multiple-selection list box, the LBN\_SELCHANGE notification code is sent whenever the user presses an arrow key, even if the selection does not change.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fec8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fec8-118">Requirements</span></span>



| <span data-ttu-id="1fec8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fec8-119">Requirement</span></span> | <span data-ttu-id="1fec8-120">Value</span><span class="sxs-lookup"><span data-stu-id="1fec8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fec8-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fec8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1fec8-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1fec8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1fec8-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fec8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1fec8-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1fec8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1fec8-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fec8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fec8-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fec8-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fec8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fec8-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="1fec8-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1fec8-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1fec8-129">**LB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="1fec8-129">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="1fec8-130">LBN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="1fec8-130">LBN\_DBLCLK</span></span>](lbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="1fec8-131">LBN \_ SELCANCEL</span><span class="sxs-lookup"><span data-stu-id="1fec8-131">LBN\_SELCANCEL</span></span>](lbn-selcancel.md)
</dt> <dt>

<span data-ttu-id="1fec8-132">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="1fec8-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1fec8-133">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="1fec8-133">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

