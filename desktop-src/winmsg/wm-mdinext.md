---
description: Una aplicación envía el mensaje de MDINEXT de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para activar la ventana secundaria siguiente o anterior.
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: Mensaje de WM_MDINEXT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e0af031c11ea37129e1405e31b07b18f023b7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809554"
---
# <a name="wm_mdinext-message"></a><span data-ttu-id="bfa8e-103">Mensaje de MDINEXT de WM \_</span><span class="sxs-lookup"><span data-stu-id="bfa8e-103">WM\_MDINEXT message</span></span>

<span data-ttu-id="bfa8e-104">Una aplicación envía el mensaje de **\_ MDINEXT de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para activar la ventana secundaria siguiente o anterior.</span><span class="sxs-lookup"><span data-stu-id="bfa8e-104">An application sends the **WM\_MDINEXT** message to a multiple-document interface (MDI) client window to activate the next or previous child window.</span></span>


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a><span data-ttu-id="bfa8e-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfa8e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa8e-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bfa8e-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfa8e-107">Identificador de la ventana secundaria MDI.</span><span class="sxs-lookup"><span data-stu-id="bfa8e-107">A handle to the MDI child window.</span></span> <span data-ttu-id="bfa8e-108">El sistema activa la ventana secundaria que está inmediatamente antes o después de la ventana secundaria especificada, en función del valor del parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="bfa8e-108">The system activates the child window that is immediately before or after the specified child window, depending on the value of the *lParam* parameter.</span></span> <span data-ttu-id="bfa8e-109">Si el parámetro *wParam* es **null**, el sistema activa la ventana secundaria que está inmediatamente antes o después de la ventana secundaria activa actualmente.</span><span class="sxs-lookup"><span data-stu-id="bfa8e-109">If the *wParam* parameter is **NULL**, the system activates the child window that is immediately before or after the currently active child window.</span></span>

</dd> <dt>

<span data-ttu-id="bfa8e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfa8e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfa8e-111">Si este parámetro es cero, el sistema activa la ventana secundaria MDI siguiente y coloca la ventana secundaria identificada por el parámetro *wParam* detrás de las demás ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="bfa8e-111">If this parameter is zero, the system activates the next MDI child window and places the child window identified by the *wParam* parameter behind all other child windows.</span></span> <span data-ttu-id="bfa8e-112">Si este parámetro es distinto de cero, el sistema activa la ventana secundaria anterior, colocándolo delante de la ventana secundaria identificada por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="bfa8e-112">If this parameter is nonzero, the system activates the previous child window, placing it in front of the child window identified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfa8e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfa8e-113">Return value</span></span>

<span data-ttu-id="bfa8e-114">Tipo: **cero**</span><span class="sxs-lookup"><span data-stu-id="bfa8e-114">Type: **zero**</span></span>

<span data-ttu-id="bfa8e-115">El valor devuelto siempre es cero.</span><span class="sxs-lookup"><span data-stu-id="bfa8e-115">The return value is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfa8e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfa8e-116">Remarks</span></span>

<span data-ttu-id="bfa8e-117">Si una ventana de cliente MDI recibe cualquier mensaje que cambie la activación de sus ventanas secundarias mientras la ventana secundaria MDI activa está maximizada, el sistema restaura la ventana secundaria activa y maximiza la ventana secundaria recién activada.</span><span class="sxs-lookup"><span data-stu-id="bfa8e-117">If an MDI client window receives any message that changes the activation of its child windows while the active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfa8e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfa8e-118">Requirements</span></span>



| <span data-ttu-id="bfa8e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfa8e-119">Requirement</span></span> | <span data-ttu-id="bfa8e-120">Value</span><span class="sxs-lookup"><span data-stu-id="bfa8e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa8e-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfa8e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa8e-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bfa8e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bfa8e-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfa8e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa8e-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bfa8e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bfa8e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfa8e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfa8e-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfa8e-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfa8e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfa8e-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="bfa8e-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="bfa8e-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bfa8e-129">**MDIACTIVATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="bfa8e-129">**WM\_MDIACTIVATE**</span></span>](wm-mdiactivate.md)
</dt> <dt>

[<span data-ttu-id="bfa8e-130">**MDIGETACTIVE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="bfa8e-130">**WM\_MDIGETACTIVE**</span></span>](wm-mdigetactive.md)
</dt> <dt>

<span data-ttu-id="bfa8e-131">**Vista**</span><span class="sxs-lookup"><span data-stu-id="bfa8e-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bfa8e-132">Interfaz de varios documentos</span><span class="sxs-lookup"><span data-stu-id="bfa8e-132">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




