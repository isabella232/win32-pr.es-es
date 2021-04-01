---
description: Este control muestra una cadena larga de texto que no cabe en su totalidad en la página. Un uso común de este control es mostrar el contrato de licencia.
ms.assetid: a49209f3-043c-4360-b1e3-9fa9538c2c9b
title: Control ScrollableText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ff807f2b0175eb411b3c45eb9d1e3b5eeaea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909810"
---
# <a name="scrollabletext-control"></a>Control ScrollableText

Este control muestra una cadena larga de texto que no cabe en su totalidad en la página. Un uso común de este control es mostrar el contrato de licencia.

Tenga en cuenta que la cadena de texto que se usa con este control no puede contener una propiedad incrustada. Para mostrar texto con propiedades incrustadas, use en su lugar el [control de texto](text-control.md).

## <a name="control-attributes"></a>Atributos de control

Puede usar los siguientes atributos con este control. Para cambiar el valor de un atributo mediante un evento, suscríbase el control a ControlEvent, en la [tabla EventMapping](eventmapping-table.md) y enumere el identificador del atributo en la columna de atributos. Escriba el identificador de ControlEvent, en la columna evento.



| Identificador de atributo                               | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)         |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas de la esquina izquierda del control en las columnas width, height, X e Y de la tabla de [control](control-table.md) o de la [tabla BBControl](bbcontrol-table.md). Use [unidades de instalador](installer-units.md) para longitud y distancia.<br/>                                            |
| [Texto](text-control-attribute.md)                 |                                  | Texto que muestra el control. Escriba la cadena de texto RTF en la columna texto de la [tabla de control](control-table.md).                                                                                                                                                                                                                                                       |
| [Visible](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Para hacer que el control esté visible u oculto en su creación, incluya este bit en la palabra de bit de la columna Attributes de la tabla de [control](control-table.md) o de la [tabla BBControl](bbcontrol-table.md).<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/> |
| [Enabled](enabled-control-attribute.md)           | 0x00000000 0x00000002<br/> | Control en estado deshabilitado. Control en un estado habilitado.<br/> Incluya este bit en la columna Attributes de las tablas [control](control-table.md) o [BBControl](bbcontrol-table.md) para habilitar el control en la creación.<br/> También puede habilitar o deshabilitar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>             |
| [Sunken](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | Mostrar el estilo visual predeterminado. Muestre el control con un aspecto hundido, 3D.<br/> Incluya estos bits en la palabra de bit de la columna Attributes de la [tabla de control](control-table.md).<br/>                                                                                                                                                                    |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | El texto del control se muestra en un orden de lectura de izquierda a derecha. El texto del control se muestra en un orden de lectura de derecha a izquierda.<br/>                                                                                                                                                                                                                               |
| [RightAligned](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | El texto del control está alineado a la izquierda. El texto del control está alineado a la derecha.<br/>                                                                                                                                                                                                                                                                            |
| [LeftScroll](leftscroll-control-attribute.md)     | 0x00000000 0x00000080<br/> | La barra de desplazamiento se encuentra en el lado derecho del control. La barra de desplazamiento se encuentra en el lado izquierdo del control.<br/>                                                                                                                                                                                                                                              |
| [Lenguas](bidi-control-attribute.md)                 | 0x000000E0                       | Establezca este valor para una combinación de los atributos [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)y [LeftScroll](leftscroll-control-attribute.md) .                                                                                                                                                                               |



 

## <a name="remarks"></a>Observaciones

Este control se puede crear a partir de la clase RICHEDIT mediante la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Tiene los estilos **es \_ multilínea**, **WS \_ VSCROLL**, **es de \_ solo lectura**, **WS \_ TABSTOP**, **es \_ AUTOVSCROLL**, **WS \_ Child**, **WS \_ Group** y **es \_ NOOLEDRAGDROP** .

 

 
