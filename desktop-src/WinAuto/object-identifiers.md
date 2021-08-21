---
title: Identificadores de objeto (Winuser.h)
description: En este tema se describe Microsoft Active Accessibility identificadores de objeto, valores de 32 bits que identifican categorías de objetos accesibles dentro de una ventana.
ms.assetid: dc1603f8-29e5-4acd-817a-c6957feaff6c
topic_type:
- apiref
api_name:
- OBJID_ALERT
- OBJID_CARET
- OBJID_CLIENT
- OBJID_CURSOR
- OBJID_HSCROLL
- OBJID_NATIVEOM
- OBJID_MENU
- OBJID_QUERYCLASSNAMEIDX
- OBJID_SIZEGRIP
- OBJID_SOUND
- OBJID_SYSMENU
- OBJID_TITLEBAR
- OBJID_VSCROLL
- OBJID_WINDOW
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b91bf70333d4ba7d607e465851f7f217aec43b0a081ec020017321fe30a7ede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565070"
---
# <a name="object-identifiers-winuserh"></a>Identificadores de objeto (Winuser.h)

En este tema se describen Microsoft Active Accessibility identificadores de objeto,  valores de 32 bits que identifican categorías de objetos accesibles dentro de una ventana. Microsoft Active Accessibility servidores y proveedores de Automatización de la interfaz de usuario microsoft usan los identificadores de objeto para determinar el objeto al que hace referencia una solicitud de mensaje [**\_ WM GETOBJECT.**](wm-getobject.md)

Los clientes reciben estos valores en su función de devolución de llamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) y los usan para identificar partes de una ventana. Los servidores usan estos valores para identificar las partes correspondientes de una ventana al llamar a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) o al responder al [**mensaje WM \_ GETOBJECT.**](wm-getobject.md)

Los servidores pueden definir los id. de objeto personalizados para identificar otras categorías de objetos dentro de sus aplicaciones. A los identificadores de objeto personalizados se les deben asignar valores positivos porque Microsoft Active Accessibility reserva cero y todos los valores negativos para los siguientes identificadores de objeto estándar.

Las siguientes constantes se definen en winuser.h:



| Constante                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OBJID_ALERT"></span><span id="objid_alert"></span><dl> <dt>**ALERTA DE \_ OBJID**</dt> </dl>                                     | Alerta asociada a una ventana o una aplicación. Los cuadros de mensaje proporcionados por el sistema son los únicos elementos de la interfaz de usuario que envían eventos con este identificador de objeto. Las aplicaciones de servidor no pueden **usar las funciones AccessibleObjectFrom**_X_ con este identificador de objeto. Se trata de un problema conocido con Microsoft Active Accessibility.<br/>          |
| <span id="OBJID_CARET"></span><span id="objid_caret"></span><dl> <dt>**OBJID \_ CARET**</dt> </dl>                                     | Barra de inserción de texto (caret) en la ventana.<br/>                                                                                                                                                                                                                                                                                               |
| <span id="OBJID_CLIENT"></span><span id="objid_client"></span><dl> <dt>**CLIENTE \_ OBJID**</dt> </dl>                                  | Área de cliente de la ventana. En la mayoría de los casos, el sistema operativo controla los elementos de marco y el objeto de cliente contiene todos los elementos controlados por la aplicación. Los servidores solo procesan los [**mensajes \_ GETOBJECT**](wm-getobject.md) de WM en los que *lParam* es OBJID \_ CLIENT, OBJID WINDOW o \_ un identificador de objeto personalizado.<br/> |
| <span id="OBJID_CURSOR"></span><span id="objid_cursor"></span><dl> <dt>**OBJID \_ CURSOR**</dt> </dl>                                  | Puntero del mouse. Solo hay un puntero del mouse en el sistema y no es un elemento secundario de ninguna ventana.<br/>                                                                                                                                                                                                                                      |
| <span id="OBJID_HSCROLL"></span><span id="objid_hscroll"></span><dl> <dt>**OBJID \_ HSCROLL**</dt> </dl>                               | Barra de desplazamiento horizontal de la ventana.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="OBJID_NATIVEOM"></span><span id="objid_nativeom"></span><dl> <dt>**OBJID \_ NATIVEOM**</dt> </dl>                            | En respuesta a este identificador de objeto, las aplicaciones de terceros pueden exponer su propio modelo de objetos. Las aplicaciones de terceros pueden devolver cualquier interfaz COM en respuesta a este identificador de objeto.<br/>                                                                                                                                             |
| <span id="OBJID_MENU"></span><span id="objid_menu"></span><dl> <dt>**MENÚ \_ OBJID**</dt> </dl>                                        | Barra de menús de la ventana.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="OBJID_QUERYCLASSNAMEIDX"></span><span id="objid_queryclassnameidx"></span><dl> <dt>**OBJID \_ QUERYCLASSNAMEIDX**</dt> </dl> | Identificador de objeto que Oleacc.dll internamente. Para obtener más información, [vea Apéndice F: Valores de identificador de objeto para OBJID \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).<br/>                                                                                                                  |
| <span id="OBJID_SIZEGRIP"></span><span id="objid_sizegrip"></span><dl> <dt>**TAMAÑO DE \_ OBJIDOBJIDOBJID**</dt> </dl>                            | Control de tamaño de la ventana: un componente de marco opcional ubicado en la esquina inferior derecha del marco de la ventana.<br/>                                                                                                                                                                                                                                  |
| <span id="OBJID_SOUND"></span><span id="objid_sound"></span><dl> <dt>**SONIDO \_ OBJID**</dt> </dl>                                     | Objeto de sonido. Los objetos de sonido no tienen ubicaciones de pantalla ni elementos secundarios, pero sí atributos de nombre y estado. Son secundarios de la aplicación que reproduce el sonido.<br/>                                                                                                                                                         |
| <span id="OBJID_SYSMENU"></span><span id="objid_sysmenu"></span><dl> <dt>**OBJID \_ SYSMENU**</dt> </dl>                               | Menú del sistema de la ventana.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="OBJID_TITLEBAR"></span><span id="objid_titlebar"></span><dl> <dt>**OBJID \_ TITLEBAR**</dt> </dl>                            | Barra de título de la ventana.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="OBJID_VSCROLL"></span><span id="objid_vscroll"></span><dl> <dt>**VSCROLL DE OBJID \_**</dt> </dl>                               | Barra de desplazamiento vertical de la ventana.<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="OBJID_WINDOW"></span><span id="objid_window"></span><dl> <dt>**VENTANA \_ OBJID**</dt> </dl>                                  | La propia ventana en lugar de un objeto secundario.<br/>                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

 





