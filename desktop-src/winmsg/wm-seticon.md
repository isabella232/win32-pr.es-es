---
description: Asocia un nuevo icono grande o pequeño a una ventana. El sistema muestra el icono grande en el cuadro de diálogo ALT + TAB y el icono pequeño en el título de la ventana.
ms.assetid: c86620f2-893b-46f8-8254-1d7c4c142f37
title: Mensaje de WM_SETICON (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bec7fc653123ba0a950c96bc1f54ebf436b0d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276846"
---
# <a name="wm_seticon-message"></a><span data-ttu-id="780a4-104">Mensaje de SETICON de WM \_</span><span class="sxs-lookup"><span data-stu-id="780a4-104">WM\_SETICON message</span></span>

<span data-ttu-id="780a4-105">Asocia un nuevo icono grande o pequeño a una ventana.</span><span class="sxs-lookup"><span data-stu-id="780a4-105">Associates a new large or small icon with a window.</span></span> <span data-ttu-id="780a4-106">El sistema muestra el icono grande en el cuadro de diálogo ALT + TAB y el icono pequeño en el título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="780a4-106">The system displays the large icon in the ALT+TAB dialog box, and the small icon in the window caption.</span></span>


```C++
#define WM_SETICON                      0x0080
```



## <a name="parameters"></a><span data-ttu-id="780a4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="780a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="780a4-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="780a4-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="780a4-109">Tipo de icono que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="780a4-109">The type of icon to be set.</span></span> <span data-ttu-id="780a4-110">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="780a4-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="780a4-111">Valor</span><span class="sxs-lookup"><span data-stu-id="780a4-111">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="780a4-112">Significado</span><span class="sxs-lookup"><span data-stu-id="780a4-112">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <span data-ttu-id="780a4-113"><dt>**Icono \_ de BIG**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="780a4-113"><dt>**ICON\_BIG**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="780a4-114">Establezca el icono grande para la ventana.</span><span class="sxs-lookup"><span data-stu-id="780a4-114">Set the large icon for the window.</span></span><br/> |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <span data-ttu-id="780a4-115"><dt>**Icono \_ de PEQUEÑO**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="780a4-115"><dt>**ICON\_SMALL**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="780a4-116">Establezca el icono pequeño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="780a4-116">Set the small icon for the window.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="780a4-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="780a4-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="780a4-118">Identificador para el nuevo icono grande o pequeño.</span><span class="sxs-lookup"><span data-stu-id="780a4-118">A handle to the new large or small icon.</span></span> <span data-ttu-id="780a4-119">Si este parámetro es **null**, se quita el icono indicado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="780a4-119">If this parameter is **NULL**, the icon indicated by *wParam* is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="780a4-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="780a4-120">Return value</span></span>

<span data-ttu-id="780a4-121">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="780a4-121">Type: **LRESULT**</span></span>

<span data-ttu-id="780a4-122">El valor devuelto es un identificador del icono grande o pequeño anterior, dependiendo del valor de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="780a4-122">The return value is a handle to the previous large or small icon, depending on the value of *wParam*.</span></span> <span data-ttu-id="780a4-123">Es **null** si la ventana no tenía previamente ningún icono del tipo indicado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="780a4-123">It is **NULL** if the window previously had no icon of the type indicated by *wParam*.</span></span>

## <a name="remarks"></a><span data-ttu-id="780a4-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="780a4-124">Remarks</span></span>

<span data-ttu-id="780a4-125">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve un identificador al icono grande o pequeño anterior asociado a la ventana, dependiendo del valor de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="780a4-125">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns a handle to the previous large or small icon associated with the window, depending on the value of *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="780a4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="780a4-126">Requirements</span></span>



| <span data-ttu-id="780a4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="780a4-127">Requirement</span></span> | <span data-ttu-id="780a4-128">Value</span><span class="sxs-lookup"><span data-stu-id="780a4-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="780a4-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="780a4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="780a4-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="780a4-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="780a4-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="780a4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="780a4-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="780a4-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="780a4-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="780a4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="780a4-134"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="780a4-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="780a4-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="780a4-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="780a4-136">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="780a4-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="780a4-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="780a4-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="780a4-138">**GETICON de WM \_**</span><span class="sxs-lookup"><span data-stu-id="780a4-138">**WM\_GETICON**</span></span>](wm-geticon.md)
</dt> <dt>

<span data-ttu-id="780a4-139">**Vista**</span><span class="sxs-lookup"><span data-stu-id="780a4-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="780a4-140">Windows</span><span class="sxs-lookup"><span data-stu-id="780a4-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
