---
title: Funciones de DWM
description: Esta sección contiene información sobre las funciones Administrador de ventanas de escritorio (DWM).
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- Administrador de ventanas de escritorio (DWM),reference
- DWM (Administrador de ventanas de escritorio),reference
- Administrador de ventanas de escritorio (DWM),functions
- DWM (Administrador de ventanas de escritorio),functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd25ecbea1f7e08d8a7d5832d01908fc088e9be2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966392"
---
# <a name="dwm-functions"></a>Funciones de DWM

Esta sección contiene información sobre las funciones Administrador de ventanas de escritorio (DWM).

## <a name="in-this-section"></a>En esta sección




| Tema | Descripción | 
|-------|-------------|
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a><br /> | Esta función no está implementada.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a><br /> | Procedimiento de ventana predeterminado para las pruebas de impacto de DWM dentro del área que no es de cliente.<br /> También debe asegurarse de que se <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>llama a DwmDefWindowProc</strong></a> para el <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> mensaje. Si no se llama a <strong>DwmDefWindowProc</strong> para el mensaje <strong>WM_NCMOUSELEAVE,</strong> DWM no <strong></strong>quita <strong></strong> el resaltado de los botones <strong>Maximizar,</strong>Minimizar y Cerrar cuando el cursor sale de la ventana.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a><br /> | Esta función no está implementada.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a><br /> | Habilita el efecto de desenfoque en una ventana especificada.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a><br /> | Habilita o deshabilita la composición de DWM. <br /><blockquote>[!Note]<br />Esta función está en desuso a Windows 8. DWM ya no se puede deshabilitar mediante programación.</blockquote><br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a><br /> | Notifica al DWM que opte por participar o no en la programación del Servicio de programación de clases multimedia (MMCSS) mientras el proceso de llamada está activo.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a><br /> | Extiende el marco de ventana al área de cliente.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a><br /> | Emite una llamada de vaciado que bloquea al autor de la llamada hasta el siguiente presente, cuando se han realizado todas las actualizaciones de la superficie de Microsoft DirectX que están pendientes actualmente. Esto compensa las escenas muy complejas o los procesos de llamada con prioridad muy baja.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a><br /> | Recupera el color actual utilizado para la composición de gafas DWM. Este valor se basa en la combinación de colores actual y el usuario puede modificarlo. Las aplicaciones pueden escuchar los cambios de color mediante el control <a href="wm-dwmcolorizationcolorchanged.md"><strong>de WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> notificación.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a><br /> | Recupera la información de tiempo de composición actual para una ventana especificada.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a><br /> | Esta función no está implementada.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a><br /> | Esta función no está implementada.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a><br /> | Recupera los atributos de transporte.<br /> | 
| <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a><br /> | <blockquote><strong>Nota</strong>  Esta función está disponible públicamente, pero no funcional, para Windows 10, versión 1803.</blockquote>Comprueba los requisitos necesarios para obtener pestañas en la barra de título de la aplicación para la ventana especificada.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a><br /> | Recupera el valor actual de un atributo especificado aplicado a una ventana.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a><br /> | Lo llama una aplicación para indicar que se deben actualizar todos los mapas de bits icono proporcionados previamente desde una ventana, tanto las miniaturas como las representaciones de peek.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a><br /> | Obtiene un valor que indica si está habilitada la composición de DWM. Las aplicaciones en máquinas que Windows 7 o versiones anteriores pueden escuchar los cambios de estado de composición controlando <a href="wm-dwmcompositionchanged.md"><strong>la notificación WM_DWMCOMPOSITIONCHANGED</strong></a> configuración.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a><br /> | Cambia el número de actualizaciones del monitor a través de las cuales se mostrará el marco anterior. <br />Ya no <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>se admite DwmModifyPreviousDxFrameDuration.</strong></a> A partir Windows 8.1, las llamadas <strong>a DwmModifyPreviousDxFrameDuration</strong> siempre devuelven E_NOTIMPL.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a><br /> | Recupera el tamaño de origen de la miniatura de DWM.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a><br /> | Crea una relación de miniatura de DWM entre las ventanas de destino y de origen.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a><br /> | Notifica a DWM que se ha reconocido un contacto táctil como gesto y que DWM debe dibujar comentarios para ese gesto.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a><br /> | Establece el número de actualizaciones del monitor a través de las cuales se va a mostrar el marco presentado. <br />Ya no <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>se admite DwmSetDxFrameDuration.</strong></a> A partir Windows 8.1, las llamadas <strong>a DwmSetDxFrameDuration</strong> siempre devuelven E_NOTIMPL.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a><br /> | Establece un mapa de bits estático e icono para mostrar una <em>vista previa en</em> directo (también conocida como vista previa de <em>Peek)</em>de una ventana o pestaña. La barra de tareas puede usar este mapa de bits para mostrar una vista previa de tamaño completo de una ventana o pestaña.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a><br /> | Establece un mapa de bits estático e icono en una ventana o pestaña para usarlo como representación en miniatura. La barra de tareas puede usar este mapa de bits como destino de conmutador de miniatura para la ventana o pestaña.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a><br /> | Establece los parámetros actuales para la composición de fotogramas. <br />Ya no <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>se admite DwmSetPresentParameters.</strong></a> A partir Windows 8.1, las llamadas <strong>a DwmSetPresentParameters</strong> siempre devuelven E_NOTIMPL.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a><br /> | Establece el valor de los atributos de representación que no son de cliente para una ventana.<br /> | 
| <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a><br /> | Lo llama una aplicación o marco de trabajo para especificar el tipo de comentarios visuales que se dibujará en respuesta a un contacto táctil o de lápiz determinado.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a><br /> | Habilita los comentarios gráficos de las interacciones táctiles y de arrastre al usuario.<br /> | 
| <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a><br /> | Coordina las animaciones de las ventanas de herramientas con el DWM.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a><br /> | Quita una relación de miniatura de DWM creada por la <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>función DwmRegisterThumbnail.</strong></a><br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a><br /> | Actualiza las propiedades de una miniatura dwm.<br /> | 




 

 

