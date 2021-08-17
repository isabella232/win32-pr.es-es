---
title: Up-Down estilos de control (CommCtrl.h)
description: En esta sección se enumeran los estilos usados al crear controles de arriba a abajo.
ms.assetid: d35198cb-6a5b-485e-a914-1b2ede53462f
topic_type:
- apiref
api_name:
- UDS_ALIGNLEFT
- UDS_ALIGNRIGHT
- UDS_ARROWKEYS
- UDS_AUTOBUDDY
- UDS_HORZ
- UDS_HOTTRACK
- UDS_NOTHOUSANDS
- UDS_SETBUDDYINT
- UDS_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809ab4ce2c4d8670363dc7f0751ae4a3756ee7b4e5dc9b75c79986c3a56d359d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957704"
---
# <a name="up-down-control-styles"></a>Up-Down estilos de control

En esta sección se enumeran los estilos usados al crear controles de arriba a abajo.



| Constante                                                                                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UDS_ALIGNLEFT"></span><span id="uds_alignleft"></span><dl> <dt>**UDS \_ ALIGNLEFT**</dt> </dl>       | Coloca el control de arriba abajo junto al borde izquierdo de la ventana del compañero. La ventana de compañeros se mueve a la derecha y su ancho se reduce para dar cabida al ancho del control de arriba a abajo.<br/>                                                                                                                                                                                                   |
| <span id="UDS_ALIGNRIGHT"></span><span id="uds_alignright"></span><dl> <dt>**UDS \_ ALIGNRIGHT**</dt> </dl>    | Coloca el control de arriba abajo junto al borde derecho de la ventana del compañero. El ancho de la ventana de compañeros se reduce para dar cabida al ancho del control de arriba a abajo.<br/>                                                                                                                                                                                                                          |
| <span id="UDS_ARROWKEYS"></span><span id="uds_arrowkeys"></span><dl> <dt>**UDS \_ ARROWKEYS**</dt> </dl>       | Hace que el control de arriba a abajo incremente y decrete la posición cuando se presionan las teclas FLECHA ARRIBA y FLECHA ABAJO.<br/>                                                                                                                                                                                                                                                                          |
| <span id="UDS_AUTOBUDDY"></span><span id="uds_autobuddy"></span><dl> <dt>**UDS \_ AUTOBUDDY**</dt> </dl>       | Selecciona automáticamente la ventana anterior en el orden Z como ventana de compañeros del control de flechas.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="UDS_HORZ"></span><span id="uds_horz"></span><dl> <dt>**UDS \_ HORZ**</dt> </dl>                      | Hace que las flechas del control de flechas hacia abajo apunten a la izquierda y a la derecha en lugar de hacia arriba y hacia abajo.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="UDS_HOTTRACK"></span><span id="uds_hottrack"></span><dl> <dt>**UDS \_ HOTTRACK**</dt> </dl>          | Hace que el control presente un comportamiento de "seguimiento en caliente". Es decir, resalta las flechas arriba y abajo del control a medida que el puntero pasa sobre ellos. Este estilo requiere Windows 98 o Windows 2000. Si el sistema se ejecuta Windows 95 o Windows NT 4.0, se omite la marca. Para comprobar si está habilitado el seguimiento en caliente, llame [**a SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/> |
| <span id="UDS_NOTHOUSANDS"></span><span id="uds_nothousands"></span><dl> <dt>**UDS \_ NOTHOUSANDS**</dt> </dl> | No inserta un separador de miles entre cada tres dígitos decimales. <br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="UDS_SETBUDDYINT"></span><span id="uds_setbuddyint"></span><dl> <dt>**UDS \_ SETBUDDYINT**</dt> </dl> | Hace que el control de arriba a abajo establezca el texto de la ventana de compañeros (mediante el [**mensaje \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) de WM) cuando cambia la posición. El texto consta de la posición con formato de cadena decimal o hexadecimal.<br/>                                                                                                                                                             |
| <span id="UDS_WRAP"></span><span id="uds_wrap"></span><dl> <dt>**UDS \_ WRAP**</dt> </dl>                      | Hace que la posición se "ajuste" si se incrementa o disminuye más allá del final o el principio del intervalo.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

