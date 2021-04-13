---
title: Mensaje de WM_RENDERALLFORMATS (Winuser. h)
description: Se envía al propietario del portapapeles antes de que se destruya, si el propietario del portapapeles ha retrasado la representación de uno o más formatos del portapapeles.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- Intercambio de datos de mensajes de WM_RENDERALLFORMATS
topic_type:
- apiref
api_name:
- WM_RENDERALLFORMATS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cdd3ce1fabdea4cdcae93b5243b89c53def0afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534941"
---
# <a name="wm_renderallformats-message"></a><span data-ttu-id="190f5-104">Mensaje de RENDERALLFORMATS de WM \_</span><span class="sxs-lookup"><span data-stu-id="190f5-104">WM\_RENDERALLFORMATS message</span></span>

<span data-ttu-id="190f5-105">Se envía al propietario del portapapeles antes de que se destruya, si el propietario del portapapeles ha retrasado la representación de uno o más formatos del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="190f5-105">Sent to the clipboard owner before it is destroyed, if the clipboard owner has delayed rendering one or more clipboard formats.</span></span> <span data-ttu-id="190f5-106">Para que el contenido del portapapeles siga estando disponible para otras aplicaciones, el propietario del portapapeles debe representar los datos en todos los formatos que es capaz de generar y colocar los datos en el portapapeles mediante una llamada a la función [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="190f5-106">For the content of the clipboard to remain available to other applications, the clipboard owner must render data in all the formats it is capable of generating, and place the data on the clipboard by calling the [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) function.</span></span>

<span data-ttu-id="190f5-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="190f5-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a><span data-ttu-id="190f5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="190f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="190f5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="190f5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="190f5-110">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="190f5-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="190f5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="190f5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="190f5-112">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="190f5-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="190f5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="190f5-113">Return value</span></span>

<span data-ttu-id="190f5-114">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="190f5-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="190f5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="190f5-115">Remarks</span></span>

<span data-ttu-id="190f5-116">Cuando se responde a un mensaje de **\_ RENDERALLFORMATS de WM** , la aplicación debe llamar a la función [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) y, a continuación, comprobar que sigue siendo el propietario del portapapeles llamando a la función [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) antes de llamar a [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span><span class="sxs-lookup"><span data-stu-id="190f5-116">When responding to a **WM\_RENDERALLFORMATS** message, the application must call the [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) function and then check that it is still the clipboard owner by calling the [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) function before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span></span>

<span data-ttu-id="190f5-117">La aplicación debe comprobar que todavía es el propietario del portapapeles después de abrir el portapapeles porque, después de recibir el mensaje de **\_ RENDERALLFORMATS de WM** , pero antes de abrir el portapapeles, es posible que otra aplicación haya abierto y tomado la propiedad del portapapeles, y que los datos de esa aplicación no se sobrescriban.</span><span class="sxs-lookup"><span data-stu-id="190f5-117">The application needs to check that it is still the clipboard owner after opening the clipboard because after it receives the **WM\_RENDERALLFORMATS** message, but before it opens the clipboard, another application may have opened and taken ownership of the clipboard, and that application's data should not be overwritten.</span></span>

<span data-ttu-id="190f5-118">En la mayoría de los casos, la aplicación no debe llamar a la función [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) antes de llamar a [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), ya que al hacerlo se borrarán los formatos del portapapeles que la aplicación ya ha representado.</span><span class="sxs-lookup"><span data-stu-id="190f5-118">In most cases, the application should not call the [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) function before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), since doing so will erase the clipboard formats that the application has already rendered.</span></span>

<span data-ttu-id="190f5-119">Cuando se devuelve la aplicación, el sistema quita los formatos no representados de la lista de formatos de Portapapeles disponibles.</span><span class="sxs-lookup"><span data-stu-id="190f5-119">When the application returns, the system removes any unrendered formats from the list of available clipboard formats.</span></span> <span data-ttu-id="190f5-120">Para obtener información sobre la representación diferida, consulte [retardo de representación](clipboard-operations.md#delayed-rendering).</span><span class="sxs-lookup"><span data-stu-id="190f5-120">For information about delayed rendering, see [Delayed Rendering](clipboard-operations.md#delayed-rendering).</span></span>

## <a name="requirements"></a><span data-ttu-id="190f5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="190f5-121">Requirements</span></span>



| <span data-ttu-id="190f5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="190f5-122">Requirement</span></span> | <span data-ttu-id="190f5-123">Value</span><span class="sxs-lookup"><span data-stu-id="190f5-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="190f5-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="190f5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="190f5-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="190f5-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="190f5-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="190f5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="190f5-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="190f5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="190f5-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="190f5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="190f5-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="190f5-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="190f5-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="190f5-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="190f5-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="190f5-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="190f5-132">**EmptyClipboard**</span><span class="sxs-lookup"><span data-stu-id="190f5-132">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[<span data-ttu-id="190f5-133">**OpenClipboard**</span><span class="sxs-lookup"><span data-stu-id="190f5-133">**OpenClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[<span data-ttu-id="190f5-134">**SetClipboardData**</span><span class="sxs-lookup"><span data-stu-id="190f5-134">**SetClipboardData**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[<span data-ttu-id="190f5-135">**RENDERFORMAT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="190f5-135">**WM\_RENDERFORMAT**</span></span>](wm-renderformat.md)
</dt> <dt>

<span data-ttu-id="190f5-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="190f5-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="190f5-137">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="190f5-137">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

