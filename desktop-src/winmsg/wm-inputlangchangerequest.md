---
description: Se envía a la ventana con el foco cuando el usuario elige un nuevo idioma de entrada, ya sea con la tecla de rápida (especificada en la aplicación del panel de control del teclado) o desde el indicador en la barra de tareas del sistema.
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: Mensaje de WM_INPUTLANGCHANGEREQUEST (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df361c479978083c29281764e65c48b131c22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697164"
---
# <a name="wm_inputlangchangerequest-message"></a><span data-ttu-id="03554-103">Mensaje de INPUTLANGCHANGEREQUEST de WM \_</span><span class="sxs-lookup"><span data-stu-id="03554-103">WM\_INPUTLANGCHANGEREQUEST message</span></span>

<span data-ttu-id="03554-104">Se envía a la ventana con el foco cuando el usuario elige un nuevo idioma de entrada, ya sea con la tecla de rápida (especificada en la aplicación del panel de control del teclado) o desde el indicador en la barra de tareas del sistema.</span><span class="sxs-lookup"><span data-stu-id="03554-104">Posted to the window with the focus when the user chooses a new input language, either with the hotkey (specified in the Keyboard control panel application) or from the indicator on the system taskbar.</span></span> <span data-ttu-id="03554-105">Una aplicación puede aceptar el cambio pasando el mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o rechazar el cambio (e impedir que tenga lugar) devolviendo inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="03554-105">An application can accept the change by passing the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function or reject the change (and prevent it from taking place) by returning immediately.</span></span>

<span data-ttu-id="03554-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="03554-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a><span data-ttu-id="03554-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03554-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03554-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03554-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03554-109">La nueva configuración regional de entrada.</span><span class="sxs-lookup"><span data-stu-id="03554-109">The new input locale.</span></span> <span data-ttu-id="03554-110">Este parámetro puede ser una combinación de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="03554-110">This parameter can be a combination of the following flags.</span></span>



| <span data-ttu-id="03554-111">Value</span><span class="sxs-lookup"><span data-stu-id="03554-111">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="03554-112">Significado</span><span class="sxs-lookup"><span data-stu-id="03554-112">Meaning</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <span data-ttu-id="03554-113"><dt>**INPUTLANGCHANGE \_**</dt> <dt>0x0004</dt> atrás</span><span class="sxs-lookup"><span data-stu-id="03554-113"><dt>**INPUTLANGCHANGE\_BACKWARD**</dt> <dt>0x0004</dt></span></span> </dl>       | <span data-ttu-id="03554-114">Se usó una tecla de acceso rápido para elegir la configuración regional de entrada anterior en la lista instalada de configuraciones regionales de entrada.</span><span class="sxs-lookup"><span data-stu-id="03554-114">A hot key was used to choose the previous input locale in the installed list of input locales.</span></span> <span data-ttu-id="03554-115">Esta marca no se puede usar con la \_ marca de avance de INPUTLANGCHANGE.</span><span class="sxs-lookup"><span data-stu-id="03554-115">This flag cannot be used with the INPUTLANGCHANGE\_FORWARD flag.</span></span><br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <span data-ttu-id="03554-116"><dt>**INPUTLANGCHANGE \_ Reenvío**</dt> de <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="03554-116"><dt>**INPUTLANGCHANGE\_FORWARD**</dt> <dt>0x0002</dt></span></span> </dl>          | <span data-ttu-id="03554-117">Se usó una tecla de acceso rápido para elegir la configuración regional de entrada siguiente en la lista instalada de configuraciones regionales de entrada.</span><span class="sxs-lookup"><span data-stu-id="03554-117">A hot key was used to choose the next input locale in the installed list of input locales.</span></span> <span data-ttu-id="03554-118">Esta marca no se puede usar con la \_ marca atrás de INPUTLANGCHANGE.</span><span class="sxs-lookup"><span data-stu-id="03554-118">This flag cannot be used with the INPUTLANGCHANGE\_BACKWARD flag.</span></span><br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <span data-ttu-id="03554-119"><dt>**INPUTLANGCHANGE \_ SYSCHARSET**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="03554-119"><dt>**INPUTLANGCHANGE\_SYSCHARSET**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="03554-120">La nueva distribución del teclado de la configuración regional de entrada se puede usar con el juego de caracteres del sistema.</span><span class="sxs-lookup"><span data-stu-id="03554-120">The new input locale's keyboard layout can be used with the system character set.</span></span><br/>                                                                               |



 

</dd> <dt>

<span data-ttu-id="03554-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03554-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03554-122">Identificador de configuración regional de entrada.</span><span class="sxs-lookup"><span data-stu-id="03554-122">The input locale identifier.</span></span> <span data-ttu-id="03554-123">Para obtener más información, consulte [idiomas, configuraciones regionales y distribuciones del teclado](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="03554-123">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03554-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03554-124">Return value</span></span>

<span data-ttu-id="03554-125">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="03554-125">Type: **LRESULT**</span></span>

<span data-ttu-id="03554-126">Este mensaje se publica, no se envía a la aplicación, por lo que se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="03554-126">This message is posted, not sent, to the application, so the return value is ignored.</span></span> <span data-ttu-id="03554-127">Para aceptar el cambio, la aplicación debe pasar el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="03554-127">To accept the change, the application should pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="03554-128">Para rechazar el cambio, la aplicación debe devolver cero sin llamar a **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="03554-128">To reject the change, the application should return zero without calling **DefWindowProc**.</span></span>

## <a name="remarks"></a><span data-ttu-id="03554-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03554-129">Remarks</span></span>

<span data-ttu-id="03554-130">Cuando la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) recibe el mensaje de **\_ INPUTLANGCHANGEREQUEST de WM** , activa la nueva configuración regional de entrada y notifica a la aplicación el cambio mediante el envío del mensaje de [**\_ INPUTLANGCHANGE de WM**](wm-inputlangchange.md) .</span><span class="sxs-lookup"><span data-stu-id="03554-130">When the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function receives the **WM\_INPUTLANGCHANGEREQUEST** message, it activates the new input locale and notifies the application of the change by sending the [**WM\_INPUTLANGCHANGE**](wm-inputlangchange.md) message.</span></span>

<span data-ttu-id="03554-131">El indicador de idioma solo está presente en la barra de tareas si se ha instalado más de una distribución de teclado y se ha habilitado el indicador mediante la aplicación del panel de control del teclado.</span><span class="sxs-lookup"><span data-stu-id="03554-131">The language indicator is present on the taskbar only if you have installed more than one keyboard layout and if you have enabled the indicator using the Keyboard control panel application.</span></span>

## <a name="requirements"></a><span data-ttu-id="03554-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03554-132">Requirements</span></span>



| <span data-ttu-id="03554-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="03554-133">Requirement</span></span> | <span data-ttu-id="03554-134">Value</span><span class="sxs-lookup"><span data-stu-id="03554-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03554-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03554-135">Minimum supported client</span></span><br/> | <span data-ttu-id="03554-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="03554-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="03554-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03554-137">Minimum supported server</span></span><br/> | <span data-ttu-id="03554-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="03554-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="03554-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03554-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="03554-140"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03554-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03554-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="03554-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="03554-142">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="03554-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="03554-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="03554-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="03554-144">**INPUTLANGCHANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="03554-144">**WM\_INPUTLANGCHANGE**</span></span>](wm-inputlangchange.md)
</dt> <dt>

<span data-ttu-id="03554-145">**Vista**</span><span class="sxs-lookup"><span data-stu-id="03554-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="03554-146">Windows</span><span class="sxs-lookup"><span data-stu-id="03554-146">Windows</span></span>](windows.md)
</dt> </dl>

 

 
