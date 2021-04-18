---
title: Identificadores de objeto (Winuser. h)
description: En este tema se describen los identificadores de objeto de Microsoft Active Accessibility, los valores de 32 bits que identifican las categorías de objetos accesibles dentro de una ventana.
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
ms.openlocfilehash: 1fa2cf2099c5177be6f295ef6455646762525b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718753"
---
# <a name="object-identifiers-winuserh"></a>Identificadores de objeto (Winuser. h)

En este tema se describen los identificadores de objeto de Microsoft Active Accessibility, los valores de 32 bits que identifican las *categorías* de objetos accesibles dentro de una ventana. Los servidores de Microsoft Active Accessibility y los proveedores de automatización de la interfaz de usuario de Microsoft usan los identificadores de objeto para determinar el objeto al que hace referencia una solicitud de mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) .

Los clientes reciben estos valores en su función de devolución de llamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) y los usan para identificar partes de una ventana. Los servidores usan estos valores para identificar las partes correspondientes de una ventana al llamar a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) o al responder al mensaje de la [**\_ GETOBJECT de WM**](wm-getobject.md) .

Los servidores pueden definir identificadores de objeto personalizados para identificar otras categorías de objetos dentro de sus aplicaciones. Los identificadores de objeto personalizados deben tener asignados valores positivos porque Microsoft Active Accessibility reserva cero y todos los valores negativos para los siguientes identificadores de objeto estándar.

Las siguientes constantes se definen en Winuser. h:



| Constante                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OBJID_ALERT"></span><span id="objid_alert"></span><dl> <dt>**alerta de OBJID \_**</dt> </dl>                                     | Una alerta que está asociada a una ventana o una aplicación. Los cuadros de mensajes proporcionados por el sistema son los únicos elementos de interfaz de usuario que envían eventos con este identificador de objeto. Las aplicaciones de servidor no pueden usar las funciones de **AccessibleObjectFrom**_X_ con este identificador de objeto. Se trata de un problema conocido con Microsoft Active Accessibility.<br/>          |
| <span id="OBJID_CARET"></span><span id="objid_caret"></span><dl> <dt>**\_símbolo de intercalación de OBJID**</dt> </dl>                                     | La barra de inserción de texto (símbolo de intercalación) en la ventana.<br/>                                                                                                                                                                                                                                                                                               |
| <span id="OBJID_CLIENT"></span><span id="objid_client"></span><dl> <dt>**cliente de OBJID \_**</dt> </dl>                                  | Área cliente de la ventana. En la mayoría de los casos, el sistema operativo controla los elementos de marco y el objeto de cliente contiene todos los elementos controlados por la aplicación. Los servidores solo procesan los mensajes de [**WM \_ GETOBJECT**](wm-getobject.md) en los que *lParam* es el \_ cliente objid, \_ la ventana objid o un identificador de objeto personalizado.<br/> |
| <span id="OBJID_CURSOR"></span><span id="objid_cursor"></span><dl> <dt>**CURSOR de OBJID \_**</dt> </dl>                                  | Puntero del mouse. Solo hay un puntero del mouse en el sistema y no es un elemento secundario de ninguna ventana.<br/>                                                                                                                                                                                                                                      |
| <span id="OBJID_HSCROLL"></span><span id="objid_hscroll"></span><dl> <dt>**OBJID \_ HSCROLL**</dt> </dl>                               | Barra de desplazamiento horizontal de la ventana.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="OBJID_NATIVEOM"></span><span id="objid_nativeom"></span><dl> <dt>**OBJID \_ NATIVEOM**</dt> </dl>                            | En respuesta a este identificador de objeto, las aplicaciones de terceros pueden exponer su propio modelo de objetos. Las aplicaciones de terceros pueden devolver cualquier interfaz COM en respuesta a este identificador de objeto.<br/>                                                                                                                                             |
| <span id="OBJID_MENU"></span><span id="objid_menu"></span><dl> <dt>**\_menú OBJID**</dt> </dl>                                        | Barra de menús de la ventana.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="OBJID_QUERYCLASSNAMEIDX"></span><span id="objid_queryclassnameidx"></span><dl> <dt>**OBJID \_ QUERYCLASSNAMEIDX**</dt> </dl> | Identificador de objeto que Oleacc.dll usa internamente. Para obtener más información, vea el [Apéndice F: valores de identificador de objeto para OBJID \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).<br/>                                                                                                                  |
| <span id="OBJID_SIZEGRIP"></span><span id="objid_sizegrip"></span><dl> <dt>**OBJID \_ SIZEGRIP**</dt> </dl>                            | Control de tamaño de la ventana: un componente de marco opcional situado en la esquina inferior derecha del marco de la ventana.<br/>                                                                                                                                                                                                                                  |
| <span id="OBJID_SOUND"></span><span id="objid_sound"></span><dl> <dt>**sonido de OBJID \_**</dt> </dl>                                     | Objeto de sonido. Los objetos de sonido no tienen ubicaciones de pantalla o elementos secundarios, pero tienen atributos de nombre y estado. Son elementos secundarios de la aplicación que está reproduciendo el sonido.<br/>                                                                                                                                                         |
| <span id="OBJID_SYSMENU"></span><span id="objid_sysmenu"></span><dl> <dt>**OBJID \_ SYSMENU**</dt> </dl>                               | Menú del sistema de la ventana.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="OBJID_TITLEBAR"></span><span id="objid_titlebar"></span><dl> <dt>**TITLEBAR de OBJID \_**</dt> </dl>                            | Barra de título de la ventana.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="OBJID_VSCROLL"></span><span id="objid_vscroll"></span><dl> <dt>**OBJID \_ VSCROLL**</dt> </dl>                               | Barra de desplazamiento vertical de la ventana.<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="OBJID_WINDOW"></span><span id="objid_window"></span><dl> <dt>**ventana de OBJID \_**</dt> </dl>                                  | La ventana en lugar de un objeto secundario.<br/>                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

 





