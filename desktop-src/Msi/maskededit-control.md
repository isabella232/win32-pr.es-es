---
description: El control MaskedEdit es un control de campo de edición que contiene una máscara en el campo de texto del control. Puede asociar el control a una propiedad de valor de cadena especificando el nombre de la propiedad en la columna de propiedades de la tabla de control.
ms.assetid: 8cc14683-3dbb-404f-87af-09a5f5b90b19
title: MaskedEdit (control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7568df9969ebabab6311e519d0a5a625feb8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678599"
---
# <a name="maskededit-control"></a>MaskedEdit (control)

El control MaskedEdit es un control de campo de edición que contiene una máscara en el campo de texto del control. Puede asociar el control a una propiedad de valor de cadena especificando el nombre de la propiedad en la columna de propiedades de la [tabla de control](control-table.md).

Puede usar el control MaskedEdit para crear una plantilla para la entrada de información del usuario, como un número de teléfono o un código de ID. de producto. Por ejemplo, el usuario puede especificar la propiedad [**PIDKEY**](pidkey.md) mediante un control MaskedEdit que se especifica estableciendo la propiedad [**PIDTemplate**](pidtemplate.md) en una cadena como la siguiente:

12345<\#\#\# -%%%%%%%>@@@@@

La cadena define la plantilla de enmascaramiento para la entrada de la propiedad [**PIDKEY**](pidkey.md) por parte del usuario. El segmento visible de la cadena se encuentra entre un par de caracteres de corchete (<>).

En la tabla siguiente se identifica la sintaxis de la máscara.



| Carácter | Significado                                                                                                                                                                                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <      | Extremo izquierdo del segmento visible de la plantilla. Este carácter y todo lo que aparece a su izquierda están ocultos en la interfaz de usuario. No debe haber más de una instancia de este carácter en la plantilla.                                                                               |
| >      | El extremo derecho del segmento visible de la plantilla. Este carácter y todo lo que se encuentre a su derecha se ocultan en la interfaz de usuario. Este carácter se sustituye por un guión durante la validación. Si hay un segmento visible que comienza con <, se debe terminar con una > coincidente. |
| \#        | Este carácter puede ser un dígito (numeral).                                                                                                                                                                                                                                                    |
| %         | Este carácter puede ser un dígito alternativo (numeral) que permite que la máscara controle la forma en que una acción personalizada distingue los campos.                                                                                                                                                          |
| @         | Este carácter puede ser un dígito aleatorio (numeral). Este carácter no debe aparecer en la parte visible de la plantilla.                                                                                                                                                                       |
| &         | Este carácter puede ser cualquier carácter.                                                                                                                                                                                                                                                        |
| ^         | Este carácter puede ser un carácter alternativo que permite a la máscara controlar el modo en que una acción personalizada distingue los campos.                                                                                                                                                                |
| ?         | Este carácter puede ser un carácter alternativo que permite a la máscara controlar el modo en que una acción personalizada distingue los campos.                                                                                                                                                                |
| \`        | Las marcas de acento grave \` (valor ASCII 96) pueden representar un carácter alternativo que permite a la máscara controlar el modo en que una acción personalizada distingue los campos.                                                                                                                                 |
| \_        | Este carácter es un carácter de subrayado literal.                                                                                                                                                                                                                                           |
| =         | Este carácter es el terminador de campo. Debe seguir a \# ,%, ^ o \` . Esto crea una posición de entrada más del mismo tipo que las posiciones anteriores y finaliza el campo con un separador "-".                                                                                 |



 

Cualquier otro carácter se trata como una constante literal.

En el caso de los caracteres que se pueden editar, el control crea ventanas de edición independientes con una ventana para cada bloque de caracteres contiguos del mismo tipo.

## <a name="control-attributes"></a>Atributos de control

Para cambiar el valor de un atributo que está utilizando un evento, suscríbase el control a un evento de control en la [tabla EventMapping](eventmapping-table.md) y enumere el identificador de atributo en la columna de atributos. Escriba el identificador del evento de control en la columna evento. Puede usar los siguientes atributos con el control MaskedEdit.



| Atributo                                                          | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Es el nombre de una propiedad indirecta que está asociada al control. Si se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Si se establece el bit de atributo indirecto, este nombre también es el valor de la propiedad que aparece en la columna de propiedades de la [tabla de control](control-table.md).                                                                                                                                   |
| [Position](position-control-attribute.md)                         |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho del control, el alto y las coordenadas de la esquina izquierda del control en las columnas width, height, X e Y de la [tabla de control](control-table.md). Use [unidades de instalador](installer-units.md) para longitud y distancia.<br/>                                                                                                                                                                                                            |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Es el nombre de la propiedad que está asociada a este control. Si no se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Este atributo se especifica en la columna de propiedades de la [tabla de control](control-table.md).                                                                                                                                                                                                           |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valor actual de la propiedad que este control muestra o modifica. Si no se establece el bit de atributo indirecto, este es el valor de PropertyName. Si se establece el bit de atributo indirecto, este es el valor de IndirectPropertyName. Si cambia el atributo, el control refleja el nuevo valor.                                                                                                                                                                                                |
| [Texto](text-control-attribute.md)                                 |                                  | Para establecer la fuente y el estilo de fuente de una cadena de texto, anteponga a la cadena de caracteres mostrados el prefijo { \\ style} o {&Style}. Donde Style es un identificador que aparece en la columna Style de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la propiedad [**DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se utiliza esa fuente. La cadena que especifica la plantilla de enmascaramiento sigue este prefijo y usa la sintaxis descrita anteriormente en este tema. |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Attributes de la [tabla de control](control-table.md) para que el control esté visible u oculto cuando se cree.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                 |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Control en estado deshabilitado. Control en un estado habilitado.<br/> Incluya este bit en la palabra de bit de la columna Attributes de la [tabla de control](control-table.md) para habilitar el control al crearlo.<br/> También puede habilitar o deshabilitar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                          |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con una apariencia en relieve y 3D.<br/> Incluya estos bits en la palabra de bit de la columna Attributes de la [tabla de control](control-table.md).<br/>                                                                                                                                                                                                                                                                                          |
| [Indirecto](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | El control muestra o cambia el valor de la propiedad en la columna de propiedades de la [tabla de control](control-table.md). El control muestra o cambia el valor de la propiedad que tiene el identificador que aparece en la columna de propiedades de la [tabla de control](control-table.md).<br/> Determina si se hace referencia indirectamente a la propiedad asociada a este control.<br/>                                                                                                 |



 

## <a name="remarks"></a>Observaciones

El control MaskedEdit crea una ventana primaria de la clase **Button** con los estilos de CONTROLPARENT de **\_ OWNERDRAW** y **WS \_ ex \_** . Crea varias ventanas secundarias en esta ventana.

-   En el caso de las partes de texto constantes, crea ventanas ESTÁTICAs con los estilos **SS \_ izquierdo** y **WS \_ secundario** .
-   En el caso de los campos modificables, crea una ventana de edición con los estilos **WS \_ Child**, **WS \_ Border** y **WS \_ TABSTOP** .
-   En el caso de los campos numéricos, la ventana también tiene el estilo de **\_ número es** .

Los campos alternativos digit,% y suplentes alternativos, ^,? y \` los campos permiten que las acciones personalizadas se diferencien entre los campos de una manera que se puede controlar mediante la máscara; por ejemplo, se puede utilizar ^ para los campos que deben estar en mayúsculas.

 

 




