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
# <a name="dwm-functions"></a>Funciones DWM

Esta sección contiene información acerca de las funciones de Administrador de ventanas de escritorio (DWM).

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a><br/></td>
<td>Esta función no está implementada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a><br/></td>
<td>Procedimiento de ventana predeterminado para la prueba de posicionamiento de DWM en el área no cliente.<br/> También debe asegurarse de que se llama a <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> para el mensaje <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> . Si no se llama a <strong>DwmDefWindowProc</strong> para el mensaje <strong>WM_NCMOUSELEAVE</strong> , DWM no quita el resaltado de los botones <strong>maximizar</strong>, <strong>minimizar</strong>y <strong>cerrar</strong> cuando el cursor sale de la ventana.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a><br/></td>
<td>Esta función no está implementada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a><br/></td>
<td>Habilita el efecto de desenfoque en una ventana especificada.<br/></td>
<b>Nota:</b> A partir de Windows 8, llamar a esta función no produce el efecto de desenfoque debido a un cambio de estilo en la forma en que se representan las ventanas.
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a><br/></td>
<td>Habilita o deshabilita la composición de DWM. <br/>
<blockquote>
[!Note]<br />
Esta función está en desuso a partir de Windows 8. DWM ya no se puede deshabilitar mediante programación.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a><br/></td>
<td>Notifica a DWM que debe participar o no en la programación del servicio de programación de clases multimedia (MMCSS) mientras el proceso de llamada está activo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a><br/></td>
<td>Extiende el marco de ventana en el área cliente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a><br/></td>
<td>Emite una llamada de vaciado que bloquea el autor de la llamada hasta el siguiente, cuando se han realizado todas las actualizaciones de la superficie de Microsoft DirectX que están pendientes actualmente. Esto compensa las escenas muy complejas o los procesos de llamada con una prioridad muy baja.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a><br/></td>
<td>Recupera el color actual utilizado para la composición de cristal DWM. Este valor se basa en la combinación de colores actual y puede ser modificado por el usuario. Las aplicaciones pueden escuchar los cambios de color mediante el control de la notificación de <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a><br/></td>
<td>Recupera la información de tiempo de composición actual para una ventana especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a><br/></td>
<td>Esta función no está implementada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a><br/></td>
<td>Esta función no está implementada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a><br/></td>
<td>Recupera los atributos de transporte.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a><br/></td>
<td><blockquote>
<strong>Nota:</strong>  Esta función está disponible públicamente, pero no funcional, para Windows 10, versión 1803.
</blockquote>
Comprueba los requisitos necesarios para obtener pestañas en la barra de título de la aplicación para la ventana especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a><br/></td>
<td>Recupera el valor actual de un atributo especificado que se aplica a una ventana.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a><br/></td>
<td>Una aplicación llama a este método para indicar que se deben actualizar todos los mapas de bits de iconos que se hayan proporcionado previamente desde una ventana, las miniaturas y las representaciones de PEEK.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a><br/></td>
<td>Obtiene un valor que indica si la composición DWM está habilitada. Las aplicaciones en equipos que ejecutan Windows 7 o versiones anteriores pueden escuchar los cambios de estado de composición mediante el control de la notificación de <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a><br/></td>
<td>Cambia el número de actualizaciones del monitor a través de las cuales se mostrará el fotograma anterior. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> ya no se admite. A partir de Windows 8.1, las llamadas a <strong>DwmModifyPreviousDxFrameDuration</strong> siempre devuelven E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a><br/></td>
<td>Recupera el tamaño de origen de la miniatura de DWM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a><br/></td>
<td>Crea una relación de miniatura de DWM entre las ventanas de origen y de destino.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a><br/></td>
<td>Notifica a DWM que un contacto táctil se ha reconocido como un gesto y que DWM debe dibujar comentarios para ese gesto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a><br/></td>
<td>Establece el número de actualizaciones del monitor a través de las cuales se va a mostrar el marco presentado. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> ya no se admite. A partir de Windows 8.1, las llamadas a <strong>DwmSetDxFrameDuration</strong> siempre devuelven E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a><br/></td>
<td>Establece un mapa de bits estático y de iconos para mostrar una <em>vista previa dinámica</em> (también conocida como <em>vista previa de PEEK</em>) de una ventana o una pestaña. La barra de tareas puede usar este mapa de bits para mostrar una vista previa de tamaño completo de una ventana o una pestaña.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a><br/></td>
<td>Establece un mapa de bits estático y de iconos en una ventana o pestaña que se va a usar como representación en miniatura. La barra de tareas puede usar este mapa de bits como destino del modificador en miniatura para la ventana o la pestaña.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a><br/></td>
<td>Establece los parámetros presentes para la composición de fotogramas. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> ya no se admite. A partir de Windows 8.1, las llamadas a <strong>DwmSetPresentParameters</strong> siempre devuelven E_NOTIMPL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a><br/></td>
<td>Establece el valor de los atributos de representación que no son de cliente para una ventana.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a><br/></td>
<td>Lo llama una aplicación o un marco de trabajo para especificar el tipo de comentarios visuales que se debe dibujar como respuesta a un contacto táctil o de lápiz determinado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a><br/></td>
<td>Habilita los comentarios gráficos de las interacciones táctiles y de arrastre para el usuario.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a><br/></td>
<td>Coordina las animaciones de las ventanas de herramientas con DWM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a><br/></td>
<td>Quita una relación de miniatura de DWM creada por la función <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a><br/></td>
<td>Actualiza las propiedades de una miniatura de DWM.<br/></td>
</tr>
</tbody>
</table>



 

 

