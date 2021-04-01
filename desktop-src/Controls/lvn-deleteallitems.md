---
title: Código de notificación de LVN_DELETEALLITEMS (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que todos los elementos del control están a punto de eliminarse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- LVN_DELETEALLITEMS controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583ad6e2372649ab5f63bd208fb97b93b1591c12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997188"
---
# <a name="lvn_deleteallitems-notification-code"></a><span data-ttu-id="b8ae8-105">Código de notificación de DELETEALLITEMS de LVN \_</span><span class="sxs-lookup"><span data-stu-id="b8ae8-105">LVN\_DELETEALLITEMS notification code</span></span>

<span data-ttu-id="b8ae8-106">Notifica a la ventana primaria de un control de vista de lista que todos los elementos del control están a punto de eliminarse.</span><span class="sxs-lookup"><span data-stu-id="b8ae8-106">Notifies a list-view control's parent window that all items in the control are about to be deleted.</span></span> <span data-ttu-id="b8ae8-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b8ae8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b8ae8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8ae8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8ae8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8ae8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8ae8-110">Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="b8ae8-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="b8ae8-111">El miembro **iItem** es-1 y los demás miembros son cero.</span><span class="sxs-lookup"><span data-stu-id="b8ae8-111">The **iItem** member is -1, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8ae8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8ae8-112">Return value</span></span>

<span data-ttu-id="b8ae8-113">Para suprimir los códigos de notificación [LVN \_ DELETEITEM](lvn-deleteitem.md) posteriores, devuelva **true**.</span><span class="sxs-lookup"><span data-stu-id="b8ae8-113">To suppress subsequent [LVN\_DELETEITEM](lvn-deleteitem.md) notification codes, return **TRUE**.</span></span>

<span data-ttu-id="b8ae8-114">Para recibir los códigos de notificación de [LVN \_ DELETEITEM](lvn-deleteitem.md) posteriores, devuelva **false**.</span><span class="sxs-lookup"><span data-stu-id="b8ae8-114">To receive subsequent [LVN\_DELETEITEM](lvn-deleteitem.md) notification codes, return **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8ae8-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8ae8-115">Remarks</span></span>

<span data-ttu-id="b8ae8-116">Un control de vista de lista envía el código de notificación del [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) cuando se destruye o cuando recibe el mensaje **\_ DELETEALLITEMS de LVM** .</span><span class="sxs-lookup"><span data-stu-id="b8ae8-116">A list-view control sends the [**LVM\_DELETEALLITEMS**](lvm-deleteallitems.md) notification code when it is destroyed or when it receives the **LVM\_DELETEALLITEMS** message.</span></span> <span data-ttu-id="b8ae8-117">Si **el \_ DELETEALLITEMS LVM** no devuelve **true**, el control también enviará un código de notificación [LVN \_ DELETEITEM](lvn-deleteitem.md) a medida que se elimine cada elemento.</span><span class="sxs-lookup"><span data-stu-id="b8ae8-117">If **LVM\_DELETEALLITEMS** does not return **TRUE**, the control will also send an [LVN\_DELETEITEM](lvn-deleteitem.md) notification code as each item is deleted.</span></span>

<span data-ttu-id="b8ae8-118">Si el controlador de mensajes [**\_ DELETEALLITEMS LVM**](lvm-deleteallitems.md) está en un procedimiento de cuadro de diálogo, devuelva **true** en el procedimiento de cuadro de diálogo y use la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL \_ MSGRESULT para establecer el valor devuelto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b8ae8-118">If the [**LVM\_DELETEALLITEMS**](lvm-deleteallitems.md) message handler is in a dialog box procedure, return **TRUE** from the dialog box procedure, and use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT to set the message return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ae8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8ae8-119">Requirements</span></span>



| <span data-ttu-id="b8ae8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8ae8-120">Requirement</span></span> | <span data-ttu-id="b8ae8-121">Value</span><span class="sxs-lookup"><span data-stu-id="b8ae8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ae8-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8ae8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ae8-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b8ae8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8ae8-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8ae8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ae8-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8ae8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8ae8-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8ae8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8ae8-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8ae8-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

