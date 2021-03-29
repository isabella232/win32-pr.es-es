---
description: Una aplicación envía el mensaje de MDIDESTROY de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para cerrar una ventana secundaria MDI.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: Mensaje de WM_MDIDESTROY (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edea8fe8dadc691ca912df4e9ee5d57421124bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809559"
---
# <a name="wm_mdidestroy-message"></a><span data-ttu-id="8c8ed-103">Mensaje de MDIDESTROY de WM \_</span><span class="sxs-lookup"><span data-stu-id="8c8ed-103">WM\_MDIDESTROY message</span></span>

<span data-ttu-id="8c8ed-104">Una aplicación envía el mensaje de **\_ MDIDESTROY de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para cerrar una ventana secundaria MDI.</span><span class="sxs-lookup"><span data-stu-id="8c8ed-104">An application sends the **WM\_MDIDESTROY** message to a multiple-document interface (MDI) client window to close an MDI child window.</span></span>


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a><span data-ttu-id="8c8ed-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c8ed-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c8ed-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c8ed-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c8ed-107">Identificador de la ventana secundaria MDI que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="8c8ed-107">A handle to the MDI child window to be closed.</span></span>

</dd> <dt>

<span data-ttu-id="8c8ed-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c8ed-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c8ed-109">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8c8ed-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c8ed-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c8ed-110">Return value</span></span>

<span data-ttu-id="8c8ed-111">Tipo: **cero**</span><span class="sxs-lookup"><span data-stu-id="8c8ed-111">Type: **zero**</span></span>

<span data-ttu-id="8c8ed-112">Este mensaje siempre devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="8c8ed-112">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c8ed-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c8ed-113">Remarks</span></span>

<span data-ttu-id="8c8ed-114">Este mensaje quita el título de la ventana secundaria MDI de la ventana de marco MDI y desactiva la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="8c8ed-114">This message removes the title of the MDI child window from the MDI frame window and deactivates the child window.</span></span> <span data-ttu-id="8c8ed-115">Una aplicación debe usar este mensaje para cerrar todas las ventanas secundarias de MDI.</span><span class="sxs-lookup"><span data-stu-id="8c8ed-115">An application should use this message to close all MDI child windows.</span></span>

<span data-ttu-id="8c8ed-116">Si una ventana de cliente MDI recibe un mensaje que cambia la activación de sus ventanas secundarias y la ventana secundaria MDI activa está maximizada, el sistema restaura la ventana secundaria activa y maximiza la ventana secundaria recién activada.</span><span class="sxs-lookup"><span data-stu-id="8c8ed-116">If an MDI client window receives a message that changes the activation of its child windows and the active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c8ed-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c8ed-117">Requirements</span></span>



| <span data-ttu-id="8c8ed-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c8ed-118">Requirement</span></span> | <span data-ttu-id="8c8ed-119">Value</span><span class="sxs-lookup"><span data-stu-id="8c8ed-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c8ed-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c8ed-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8c8ed-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8c8ed-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8c8ed-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c8ed-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8c8ed-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8c8ed-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8c8ed-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c8ed-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c8ed-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c8ed-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c8ed-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c8ed-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c8ed-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="8c8ed-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8c8ed-128">**MDICREATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="8c8ed-128">**WM\_MDICREATE**</span></span>](wm-mdicreate.md)
</dt> <dt>

<span data-ttu-id="8c8ed-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="8c8ed-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8c8ed-130">Interfaz de varios documentos</span><span class="sxs-lookup"><span data-stu-id="8c8ed-130">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




