---
title: Código de notificación de TDN_CREATED (commctrl. h)
description: Enviado por el cuadro de diálogo de tareas después de crear el cuadro de diálogo y antes de que se muestre. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: cfe13db3-9c3c-425c-a6ef-17c5cb33eeb6
keywords:
- TDN_CREATED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TDN_CREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a25aa40af6b2cb002f2da7aab7c71fd68702ae65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997107"
---
# <a name="tdn_created-notification-code"></a><span data-ttu-id="dd634-105">TDN \_ código de notificación creado</span><span class="sxs-lookup"><span data-stu-id="dd634-105">TDN\_CREATED notification code</span></span>

<span data-ttu-id="dd634-106">Enviado por el cuadro de diálogo de tareas después de crear el cuadro de diálogo y antes de que se muestre.</span><span class="sxs-lookup"><span data-stu-id="dd634-106">Sent by the task dialog after the dialog has been created and before it is displayed.</span></span> <span data-ttu-id="dd634-107">Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="dd634-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_CREATED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="dd634-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd634-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd634-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd634-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd634-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dd634-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dd634-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd634-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd634-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dd634-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd634-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd634-113">Return value</span></span>

<span data-ttu-id="dd634-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="dd634-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd634-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd634-115">Requirements</span></span>



| <span data-ttu-id="dd634-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd634-116">Requirement</span></span> | <span data-ttu-id="dd634-117">Value</span><span class="sxs-lookup"><span data-stu-id="dd634-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd634-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd634-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dd634-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dd634-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd634-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd634-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dd634-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd634-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd634-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd634-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd634-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd634-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





