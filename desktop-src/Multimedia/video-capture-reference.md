---
title: Referencia de captura de vídeo
description: Referencia de captura de vídeo
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- Vídeo para Windows (VFW), referencia de captura de vídeo
- VFW (vídeo para Windows),referencia de captura de vídeo
- AVICap,reference
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef19834e244f6070a1d8bb3383dcac017e4d161
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245618"
---
# <a name="video-capture-reference"></a>Referencia de captura de vídeo

En esta sección se describen las funciones, estructuras, mensajes y macros asociados a la clase de ventana AVICap. Estos elementos se agrupan como se muestra a continuación.

## <a name="basic-capture-operations"></a>Operaciones básicas de captura

-   [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [**WM \_ CAP \_ ABORT**](wm-cap-abort.md)
-   [**WM \_ CAP \_ DRIVER \_ CONNECT**](wm-cap-driver-connect.md)
-   [**SECUENCIA \_ DE LÍMITE DE \_ WM**](wm-cap-sequence.md)
-   [**WM \_ CAP \_ STOP**](wm-cap-stop.md)

## <a name="capture-windows"></a>Capturar Windows

-   [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [**WM \_ CAP \_ DRIVER \_ CONNECT**](wm-cap-driver-connect.md)
-   [**DESCONEXIÓN DEL CONTROLADOR WM \_ CAP \_ \_**](wm-cap-driver-disconnect.md)
-   [**WM \_ CAP \_ GET \_ STATUS**](wm-cap-get-status.md)

## <a name="capture-drivers"></a>Controladores de captura

-   [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [**LÍMITES \_ GET \_ DEL CONTROLADOR \_ WM CAP \_**](wm-cap-driver-get-caps.md)
-   [**WM \_ CAP \_ DRIVER \_ GET \_ NAME**](wm-cap-driver-get-name.md)
-   [**VERSIÓN GET DEL CONTROLADOR WM \_ CAP \_ \_ \_**](wm-cap-driver-get-version.md)
-   [**WM \_ CAP \_ GET \_ AUDIOFORMAT**](wm-cap-get-audioformat.md)
-   [**WM \_ CAP \_ GET \_ VIDEOFORMAT**](wm-cap-get-videoformat.md)
-   [**WM \_ CAP \_ SET \_ AUDIOFORMAT**](wm-cap-set-audioformat.md)
-   [**WM \_ CAP \_ SET \_ VIDEOFORMAT**](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a>Capturar modos de vista previa y superposición del controlador

-   [**SUPERPOSICIÓN \_ DE CONJUNTO DE LÍMITE DE \_ \_ WM**](wm-cap-set-overlay.md)
-   [**WM \_ CAP \_ SET \_ PREVIEW**](wm-cap-set-preview.md)
-   [**WM \_ CAP \_ SET \_ PREVIEWRATE**](wm-cap-set-previewrate.md)
-   [**ESCALA \_ DE CONJUNTO DE \_ \_ LÍMITES DE WM**](wm-cap-set-scale.md)
-   [**DESPLAZAMIENTO \_ DE WM CAP \_ SET \_**](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a>Cuadros de diálogo Capturar vídeo del controlador

-   [**WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md)
-   [**WM \_ CAP \_ DLG \_ VIDEODISPLAY**](wm-cap-dlg-videodisplay.md)
-   [**WM \_ CAP \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md)
-   [**WM \_ CAP \_ DLG \_ VIDEOSOURCE**](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a>Formato de audio

-   [**WM \_ CAP \_ GET \_ AUDIOFORMAT**](wm-cap-get-audioformat.md)
-   [**WM \_ CAP \_ SET \_ AUDIOFORMAT**](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a>Captura de vídeo Configuración

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**CONFIGURACIÓN DE SECUENCIA GET DE WM \_ CAP \_ \_ \_**](wm-cap-get-sequence-setup.md)
-   [**CONFIGURACIÓN DE \_ SECUENCIA DEL CONJUNTO DE \_ \_ LÍMITES \_ DE WM**](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a>Capturar archivos y búferes

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**WM \_ CAP \_ FILE \_ ALLOCATE**](wm-cap-file-allocate.md)
-   [**ARCHIVO WM \_ CAP \_ GET CAPTURE \_ \_ \_ FILE**](wm-cap-file-get-capture-file.md)
-   [**WM \_ CAP \_ FILE \_ SAVEAS**](wm-cap-file-saveas.md)
-   [**ARCHIVO DE CAPTURA DE CONJUNTO DE ARCHIVOS DE LÍMITE \_ \_ \_ \_ \_ DE WM**](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a>Uso directo de capturar datos

-   [**WM \_ CAP \_ SEQUENCE \_ NOFILE**](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a>Captura desde el dispositivo MCI

-   [**WM \_ CAP \_ SET \_ MCI \_ DEVICE**](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a>Captura manual de fotogramas

-   [**WM \_ CAP \_ SINGLE \_ FRAME**](wm-cap-single-frame.md)
-   [**CIERRE DE MARCO ÚNICO DE WM \_ CAP \_ \_ \_**](wm-cap-single-frame-close.md)
-   [**WM \_ CAP \_ SINGLE \_ FRAME \_ OPEN**](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a>Still-Image capture

-   [**WM \_ CAP \_ EDIT \_ COPY**](wm-cap-edit-copy.md)
-   [**ARCHIVO \_ DE LÍMITE DE WM \_ \_ SAVEDIB**](wm-cap-file-savedib.md)
-   [**MARCO DE \_ CAPTURA DE EXTREMO DE \_ \_ WM**](wm-cap-grab-frame.md)
-   [**NOSTOP \_ DEL MARCO DE CAPTURA DE EXTREMO \_ \_ \_ DE WM**](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a>Opciones avanzadas de captura

-   [**WM \_ CAP \_ FILE \_ SET \_ INFOCHUNK**](wm-cap-file-set-infochunk.md)
-   [**WM \_ CAP \_ GET \_ USER \_ DATA**](wm-cap-get-user-data.md)
-   [**DATOS \_ DE USUARIO DE WM CAP \_ SET \_ \_**](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a>Trabajar con paletas

-   [**WM \_ CAP \_ EDIT \_ COPY**](wm-cap-edit-copy.md)
-   [**WM \_ CAP \_ PAL \_ AUTOCREATE**](wm-cap-pal-autocreate.md)
-   [**WM \_ CAP \_ PAL \_ MANUALCREATE**](wm-cap-pal-manualcreate.md)
-   [**WM \_ CAP \_ PAL \_ OPEN**](wm-cap-pal-open.md)
-   [**WM \_ CAP \_ PAL \_ PASTE**](wm-cap-pal-paste.md)
-   [**WM \_ CAP \_ PAL \_ SAVE**](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a>Rendimiento a otras aplicaciones

-   [**CONFIGURACIÓN DE SECUENCIA GET DE WM \_ CAP \_ \_ \_**](wm-cap-get-sequence-setup.md)
-   [**RENDIMIENTO DE DEVOLUCIÓN DE LLAMADA DEL CONJUNTO DE \_ \_ \_ LÍMITES \_ DE WM**](wm-cap-set-callback-yield.md)
-   [**CONFIGURACIÓN DE \_ SECUENCIA DEL CONJUNTO DE \_ \_ LÍMITES \_ DE WM**](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a>Funciones de devolución de llamada de AVICap

-   [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ CAPCONTROL**](wm-cap-set-callback-capcontrol.md)
-   [**ERROR DE \_ DEVOLUCIÓN \_ DE LLAMADA DEL CONJUNTO \_ DE LÍMITES DE \_ WM**](wm-cap-set-callback-error.md)
-   [**MARCO DE DEVOLUCIÓN DE LLAMADA DE WM \_ CAP \_ SET \_ \_**](wm-cap-set-callback-frame.md)
-   [**ESTADO DE DEVOLUCIÓN DE LLAMADA DEL CONJUNTO DE \_ \_ \_ LÍMITES \_ DE WM**](wm-cap-set-callback-status.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)
-   [**RENDIMIENTO DE DEVOLUCIÓN DE LLAMADA DEL CONJUNTO DE \_ \_ \_ LÍMITES \_ DE WM**](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 




