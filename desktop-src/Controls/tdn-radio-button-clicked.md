---
title: Código de notificación de TDN_RADIO_BUTTON_CLICKED (commctrl. h)
description: Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón de radio o un vínculo de comando en el cuadro de diálogo de tarea. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: d9a29874-6755-4754-bcaf-94746b218b47
keywords:
- TDN_RADIO_BUTTON_CLICKED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TDN_RADIO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c8b16f738e4807c94a060b41b3932d0f3e07ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997102"
---
# <a name="tdn_radio_button_clicked-notification-code"></a><span data-ttu-id="ee474-105">\_Código de \_ notificación del clic del botón de radio TDN \_</span><span class="sxs-lookup"><span data-stu-id="ee474-105">TDN\_RADIO\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="ee474-106">Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón de radio o un vínculo de comando en el cuadro de diálogo de tarea.</span><span class="sxs-lookup"><span data-stu-id="ee474-106">Sent by a task dialog when the user selects a radio button or command link in the task dialog.</span></span> <span data-ttu-id="ee474-107">Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="ee474-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_RADIO_BUTTON_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="ee474-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee474-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee474-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee474-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee474-110">Un valor **int** que especifica el identificador que corresponde al botón de radio en el que se hizo clic.</span><span class="sxs-lookup"><span data-stu-id="ee474-110">An **int** that specifies the ID corresponding to the radio button that was clicked.</span></span>

</dd> <dt>

<span data-ttu-id="ee474-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee474-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee474-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ee474-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee474-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee474-113">Return value</span></span>

<span data-ttu-id="ee474-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="ee474-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee474-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee474-115">Requirements</span></span>



| <span data-ttu-id="ee474-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee474-116">Requirement</span></span> | <span data-ttu-id="ee474-117">Value</span><span class="sxs-lookup"><span data-stu-id="ee474-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee474-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee474-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ee474-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ee474-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ee474-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee474-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ee474-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ee474-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee474-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee474-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee474-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee474-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





