---
title: Recurso MENUEX
description: Define el contenido de un recurso de menú. | Recurso MENUEX
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- Menús de recursos de MENUEX y otros recursos
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ed379fb97d2795a166571fb48cde2c233021a33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571624"
---
# <a name="menuex-resource"></a>Recurso MENUEX

Define el contenido de un recurso de menú. Un recurso de menú es una colección de información que define la apariencia y la función de un menú de aplicación. Un menú es una herramienta de entrada especial que permite a un usuario seleccionar comandos y abrir submenús desde una lista de elementos de menú. También define lo siguiente:

-   Identificadores de ayuda en los menús.
-   Identificadores en los menús.
-   Uso de las marcas de tipo **MFT \_ \** _ y las marcas de estado _*\_ \* MFS.*_ Para obtener más información sobre estas marcas, vea [la estructura _ *MENUITEMINFO.* *](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)
</dt> <dd>

Define un elemento de menú.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

Cadena que contiene el texto del elemento de menú. Para obtener más información, vea [**MENUITEM**](menuitem-statement.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Expresión numérica que indica el identificador del elemento de menú.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Tipo*
</dt> <dd>

Expresión numérica que indica el tipo del elemento de menú Para usar los valores de tipo de MFT predefinidos, incluya la siguiente instrucción \_ \* en el archivo .rc:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*Estado*
</dt> <dd>

Expresión numérica que indica el estado del elemento de menú Para usar los valores de estado de MFS \_ \* predefinidos, incluya la siguiente instrucción en . Archivo RC:`#include "winuser.h"`

</dd> </dl> </dd> <dt>

<span id="POPUP"></span><span id="popup"></span>[**POPUP**](popup-resource.md)
</dt> <dd>

Define un elemento de menú que tiene un submenú asociado.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

Cadena que contiene el texto del elemento de menú.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Expresión numérica que indica el identificador del elemento de menú.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Tipo*
</dt> <dd>

Expresión numérica que indica el tipo del elemento de menú Para usar los valores de tipo de MFT \_ \* predefinidos, incluya la siguiente instrucción en . Archivo RC:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*Estado*
</dt> <dd>

Expresión numérica que indica el estado del elemento de menú Para usar los valores de estado MFS predefinidos, incluya la siguiente instrucción \_ \* en el archivo .rc:`#include "winuser.h"`

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*
</dt> <dd>

Expresión numérica que indica el identificador utilizado para identificar el menú durante el [**procesamiento de WM \_ HELP.**](../shell/wm-help.md)

</dd> </dl> </dd> <dt>

<span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*
</dt> <dd>

Contiene cualquier combinación de las [**instrucciones MENUITEM**](menuitem-statement.md) [**y POPUP.**](popup-resource.md)

</dd> </dl>

Algunos atributos también se admiten por compatibilidad con versiones anteriores. Para más información, consulte [Atributos de recursos comunes.](common-resource-attributes.md)

## <a name="remarks"></a>Observaciones

Las operaciones aritméticas y booleanas válidas que se pueden incluir en cualquiera de las expresiones numéricas de las instrucciones **de MENUEX** son las siguientes:

-   Agregar ('+')
-   Restar ('-')
-   Unario menos ('-')
-   UNARY NOT ('~')
-   AND ('&')
-   OR (' \| ')

## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de los menús](./using-menus.md)
</dt> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**CARACTERÍSTICAS**](characteristics-statement.md)
</dt> <dt>

[**DIÁLOGO**](dialog-resource.md)
</dt> <dt>

[**LENGUA**](language-statement.md)
</dt> <dt>

[**MENÚ**](menu-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> <dt>

[**POPUP**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**VERSIÓN**](version-statement.md)
</dt> </dl>

 

 
