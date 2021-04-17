---
description: Se envía a una ventana cuando se debe cambiar su área no cliente para indicar un estado activo o inactivo.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: Mensaje de WM_NCACTIVATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23cc5e0495d6679efea805eab80290b209906d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677917"
---
# <a name="wm_ncactivate-message"></a><span data-ttu-id="2e95b-103">Mensaje de NCACTIVATE de WM \_</span><span class="sxs-lookup"><span data-stu-id="2e95b-103">WM\_NCACTIVATE message</span></span>

<span data-ttu-id="2e95b-104">Se envía a una ventana cuando se debe cambiar su área no cliente para indicar un estado activo o inactivo.</span><span class="sxs-lookup"><span data-stu-id="2e95b-104">Sent to a window when its nonclient area needs to be changed to indicate an active or inactive state.</span></span>

<span data-ttu-id="2e95b-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2e95b-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a><span data-ttu-id="2e95b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e95b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e95b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e95b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e95b-108">Indica cuándo es necesario cambiar una barra de título o un icono para indicar un estado activo o inactivo.</span><span class="sxs-lookup"><span data-stu-id="2e95b-108">Indicates when a title bar or icon needs to be changed to indicate an active or inactive state.</span></span> <span data-ttu-id="2e95b-109">Si se va a dibujar una barra de título o un icono activo, el parámetro *wParam* es **true**.</span><span class="sxs-lookup"><span data-stu-id="2e95b-109">If an active title bar or icon is to be drawn, the *wParam* parameter is **TRUE**.</span></span> <span data-ttu-id="2e95b-110">Si se va a dibujar una barra de título o un icono inactivo, *wParam* es **false**.</span><span class="sxs-lookup"><span data-stu-id="2e95b-110">If an inactive title bar or icon is to be drawn, *wParam* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="2e95b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e95b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e95b-112">Cuando hay un [estilo visual](../controls/themes-overview.md) activo para esta ventana, no se utiliza este parámetro.</span><span class="sxs-lookup"><span data-stu-id="2e95b-112">When a [visual style](../controls/themes-overview.md) is active for this window, this parameter is not used.</span></span>

<span data-ttu-id="2e95b-113">Cuando no hay ningún estilo visual activo para esta ventana, este parámetro es un identificador de una región de actualización opcional para el área no cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="2e95b-113">When a visual style is not active for this window, this parameter is a handle to an optional update region for the nonclient area of the window.</span></span> <span data-ttu-id="2e95b-114">Si este parámetro se establece en-1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) no vuelve a dibujar el área no cliente para reflejar el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="2e95b-114">If this parameter is set to -1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) does not repaint the nonclient area to reflect the state change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e95b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e95b-115">Return value</span></span>

<span data-ttu-id="2e95b-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="2e95b-116">Type: **LRESULT**</span></span>

<span data-ttu-id="2e95b-117">Cuando el parámetro *wParam* es **false**, una aplicación debe devolver **true** para indicar que el sistema debe continuar con el procesamiento predeterminado, o bien debe devolver **false** para evitar el cambio.</span><span class="sxs-lookup"><span data-stu-id="2e95b-117">When the *wParam* parameter is **FALSE**, an application should return **TRUE** to indicate that the system should proceed with the default processing, or it should return **FALSE** to prevent the change.</span></span> <span data-ttu-id="2e95b-118">Cuando *wParam* es **true**, se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="2e95b-118">When *wParam* is **TRUE**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e95b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e95b-119">Remarks</span></span>

<span data-ttu-id="2e95b-120">No se recomienda el procesamiento de mensajes relacionados con el área no cliente de una ventana estándar, ya que la aplicación debe ser capaz de dibujar todas las partes necesarias del área no cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="2e95b-120">Processing messages related to the nonclient area of a standard window is not recommended, because the application must be able to draw all the required parts of the nonclient area for the window.</span></span> <span data-ttu-id="2e95b-121">Si una aplicación procesa este mensaje, debe devolver **true** para indicar al sistema que complete el cambio de la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="2e95b-121">If an application does process this message, it must return **TRUE** to direct the system to complete the change of active window.</span></span> <span data-ttu-id="2e95b-122">Si se minimiza la ventana cuando se recibe este mensaje, la aplicación debe pasar el mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="2e95b-122">If the window is minimized when this message is received, the application should pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="2e95b-123">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dibuja el título de la barra de título o el icono en sus colores activos cuando el parámetro *wParam* es **true** y en sus colores inactivos cuando *wParam* es **false**.</span><span class="sxs-lookup"><span data-stu-id="2e95b-123">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function draws the title bar or icon title in its active colors when the *wParam* parameter is **TRUE** and in its inactive colors when *wParam* is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e95b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e95b-124">Requirements</span></span>



| <span data-ttu-id="2e95b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e95b-125">Requirement</span></span> | <span data-ttu-id="2e95b-126">Value</span><span class="sxs-lookup"><span data-stu-id="2e95b-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e95b-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e95b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2e95b-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2e95b-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2e95b-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e95b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2e95b-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e95b-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2e95b-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e95b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e95b-132"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e95b-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e95b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e95b-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="2e95b-134">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2e95b-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2e95b-135">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="2e95b-135">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="2e95b-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="2e95b-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2e95b-137">Windows</span><span class="sxs-lookup"><span data-stu-id="2e95b-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
