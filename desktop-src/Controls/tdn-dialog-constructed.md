---
title: Código de notificación de TDN_DIALOG_CONSTRUCTED (commctrl. h)
description: Enviado por un cuadro de diálogo de tarea después de crear el cuadro de diálogo y antes de que se muestre. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: e8556039-a74d-4e33-931d-a63ad5b2d4b0
keywords:
- TDN_DIALOG_CONSTRUCTED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TDN_DIALOG_CONSTRUCTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d3360a8cee3542037ea927363de8cab69977e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997105"
---
# <a name="tdn_dialog_constructed-notification-code"></a><span data-ttu-id="63adf-105">TDN \_ cuadro de diálogo \_ construido código de notificación</span><span class="sxs-lookup"><span data-stu-id="63adf-105">TDN\_DIALOG\_CONSTRUCTED notification code</span></span>

<span data-ttu-id="63adf-106">Enviado por un cuadro de diálogo de tarea después de crear el cuadro de diálogo y antes de que se muestre.</span><span class="sxs-lookup"><span data-stu-id="63adf-106">Sent by a task dialog after the dialog has been created and before it is displayed.</span></span> <span data-ttu-id="63adf-107">Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="63adf-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_DIALOG_CONSTRUCTED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="63adf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63adf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63adf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63adf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63adf-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="63adf-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="63adf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63adf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63adf-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="63adf-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63adf-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63adf-113">Return value</span></span>

<span data-ttu-id="63adf-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="63adf-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="63adf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63adf-115">Requirements</span></span>



| <span data-ttu-id="63adf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="63adf-116">Requirement</span></span> | <span data-ttu-id="63adf-117">Value</span><span class="sxs-lookup"><span data-stu-id="63adf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63adf-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63adf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="63adf-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="63adf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63adf-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63adf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="63adf-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="63adf-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63adf-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63adf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="63adf-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="63adf-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





