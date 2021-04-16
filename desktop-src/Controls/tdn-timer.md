---
title: Código de notificación de TDN_TIMER (commctrl. h)
description: Enviado por un cuadro de diálogo de tarea aproximadamente cada 200 milisegundos.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- TDN_TIMER controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TDN_TIMER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eea7a1604c70c187299c9f2c99abbe934926317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658383"
---
# <a name="tdn_timer-notification-code"></a><span data-ttu-id="b04e5-104">\_Código de notificación del temporizador de TDN</span><span class="sxs-lookup"><span data-stu-id="b04e5-104">TDN\_TIMER notification code</span></span>

<span data-ttu-id="b04e5-105">Enviado por un cuadro de diálogo de tarea aproximadamente cada 200 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="b04e5-105">Sent by a task dialog approximately every 200 milliseconds.</span></span> <span data-ttu-id="b04e5-106">Este código de notificación se envía cuando se ha \_ establecido la marca de temporizador de devolución de llamada TDF \_ en el miembro **dwFlags** de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) que se pasó a la función [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="b04e5-106">This notification code is sent when the TDF\_CALLBACK\_TIMER flag has been set in the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure that was passed to the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span> <span data-ttu-id="b04e5-107">Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método **TaskDialogIndirect** .</span><span class="sxs-lookup"><span data-stu-id="b04e5-107">This notification code is received only through the task dialog callback function, which can be registered using the **TaskDialogIndirect** method.</span></span>


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="b04e5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b04e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b04e5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b04e5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b04e5-110">**DWORD** que especifica el número de milisegundos transcurridos desde que se creó el cuadro de diálogo o el código de notificación devolvió **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="b04e5-110">A **DWORD** that specifies the number of milliseconds since the dialog was created or this notification code returned **S\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b04e5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b04e5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b04e5-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b04e5-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b04e5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b04e5-113">Return value</span></span>

<span data-ttu-id="b04e5-114">Para restablecer el TickCount, la aplicación debe devolver **S \_ false**; de lo contrario, el TickCount seguirá aumentando.</span><span class="sxs-lookup"><span data-stu-id="b04e5-114">To reset the tickcount, the application must return **S\_FALSE**, otherwise the tickcount will continue to increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="b04e5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b04e5-115">Requirements</span></span>



| <span data-ttu-id="b04e5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b04e5-116">Requirement</span></span> | <span data-ttu-id="b04e5-117">Value</span><span class="sxs-lookup"><span data-stu-id="b04e5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b04e5-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b04e5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b04e5-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b04e5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b04e5-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b04e5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b04e5-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b04e5-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b04e5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b04e5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b04e5-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b04e5-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





