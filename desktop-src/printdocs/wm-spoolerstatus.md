---
description: El \_ mensaje de SPOOLERSTATUS de WM se envía desde el administrador de impresión siempre que se agrega o se quita un trabajo de la cola del administrador de impresión.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: Mensaje de WM_SPOOLERSTATUS (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460e36e44f219bcbe6f514d7d368accddae46b83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156648"
---
# <a name="wm_spoolerstatus-message"></a><span data-ttu-id="df834-103">Mensaje de SPOOLERSTATUS de WM \_</span><span class="sxs-lookup"><span data-stu-id="df834-103">WM\_SPOOLERSTATUS message</span></span>

<span data-ttu-id="df834-104">El mensaje de **\_ SPOOLERSTATUS de WM** se envía desde el administrador de impresión siempre que se agrega o se quita un trabajo de la cola del administrador de impresión.</span><span class="sxs-lookup"><span data-stu-id="df834-104">The **WM\_SPOOLERSTATUS** message is sent from Print Manager whenever a job is added to or removed from the Print Manager queue.</span></span>

<span data-ttu-id="df834-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="df834-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="df834-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df834-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df834-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df834-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df834-108">\_Marca JOBSTATUS de PR.</span><span class="sxs-lookup"><span data-stu-id="df834-108">The PR\_JOBSTATUS flag.</span></span>

</dd> <dt>

<span data-ttu-id="df834-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df834-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df834-110">La palabra de orden inferior especifica el número de trabajos que quedan en la cola del administrador de impresión.</span><span class="sxs-lookup"><span data-stu-id="df834-110">The low-order word specifies the number of jobs remaining in the Print Manager queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df834-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df834-111">Return value</span></span>

<span data-ttu-id="df834-112">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="df834-112">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="df834-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df834-113">Remarks</span></span>

<span data-ttu-id="df834-114">Este mensaje es meramente informativo.</span><span class="sxs-lookup"><span data-stu-id="df834-114">This message is for informational purposes only.</span></span> <span data-ttu-id="df834-115">Este mensaje es un aviso y no tiene una semántica de entrega garantizada.</span><span class="sxs-lookup"><span data-stu-id="df834-115">This message is advisory and does not have guaranteed delivery semantics.</span></span> <span data-ttu-id="df834-116">Las aplicaciones no deben suponer que recibirán un \_ mensaje de SPOOLERSTATUS de WM por cada cambio en el estado de la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="df834-116">Applications should not assume that they will receive a WM\_SPOOLERSTATUS message for every change in spooler status.</span></span>

<span data-ttu-id="df834-117">El mensaje de SPOOLERSTATUS de WM \_ no se admite después de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="df834-117">The WM\_SPOOLERSTATUS message is not supported after Windows XP.</span></span> <span data-ttu-id="df834-118">Para recibir notificaciones de los cambios en el estado de la cola de impresión, puede usar [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) y [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span><span class="sxs-lookup"><span data-stu-id="df834-118">To be notified of changes to the print queue status, you can use [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) and [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df834-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df834-119">Requirements</span></span>



| <span data-ttu-id="df834-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="df834-120">Requirement</span></span> | <span data-ttu-id="df834-121">Value</span><span class="sxs-lookup"><span data-stu-id="df834-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df834-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df834-122">Minimum supported client</span></span><br/> | <span data-ttu-id="df834-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="df834-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="df834-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df834-124">Minimum supported server</span></span><br/> | <span data-ttu-id="df834-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="df834-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="df834-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df834-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="df834-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df834-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df834-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="df834-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df834-129">Impresión</span><span class="sxs-lookup"><span data-stu-id="df834-129">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="df834-130">Mensajes de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="df834-130">Print Spooler API Messages</span></span>](printing-and-print-spooler-messages.md)
</dt> <dt>

[<span data-ttu-id="df834-131">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="df834-131">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="df834-132">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="df834-132">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> </dl>

 

