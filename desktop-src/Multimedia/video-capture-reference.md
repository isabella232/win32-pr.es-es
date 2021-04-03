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
# <a name="video-capture-reference"></a>Referencia de captura de vídeo

En esta sección se describen las funciones, las estructuras, los mensajes y las macros asociadas a la clase de ventana AVICap. Estos elementos se agrupan de la siguiente manera.

## <a name="basic-capture-operations"></a>Operaciones de captura básicas

-   [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [**\_anulación de Cap de WM \_**](wm-cap-abort.md)
-   [**\_conexión del \_ controlador \_ Cap de WM**](wm-cap-driver-connect.md)
-   [**\_secuencia de Cap de WM \_**](wm-cap-sequence.md)
-   [**\_detención de Cap de WM \_**](wm-cap-stop.md)

## <a name="capture-windows"></a>Capturar ventanas

-   [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [**\_conexión del \_ controlador \_ Cap de WM**](wm-cap-driver-connect.md)
-   [**desconexión del \_ controlador Cap de WM \_ \_**](wm-cap-driver-disconnect.md)
-   [**\_Estado de \_ obtención de Cap de WM \_**](wm-cap-get-status.md)

## <a name="capture-drivers"></a>Controladores de captura

-   [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [**los Cap del \_ controlador Cap de WM \_ \_ \_**](wm-cap-driver-get-caps.md)
-   [**\_ \_ \_ obtener nombre de controlador de Cap de WM \_**](wm-cap-driver-get-name.md)
-   [**\_ \_ versión get del controlador Cap \_ de \_ WM**](wm-cap-driver-get-version.md)
-   [**\_límite de \_ \_ AUDIOFORMAT de Cap de WM**](wm-cap-get-audioformat.md)
-   [**\_obtención de \_ \_ formato de Cap de WM**](wm-cap-get-videoformat.md)
-   [**\_AUDIOFORMAT del \_ conjunto de Cap de WM \_**](wm-cap-set-audioformat.md)
-   [**videojuego de límite de WM \_ \_ \_**](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a>Vista previa del controlador de captura y modos de superposición

-   [**superposición de conjunto de Cap de WM \_ \_ \_**](wm-cap-set-overlay.md)
-   [**\_ \_ vista previa del conjunto de Cap de WM \_**](wm-cap-set-preview.md)
-   [**\_PREVIEWRATE del \_ conjunto de Cap de WM \_**](wm-cap-set-previewrate.md)
-   [**\_escala del \_ conjunto de Cap de WM \_**](wm-cap-set-scale.md)
-   [**\_desplazamiento de \_ conjunto de Cap de WM \_**](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a>Cuadros de diálogo de vídeo de controlador de captura

-   [**videocompresión de Cap de WM \_ \_ Dlg \_**](wm-cap-dlg-videocompression.md)
-   [**\_vídeo de \_ \_ presentación de Cap de WM**](wm-cap-dlg-videodisplay.md)
-   [**videoformateador de Cap de WM \_ \_ \_**](wm-cap-dlg-videoformat.md)
-   [**videosource de Cap de WM \_ \_ \_**](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a>Formato de audio

-   [**\_límite de \_ \_ AUDIOFORMAT de Cap de WM**](wm-cap-get-audioformat.md)
-   [**\_AUDIOFORMAT del \_ conjunto de Cap de WM \_**](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a>Configuración de captura de vídeo

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**\_configuración de \_ secuencia de obtención de Cap de WM \_ \_**](wm-cap-get-sequence-setup.md)
-   [**configuración de la secuencia de conjuntos de \_ Cap de WM \_ \_ \_**](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a>Capturar archivos y búferes

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**\_asignación de \_ archivo \_ Cap de WM**](wm-cap-file-allocate.md)
-   [**\_archivo Cap de la obtención de archivo Cap de WM \_ \_ \_ \_**](wm-cap-file-get-capture-file.md)
-   [**\_ \_ Guardar archivo Cap de WM \_**](wm-cap-file-saveas.md)
-   [**\_archivo de \_ captura de conjunto de archivos de Cap de \_ \_ WM \_**](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a>Uso directo de datos de captura

-   [**\_archivo de \_ secuencia de Cap de WM \_**](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a>Captura del dispositivo MCI

-   [**\_ \_ dispositivo MCI de conjunto de Cap de \_ WM \_**](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a>Captura de fotogramas manual

-   [**\_ \_ marco único de Cap de WM \_**](wm-cap-single-frame.md)
-   [**\_cierre de \_ \_ fotograma único de Cap de WM \_**](wm-cap-single-frame-close.md)
-   [**\_marco único de Cap de WM \_ \_ \_ abierto**](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a>Still-Image captura

-   [**\_copia de \_ edición de Cap de WM \_**](wm-cap-edit-copy.md)
-   [**\_SAVEDIB de \_ archivo \_ Cap de WM**](wm-cap-file-savedib.md)
-   [**\_marco de \_ captación de Cap de WM \_**](wm-cap-grab-frame.md)
-   [**\_marco de \_ captación de Cap de \_ WM \_**](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a>Opciones de captura avanzadas

-   [**conjunto de archivos de Cap de WM \_ \_ \_ \_ INFOCHUNK**](wm-cap-file-set-infochunk.md)
-   [**límite de WM \_ \_ obtener \_ datos de usuario \_**](wm-cap-get-user-data.md)
-   [**\_datos de \_ usuario del conjunto de Cap de WM \_ \_**](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a>Trabajar con paletas

-   [**\_copia de \_ edición de Cap de WM \_**](wm-cap-edit-copy.md)
-   [**CREACIÓN de la PAL de Cap de WM \_ \_ \_**](wm-cap-pal-autocreate.md)
-   [**MANUALCREATE de la \_ PAL Cap de WM \_ \_**](wm-cap-pal-manualcreate.md)
-   [**PAL de Cap de WM \_ \_ \_ abierto**](wm-cap-pal-open.md)
-   [**\_ \_ pegado PAL de Cap de WM \_**](wm-cap-pal-paste.md)
-   [**\_ \_ almacenamiento PAL de Cap de WM \_**](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a>Producir a otras aplicaciones

-   [**\_configuración de \_ secuencia de obtención de Cap de WM \_ \_**](wm-cap-get-sequence-setup.md)
-   [**\_rendimiento de \_ devolución de llamada de conjunto de Cap de \_ WM \_**](wm-cap-set-callback-yield.md)
-   [**configuración de la secuencia de conjuntos de \_ Cap de WM \_ \_ \_**](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a>Funciones de devolución de llamada AVICap

-   [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [**devolución de llamada de conjunto de Cap de WM \_ \_ \_ \_ CAPCONTROL**](wm-cap-set-callback-capcontrol.md)
-   [**\_error de \_ devolución de llamada del conjunto de Cap de \_ WM \_**](wm-cap-set-callback-error.md)
-   [**\_marco de \_ devolución de llamada de conjunto de Cap de \_ WM \_**](wm-cap-set-callback-frame.md)
-   [**\_Estado de \_ devolución de llamada del conjunto de Cap de \_ WM \_**](wm-cap-set-callback-status.md)
-   [**\_secuencia de \_ devolución de llamada del conjunto de Cap de \_ WM \_**](wm-cap-set-callback-videostream.md)
-   [**\_WAVESTREAM de \_ devolución de llamada del conjunto de Cap de \_ WM \_**](wm-cap-set-callback-wavestream.md)
-   [**\_rendimiento de \_ devolución de llamada de conjunto de Cap de \_ WM \_**](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 




