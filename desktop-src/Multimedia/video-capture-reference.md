---
title: Referencia de captura de vídeo
description: Referencia de captura de vídeo
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- Vídeo para Windows (VFW), referencia de captura de vídeo
- VFW (vídeo para Windows), referencia de captura de vídeo
- AVICap, referencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef19834e244f6070a1d8bb3383dcac017e4d161
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075320"
---
# <a name="video-capture-reference"></a><span data-ttu-id="61c65-106">Referencia de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="61c65-106">Video Capture Reference</span></span>

<span data-ttu-id="61c65-107">En esta sección se describen las funciones, las estructuras, los mensajes y las macros asociadas a la clase de ventana AVICap.</span><span class="sxs-lookup"><span data-stu-id="61c65-107">This section describes the functions, structures, messages, and macros associated with the AVICap window class.</span></span> <span data-ttu-id="61c65-108">Estos elementos se agrupan de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="61c65-108">These elements are grouped as follows.</span></span>

## <a name="basic-capture-operations"></a><span data-ttu-id="61c65-109">Operaciones de captura básicas</span><span class="sxs-lookup"><span data-stu-id="61c65-109">Basic Capture Operations</span></span>

-   [<span data-ttu-id="61c65-110">**capCreateCaptureWindow**</span><span class="sxs-lookup"><span data-stu-id="61c65-110">**capCreateCaptureWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [<span data-ttu-id="61c65-111">**\_anulación de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-111">**WM\_CAP\_ABORT**</span></span>](wm-cap-abort.md)
-   [<span data-ttu-id="61c65-112">**\_conexión del \_ controlador \_ Cap de WM**</span><span class="sxs-lookup"><span data-stu-id="61c65-112">**WM\_CAP\_DRIVER\_CONNECT**</span></span>](wm-cap-driver-connect.md)
-   [<span data-ttu-id="61c65-113">**\_secuencia de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-113">**WM\_CAP\_SEQUENCE**</span></span>](wm-cap-sequence.md)
-   [<span data-ttu-id="61c65-114">**\_detención de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-114">**WM\_CAP\_STOP**</span></span>](wm-cap-stop.md)

## <a name="capture-windows"></a><span data-ttu-id="61c65-115">Capturar ventanas</span><span class="sxs-lookup"><span data-stu-id="61c65-115">Capture Windows</span></span>

-   [<span data-ttu-id="61c65-116">**CAPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="61c65-116">**CAPSTATUS**</span></span>](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [<span data-ttu-id="61c65-117">**capGetDriverDescription**</span><span class="sxs-lookup"><span data-stu-id="61c65-117">**capGetDriverDescription**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [<span data-ttu-id="61c65-118">**\_conexión del \_ controlador \_ Cap de WM**</span><span class="sxs-lookup"><span data-stu-id="61c65-118">**WM\_CAP\_DRIVER\_CONNECT**</span></span>](wm-cap-driver-connect.md)
-   [<span data-ttu-id="61c65-119">**desconexión del \_ controlador Cap de WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-119">**WM\_CAP\_DRIVER\_DISCONNECT**</span></span>](wm-cap-driver-disconnect.md)
-   [<span data-ttu-id="61c65-120">**\_Estado de \_ obtención de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-120">**WM\_CAP\_GET\_STATUS**</span></span>](wm-cap-get-status.md)

## <a name="capture-drivers"></a><span data-ttu-id="61c65-121">Controladores de captura</span><span class="sxs-lookup"><span data-stu-id="61c65-121">Capture Drivers</span></span>

-   [<span data-ttu-id="61c65-122">**CAPDRIVERCAPS**</span><span class="sxs-lookup"><span data-stu-id="61c65-122">**CAPDRIVERCAPS**</span></span>](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [<span data-ttu-id="61c65-123">**los Cap del \_ controlador Cap de WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-123">**WM\_CAP\_DRIVER\_GET\_CAPS**</span></span>](wm-cap-driver-get-caps.md)
-   [<span data-ttu-id="61c65-124">**\_ \_ \_ obtener nombre de controlador de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-124">**WM\_CAP\_DRIVER\_GET\_NAME**</span></span>](wm-cap-driver-get-name.md)
-   [<span data-ttu-id="61c65-125">**\_ \_ versión get del controlador Cap \_ de \_ WM**</span><span class="sxs-lookup"><span data-stu-id="61c65-125">**WM\_CAP\_DRIVER\_GET\_VERSION**</span></span>](wm-cap-driver-get-version.md)
-   [<span data-ttu-id="61c65-126">**\_límite de \_ \_ AUDIOFORMAT de Cap de WM**</span><span class="sxs-lookup"><span data-stu-id="61c65-126">**WM\_CAP\_GET\_AUDIOFORMAT**</span></span>](wm-cap-get-audioformat.md)
-   [<span data-ttu-id="61c65-127">**\_obtención de \_ \_ formato de Cap de WM**</span><span class="sxs-lookup"><span data-stu-id="61c65-127">**WM\_CAP\_GET\_VIDEOFORMAT**</span></span>](wm-cap-get-videoformat.md)
-   [<span data-ttu-id="61c65-128">**\_AUDIOFORMAT del \_ conjunto de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-128">**WM\_CAP\_SET\_AUDIOFORMAT**</span></span>](wm-cap-set-audioformat.md)
-   [<span data-ttu-id="61c65-129">**videojuego de límite de WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-129">**WM\_CAP\_SET\_VIDEOFORMAT**</span></span>](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a><span data-ttu-id="61c65-130">Vista previa del controlador de captura y modos de superposición</span><span class="sxs-lookup"><span data-stu-id="61c65-130">Capture Driver Preview and Overlay Modes</span></span>

-   [<span data-ttu-id="61c65-131">**superposición de conjunto de Cap de WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-131">**WM\_CAP\_SET\_OVERLAY**</span></span>](wm-cap-set-overlay.md)
-   [<span data-ttu-id="61c65-132">**\_ \_ vista previa del conjunto de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-132">**WM\_CAP\_SET\_PREVIEW**</span></span>](wm-cap-set-preview.md)
-   [<span data-ttu-id="61c65-133">**\_PREVIEWRATE del \_ conjunto de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-133">**WM\_CAP\_SET\_PREVIEWRATE**</span></span>](wm-cap-set-previewrate.md)
-   [<span data-ttu-id="61c65-134">**\_escala del \_ conjunto de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-134">**WM\_CAP\_SET\_SCALE**</span></span>](wm-cap-set-scale.md)
-   [<span data-ttu-id="61c65-135">**\_desplazamiento de \_ conjunto de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-135">**WM\_CAP\_SET\_SCROLL**</span></span>](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a><span data-ttu-id="61c65-136">Cuadros de diálogo de vídeo de controlador de captura</span><span class="sxs-lookup"><span data-stu-id="61c65-136">Capture Driver Video Dialog Boxes</span></span>

-   [<span data-ttu-id="61c65-137">**videocompresión de Cap de WM \_ \_ Dlg \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-137">**WM\_CAP\_DLG\_VIDEOCOMPRESSION**</span></span>](wm-cap-dlg-videocompression.md)
-   [<span data-ttu-id="61c65-138">**\_vídeo de \_ \_ presentación de Cap de WM**</span><span class="sxs-lookup"><span data-stu-id="61c65-138">**WM\_CAP\_DLG\_VIDEODISPLAY**</span></span>](wm-cap-dlg-videodisplay.md)
-   [<span data-ttu-id="61c65-139">**videoformateador de Cap de WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-139">**WM\_CAP\_DLG\_VIDEOFORMAT**</span></span>](wm-cap-dlg-videoformat.md)
-   [<span data-ttu-id="61c65-140">**videosource de Cap de WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-140">**WM\_CAP\_DLG\_VIDEOSOURCE**</span></span>](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a><span data-ttu-id="61c65-141">Formato de audio</span><span class="sxs-lookup"><span data-stu-id="61c65-141">Audio Format</span></span>

-   [<span data-ttu-id="61c65-142">**\_límite de \_ \_ AUDIOFORMAT de Cap de WM**</span><span class="sxs-lookup"><span data-stu-id="61c65-142">**WM\_CAP\_GET\_AUDIOFORMAT**</span></span>](wm-cap-get-audioformat.md)
-   [<span data-ttu-id="61c65-143">**\_AUDIOFORMAT del \_ conjunto de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-143">**WM\_CAP\_SET\_AUDIOFORMAT**</span></span>](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a><span data-ttu-id="61c65-144">Configuración de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="61c65-144">Video Capture Settings</span></span>

-   [<span data-ttu-id="61c65-145">**CAPTUREPARMS**</span><span class="sxs-lookup"><span data-stu-id="61c65-145">**CAPTUREPARMS**</span></span>](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [<span data-ttu-id="61c65-146">**\_configuración de \_ secuencia de obtención de Cap de WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-146">**WM\_CAP\_GET\_SEQUENCE\_SETUP**</span></span>](wm-cap-get-sequence-setup.md)
-   [<span data-ttu-id="61c65-147">**configuración de la secuencia de conjuntos de \_ Cap de WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-147">**WM\_CAP\_SET\_SEQUENCE\_SETUP**</span></span>](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a><span data-ttu-id="61c65-148">Capturar archivos y búferes</span><span class="sxs-lookup"><span data-stu-id="61c65-148">Capture File and Buffers</span></span>

-   [<span data-ttu-id="61c65-149">**CAPTUREPARMS**</span><span class="sxs-lookup"><span data-stu-id="61c65-149">**CAPTUREPARMS**</span></span>](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [<span data-ttu-id="61c65-150">**\_asignación de \_ archivo \_ Cap de WM**</span><span class="sxs-lookup"><span data-stu-id="61c65-150">**WM\_CAP\_FILE\_ALLOCATE**</span></span>](wm-cap-file-allocate.md)
-   [<span data-ttu-id="61c65-151">**\_archivo Cap de la obtención de archivo Cap de WM \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-151">**WM\_CAP\_FILE\_GET\_CAPTURE\_FILE**</span></span>](wm-cap-file-get-capture-file.md)
-   [<span data-ttu-id="61c65-152">**\_ \_ Guardar archivo Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-152">**WM\_CAP\_FILE\_SAVEAS**</span></span>](wm-cap-file-saveas.md)
-   [<span data-ttu-id="61c65-153">**\_archivo de \_ captura de conjunto de archivos de Cap de \_ \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-153">**WM\_CAP\_FILE\_SET\_CAPTURE\_FILE**</span></span>](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a><span data-ttu-id="61c65-154">Uso directo de datos de captura</span><span class="sxs-lookup"><span data-stu-id="61c65-154">Directly Using Capture Data</span></span>

-   [<span data-ttu-id="61c65-155">**\_archivo de \_ secuencia de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-155">**WM\_CAP\_SEQUENCE\_NOFILE**</span></span>](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a><span data-ttu-id="61c65-156">Captura del dispositivo MCI</span><span class="sxs-lookup"><span data-stu-id="61c65-156">Capture from MCI Device</span></span>

-   [<span data-ttu-id="61c65-157">**\_ \_ dispositivo MCI de conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-157">**WM\_CAP\_SET\_MCI\_DEVICE**</span></span>](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a><span data-ttu-id="61c65-158">Captura de fotogramas manual</span><span class="sxs-lookup"><span data-stu-id="61c65-158">Manual Frame Capture</span></span>

-   [<span data-ttu-id="61c65-159">**\_ \_ marco único de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-159">**WM\_CAP\_SINGLE\_FRAME**</span></span>](wm-cap-single-frame.md)
-   [<span data-ttu-id="61c65-160">**\_cierre de \_ \_ fotograma único de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-160">**WM\_CAP\_SINGLE\_FRAME\_CLOSE**</span></span>](wm-cap-single-frame-close.md)
-   [<span data-ttu-id="61c65-161">**\_marco único de Cap de WM \_ \_ \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="61c65-161">**WM\_CAP\_SINGLE\_FRAME\_OPEN**</span></span>](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a><span data-ttu-id="61c65-162">Still-Image captura</span><span class="sxs-lookup"><span data-stu-id="61c65-162">Still-Image Capture</span></span>

-   [<span data-ttu-id="61c65-163">**\_copia de \_ edición de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-163">**WM\_CAP\_EDIT\_COPY**</span></span>](wm-cap-edit-copy.md)
-   [<span data-ttu-id="61c65-164">**\_SAVEDIB de \_ archivo \_ Cap de WM**</span><span class="sxs-lookup"><span data-stu-id="61c65-164">**WM\_CAP\_FILE\_SAVEDIB**</span></span>](wm-cap-file-savedib.md)
-   [<span data-ttu-id="61c65-165">**\_marco de \_ captación de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-165">**WM\_CAP\_GRAB\_FRAME**</span></span>](wm-cap-grab-frame.md)
-   [<span data-ttu-id="61c65-166">**\_marco de \_ captación de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-166">**WM\_CAP\_GRAB\_FRAME\_NOSTOP**</span></span>](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a><span data-ttu-id="61c65-167">Opciones de captura avanzadas</span><span class="sxs-lookup"><span data-stu-id="61c65-167">Advanced Capture Options</span></span>

-   [<span data-ttu-id="61c65-168">**conjunto de archivos de Cap de WM \_ \_ \_ \_ INFOCHUNK**</span><span class="sxs-lookup"><span data-stu-id="61c65-168">**WM\_CAP\_FILE\_SET\_INFOCHUNK**</span></span>](wm-cap-file-set-infochunk.md)
-   [<span data-ttu-id="61c65-169">**límite de WM \_ \_ obtener \_ datos de usuario \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-169">**WM\_CAP\_GET\_USER\_DATA**</span></span>](wm-cap-get-user-data.md)
-   [<span data-ttu-id="61c65-170">**\_datos de \_ usuario del conjunto de Cap de WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-170">**WM\_CAP\_SET\_USER\_DATA**</span></span>](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a><span data-ttu-id="61c65-171">Trabajar con paletas</span><span class="sxs-lookup"><span data-stu-id="61c65-171">Working with Palettes</span></span>

-   [<span data-ttu-id="61c65-172">**\_copia de \_ edición de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-172">**WM\_CAP\_EDIT\_COPY**</span></span>](wm-cap-edit-copy.md)
-   [<span data-ttu-id="61c65-173">**CREACIÓN de la PAL de Cap de WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-173">**WM\_CAP\_PAL\_AUTOCREATE**</span></span>](wm-cap-pal-autocreate.md)
-   [<span data-ttu-id="61c65-174">**MANUALCREATE de la \_ PAL Cap de WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-174">**WM\_CAP\_PAL\_MANUALCREATE**</span></span>](wm-cap-pal-manualcreate.md)
-   [<span data-ttu-id="61c65-175">**PAL de Cap de WM \_ \_ \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="61c65-175">**WM\_CAP\_PAL\_OPEN**</span></span>](wm-cap-pal-open.md)
-   [<span data-ttu-id="61c65-176">**\_ \_ pegado PAL de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-176">**WM\_CAP\_PAL\_PASTE**</span></span>](wm-cap-pal-paste.md)
-   [<span data-ttu-id="61c65-177">**\_ \_ almacenamiento PAL de Cap de WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-177">**WM\_CAP\_PAL\_SAVE**</span></span>](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a><span data-ttu-id="61c65-178">Producir a otras aplicaciones</span><span class="sxs-lookup"><span data-stu-id="61c65-178">Yielding to Other Applications</span></span>

-   [<span data-ttu-id="61c65-179">**\_configuración de \_ secuencia de obtención de Cap de WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-179">**WM\_CAP\_GET\_SEQUENCE\_SETUP**</span></span>](wm-cap-get-sequence-setup.md)
-   [<span data-ttu-id="61c65-180">**\_rendimiento de \_ devolución de llamada de conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-180">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="61c65-181">**configuración de la secuencia de conjuntos de \_ Cap de WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-181">**WM\_CAP\_SET\_SEQUENCE\_SETUP**</span></span>](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a><span data-ttu-id="61c65-182">Funciones de devolución de llamada AVICap</span><span class="sxs-lookup"><span data-stu-id="61c65-182">AVICap Callback Functions</span></span>

-   [<span data-ttu-id="61c65-183">**capControlCallback**</span><span class="sxs-lookup"><span data-stu-id="61c65-183">**capControlCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [<span data-ttu-id="61c65-184">**capErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="61c65-184">**capErrorCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [<span data-ttu-id="61c65-185">**capStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="61c65-185">**capStatusCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [<span data-ttu-id="61c65-186">**capVideoStreamCallback**</span><span class="sxs-lookup"><span data-stu-id="61c65-186">**capVideoStreamCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [<span data-ttu-id="61c65-187">**capWaveStreamCallback**</span><span class="sxs-lookup"><span data-stu-id="61c65-187">**capWaveStreamCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [<span data-ttu-id="61c65-188">**capYieldCallback**</span><span class="sxs-lookup"><span data-stu-id="61c65-188">**capYieldCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [<span data-ttu-id="61c65-189">**devolución de llamada de conjunto de Cap de WM \_ \_ \_ \_ CAPCONTROL**</span><span class="sxs-lookup"><span data-stu-id="61c65-189">**WM\_CAP\_SET\_CALLBACK\_CAPCONTROL**</span></span>](wm-cap-set-callback-capcontrol.md)
-   [<span data-ttu-id="61c65-190">**\_error de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-190">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="61c65-191">**\_marco de \_ devolución de llamada de conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-191">**WM\_CAP\_SET\_CALLBACK\_FRAME**</span></span>](wm-cap-set-callback-frame.md)
-   [<span data-ttu-id="61c65-192">**\_Estado de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-192">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="61c65-193">**\_secuencia de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-193">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="61c65-194">**\_WAVESTREAM de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-194">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)
-   [<span data-ttu-id="61c65-195">**\_rendimiento de \_ devolución de llamada de conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="61c65-195">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a><span data-ttu-id="61c65-196">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="61c65-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61c65-197">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="61c65-197">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 




