---
title: Identificador DPI_AWARENESS_CONTEXT (WINDEF. h)
description: Identifica el contexto de reconocimiento para una ventana.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359748"
---
# <a name="dpi_awareness_context-handle"></a><span data-ttu-id="ad7c6-103">Identificador de contexto de \_ reconocimiento de PPP \_</span><span class="sxs-lookup"><span data-stu-id="ad7c6-103">DPI\_AWARENESS\_CONTEXT handle</span></span>

<span data-ttu-id="ad7c6-104">Identifica el contexto de reconocimiento para una ventana.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-104">Identifies the awareness context for a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad7c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad7c6-105">Syntax</span></span>

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a><span data-ttu-id="ad7c6-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ad7c6-106">Constants</span></span>

<span data-ttu-id="ad7c6-107">**contexto de reconocimiento de PPP no \_ \_ \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="ad7c6-107">**DPI\_AWARENESS\_CONTEXT\_UNAWARE**</span></span><dl> <span data-ttu-id="ad7c6-108">PPP no compatible.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-108">DPI unaware.</span></span> <span data-ttu-id="ad7c6-109">Esta ventana no escala para los cambios de PPP y siempre se supone que tiene un factor de escala del 100% (96 PPP).</span><span class="sxs-lookup"><span data-stu-id="ad7c6-109">This window does not scale for DPI changes and is always assumed to have a scale factor of 100% (96 DPI).</span></span> <span data-ttu-id="ad7c6-110">El sistema lo escalará automáticamente con cualquier otro valor de PPP.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-110">It will be automatically scaled by the system on any other DPI setting.</span></span>  
</dl>

<span data-ttu-id="ad7c6-111">**conocimiento \_ \_ del sistema de contexto de reconocimiento de \_ PPP \_**</span><span class="sxs-lookup"><span data-stu-id="ad7c6-111">**DPI\_AWARENESS\_CONTEXT\_SYSTEM\_AWARE**</span></span><dl> <span data-ttu-id="ad7c6-112">Reconocimiento de PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-112">System DPI aware.</span></span> <span data-ttu-id="ad7c6-113">Esta ventana no escala para los cambios de PPP.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-113">This window does not scale for DPI changes.</span></span> <span data-ttu-id="ad7c6-114">Consultará el valor de PPP una vez y lo utilizará durante la vigencia del proceso.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-114">It will query for the DPI once and use that value for the lifetime of the process.</span></span> <span data-ttu-id="ad7c6-115">Si cambia el valor de PPP, el proceso no se ajustará al nuevo valor de PPP.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-115">If the DPI changes, the process will not adjust to the new DPI value.</span></span> <span data-ttu-id="ad7c6-116">El sistema se escala o reduce verticalmente de forma automática cuando cambia el valor de PPP del valor del sistema.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-116">It will be automatically scaled up or down by the system when the DPI changes from the system value.</span></span>  
</dl>

<span data-ttu-id="ad7c6-117">**contexto de reconocimiento de PPP \_ \_ \_ por \_ monitor \_**</span><span class="sxs-lookup"><span data-stu-id="ad7c6-117">**DPI\_AWARENESS\_CONTEXT\_PER\_MONITOR\_AWARE**</span></span><dl> <span data-ttu-id="ad7c6-118">Con reconocimiento de PPP por monitor.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-118">Per monitor DPI aware.</span></span> <span data-ttu-id="ad7c6-119">Esta ventana comprueba el PPP cuando se crea y ajusta el factor de escala cada vez que cambia el PPP.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-119">This window checks for the DPI when it is created and adjusts the scale factor whenever the DPI changes.</span></span> <span data-ttu-id="ad7c6-120">El sistema no escala automáticamente estos procesos.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-120">These processes are not automatically scaled by the system.</span></span>  
</dl>

<span data-ttu-id="ad7c6-121">**Contexto de reconocimiento de PPP \_ \_ \_ por \_ monitor \_ compatible con \_ V2**</span><span class="sxs-lookup"><span data-stu-id="ad7c6-121">**DPI\_AWARENESS\_CONTEXT\_PER\_MONITOR\_AWARE\_V2**</span></span><dl> <span data-ttu-id="ad7c6-122">También se conoce como **por monitor V2**.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-122">Also known as **Per Monitor v2**.</span></span> <span data-ttu-id="ad7c6-123">Un avance sobre el modo de reconocimiento de PPP por monitor original, que permite a las aplicaciones tener acceso a nuevos comportamientos de escalado relacionados con los PPP en cada ventana de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-123">An advancement over the original per-monitor DPI awareness mode, which enables applications to access new DPI-related scaling behaviors on a per top-level window basis.</span></span>  
<span data-ttu-id="ad7c6-124">Por monitor V2 estaba disponible en la actualización de Creators de Windows 10 y no está disponible en versiones anteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-124">Per Monitor v2 was made available in the Creators Update of Windows 10, and is not available on earlier versions of the operating system.</span></span>  
<span data-ttu-id="ad7c6-125">Los comportamientos adicionales introducidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ad7c6-125">The additional behaviors introduced are as follows:</span></span>

-   <span data-ttu-id="ad7c6-126">**Notificaciones de cambio de PPP de ventana secundaria** : en los contextos de cada monitor V2, se notifica a todo el árbol de la ventana todos los cambios de PPP que se produzcan.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-126">**Child window DPI change notifications** - In Per Monitor v2 contexts, the entire window tree is notified of any DPI changes that occur.</span></span>
-   <span data-ttu-id="ad7c6-127">**Escalado de área no cliente** : todas las ventanas tendrán automáticamente el área no cliente dibujada con distinción de PPP.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-127">**Scaling of non-client area** - All windows will automatically have their non-client area drawn in a DPI sensitive fashion.</span></span> <span data-ttu-id="ad7c6-128">No es necesario realizar llamadas a [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) .</span><span class="sxs-lookup"><span data-stu-id="ad7c6-128">Calls to [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) are unnecessary.</span></span>
-   <span data-ttu-id="ad7c6-129">**Escalado de menús de Win32** : todos los menús de Ntuser creados en los contextos de por monitor V2 se escalarán en un modo por monitor.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-129">**Scaling of Win32 menus** - All NTUSER menus created in Per Monitor v2 contexts will be scaling in a per-monitor fashion.</span></span>
-   <span data-ttu-id="ad7c6-130">**Escalado de cuadros de diálogo** : los cuadros de diálogo de Win32 creados en los contextos de por monitor V2 responderán automáticamente a los cambios de PPP.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-130">**Dialog Scaling** - Win32 dialogs created in Per Monitor v2 contexts will automatically respond to DPI changes.</span></span>
-   <span data-ttu-id="ad7c6-131">**Escalado mejorado de los controles comctl32** : varios controles comctl32 tienen un comportamiento de escalado de PPP mejorado en contextos de por monitor V2.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-131">**Improved scaling of comctl32 controls** - Various comctl32 controls have improved DPI scaling behavior in Per Monitor v2 contexts.</span></span>
-   <span data-ttu-id="ad7c6-132">**Comportamiento mejorado** : los identificadores de uxtheme abiertos en el contexto de una ventana por monitor V2 funcionarán en función de los PPP asociados a esa ventana.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-132">**Improved theming behavior** - UxTheme handles opened in the context of a Per Monitor v2 window will operate in terms of the DPI associated with that window.</span></span>

  
</dl>

<span data-ttu-id="ad7c6-133">**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**</span><span class="sxs-lookup"><span data-stu-id="ad7c6-133">**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**</span></span>

<span data-ttu-id="ad7c6-134">DPI no es consciente de la mejora de la calidad del contenido basado en GDI.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-134">DPI unaware with improved quality of GDI-based content.</span></span> <span data-ttu-id="ad7c6-135">Este modo se comporta de forma similar a DPI_AWARENESS_CONTEXT_UNAWARE, pero también permite al sistema mejorar automáticamente la calidad de representación de texto y otras primitivas basadas en GDI cuando la ventana se muestra en un monitor de alta ppp.</span><span class="sxs-lookup"><span data-stu-id="ad7c6-135">This mode behaves similarly to DPI_AWARENESS_CONTEXT_UNAWARE, but also enables the system to automatically improve the rendering quality of text and other GDI-based primitives when the window is displayed on a high-DPI monitor.</span></span>

<span data-ttu-id="ad7c6-136">Para obtener más información, consulte [mejorar la experiencia de PPP alta en aplicaciones de escritorio basadas en GDI](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).</span><span class="sxs-lookup"><span data-stu-id="ad7c6-136">For more details, see [Improving the high-DPI experience in GDI-based Desktop apps](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).</span></span>

<span data-ttu-id="ad7c6-137">DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED se presentó en la actualización de octubre de 2018 de Windows 10 (también conocida como versión 1809).</span><span class="sxs-lookup"><span data-stu-id="ad7c6-137">DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED was introduced in the October 2018 update of Windows 10 (also known as version 1809).</span></span>


## <a name="requirements"></a><span data-ttu-id="ad7c6-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad7c6-138">Requirements</span></span>

| <span data-ttu-id="ad7c6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad7c6-139">Requirement</span></span> | <span data-ttu-id="ad7c6-140">Value</span><span class="sxs-lookup"><span data-stu-id="ad7c6-140">Value</span></span> |
|----|-----------|
| <span data-ttu-id="ad7c6-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad7c6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ad7c6-142">Solo aplicaciones de escritorio de Windows 10, versión 1607 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad7c6-142">Windows 10, version 1607 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ad7c6-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad7c6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ad7c6-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ad7c6-144">None supported</span></span> <br/>  |
| <span data-ttu-id="ad7c6-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad7c6-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad7c6-146"><dt>WINDEF. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad7c6-146"><dt>windef.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="ad7c6-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad7c6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad7c6-148">**AreDpiAwarenessContextsEqual**</span><span class="sxs-lookup"><span data-stu-id="ad7c6-148">**AreDpiAwarenessContextsEqual**</span></span>](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[<span data-ttu-id="ad7c6-149">**GetAwarenessFromDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="ad7c6-149">**GetAwarenessFromDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="ad7c6-150">**GetDpiFromDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="ad7c6-150">**GetDpiFromDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="ad7c6-151">**GetThreadDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="ad7c6-151">**GetThreadDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="ad7c6-152">**GetWindowDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="ad7c6-152">**GetWindowDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="ad7c6-153">**IsValidDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="ad7c6-153">**IsValidDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="ad7c6-154">**SetProcessDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="ad7c6-154">**SetProcessDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="ad7c6-155">**SetThreadDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="ad7c6-155">**SetThreadDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
