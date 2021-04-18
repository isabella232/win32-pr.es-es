---
description: Se envía a una ventana para recuperar un identificador del icono grande o pequeño asociado a una ventana. El sistema muestra el icono grande en el cuadro de diálogo ALT + TAB y el icono pequeño en el título de la ventana.
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: Mensaje de WM_GETICON (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d2444e70646d8122a7228094187738811a3f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706667"
---
# <a name="wm_geticon-message"></a><span data-ttu-id="49340-104">Mensaje de GETICON de WM \_</span><span class="sxs-lookup"><span data-stu-id="49340-104">WM\_GETICON message</span></span>

<span data-ttu-id="49340-105">Se envía a una ventana para recuperar un identificador del icono grande o pequeño asociado a una ventana.</span><span class="sxs-lookup"><span data-stu-id="49340-105">Sent to a window to retrieve a handle to the large or small icon associated with a window.</span></span> <span data-ttu-id="49340-106">El sistema muestra el icono grande en el cuadro de diálogo ALT + TAB y el icono pequeño en el título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="49340-106">The system displays the large icon in the ALT+TAB dialog, and the small icon in the window caption.</span></span>

<span data-ttu-id="49340-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="49340-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a><span data-ttu-id="49340-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49340-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49340-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49340-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49340-110">Tipo de icono que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="49340-110">The type of icon being retrieved.</span></span> <span data-ttu-id="49340-111">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="49340-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="49340-112">Valor</span><span class="sxs-lookup"><span data-stu-id="49340-112">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="49340-113">Significado</span><span class="sxs-lookup"><span data-stu-id="49340-113">Meaning</span></span>                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <span data-ttu-id="49340-114"><dt>**Icono \_ de BIG**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="49340-114"><dt>**ICON\_BIG**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="49340-115">Recupere el icono grande de la ventana.</span><span class="sxs-lookup"><span data-stu-id="49340-115">Retrieve the large icon for the window.</span></span><br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <span data-ttu-id="49340-116"><dt>**Icono \_ de PEQUEÑO**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="49340-116"><dt>**ICON\_SMALL**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="49340-117">Recupere el icono pequeño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="49340-117">Retrieve the small icon for the window.</span></span><br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <span data-ttu-id="49340-118"><dt>**Icono \_ de SMALL2**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="49340-118"><dt>**ICON\_SMALL2**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="49340-119">Recupera el icono pequeño proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="49340-119">Retrieves the small icon provided by the application.</span></span> <span data-ttu-id="49340-120">Si la aplicación no proporciona ninguna, el sistema utiliza el icono generado por el sistema para esa ventana.</span><span class="sxs-lookup"><span data-stu-id="49340-120">If the application does not provide one, the system uses the system-generated icon for that window.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="49340-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49340-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49340-122">DPI del icono que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="49340-122">The DPI of the icon being retrieved.</span></span> <span data-ttu-id="49340-123">Se puede usar para proporcionar iconos diferentes en función del tamaño del icono.</span><span class="sxs-lookup"><span data-stu-id="49340-123">This can be used to provide different icons depending on the icon size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49340-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49340-124">Return value</span></span>

<span data-ttu-id="49340-125">Tipo: **HICON**</span><span class="sxs-lookup"><span data-stu-id="49340-125">Type: **HICON**</span></span>

<span data-ttu-id="49340-126">El valor devuelto es un identificador del icono grande o pequeño, dependiendo del valor de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="49340-126">The return value is a handle to the large or small icon, depending on the value of *wParam*.</span></span> <span data-ttu-id="49340-127">Cuando una aplicación recibe este mensaje, puede devolver un identificador a un icono grande o pequeño, o pasar el mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="49340-127">When an application receives this message, it can return a handle to a large or small icon, or pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="49340-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49340-128">Remarks</span></span>

<span data-ttu-id="49340-129">Cuando una aplicación recibe este mensaje, puede devolver un identificador a un icono grande o pequeño, o pasar el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="49340-129">When an application receives this message, it can return a handle to a large or small icon, or pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="49340-130">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve un identificador para el icono grande o pequeño asociado a la ventana, dependiendo del valor de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="49340-130">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns a handle to the large or small icon associated with the window, depending on the value of *wParam*.</span></span>

<span data-ttu-id="49340-131">Una ventana que no tiene ningún icono establecido explícitamente (con **WM \_ SETICON**) utiliza el icono de la clase de ventana registrada y, en este caso, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devolverá 0 para un mensaje de **\_ GETICON de WM** .</span><span class="sxs-lookup"><span data-stu-id="49340-131">A window that has no icon explicitly set (with **WM\_SETICON**) uses the icon for the registered window class, and in this case [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) will return 0 for a **WM\_GETICON** message.</span></span> <span data-ttu-id="49340-132">Si el envío de un mensaje de **WM \_ GETICON** a una ventana devuelve 0, intente llamar a la función [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) para la ventana.</span><span class="sxs-lookup"><span data-stu-id="49340-132">If sending a **WM\_GETICON** message to a window returns 0, next try calling the [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) function for the window.</span></span> <span data-ttu-id="49340-133">Si devuelve 0, pruebe la función [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) .</span><span class="sxs-lookup"><span data-stu-id="49340-133">If that returns 0 then try the [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="49340-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49340-134">Requirements</span></span>



| <span data-ttu-id="49340-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="49340-135">Requirement</span></span> | <span data-ttu-id="49340-136">Value</span><span class="sxs-lookup"><span data-stu-id="49340-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49340-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49340-137">Minimum supported client</span></span><br/> | <span data-ttu-id="49340-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="49340-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="49340-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49340-139">Minimum supported server</span></span><br/> | <span data-ttu-id="49340-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="49340-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="49340-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49340-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="49340-142"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49340-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49340-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="49340-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="49340-144">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="49340-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="49340-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="49340-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="49340-146">**SETICON de WM \_**</span><span class="sxs-lookup"><span data-stu-id="49340-146">**WM\_SETICON**</span></span>](wm-seticon.md)
</dt> <dt>

<span data-ttu-id="49340-147">**Vista**</span><span class="sxs-lookup"><span data-stu-id="49340-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="49340-148">Windows</span><span class="sxs-lookup"><span data-stu-id="49340-148">Windows</span></span>](windows.md)
</dt> </dl>

 

 
