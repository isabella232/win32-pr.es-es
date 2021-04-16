---
title: Estilos de control de Up-Down (CommCtrl. h)
description: En esta sección se enumeran los estilos usados al crear controles de flechas.
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
ms.openlocfilehash: 9b27cd27123f4c1a071314fd20d1874e61b590d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649964"
---
# <a name="up-down-control-styles"></a>Estilos de control de Up-Down

En esta sección se enumeran los estilos usados al crear controles de flechas.



| Constante                                                                                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UDS_ALIGNLEFT"></span><span id="uds_alignleft"></span><dl> <dt>**UDS \_ ALIGNLEFT**</dt> </dl>       | Coloca el control de flechas situado junto al borde izquierdo de la ventana relacionada. La ventana relacionada se mueve a la derecha y su ancho se reduce para acomodar el ancho del control de flechas.<br/>                                                                                                                                                                                                   |
| <span id="UDS_ALIGNRIGHT"></span><span id="uds_alignright"></span><dl> <dt>**UDS \_ ALIGNRIGHT**</dt> </dl>    | Coloca el control de flechas situado junto al borde derecho de la ventana relacionada. El ancho de la ventana relacionada se reduce para acomodar el ancho del control de flechas.<br/>                                                                                                                                                                                                                          |
| <span id="UDS_ARROWKEYS"></span><span id="uds_arrowkeys"></span><dl> <dt>**UDS \_ ARROWKEYS**</dt> </dl>       | Hace que el control de flechas aumente y disminuya la posición cuando se presionan las teclas flecha arriba y flecha abajo.<br/>                                                                                                                                                                                                                                                                          |
| <span id="UDS_AUTOBUDDY"></span><span id="uds_autobuddy"></span><dl> <dt>**UDS \_ AUTOcompañero**</dt> </dl>       | Selecciona automáticamente la ventana anterior en el orden z como la ventana relacionada del control de flechas.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="UDS_HORZ"></span><span id="uds_horz"></span><dl> <dt>**UDS \_ horizontal**</dt> </dl>                      | Hace que las flechas del control de flechas señalen hacia la izquierda y la derecha en lugar de hacia arriba y hacia abajo.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="UDS_HOTTRACK"></span><span id="uds_hottrack"></span><dl> <dt>**UDS \_ HOTTRACK**</dt> </dl>          | Hace que el control muestre el comportamiento de "seguimiento activo". Es decir, resalta la flecha arriba y la flecha abajo en el control cuando el puntero pasa sobre ellos. Este estilo requiere Windows 98 o Windows 2000. Si el sistema ejecuta Windows 95 o Windows NT 4,0, se omite la marca. Para comprobar si el seguimiento activo está habilitado, llame a [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/> |
| <span id="UDS_NOTHOUSANDS"></span><span id="uds_nothousands"></span><dl> <dt>**UDS \_ NOmilla**</dt> </dl> | No inserta un separador de miles entre cada tres dígitos decimales. <br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="UDS_SETBUDDYINT"></span><span id="uds_setbuddyint"></span><dl> <dt>**UDS \_ SETBUDDYINT**</dt> </dl> | Hace que el control de flechas establezca el texto de la ventana relacionada (mediante el mensaje de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) ) cuando cambie la posición. El texto se compone de la posición con formato de cadena decimal o hexadecimal.<br/>                                                                                                                                                             |
| <span id="UDS_WRAP"></span><span id="uds_wrap"></span><dl> <dt>**ajuste de UDS \_**</dt> </dl>                      | Hace que la posición se "ajuste" si se incrementa o disminuye más allá del final o del principio del intervalo.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

