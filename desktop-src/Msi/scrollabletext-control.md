---
description: Este control muestra una cadena larga de texto que no cabe completamente en la página. Un uso común de este control es mostrar el contrato de licencia.
ms.assetid: a49209f3-043c-4360-b1e3-9fa9538c2c9b
title: ScrollableText (Control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ff807f2b0175eb411b3c45eb9d1e3b5eeaea01
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274116"
---
# <a name="scrollabletext-control"></a>ScrollableText (Control)

Este control muestra una cadena larga de texto que no cabe completamente en la página. Un uso común de este control es mostrar el contrato de licencia.

Tenga en cuenta que la cadena de texto utilizada con este control no puede contener una propiedad incrustada. Para mostrar texto con propiedades incrustadas, use en su lugar el [Control de texto](text-control.md).

## <a name="control-attributes"></a>Atributos de control

Puede usar los siguientes atributos con este control. Para cambiar el valor de un atributo mediante un evento, suscriba el control a un control ControlEvent en la [tabla EventMapping](eventmapping-table.md) y enumézcalo en la columna Atributo . Escriba el identificador de ControlEvent en la columna Evento.



| Identificador de atributo                               | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)         |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, alto y coordenadas del control de la esquina izquierda del control en las columnas Width, Height, X e Y de la tabla [Control](control-table.md) o [BBControl](bbcontrol-table.md). Use [las unidades del](installer-units.md) instalador para la longitud y la distancia.<br/>                                            |
| [Texto](text-control-attribute.md)                 |                                  | Texto mostrado por el control . Escriba la cadena de texto RTF en la columna Texto de la [tabla Control](control-table.md).                                                                                                                                                                                                                                                       |
| [Visible](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Para que el control sea visible u oculto en su creación, incluya este bit en la palabra de bits de la columna Atributos de la tabla [Control](control-table.md) o [de la tabla BBControl](bbcontrol-table.md).<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/> |
| [Enabled](enabled-control-attribute.md)           | 0x00000000 0x00000002<br/> | Control en estado deshabilitado. Control en un estado habilitado.<br/> Incluya este bit en la columna Atributos de las [tablas Control](control-table.md) o [BBControl](bbcontrol-table.md) para habilitar el control durante la creación.<br/> También puede habilitar o deshabilitar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>             |
| [Sunken](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestre el control con un aspecto 3D y desconsolado.<br/> Incluya estos bits en la palabra de bits en la columna Atributos de la [tabla Control](control-table.md).<br/>                                                                                                                                                                    |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | El texto del control se muestra en un orden de lectura de izquierda a derecha. El texto del control se muestra en un orden de lectura de derecha a izquierda.<br/>                                                                                                                                                                                                                               |
| [Alineado a la derecha](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | El texto del control se alinea a la izquierda. El texto del control se alinea a la derecha.<br/>                                                                                                                                                                                                                                                                            |
| [LeftScroll](leftscroll-control-attribute.md)     | 0x00000000 0x00000080<br/> | La barra de desplazamiento se encuentra en el lado derecho del control. La barra de desplazamiento se encuentra en el lado izquierdo del control.<br/>                                                                                                                                                                                                                                              |
| [Bidi](bidi-control-attribute.md)                 | 0x000000E0                       | Establezca este valor para una combinación de los atributos [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)y [LeftScroll.](leftscroll-control-attribute.md)                                                                                                                                                                               |



 

## <a name="remarks"></a>Observaciones

Este control se puede crear a partir de la clase RICHEDIT mediante [**la función CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Tiene los estilos **ES \_ MULTILINE,** **WS \_ VSCROLL,** **ES \_ READONLY,** **WS \_ TABSTOP,** **ES \_ AUTOVSCROLL,** **WS \_ CHILD,** **WS \_ GROUP** y **ES \_ NOOLEDRAGDROP.**

 

 
