---
description: Una aplicación envía el mensaje de MDIMAXIMIZE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para maximizar una ventana secundaria MDI.
ms.assetid: 7c5e4157-13f6-40d7-a64a-076bd14aca0d
title: Mensaje de WM_MDIMAXIMIZE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8372bcb25f35a52793292de4fd94a4a9dadafe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715063"
---
# <a name="wm_mdimaximize-message"></a><span data-ttu-id="175ba-103">Mensaje de MDIMAXIMIZE de WM \_</span><span class="sxs-lookup"><span data-stu-id="175ba-103">WM\_MDIMAXIMIZE message</span></span>

<span data-ttu-id="175ba-104">Una aplicación envía el mensaje de **\_ MDIMAXIMIZE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para maximizar una ventana secundaria MDI.</span><span class="sxs-lookup"><span data-stu-id="175ba-104">An application sends the **WM\_MDIMAXIMIZE** message to a multiple-document interface (MDI) client window to maximize an MDI child window.</span></span> <span data-ttu-id="175ba-105">El sistema cambia el tamaño de la ventana secundaria para que su área cliente rellene la ventana del cliente.</span><span class="sxs-lookup"><span data-stu-id="175ba-105">The system resizes the child window to make its client area fill the client window.</span></span> <span data-ttu-id="175ba-106">El sistema coloca el icono de menú ventana de la ventana secundaria en la posición más a la derecha de la barra de menús de la ventana de marco y coloca el icono de restauración de la ventana secundaria en la posición más a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="175ba-106">The system places the child window's window menu icon in the rightmost position of the frame window's menu bar, and places the child window's restore icon in the leftmost position.</span></span> <span data-ttu-id="175ba-107">El sistema también anexa el texto de la barra de título de la ventana secundaria al de la ventana de marco.</span><span class="sxs-lookup"><span data-stu-id="175ba-107">The system also appends the title bar text of the child window to that of the frame window.</span></span>


```C++
#define WM_MDIMAXIMIZE                  0x0225
```



## <a name="parameters"></a><span data-ttu-id="175ba-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="175ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="175ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="175ba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="175ba-110">Identificador de la ventana secundaria MDI que se va a maximizar.</span><span class="sxs-lookup"><span data-stu-id="175ba-110">A handle to the MDI child window to be maximized.</span></span>

</dd> <dt>

<span data-ttu-id="175ba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="175ba-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="175ba-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="175ba-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="175ba-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="175ba-113">Return value</span></span>

<span data-ttu-id="175ba-114">Tipo: **cero**</span><span class="sxs-lookup"><span data-stu-id="175ba-114">Type: **zero**</span></span>

<span data-ttu-id="175ba-115">El valor devuelto siempre es cero.</span><span class="sxs-lookup"><span data-stu-id="175ba-115">The return value is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="175ba-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="175ba-116">Remarks</span></span>

<span data-ttu-id="175ba-117">Si una ventana de cliente MDI recibe cualquier mensaje que cambie la activación de sus ventanas secundarias mientras se maximiza la ventana secundaria MDI activa actualmente, el sistema restaura la ventana secundaria activa y maximiza la ventana secundaria recién activada.</span><span class="sxs-lookup"><span data-stu-id="175ba-117">If an MDI client window receives any message that changes the activation of its child windows while the currently active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="175ba-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="175ba-118">Requirements</span></span>



| <span data-ttu-id="175ba-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="175ba-119">Requirement</span></span> | <span data-ttu-id="175ba-120">Value</span><span class="sxs-lookup"><span data-stu-id="175ba-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="175ba-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="175ba-121">Minimum supported client</span></span><br/> | <span data-ttu-id="175ba-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="175ba-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="175ba-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="175ba-123">Minimum supported server</span></span><br/> | <span data-ttu-id="175ba-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="175ba-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="175ba-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="175ba-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="175ba-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="175ba-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="175ba-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="175ba-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="175ba-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="175ba-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="175ba-129">**MDIRESTORE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="175ba-129">**WM\_MDIRESTORE**</span></span>](wm-mdirestore.md)
</dt> <dt>

<span data-ttu-id="175ba-130">**Vista**</span><span class="sxs-lookup"><span data-stu-id="175ba-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="175ba-131">Interfaz de varios documentos</span><span class="sxs-lookup"><span data-stu-id="175ba-131">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




