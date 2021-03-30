---
title: Recurso DIALOGEX
description: Define un cuadro de diálogo. | Recurso DIALOGEX
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- Menús de recursos de DIALOGEX y otros recursos
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd55bfb06b678742aa5e356c9e62b14229aa8d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280116"
---
# <a name="dialogex-resource"></a>Recurso DIALOGEX

Define un cuadro de diálogo. La instrucción define la posición y las dimensiones del cuadro de diálogo en la pantalla, así como el estilo del cuadro de diálogo. También define lo siguiente:

-   Los identificadores de la ayuda en el cuadro de diálogo en sí, así como en los controles del cuadro de diálogo.
-   Uso de la instrucción de [**ExStyle**](exstyle-statement.md) para el cuadro de diálogo en sí, así como en los controles del cuadro de diálogo.
-   Configuración de espesor de fuente y cursiva para la fuente que se va a utilizar en el cuadro de diálogo.
-   Datos específicos del control para los controles del cuadro de diálogo.
-   Uso de los nombres de clase del sistema predefinido **BEDIT**, **IEDIT** y **HEDIT** .

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nombre único o un valor entero de 16 bits sin signo único que identifica el cuadro de diálogo.

</dd> <dt>

<span id="x"></span><span id="X"></span>*x1*
</dt> <dd>

Ubicación en la pantalla del lado izquierdo del cuadro de diálogo, en unidades de cuadro de diálogo.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*sí*
</dt> <dd>

Ubicación en la pantalla de la parte superior del cuadro de diálogo, en unidades de cuadro de diálogo.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Ancho*
</dt> <dd>

Ancho del cuadro de diálogo, en unidades de cuadro de diálogo.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*alto*
</dt> <dd>

Alto del cuadro de diálogo, en unidades de cuadro de diálogo.

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*
</dt> <dd>

Expresión numérica que indica el identificador usado para identificar el cuadro de diálogo durante el procesamiento de la [**\_ ayuda de WM**](../shell/wm-help.md) .

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instrucciones opcionales*
</dt> <dd>

Opciones del cuadro de diálogo. Puede ser cero o más de las instrucciones siguientes.



| .                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título** de "*texto*"                                              | Título del cuadro de diálogo si tiene una barra de título. Para obtener más información, vea la [**instrucción Caption**](caption-statement.md).                                                                                                                                                                                                                                                                                                                                                            |
| **Características** *DWORD*                                       | Valor **DWORD** definido por el usuario para que lo usen las herramientas de recursos. El sistema no utiliza este valor. Para obtener más información, vea la [**instrucción Characteristics**](characteristics-statement.md).                                                                                                                                                                                                                                                                                               |
| _Clase de_ clase                                                  | Entero de 16 bits sin signo o cadena, entre comillas dobles ("), que identifica la clase del cuadro de diálogo. Para obtener más información, vea [**Class (instrucción**](class-statement.md)).                                                                                                                                                                                                                                                                                     |
| **EXstyle** =  *estilos extendidos*                                    | Estilo de ventana extendida del cuadro de diálogo. Para obtener más información, vea la [**instrucción de ExStyle**](exstyle-statement.md).                                                                                                                                                                                                                                                                                                                                                                    |
|  *Puntuación* de fuente, "tipo de *letra*", *peso*, *cursiva*, *juego de caracteres* | Tamaño de punto y tipo de letra de la fuente. En *peso*, use los valores ** \_ \* FW* _ definidos en WinGDI. h. En _italic *, especifique TRUE para utilizar una fuente en cursiva; de lo contrario, FALSE. Para *CharSet*, use el valor definido en el miembro **lfCharSet** de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . Para obtener la fuente definitiva de un cuadro de diálogo, una aplicación debe especificar *CharSet* junto con otras propiedades de fuente. Para obtener más información, vea la [**instrucción Font**](font-statement.md). |
|  *Idioma* del idioma, *subidioma*                            | Idioma del cuadro de diálogo. Para obtener más información, vea [**Language Statement**](language-statement.md).                                                                                                                                                                                                                                                                                                                                                                               |
|  *NombreMenú* de menú                                               | Menú que se va a usar. Este valor es el nombre del menú o su identificador entero. Para obtener más información, vea [**instrucción de menú**](menu-statement.md).                                                                                                                                                                                                                                                                                                                             |
|  *Estilos* de estilo                                                | Estilos del cuadro de diálogo. Para obtener más información, vea [**Style (instrucción**](style-statement.md)).                                                                                                                                                                                                                                                                                                                                                                                       |
| **Versión** *DWORD*                                               | Valor **DWORD** definido por el usuario. Esta instrucción está pensada para su uso por parte de herramientas de recursos adicionales y el sistema no la utiliza. Para obtener más información, vea la [**instrucción version**](version-statement.md).                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*instrucciones de control*
</dt> <dd>

El cuerpo del recurso **DIALOGEX** se compone de cualquier número de instrucciones de control. Hay cuatro familias de instrucciones de control: genérica, estática, de botón y de edición. Para obtener más información, vea la sección Comentarios.

</dd> </dl>

Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores. Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).

## <a name="remarks"></a>Observaciones

Las operaciones válidas que pueden incluirse en cualquiera de las expresiones numéricas de las instrucciones de **DIALOGEX** son las siguientes:

-   Agregar (' + ')
-   Resta ('-')
-   Unario menos ('-')
-   Unario no (' ~ ')
-   Y (' & ')
-   O (' \| ')

El cuerpo del recurso se compone de instrucciones de control genérico, estático, de botón y de edición. Aunque cada una de estas familias de instrucciones usa una sintaxis diferente para definir características específicas de sus controles, todos comparten una sintaxis común para definir la posición, el tamaño, los estilos extendidos, el número de identificación de la ayuda y los datos específicos del control. Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).

### <a name="generic-control-statements"></a>Instrucciones de control genérico

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Texto de la ventana para el control. Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*sesión*
</dt> <dd>

Identificador de control. Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).

</dd> <dt>

<span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*
</dt> <dd>

Nombre de la clase. Puede ser una cadena entre comillas dobles (") o una de las siguientes clases del sistema predefinidas: **Button**, **static**, **Edit**, **ListBox**, **ScrollBar** o **ComboBox**.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Los estilos de ventana (valores explícitos **WS \_ \* *_, _* BS \_ \* *_, _* SS \_ \* *_, _* es \_ \* *_, _* lb \_ \* *_, _* SBS \_ \* *_ y _* \_ \*** valor de estilo CBS definidos en Winuser. H se pueden usar agregando una inclusión al archivo. RC: `#include "winuser.h"` ). Para obtener más información, consulte [estilos de ventana](/windows/desktop/winmsg/window-styles).

</dd> </dl>

### <a name="static-control-statements"></a>Instrucciones de control estático

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*
</dt> <dd>

**LTEXT**, **RText** o **CTEXT**.

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Texto de la ventana para el control. Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*sesión*
</dt> <dd>

Identificador de control. Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).

</dd> </dl>

### <a name="button-control-statements"></a>Instrucciones de control de botón

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*
</dt> <dd>

**AUTO3STATE**, **autocheckbox**, **autoradiobutton**, **CheckBox**, **PUSHBOX**, **PUSHBUTTON**, **RADIOBUTTON**, **STATE3** o **USERBUTTON**.

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Texto de la ventana para el control. Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*sesión*
</dt> <dd>

Identificador de control. Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).

</dd> </dl>

### <a name="edit-control-statements"></a>Editar instrucciones de control

``` syntax
editClass id
```

<dl> <dt>

<span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*
</dt> <dd>

**EDITTEXT**, **BEDIT**, **HEDIT** o **IEDIT**.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*sesión*
</dt> <dd>

Identificador de control. Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).

</dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar cuadros de diálogo](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**SUS**](characteristics-statement.md)
</dt> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[**CreateDialog**](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**MÓDULO**](language-statement.md)
</dt> <dt>

[**NDPTECGDI**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[MENU](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versión**](version-statement.md)
</dt> </dl>

 

 
