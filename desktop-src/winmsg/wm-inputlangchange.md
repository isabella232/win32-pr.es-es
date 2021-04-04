---
description: Se envía a la ventana de nivel superior afectada después de cambiar el idioma de entrada de una aplicación. Debe establecer cualquier configuración específica de la aplicación y pasar el mensaje a la función DefWindowProc, que pasa el mensaje a todas las ventanas secundarias de primer nivel.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Mensaje de WM_INPUTLANGCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0cdf04a775873e4cefe2c79269c14bd3d4da8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154168"
---
# <a name="wm_inputlangchange-message"></a><span data-ttu-id="97e6d-104">Mensaje de INPUTLANGCHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="97e6d-104">WM\_INPUTLANGCHANGE message</span></span>

<span data-ttu-id="97e6d-105">Se envía a la ventana de nivel superior afectada después de cambiar el idioma de entrada de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="97e6d-105">Sent to the topmost affected window after an application's input language has been changed.</span></span> <span data-ttu-id="97e6d-106">Debe establecer cualquier configuración específica de la aplicación y pasar el mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , que pasa el mensaje a todas las ventanas secundarias de primer nivel.</span><span class="sxs-lookup"><span data-stu-id="97e6d-106">You should make any application-specific settings and pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which passes the message to all first-level child windows.</span></span> <span data-ttu-id="97e6d-107">Estas ventanas secundarias pueden pasar el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para que pase el mensaje a sus ventanas secundarias, etc.</span><span class="sxs-lookup"><span data-stu-id="97e6d-107">These child windows can pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to have it pass the message to their child windows, and so on.</span></span>

<span data-ttu-id="97e6d-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="97e6d-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INPUTLANGCHANGE              0x0051
```



## <a name="parameters"></a><span data-ttu-id="97e6d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97e6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97e6d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97e6d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97e6d-111">Juego de caracteres de la nueva configuración regional.</span><span class="sxs-lookup"><span data-stu-id="97e6d-111">The character set of the new locale.</span></span>

</dd> <dt>

<span data-ttu-id="97e6d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97e6d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97e6d-113">Identificador de configuración regional de entrada.</span><span class="sxs-lookup"><span data-stu-id="97e6d-113">The input locale identifier.</span></span> <span data-ttu-id="97e6d-114">Para obtener más información, consulte [idiomas, configuraciones regionales y distribuciones del teclado](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="97e6d-114">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97e6d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97e6d-115">Return value</span></span>

<span data-ttu-id="97e6d-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="97e6d-116">Type: **LRESULT**</span></span>

<span data-ttu-id="97e6d-117">Una aplicación debe devolver un valor distinto de cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="97e6d-117">An application should return nonzero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="97e6d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97e6d-118">Requirements</span></span>



| <span data-ttu-id="97e6d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="97e6d-119">Requirement</span></span> | <span data-ttu-id="97e6d-120">Value</span><span class="sxs-lookup"><span data-stu-id="97e6d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97e6d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97e6d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="97e6d-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="97e6d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="97e6d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97e6d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="97e6d-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="97e6d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="97e6d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97e6d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="97e6d-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97e6d-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97e6d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="97e6d-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="97e6d-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="97e6d-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="97e6d-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="97e6d-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="97e6d-130">**INPUTLANGCHANGEREQUEST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="97e6d-130">**WM\_INPUTLANGCHANGEREQUEST**</span></span>](wm-inputlangchangerequest.md)
</dt> <dt>

<span data-ttu-id="97e6d-131">**Vista**</span><span class="sxs-lookup"><span data-stu-id="97e6d-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="97e6d-132">Windows</span><span class="sxs-lookup"><span data-stu-id="97e6d-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
