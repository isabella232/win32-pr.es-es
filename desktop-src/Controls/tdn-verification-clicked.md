---
title: Código de notificación de TDN_VERIFICATION_CLICKED (commctrl. h)
description: Enviado por un cuadro de diálogo de tarea cuando el usuario hace clic en la casilla comprobación del cuadro de diálogo de tareas. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: cd7bc07a-9a70-4361-abfa-986a5a2e13e0
keywords:
- TDN_VERIFICATION_CLICKED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TDN_VERIFICATION_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7887a4d696f5294ebffc6fc6cc7183ff2c0aed8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997101"
---
# <a name="tdn_verification_clicked-notification-code"></a><span data-ttu-id="96b67-105">\_Código de notificación de clic de comprobación de TDN \_</span><span class="sxs-lookup"><span data-stu-id="96b67-105">TDN\_VERIFICATION\_CLICKED notification code</span></span>

<span data-ttu-id="96b67-106">Enviado por un cuadro de diálogo de tarea cuando el usuario hace clic en la casilla comprobación del cuadro de diálogo de tareas.</span><span class="sxs-lookup"><span data-stu-id="96b67-106">Sent by a task dialog when the user clicks the task dialog verification check box.</span></span> <span data-ttu-id="96b67-107">Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="96b67-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_VERIFICATION_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="96b67-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96b67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96b67-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96b67-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96b67-110">Un **booleano** que especifica el estado de la casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="96b67-110">A **BOOL** that specifies the status of the verification checkbox.</span></span> <span data-ttu-id="96b67-111">Es **true** si la casilla de verificación está activada o **false** si está desactivada.</span><span class="sxs-lookup"><span data-stu-id="96b67-111">It is **TRUE** if the verification checkbox is checked, or **FALSE** if it is unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="96b67-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96b67-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96b67-113">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="96b67-113">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96b67-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96b67-114">Return value</span></span>

<span data-ttu-id="96b67-115">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="96b67-115">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="96b67-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96b67-116">Requirements</span></span>



| <span data-ttu-id="96b67-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="96b67-117">Requirement</span></span> | <span data-ttu-id="96b67-118">Value</span><span class="sxs-lookup"><span data-stu-id="96b67-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96b67-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96b67-119">Minimum supported client</span></span><br/> | <span data-ttu-id="96b67-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="96b67-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="96b67-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96b67-121">Minimum supported server</span></span><br/> | <span data-ttu-id="96b67-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="96b67-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96b67-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96b67-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="96b67-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="96b67-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96b67-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="96b67-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="96b67-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="96b67-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="96b67-127">*TaskDialogCallbackProc*</span><span class="sxs-lookup"><span data-stu-id="96b67-127">*TaskDialogCallbackProc*</span></span>](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)
</dt> </dl>

 

