---
title: Código de notificación de TDN_HELP (commctrl. h)
description: Enviado por un cuadro de diálogo de tarea cuando el usuario presiona F1 en el teclado mientras el cuadro de diálogo tiene el foco. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: 207ba231-639d-4906-b5dc-1592f2717f1c
keywords:
- TDN_HELP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TDN_HELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d5e08342094aec5adc3da42621307d1577cd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151138"
---
# <a name="tdn_help-notification-code"></a><span data-ttu-id="dcacf-105">Código de notificación de ayuda de TDN \_</span><span class="sxs-lookup"><span data-stu-id="dcacf-105">TDN\_HELP notification code</span></span>

<span data-ttu-id="dcacf-106">Enviado por un cuadro de diálogo de tarea cuando el usuario presiona F1 en el teclado mientras el cuadro de diálogo tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="dcacf-106">Sent by a task dialog when the user presses F1 on the keyboard while the dialog has focus.</span></span> <span data-ttu-id="dcacf-107">Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="dcacf-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_HELP
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="dcacf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcacf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcacf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dcacf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dcacf-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dcacf-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dcacf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dcacf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dcacf-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dcacf-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcacf-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcacf-113">Return value</span></span>

<span data-ttu-id="dcacf-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="dcacf-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcacf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcacf-115">Requirements</span></span>



| <span data-ttu-id="dcacf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcacf-116">Requirement</span></span> | <span data-ttu-id="dcacf-117">Value</span><span class="sxs-lookup"><span data-stu-id="dcacf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dcacf-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcacf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dcacf-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dcacf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dcacf-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcacf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dcacf-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dcacf-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dcacf-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcacf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcacf-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcacf-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





