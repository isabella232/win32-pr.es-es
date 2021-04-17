---
description: Mensaje que se envía siempre que se produce un cambio en la hora del sistema.
ms.assetid: 94b5b6f7-04bb-4e0a-848b-e2b31ffc2938
title: Mensaje de WM_TIMECHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d43bb5cd4284813c45ab074a93a9cd9699883aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666924"
---
# <a name="wm_timechange-message"></a><span data-ttu-id="ce2fb-103">Mensaje de TIMECHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="ce2fb-103">WM\_TIMECHANGE message</span></span>

<span data-ttu-id="ce2fb-104">Mensaje que se envía siempre que se produce un cambio en la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-104">A message that is sent whenever there is a change in the system time.</span></span>

<span data-ttu-id="ce2fb-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ce2fb-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // message identifier
  WPARAM wParam,   // not used; must be zero
  LPARAM lParam    // not used; must be zero
);
```



## <a name="parameters"></a><span data-ttu-id="ce2fb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce2fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce2fb-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="ce2fb-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ce2fb-108">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-108">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="ce2fb-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="ce2fb-110">**WM \_** Identificador de TIMECHANGE.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-110">**WM\_TIMECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce2fb-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce2fb-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce2fb-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce2fb-114">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce2fb-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce2fb-115">Return value</span></span>

<span data-ttu-id="ce2fb-116">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-116">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce2fb-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce2fb-117">Remarks</span></span>

<span data-ttu-id="ce2fb-118">Una aplicación no debe difundir este mensaje, porque el sistema difundirá este mensaje cuando la aplicación cambie la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-118">An application should not broadcast this message, because the system will broadcast this message when the application changes the system time.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce2fb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce2fb-119">Requirements</span></span>



| <span data-ttu-id="ce2fb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce2fb-120">Requirement</span></span> | <span data-ttu-id="ce2fb-121">Value</span><span class="sxs-lookup"><span data-stu-id="ce2fb-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2fb-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce2fb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ce2fb-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ce2fb-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ce2fb-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce2fb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ce2fb-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ce2fb-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ce2fb-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce2fb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce2fb-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce2fb-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce2fb-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce2fb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce2fb-129">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-129">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

