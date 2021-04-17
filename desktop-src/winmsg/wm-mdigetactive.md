---
description: Una aplicación envía el mensaje de MDIGETACTIVE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para recuperar el identificador de la ventana secundaria MDI activa.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: Mensaje de WM_MDIGETACTIVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49f4ec321f526cd4c9766555e2361ef2cfbd040
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706665"
---
# <a name="wm_mdigetactive-message"></a><span data-ttu-id="1d21e-103">Mensaje de MDIGETACTIVE de WM \_</span><span class="sxs-lookup"><span data-stu-id="1d21e-103">WM\_MDIGETACTIVE message</span></span>

<span data-ttu-id="1d21e-104">Una aplicación envía el mensaje de **\_ MDIGETACTIVE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para recuperar el identificador de la ventana secundaria MDI activa.</span><span class="sxs-lookup"><span data-stu-id="1d21e-104">An application sends the **WM\_MDIGETACTIVE** message to a multiple-document interface (MDI) client window to retrieve the handle to the active MDI child window.</span></span>


```C++
#define WM_MDIGETACTIVE                  0x0229
```



## <a name="parameters"></a><span data-ttu-id="1d21e-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d21e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d21e-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d21e-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d21e-107">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1d21e-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1d21e-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d21e-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d21e-109">Estado maximizado.</span><span class="sxs-lookup"><span data-stu-id="1d21e-109">The maximized state.</span></span> <span data-ttu-id="1d21e-110">Si este parámetro no es **null**, es un puntero a un valor que indica el estado maximizado de la ventana secundaria MDI.</span><span class="sxs-lookup"><span data-stu-id="1d21e-110">If this parameter is not **NULL**, it is a pointer to a value that indicates the maximized state of the MDI child window.</span></span> <span data-ttu-id="1d21e-111">Si el valor es **true**, la ventana está maximizada; un valor de **false** indica que no lo es.</span><span class="sxs-lookup"><span data-stu-id="1d21e-111">If the value is **TRUE**, the window is maximized; a value of **FALSE** indicates that it is not.</span></span> <span data-ttu-id="1d21e-112">Si este parámetro es **null**, se omite el parámetro.</span><span class="sxs-lookup"><span data-stu-id="1d21e-112">If this parameter is **NULL**, the parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d21e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d21e-113">Return value</span></span>

<span data-ttu-id="1d21e-114">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="1d21e-114">Type: **HWND**</span></span>

<span data-ttu-id="1d21e-115">El valor devuelto es el identificador de la ventana secundaria MDI activa.</span><span class="sxs-lookup"><span data-stu-id="1d21e-115">The return value is the handle to the active MDI child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d21e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d21e-116">Requirements</span></span>



| <span data-ttu-id="1d21e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d21e-117">Requirement</span></span> | <span data-ttu-id="1d21e-118">Value</span><span class="sxs-lookup"><span data-stu-id="1d21e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d21e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d21e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1d21e-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1d21e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1d21e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d21e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1d21e-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1d21e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1d21e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d21e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d21e-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d21e-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d21e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d21e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d21e-126">Información general sobre la interfaz de varios documentos</span><span class="sxs-lookup"><span data-stu-id="1d21e-126">Multiple Document Interface Overview</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




