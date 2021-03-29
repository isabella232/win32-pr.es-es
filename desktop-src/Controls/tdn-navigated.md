---
title: Código de notificación de TDN_NAVIGATED (commctrl. h)
description: Enviado por un cuadro de diálogo de tarea cuando se ha producido la navegación. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: e7668ab3-3a11-4bf4-8cb4-067d3204fb3f
keywords:
- TDN_NAVIGATED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TDN_NAVIGATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9d8e9244889d7e55aad2b89f8ca4bb1c0bb1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535434"
---
# <a name="tdn_navigated-notification-code"></a><span data-ttu-id="145a0-105">TDN \_ código de notificación navegado</span><span class="sxs-lookup"><span data-stu-id="145a0-105">TDN\_NAVIGATED notification code</span></span>

<span data-ttu-id="145a0-106">Enviado por un cuadro de diálogo de tarea cuando se ha producido la navegación.</span><span class="sxs-lookup"><span data-stu-id="145a0-106">Sent by a task dialog when navigation has occurred.</span></span> <span data-ttu-id="145a0-107">Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="145a0-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_NAVIGATED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="145a0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="145a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="145a0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="145a0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="145a0-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="145a0-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="145a0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="145a0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="145a0-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="145a0-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="145a0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="145a0-113">Return value</span></span>

<span data-ttu-id="145a0-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="145a0-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="145a0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="145a0-115">Requirements</span></span>



| <span data-ttu-id="145a0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="145a0-116">Requirement</span></span> | <span data-ttu-id="145a0-117">Value</span><span class="sxs-lookup"><span data-stu-id="145a0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="145a0-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="145a0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="145a0-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="145a0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="145a0-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="145a0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="145a0-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="145a0-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="145a0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="145a0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="145a0-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="145a0-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





