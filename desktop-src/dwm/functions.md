---
title: Funciones DWM
description: Esta sección contiene información acerca de las funciones de Administrador de ventanas de escritorio (DWM).
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- Administrador de ventanas de escritorio (DWM), referencia
- DWM (Administrador de ventanas de escritorio), referencia
- Administrador de ventanas de escritorio (DWM), funciones
- DWM (Administrador de ventanas de escritorio), funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067f836e7fa8b5b84be02a402a3e0b3d0f78d1c1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104359463"
---
# <a name="dwm-functions"></a><span data-ttu-id="d029a-107">Funciones DWM</span><span class="sxs-lookup"><span data-stu-id="d029a-107">DWM Functions</span></span>

<span data-ttu-id="d029a-108">Esta sección contiene información acerca de las funciones de Administrador de ventanas de escritorio (DWM).</span><span class="sxs-lookup"><span data-stu-id="d029a-108">This section contains information about the Desktop Window Manager (DWM) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d029a-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d029a-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d029a-110">Tema</span><span class="sxs-lookup"><span data-stu-id="d029a-110">Topic</span></span></th>
<th><span data-ttu-id="d029a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d029a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d029a-112"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-112"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-113">Esta función no está implementada.</span><span class="sxs-lookup"><span data-stu-id="d029a-113">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-114"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-114"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-115">Procedimiento de ventana predeterminado para la prueba de posicionamiento de DWM en el área no cliente.</span><span class="sxs-lookup"><span data-stu-id="d029a-115">Default window procedure for DWM hit testing within the non-client area.</span></span><br/> <span data-ttu-id="d029a-116">También debe asegurarse de que se llama a <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> para el mensaje <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d029a-116">You also need to ensure that <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> is called for the <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> message.</span></span> <span data-ttu-id="d029a-117">Si no se llama a <strong>DwmDefWindowProc</strong> para el mensaje <strong>WM_NCMOUSELEAVE</strong> , DWM no quita el resaltado de los botones <strong>maximizar</strong>, <strong>minimizar</strong>y <strong>cerrar</strong> cuando el cursor sale de la ventana.</span><span class="sxs-lookup"><span data-stu-id="d029a-117">If <strong>DwmDefWindowProc</strong> is not called for the <strong>WM_NCMOUSELEAVE</strong> message, DWM does not remove the highlighting from the <strong>Maximize</strong>, <strong>Minimize</strong>, and <strong>Close</strong> buttons when the cursor leaves the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-118"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-118"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-119">Esta función no está implementada.</span><span class="sxs-lookup"><span data-stu-id="d029a-119">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-120"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-120"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-121">Habilita el efecto de desenfoque en una ventana especificada.</span><span class="sxs-lookup"><span data-stu-id="d029a-121">Enables the blur effect on a specified window.</span></span><br/></td><span data-ttu-id="d029a-122">
<b>Nota:</b> A partir de Windows 8, llamar a esta función no produce el efecto de desenfoque debido a un cambio de estilo en la forma en que se representan las ventanas.</span><span class="sxs-lookup"><span data-stu-id="d029a-122">
<b>Note</b> Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.</span></span>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-123"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-123"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-124">Habilita o deshabilita la composición de DWM.</span><span class="sxs-lookup"><span data-stu-id="d029a-124">Enables or disables DWM composition.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d029a-125">Esta función está en desuso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d029a-125">This function is deprecated as of Windows 8.</span></span> <span data-ttu-id="d029a-126">DWM ya no se puede deshabilitar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="d029a-126">DWM can no longer be programmatically disabled.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-127"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-127"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-128">Notifica a DWM que debe participar o no en la programación del servicio de programación de clases multimedia (MMCSS) mientras el proceso de llamada está activo.</span><span class="sxs-lookup"><span data-stu-id="d029a-128">Notifies the DWM to opt in to or out of Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-129"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-129"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-130">Extiende el marco de ventana en el área cliente.</span><span class="sxs-lookup"><span data-stu-id="d029a-130">Extends the window frame into the client area.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-131"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-131"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-132">Emite una llamada de vaciado que bloquea el autor de la llamada hasta el siguiente, cuando se han realizado todas las actualizaciones de la superficie de Microsoft DirectX que están pendientes actualmente.</span><span class="sxs-lookup"><span data-stu-id="d029a-132">Issues a flush call that blocks the caller until the next present, when all of the Microsoft DirectX surface updates that are currently outstanding have been made.</span></span> <span data-ttu-id="d029a-133">Esto compensa las escenas muy complejas o los procesos de llamada con una prioridad muy baja.</span><span class="sxs-lookup"><span data-stu-id="d029a-133">This compensates for very complex scenes or calling processes with very low priority.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-134"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-134"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-135">Recupera el color actual utilizado para la composición de cristal DWM.</span><span class="sxs-lookup"><span data-stu-id="d029a-135">Retrieves the current color used for DWM glass composition.</span></span> <span data-ttu-id="d029a-136">Este valor se basa en la combinación de colores actual y puede ser modificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d029a-136">This value is based on the current color scheme and can be modified by the user.</span></span> <span data-ttu-id="d029a-137">Las aplicaciones pueden escuchar los cambios de color mediante el control de la notificación de <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d029a-137">Applications can listen for color changes by handling the <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-138"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-138"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-139">Recupera la información de tiempo de composición actual para una ventana especificada.</span><span class="sxs-lookup"><span data-stu-id="d029a-139">Retrieves the current composition timing information for a specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-140"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-140"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-141">Esta función no está implementada.</span><span class="sxs-lookup"><span data-stu-id="d029a-141">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-142"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-142"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-143">Esta función no está implementada.</span><span class="sxs-lookup"><span data-stu-id="d029a-143">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-144"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-144"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-145">Recupera los atributos de transporte.</span><span class="sxs-lookup"><span data-stu-id="d029a-145">Retrieves transport attributes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-146"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-146"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a></span></span><br/></td>
<td><blockquote><span data-ttu-id="d029a-147">
<strong>Nota:</strong>  Esta función está disponible públicamente, pero no funcional, para Windows 10, versión 1803.</span><span class="sxs-lookup"><span data-stu-id="d029a-147">
<strong>Note</strong>  This function is publically available, but nonfunctional, for Windows 10, version 1803.</span></span>
</blockquote>
<span data-ttu-id="d029a-148">Comprueba los requisitos necesarios para obtener pestañas en la barra de título de la aplicación para la ventana especificada.</span><span class="sxs-lookup"><span data-stu-id="d029a-148">Checks the requirements needed to get tabs in the application title bar for the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-149"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-149"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-150">Recupera el valor actual de un atributo especificado que se aplica a una ventana.</span><span class="sxs-lookup"><span data-stu-id="d029a-150">Retrieves the current value of a specified attribute applied to a window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-151"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-151"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-152">Una aplicación llama a este método para indicar que se deben actualizar todos los mapas de bits de iconos que se hayan proporcionado previamente desde una ventana, las miniaturas y las representaciones de PEEK.</span><span class="sxs-lookup"><span data-stu-id="d029a-152">Called by an application to indicate that all previously provided iconic bitmaps from a window, both thumbnails and peek representations, should be refreshed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-153"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-153"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-154">Obtiene un valor que indica si la composición DWM está habilitada.</span><span class="sxs-lookup"><span data-stu-id="d029a-154">Obtains a value that indicates whether DWM composition is enabled.</span></span> <span data-ttu-id="d029a-155">Las aplicaciones en equipos que ejecutan Windows 7 o versiones anteriores pueden escuchar los cambios de estado de composición mediante el control de la notificación de <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d029a-155">Applications on machines running Windows 7 or earlier can listen for composition state changes by handling the <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-156"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-156"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-157">Cambia el número de actualizaciones del monitor a través de las cuales se mostrará el fotograma anterior.</span><span class="sxs-lookup"><span data-stu-id="d029a-157">Changes the number of monitor refreshes through which the previous frame will be displayed.</span></span> <br/> <span data-ttu-id="d029a-158"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="d029a-158"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> is no longer supported.</span></span> <span data-ttu-id="d029a-159">A partir de Windows 8.1, las llamadas a <strong>DwmModifyPreviousDxFrameDuration</strong> siempre devuelven E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="d029a-159">Starting with Windows 8.1, calls to <strong>DwmModifyPreviousDxFrameDuration</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-160"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-160"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-161">Recupera el tamaño de origen de la miniatura de DWM.</span><span class="sxs-lookup"><span data-stu-id="d029a-161">Retrieves the source size of the DWM thumbnail.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-162"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-162"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-163">Crea una relación de miniatura de DWM entre las ventanas de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="d029a-163">Creates a DWM thumbnail relationship between the destination and source windows.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-164"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-164"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-165">Notifica a DWM que un contacto táctil se ha reconocido como un gesto y que DWM debe dibujar comentarios para ese gesto.</span><span class="sxs-lookup"><span data-stu-id="d029a-165">Notifies DWM that a touch contact has been recognized as a gesture, and that DWM should draw feedback for that gesture.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-166"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-166"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-167">Establece el número de actualizaciones del monitor a través de las cuales se va a mostrar el marco presentado.</span><span class="sxs-lookup"><span data-stu-id="d029a-167">Sets the number of monitor refreshes through which to display the presented frame.</span></span> <br/> <span data-ttu-id="d029a-168"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="d029a-168"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> is no longer supported.</span></span> <span data-ttu-id="d029a-169">A partir de Windows 8.1, las llamadas a <strong>DwmSetDxFrameDuration</strong> siempre devuelven E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="d029a-169">Starting with Windows 8.1, calls to <strong>DwmSetDxFrameDuration</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-170"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-170"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-171">Establece un mapa de bits estático y de iconos para mostrar una <em>vista previa dinámica</em> (también conocida como <em>vista previa de PEEK</em>) de una ventana o una pestaña. La barra de tareas puede usar este mapa de bits para mostrar una vista previa de tamaño completo de una ventana o una pestaña.</span><span class="sxs-lookup"><span data-stu-id="d029a-171">Sets a static, iconic bitmap to display a <em>live preview</em> (also known as a <em>Peek preview</em>) of a window or tab. The taskbar can use this bitmap to show a full-sized preview of a window or tab.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-172"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-172"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-173">Establece un mapa de bits estático y de iconos en una ventana o pestaña que se va a usar como representación en miniatura.</span><span class="sxs-lookup"><span data-stu-id="d029a-173">Sets a static, iconic bitmap on a window or tab to use as a thumbnail representation.</span></span> <span data-ttu-id="d029a-174">La barra de tareas puede usar este mapa de bits como destino del modificador en miniatura para la ventana o la pestaña.</span><span class="sxs-lookup"><span data-stu-id="d029a-174">The taskbar can use this bitmap as a thumbnail switch target for the window or tab.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-175"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-175"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-176">Establece los parámetros presentes para la composición de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="d029a-176">Sets the present parameters for frame composition.</span></span> <br/> <span data-ttu-id="d029a-177"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="d029a-177"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> is no longer supported.</span></span> <span data-ttu-id="d029a-178">A partir de Windows 8.1, las llamadas a <strong>DwmSetPresentParameters</strong> siempre devuelven E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="d029a-178">Starting with Windows 8.1, calls to <strong>DwmSetPresentParameters</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-179"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-179"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-180">Establece el valor de los atributos de representación que no son de cliente para una ventana.</span><span class="sxs-lookup"><span data-stu-id="d029a-180">Sets the value of non-client rendering attributes for a window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-181"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-181"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-182">Lo llama una aplicación o un marco de trabajo para especificar el tipo de comentarios visuales que se debe dibujar como respuesta a un contacto táctil o de lápiz determinado.</span><span class="sxs-lookup"><span data-stu-id="d029a-182">Called by an app or framework to specify the visual feedback type to draw in response to a particular touch or pen contact.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-183"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-183"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-184">Habilita los comentarios gráficos de las interacciones táctiles y de arrastre para el usuario.</span><span class="sxs-lookup"><span data-stu-id="d029a-184">Enables the graphical feedback of touch and drag interactions to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-185"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-185"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-186">Coordina las animaciones de las ventanas de herramientas con DWM.</span><span class="sxs-lookup"><span data-stu-id="d029a-186">Coordinates the animations of tool windows with the DWM.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d029a-187"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-187"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-188">Quita una relación de miniatura de DWM creada por la función <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d029a-188">Removes a DWM thumbnail relationship created by the <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d029a-189"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="d029a-189"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a></span></span><br/></td>
<td><span data-ttu-id="d029a-190">Actualiza las propiedades de una miniatura de DWM.</span><span class="sxs-lookup"><span data-stu-id="d029a-190">Updates the properties for a DWM thumbnail.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

