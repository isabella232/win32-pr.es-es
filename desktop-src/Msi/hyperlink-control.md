---
description: El control de hipervínculo muestra un vínculo HTML a una dirección, que se abre en el explorador predeterminado del equipo.
ms.assetid: 06678b10-0915-4649-b917-ec90c40d5160
title: Control de hipervínculo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d074efa00fcf51fec979d9df07f1854631279d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910926"
---
# <a name="hyperlink-control"></a>Control de hipervínculo

El control de hipervínculo muestra un vínculo HTML a una dirección, que se abre en el explorador predeterminado del equipo. No se admiten vínculos para protocolos distintos de HTML.

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. Este control está disponible a partir de Windows Installer 5,0.

El valor de texto del control de hipervínculo utiliza la etiqueta delimitadora <a> y el valor del atributo href para especificar la dirección URL y el texto mostrado del vínculo.

``` syntax
[Blue Yonder Airlines](https://www.blueyonderairlines.com)
```

## <a name="control-attributes"></a>Atributos de control

Puede usar los siguientes atributos con el control de hipervínculo. Para cambiar el valor de un atributo mediante un evento, suscríbase el control a ControlEvent, en la [tabla EventMapping](eventmapping-table.md) y enumere el identificador del atributo en la columna de atributos. Escriba el identificador de ControlEvent, en la columna evento.



| Identificador de atributo                             | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)       |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas de la esquina izquierda del control en las columnas width, height, X e Y de la tabla de [control](control-table.md) o de la [tabla BBControl](bbcontrol-table.md). Use [unidades de instalador](installer-units.md) para longitud y distancia.<br/>                                                                                                                                                                       |
| [Texto](text-control-attribute.md)               |                                  | Texto que muestra el control. Para establecer la fuente y el estilo de fuente de una cadena de texto, anteponga a la cadena de caracteres mostrados el prefijo { \\ style} o {&Style}. Donde Style es un identificador que aparece en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la propiedad [**DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usará esa fuente. El valor de texto también resolverá la \[ propiedad \] en la propiedad a la que se hace referencia. <br/> |
| [Visible](visible-control-attribute.md)         | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bit de la columna Attributes de la tabla de [control](control-table.md) o de la [tabla BBControl](bbcontrol-table.md). para hacer que el control esté visible u oculto en su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                                                                           |
| [Enabled](enabled-control-attribute.md)         | 0x00000000 0x00000002<br/> | Control en estado deshabilitado. Control en un estado habilitado.<br/> Incluya este bit en la palabra de bit de la columna Attributes de las [tablas](bbcontrol-table.md) [control](control-table.md) o BBControl para habilitar el control en la creación.<br/> También puede habilitar o deshabilitar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                                                                        |
| [Sunken](sunken-control-attribute.md)           | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con un aspecto hundido, 3D.<br/> Incluya estos bits en la palabra de bit de la columna Attributes de la [tabla de control](control-table.md).<br/>                                                                                                                                                                                                                                                                                            |
| [Transparente](transparent-control-attribute.md) | 0x00000000 0x00010000<br/> | Control opaco. Fondo muestra a través del control. El control tiene el \_ estilo WS ex \_ transparente.<br/> Incluya este bit en la columna Attributes de las tablas [control](control-table.md) o [BBControl](bbcontrol-table.md).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Observaciones

Este control se puede crear a partir de la clase de vínculo WC mediante \_ la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Tiene los estilos WS \_ Child, WS \_ TABSTOP y WS \_ Group.

No coloque controles de [texto](text-control.md) transparente sobre los mapas de bits de color. Es posible que el texto no esté visible si el usuario cambia la combinación de colores de la pantalla. Por ejemplo, el texto puede volverse invisible si el usuario establece el parámetro de contraste alto por motivos de accesibilidad.

Si el texto del control es mayor que el ancho del control, el texto se ajusta o se trunca, en función de si el alto es suficiente para ajustarse al texto ajustado.

 

 
