---
description: El control MaskedEdit es un control de campo de edición que contiene una máscara en el campo de texto del control. Para asociar el control a una propiedad de valor de cadena, escriba el nombre de la propiedad en la columna Propiedad de la tabla de controles.
ms.assetid: 8cc14683-3dbb-404f-87af-09a5f5b90b19
title: MaskedEdit (Control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7568df9969ebabab6311e519d0a5a625feb8dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071913"
---
# <a name="maskededit-control"></a>MaskedEdit (Control)

El control MaskedEdit es un control de campo de edición que contiene una máscara en el campo de texto del control. Para asociar el control a una propiedad de valor de cadena, escriba el nombre de la propiedad en la columna Propiedad de la [tabla de control](control-table.md).

Puede usar el control MaskedEdit para crear una plantilla para la entrada de información del usuario, como un número de teléfono o un código de id. de producto. Por ejemplo, el usuario puede especificar la propiedad [**PIDKEY**](pidkey.md) a través de un control MaskedEdit que se especifica estableciendo la propiedad [**PIDTemplate**](pidtemplate.md) en una cadena como la siguiente:

12345<\#\#\# -%%%%%%%>@@@@@

La cadena define la plantilla de enmascaramiento para la entrada de [**la propiedad PIDKEY**](pidkey.md) por parte del usuario. El segmento visible de la cadena se incluye entre corchetes (<>).

En la tabla siguiente se identificó la sintaxis de la máscara.



| Carácter | Significado                                                                                                                                                                                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <      | Extremo izquierdo del segmento visible de la plantilla. Este carácter y todo lo que se encuentra a su izquierda están ocultos en la interfaz de usuario. No debería haber más de una instancia de este carácter en la plantilla.                                                                               |
| >      | Extremo derecho del segmento visible de la plantilla. Este carácter y todo lo que se encuentra a su derecha están ocultos en la interfaz de usuario. Este carácter se reemplaza por un guión durante la validación. Si hay un segmento visible que comienza con <, debe terminarse con una >. |
| \#        | Este carácter puede ser un dígito (numeral).                                                                                                                                                                                                                                                    |
| %         | Este carácter puede ser un dígito alternativo (numeral) que permite a la máscara controlar la manera en que una acción personalizada diferencia los campos.                                                                                                                                                          |
| @         | Este carácter puede ser un dígito aleatorio (numeral). Este carácter no debe aparecer en la parte visible de la plantilla.                                                                                                                                                                       |
| &         | Este carácter puede ser cualquier carácter.                                                                                                                                                                                                                                                        |
| ^         | Este carácter puede ser un carácter alternativo que permite a la máscara controlar la manera en que una acción personalizada diferencia los campos.                                                                                                                                                                |
| ?         | Este carácter puede ser un carácter alternativo que permite a la máscara controlar la manera en que una acción personalizada diferencia los campos.                                                                                                                                                                |
| \`        | Las marcas de acento grave (valor ASCII 96) pueden representar un carácter alternativo que permite a la máscara controlar la forma en que una \` acción personalizada diferencia los campos.                                                                                                                                 |
| \_        | Este carácter es un carácter de subrayado literal.                                                                                                                                                                                                                                           |
| =         | Este carácter es el terminador de campo. Debe seguir , \# %, ^o \` . Esto crea una posición de entrada más del mismo tipo que las posiciones anteriores y finaliza el campo con un separador "-".                                                                                 |



 

Cualquier otro carácter se trata como una constante literal.

Para los caracteres que se pueden editar, el control crea ventanas de edición independientes con una ventana para cada bloque de caracteres contiguos del mismo tipo.

## <a name="control-attributes"></a>Atributos de control

Para cambiar el valor de un atributo que usa un evento, suscriba el control a un evento Control en la [tabla EventMapping y](eventmapping-table.md) enumlíe el identificador de atributo en la columna Atributo . Escriba el identificador del evento Control en la columna Evento . Puede usar los atributos siguientes con el control MaskedEdit.



| Atributo                                                          | Hexadecimal Bit                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Este es el nombre de una propiedad indirecta asociada al control . Si se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Si se establece el bit de atributo indirecto, este nombre también es el valor de la propiedad que aparece en la columna Propiedad de [la tabla de control](control-table.md).                                                                                                                                   |
| [Position](position-control-attribute.md)                         |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, alto y coordenadas del control de la esquina izquierda del control en las columnas Width, Height, X e Y de [la tabla de control](control-table.md). Use [Unidades del instalador](installer-units.md) para la longitud y la distancia.<br/>                                                                                                                                                                                                            |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Este es el nombre de la propiedad asociada a este control. Si no se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Este atributo se especifica en la columna Property de la [tabla de control](control-table.md).                                                                                                                                                                                                           |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valor actual de la propiedad que este control muestra o cambia. Si no se establece el bit de atributo indirecto, este es el valor de PropertyName. Si se establece el bit de atributo indirecto, este es el valor de IndirectPropertyName. Si el atributo cambia, el control refleja el nuevo valor.                                                                                                                                                                                                |
| [Texto](text-control-attribute.md)                                 |                                  | Para establecer la fuente y el estilo de fuente de una cadena de texto, antefise la cadena de caracteres mostrados con { style} o \\ {&style}. Donde style es un identificador enumerado en la columna Style de [la tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la propiedad [**DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usa esa fuente. La cadena que especifica la plantilla de enmascaramiento sigue este prefijo y usa la sintaxis descrita anteriormente en este tema. |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Atributos de la tabla [de control](control-table.md) para que el control sea visible u oculto cuando se cree.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                 |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Control en estado deshabilitado. Control en un estado habilitado.<br/> Incluya este bit en la palabra bit en la columna Atributos de la [tabla de control](control-table.md) para habilitar el control durante la creación.<br/> También puede habilitar o deshabilitar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                          |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con un aspecto 3D desconsolado.<br/> Incluya estos bits en la palabra de bits en la columna Atributos de la [tabla de control](control-table.md).<br/>                                                                                                                                                                                                                                                                                          |
| [Indirecto](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | El control muestra o cambia el valor de la propiedad en la columna Propiedad de la [tabla de control](control-table.md). El control muestra o cambia el valor de la propiedad que tiene el identificador enumerado en la columna Propiedad de la [tabla de control](control-table.md).<br/> Determina si se hace referencia indirectamente a la propiedad asociada a este control.<br/>                                                                                                 |



 

## <a name="remarks"></a>Observaciones

El control MaskedEdit crea una ventana primaria de la clase **BUTTON** con los estilos **BS \_ OWNERDRAW** y **WS \_ EX \_ CONTROLPARENT.** Crea varias ventanas secundarias en esta ventana.

-   Para los elementos de texto constantes, crea ventanas ESTÁTICAs con los estilos **SS \_ LEFT** y **WS \_ CHILD.**
-   Para los campos editables, crea una ventana EDIT con los estilos **WS \_ CHILD**, **WS \_ BORDER** y **WS \_ TABSTOP.**
-   Para los campos numéricos, la ventana también tiene el **estilo ES \_ NUMBER.**

Los campos de dígito alternativo, %y caracteres alfanuméricos alternativos, ^, ?, y permiten que las acciones personalizadas diferencien entre los campos de una manera que se pueda controlar mediante la máscara, por ejemplo, ^ se puede usar para los campos que deben estar en \` mayúsculas.

 

 




