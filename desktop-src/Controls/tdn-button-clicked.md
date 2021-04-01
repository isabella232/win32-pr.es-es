---
title: Código de notificación de TDN_BUTTON_CLICKED (commctrl. h)
description: Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón o vínculo de comando en el cuadro de diálogo de tarea. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: eefe48f8-8a80-4280-8a7e-244d9b699ec7
keywords:
- TDN_BUTTON_CLICKED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TDN_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7a0b799f4163633194306edaa1703e068e93c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997106"
---
# <a name="tdn_button_clicked-notification-code"></a><span data-ttu-id="59ff8-105">\_Código de notificación de clic del botón TDN \_</span><span class="sxs-lookup"><span data-stu-id="59ff8-105">TDN\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="59ff8-106">Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón o vínculo de comando en el cuadro de diálogo de tarea.</span><span class="sxs-lookup"><span data-stu-id="59ff8-106">Sent by a task dialog when the user selects a button or command link in the task dialog.</span></span> <span data-ttu-id="59ff8-107">Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="59ff8-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_BUTTON_CLICKED  

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="59ff8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59ff8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59ff8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59ff8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59ff8-110">Un valor **int** que especifica el identificador del botón o vínculo de la selección que se ha seleccionado.</span><span class="sxs-lookup"><span data-stu-id="59ff8-110">An **int** that specifies the ID of the button or comand link that was selected.</span></span>

</dd> <dt>

<span data-ttu-id="59ff8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59ff8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59ff8-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="59ff8-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59ff8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59ff8-113">Return value</span></span>

<span data-ttu-id="59ff8-114">Para evitar que se cierre el cuadro de diálogo de tarea, la aplicación debe devolver **S \_ false**; de lo contrario, se cerrará el cuadro de diálogo de tarea y se devolverá el identificador de botón a través de la llamada de aplicación original.</span><span class="sxs-lookup"><span data-stu-id="59ff8-114">To prevent the task dialog from closing, the application must return **S\_FALSE**, otherwise the task dialog is closed and the button ID is returned via the original application call.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ff8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59ff8-115">Requirements</span></span>



| <span data-ttu-id="59ff8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="59ff8-116">Requirement</span></span> | <span data-ttu-id="59ff8-117">Value</span><span class="sxs-lookup"><span data-stu-id="59ff8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59ff8-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59ff8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="59ff8-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="59ff8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59ff8-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59ff8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="59ff8-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="59ff8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59ff8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59ff8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="59ff8-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="59ff8-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





