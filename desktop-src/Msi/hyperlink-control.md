---
description: El control Hipervínculo muestra un vínculo HTML a una dirección, que se abre en el explorador predeterminado del equipo.
ms.assetid: 06678b10-0915-4649-b917-ec90c40d5160
title: Hyperlink (Control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce515b64a518012ea187eb2c3a933e653b1ea5cf99b316028f9cfe3b397c5f96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129465"
---
# <a name="hyperlink-control"></a>Hyperlink (Control)

El control Hipervínculo muestra un vínculo HTML a una dirección, que se abre en el explorador predeterminado del equipo. Los vínculos no se admiten para protocolos que no sean HTML.

**[Windows Installer 4.5 o versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite. Este control está disponible a partir de Windows Installer 5.0.

El valor Text del control HyperLink usa la etiqueta delimitadora y el valor del atributo HREF para especificar la dirección URL y el texto mostrado <a> del vínculo.

``` syntax
[Blue Yonder Airlines](https://www.blueyonderairlines.com)
```

## <a name="control-attributes"></a>Atributos de control

Puede usar los atributos siguientes con el control Hyperlink. Para cambiar el valor de un atributo mediante un evento, suscriba el control a un control ControlEvent en la [tabla EventMapping](eventmapping-table.md) y enumézcalo en la columna Attribute . Escriba el identificador de ControlEvent en la columna Evento.



| Identificador de atributo                             | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)       |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, alto y coordenadas del control de la esquina izquierda del control en las columnas Width, Height, X e Y de la tabla [Control](control-table.md) o [BBControl](bbcontrol-table.md). Use [las unidades del](installer-units.md) instalador para la longitud y la distancia.<br/>                                                                                                                                                                       |
| [Texto](text-control-attribute.md)               |                                  | Texto mostrado por el control . Para establecer la fuente y el estilo de fuente de una cadena de texto, antefise la cadena de caracteres mostrados con { style} o \\ {&style}. Donde style es un identificador enumerado en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la [**propiedad DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usará esa fuente. El valor de texto también resolverá \[ Property en la propiedad a la que se hace \] referencia. <br/> |
| [Visible](visible-control-attribute.md)         | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Atributos de la [tabla Control](control-table.md) o de la tabla [BBControl](bbcontrol-table.md)para que el control sea visible u oculto tras su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                                                                           |
| [Habilitado](enabled-control-attribute.md)         | 0x00000000 0x00000002<br/> | Control en estado deshabilitado. Control en un estado habilitado.<br/> Incluya este bit en la palabra bit en la columna Atributos de las [tablas Control](control-table.md) o [BBControl](bbcontrol-table.md) para habilitar el control durante la creación.<br/> También puede habilitar o deshabilitar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                                                                        |
| [Sunken](sunken-control-attribute.md)           | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con un aspecto 3D desconsolado.<br/> Incluya estos bits en la palabra de bits en la columna Atributos de la [tabla Control](control-table.md).<br/>                                                                                                                                                                                                                                                                                            |
| [Transparente](transparent-control-attribute.md) | 0x00000000 0x00010000<br/> | Control opaco. El fondo se muestra a través del control . El control tiene el estilo TRANSPARENTE de WS \_ \_ EX.<br/> Incluya este bit en la columna Atributos de las [tablas Control](control-table.md) [o BBControl](bbcontrol-table.md).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentarios

Este control se puede crear a partir de la clase WC \_ LINK mediante la función [**CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Tiene los estilos WS \_ CHILD, WS \_ TABSTOP y WS \_ GROUP.

No coloque controles de [texto transparentes sobre](text-control.md) mapas de bits de color. Es posible que el texto no esté visible si el usuario cambia la combinación de colores para mostrar. Por ejemplo, el texto puede hacerse invisible si el usuario establece el parámetro de contraste alto por motivos de accesibilidad.

Si el texto del control es mayor que el ancho del control, el texto se ajusta o trunca, dependiendo de si el alto es suficiente para ajustarse al texto ajustado.

 

 
