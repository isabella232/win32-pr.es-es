---
title: Código de notificación de TDN_HYPERLINK_CLICKED (commctrl. h)
description: Enviado por un cuadro de diálogo de tarea cuando el usuario hace clic en un hipervínculo en el contenido del cuadro de diálogo de tarea. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: b769af31-32d0-463e-be15-6abf5dcb425c
keywords:
- TDN_HYPERLINK_CLICKED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TDN_HYPERLINK_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edd79406eb59f9bafd93269f8982db6213ef882c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151137"
---
# <a name="tdn_hyperlink_clicked-notification-code"></a><span data-ttu-id="93616-105">TDN \_ \_ código de notificación clic en hipervínculo</span><span class="sxs-lookup"><span data-stu-id="93616-105">TDN\_HYPERLINK\_CLICKED notification code</span></span>

<span data-ttu-id="93616-106">Enviado por un cuadro de diálogo de tarea cuando el usuario hace clic en un hipervínculo en el contenido del cuadro de diálogo de tarea.</span><span class="sxs-lookup"><span data-stu-id="93616-106">Sent by a task dialog when the user clicks a hyperlink in the task dialog content.</span></span> <span data-ttu-id="93616-107">Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="93616-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_HYPERLINK_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="93616-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93616-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93616-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93616-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93616-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="93616-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="93616-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93616-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93616-112">Puntero a una cadena de caracteres anchos que contiene la dirección URL del hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="93616-112">Pointer to a wide-character string containing the URL of the hyperlink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93616-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93616-113">Return value</span></span>

<span data-ttu-id="93616-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="93616-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="93616-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93616-115">Requirements</span></span>



| <span data-ttu-id="93616-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="93616-116">Requirement</span></span> | <span data-ttu-id="93616-117">Value</span><span class="sxs-lookup"><span data-stu-id="93616-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93616-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93616-118">Minimum supported client</span></span><br/> | <span data-ttu-id="93616-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="93616-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="93616-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93616-120">Minimum supported server</span></span><br/> | <span data-ttu-id="93616-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="93616-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="93616-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93616-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="93616-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="93616-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





