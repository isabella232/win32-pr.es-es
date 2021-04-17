---
title: Mensaje de WM_INITMENU (Winuser. h)
description: Se envía cuando un menú está a punto de activarse.
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- WM_INITMENU menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_INITMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94626b99a5016efaa9427d1ae8b3b3122e599965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714631"
---
# <a name="wm_initmenu-message"></a><span data-ttu-id="ab40b-104">Mensaje de INITMENU de WM \_</span><span class="sxs-lookup"><span data-stu-id="ab40b-104">WM\_INITMENU message</span></span>

<span data-ttu-id="ab40b-105">Se envía cuando un menú está a punto de activarse.</span><span class="sxs-lookup"><span data-stu-id="ab40b-105">Sent when a menu is about to become active.</span></span> <span data-ttu-id="ab40b-106">Se produce cuando el usuario hace clic en un elemento de la barra de menús o presiona una tecla de menú.</span><span class="sxs-lookup"><span data-stu-id="ab40b-106">It occurs when the user clicks an item on the menu bar or presses a menu key.</span></span> <span data-ttu-id="ab40b-107">Esto permite que la aplicación modifique el menú antes de que se muestre.</span><span class="sxs-lookup"><span data-stu-id="ab40b-107">This allows the application to modify the menu before it is displayed.</span></span>

<span data-ttu-id="ab40b-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ab40b-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a><span data-ttu-id="ab40b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab40b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab40b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ab40b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab40b-111">Identificador del menú que se va a inicializar.</span><span class="sxs-lookup"><span data-stu-id="ab40b-111">A handle to the menu to be initialized.</span></span>

</dd> <dt>

<span data-ttu-id="ab40b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab40b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab40b-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ab40b-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab40b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab40b-114">Return value</span></span>

<span data-ttu-id="ab40b-115">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="ab40b-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab40b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab40b-116">Remarks</span></span>

<span data-ttu-id="ab40b-117">Un mensaje de **\_ INITMENU de WM** se envía solo cuando se tiene acceso por primera vez a un menú; solo se genera un mensaje de **WM \_ INITMENU** para cada acceso.</span><span class="sxs-lookup"><span data-stu-id="ab40b-117">A **WM\_INITMENU** message is sent only when a menu is first accessed; only one **WM\_INITMENU** message is generated for each access.</span></span> <span data-ttu-id="ab40b-118">Por ejemplo, al mover el mouse por varios elementos de menú mientras mantiene presionado el botón no se generan mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="ab40b-118">For example, moving the mouse across several menu items while holding down the button does not generate new messages.</span></span> <span data-ttu-id="ab40b-119">**WM \_ INITMENU** no proporciona información sobre los elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="ab40b-119">**WM\_INITMENU** does not provide information about menu items.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab40b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab40b-120">Requirements</span></span>



| <span data-ttu-id="ab40b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab40b-121">Requirement</span></span> | <span data-ttu-id="ab40b-122">Value</span><span class="sxs-lookup"><span data-stu-id="ab40b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab40b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab40b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ab40b-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ab40b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ab40b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab40b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ab40b-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ab40b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ab40b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab40b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab40b-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab40b-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab40b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab40b-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab40b-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ab40b-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ab40b-131">**INITMENUPOPUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ab40b-131">**WM\_INITMENUPOPUP**</span></span>](wm-initmenupopup.md)
</dt> <dt>

<span data-ttu-id="ab40b-132">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ab40b-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ab40b-133">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="ab40b-133">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

