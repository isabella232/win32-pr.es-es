---
title: Código de notificación de TDN_EXPANDO_BUTTON_CLICKED (commctrl. h)
description: Enviado por el cuadro de diálogo de tarea cuando el usuario hace clic en el botón Expando del cuadro de diálogo. Esta notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: 15e2a9d0-9986-4fb1-a15e-dd4839e45146
keywords:
- TDN_EXPANDO_BUTTON_CLICKED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TDN_EXPANDO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3c36379a8efc40c7873d817b832705b3c1e084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658385"
---
# <a name="tdn_expando_button_clicked-notification-code"></a><span data-ttu-id="e485e-105">TDN \_ botón Expando con \_ \_ clic en el código de notificación</span><span class="sxs-lookup"><span data-stu-id="e485e-105">TDN\_EXPANDO\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="e485e-106">Enviado por el cuadro de diálogo de tarea cuando el usuario hace clic en el botón Expando del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e485e-106">Sent by the task dialog when the user clicks on the dialog's expando button.</span></span> <span data-ttu-id="e485e-107">Esta notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="e485e-107">This notification is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_EXPANDO_BUTTON_CLICKED
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="e485e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e485e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e485e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e485e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e485e-110">Valor **booleano** que es **true** si el cuadro de diálogo está expandido, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e485e-110">A **BOOL** that is **TRUE** if the dialog is expanded, or **FALSE** if not.</span></span>

</dd> <dt>

<span data-ttu-id="e485e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e485e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e485e-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e485e-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e485e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e485e-113">Return value</span></span>

<span data-ttu-id="e485e-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="e485e-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="e485e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e485e-115">Remarks</span></span>

<span data-ttu-id="e485e-116">En el ejemplo de la sección sintaxis se muestra la conversión a wParam antes de enviar la notificación.</span><span class="sxs-lookup"><span data-stu-id="e485e-116">The example in the Syntax section shows the cast to wParam before sending the notification.</span></span> <span data-ttu-id="e485e-117">**LParam** no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e485e-117">**LPARAM** is not used and must be zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="e485e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e485e-118">Requirements</span></span>



| <span data-ttu-id="e485e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e485e-119">Requirement</span></span> | <span data-ttu-id="e485e-120">Value</span><span class="sxs-lookup"><span data-stu-id="e485e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e485e-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e485e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e485e-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e485e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e485e-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e485e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e485e-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e485e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e485e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e485e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e485e-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e485e-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





