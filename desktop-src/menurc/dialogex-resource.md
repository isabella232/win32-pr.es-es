---
title: Recurso DIALOGEX
description: Define un cuadro de diálogo. | Recurso DIALOGEX
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- Menús de recursos DIALOGEX y otros recursos
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd55bfb06b678742aa5e356c9e62b14229aa8d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252429"
---
# <a name="dialogex-resource"></a>Recurso DIALOGEX

Define un cuadro de diálogo. La instrucción define la posición y las dimensiones del cuadro de diálogo en la pantalla, así como el estilo del cuadro de diálogo. También define lo siguiente:

-   Los IDs de ayuda en el propio cuadro de diálogo, así como en los controles dentro del cuadro de diálogo.
-   Uso de la [**instrucción EXSTYLE**](exstyle-statement.md) para el propio cuadro de diálogo, así como en los controles del cuadro de diálogo.
-   Valores de peso de fuente y cursiva para la fuente que se va a usar en el cuadro de diálogo.
-   Datos específicos del control para los controles del cuadro de diálogo.
-   Uso de los nombres de clase del sistema **predefinidos BEDIT,** **IEDIT** y **HEDIT.**

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nombre único o un valor entero único de 16 bits sin signo que identifica el cuadro de diálogo.

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Ubicación en la pantalla del lado izquierdo del cuadro de diálogo, en unidades de diálogo.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Ubicación en la pantalla de la parte superior del cuadro de diálogo, en unidades de diálogo.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Ancho*
</dt> <dd>

Ancho del cuadro de diálogo, en unidades de diálogo.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*Altura*
</dt> <dd>

Alto del cuadro de diálogo, en unidades de diálogo.

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*
</dt> <dd>

Expresión numérica que indica el identificador usado para identificar el cuadro de diálogo durante el [**procesamiento de WM \_ HELP.**](../shell/wm-help.md)

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*
</dt> <dd>

Opciones para el cuadro de diálogo. Puede ser cero o más de las siguientes instrucciones.



| .                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CAPTION** "*text*"                                              | Título del cuadro de diálogo si tiene una barra de título. Para obtener más información, vea [**CAPTION (Instrucción).**](caption-statement.md)                                                                                                                                                                                                                                                                                                                                                            |
| **CHARACTERISTICS** *dword*                                       | Valor **DWORD** definido por el usuario para que lo usen las herramientas de recursos. El sistema no usa este valor. Para obtener más información, vea [**CHARACTERISTICS (Instrucción**](characteristics-statement.md)).                                                                                                                                                                                                                                                                                               |
| **Clase**_CLASS_                                                  | Entero de 16 bits sin signo o cadena, entre comillas dobles ("), que identifica la clase del cuadro de diálogo. Para obtener más información, vea [**CLASS (Instrucción**](class-statement.md)).                                                                                                                                                                                                                                                                                     |
| **EXSTYLE** =  *estilos extendidos*                                    | Estilo de ventana extendido del cuadro de diálogo. Para obtener más información, vea [**EXSTYLE (Instrucción).**](exstyle-statement.md)                                                                                                                                                                                                                                                                                                                                                                    |
| **FONT** *apunta a*, " tipo de *letra*", *peso,* *cursiva,* *juego de caracteres* | Tamaño de punto y tipo de letra de la fuente. Para *weight*, use los valores **FW \_ \** _ definidos en WinGDI.h. Para _italic*, especifique TRUE para usar una fuente en cursiva, FALSE en caso contrario. Para *charset*, use el valor definido en el **miembro lfCharSet** de la [**estructura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta) Para obtener la fuente definitiva de un cuadro de diálogo, una aplicación debe especificar *el juego de caracteres* junto con otras propiedades de fuente. Para obtener más información, vea [**Font (Instrucción).**](font-statement.md) |
| **Language** *Language*, *sublanguage*                            | Idioma del cuadro de diálogo. Para obtener más información, vea [**LANGUAGE (Instrucción**](language-statement.md)).                                                                                                                                                                                                                                                                                                                                                                               |
| **MENU** *menuname*                                               | Menú que se va a usar. Este valor es el nombre del menú o su identificador entero. Para obtener más información, vea [**INSTRUCCIÓN MENU**](menu-statement.md).                                                                                                                                                                                                                                                                                                                             |
| **Estilos STYLE**                                                 | Estilos del cuadro de diálogo. Para obtener más información, vea [**STYLE (Instrucción).**](style-statement.md)                                                                                                                                                                                                                                                                                                                                                                                       |
| **VERSION** *dword*                                               | Valor **DWORD** definido por el usuario. Esta instrucción está pensada para su uso por herramientas de recursos adicionales y el sistema no la usa. Para obtener más información, vea [**VERSION (Instrucción ).**](version-statement.md)                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*control-statements*
</dt> <dd>

El cuerpo del **recurso DIALOGEX** se forma de cualquier número de instrucciones de control. Hay cuatro familias de instrucciones de control: genéricas, estáticas, de botón y de edición. Para obtener más información, vea la sección Comentarios.

</dd> </dl>

Algunos atributos también se admiten para la compatibilidad con versiones anteriores. Para obtener más información, vea [Atributos de recursos comunes](common-resource-attributes.md).

## <a name="remarks"></a>Observaciones

Las operaciones válidas que pueden estar contenidas en cualquiera de las expresiones numéricas de las instrucciones de **DIALOGEX** son las siguientes:

-   Agregar ('+')
-   Restar ('-')
-   Unario menos ('-')
-   NOT unario ('~')
-   AND ('&')
-   OR (' \| ')

El cuerpo del recurso se forma de instrucciones genéricas, estáticas, de botón y de control de edición. Aunque cada una de estas familias de instrucciones usa una sintaxis diferente para definir características específicas de sus controles, todas comparten una sintaxis común para definir la posición, el tamaño, los estilos extendidos, el número de identificación de ayuda y los datos específicos del control. Para obtener más información, vea [Parámetros de control comunes](common-control-parameters.md).

### <a name="generic-control-statements"></a>Instrucciones de control genérico

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Texto de ventana para el control. Para obtener más información, vea [Parámetros de control comunes](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Identificador de control. Para obtener más información, vea [Parámetros de control comunes](common-control-parameters.md).

</dd> <dt>

<span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*Classname*
</dt> <dd>

Nombre de la clase. Puede ser una cadena entre comillas dobles (") o una de las siguientes clases predefinidas del sistema: **BUTTON,** **STATIC,** **EDIT,** **LISTBOX,** **SCROLLBAR** o **COMBOBOX.**

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Los estilos de ventana **(WS \_ \* *_, _* BS \_ \* *_, _* SS \_ \* *_, _* ES \_ \* *_, _* LBS \_ \* *_, _* SBS \_ \* *_, y _* CBS \_ \*** style values definidos en Winuser.H se pueden usar agregando un elemento include al archivo .rc: `#include "winuser.h"` ). Para obtener más información, vea [Estilos de ventana](/windows/desktop/winmsg/window-styles).

</dd> </dl>

### <a name="static-control-statements"></a>Instrucciones de control estático

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*
</dt> <dd>

**LTEXT,** **RTEXT** o **CTEXT**.

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Texto de ventana para el control. Para obtener más información, vea [Parámetros de control comunes](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Identificador de control. Para obtener más información, vea [Parámetros de control comunes](common-control-parameters.md).

</dd> </dl>

### <a name="button-control-statements"></a>Instrucciones de control de botón

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*
</dt> <dd>

**AUTO3STATE,** **AUTOCHECKBOX,** **AUTORADIOBUTTON**, **CHECKBOX**, **PUSHBOX,** **PUSHBUTTON,** **RADIOBUTTON,** **STATE3** o **USERBUTTON**.

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Texto de ventana para el control. Para obtener más información, vea [Parámetros de control comunes](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Identificador de control. Para obtener más información, vea [Parámetros de control comunes](common-control-parameters.md).

</dd> </dl>

### <a name="edit-control-statements"></a>Editar instrucciones de control

``` syntax
editClass id
```

<dl> <dt>

<span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*
</dt> <dd>

**EDITTEXT,** **BEDIT,** **HEDIT** o **IEDIT**.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Identificador de control. Para obtener más información, vea [Parámetros de control comunes](common-control-parameters.md).

</dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar cuadros de diálogo](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**CARACTERÍSTICAS**](characteristics-statement.md)
</dt> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[**CreateDialog**](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**Cuadro de diálogo**](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**LENGUA**](language-statement.md)
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[MENÚ](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**VERSIÓN**](version-statement.md)
</dt> </dl>

 

 
