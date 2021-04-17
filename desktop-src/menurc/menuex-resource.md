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
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717505"
---
# <a name="menuex-resource"></a>Recurso MENUEX

Define el contenido de un recurso de menú. Un recurso de menú es una colección de información que define la apariencia y la función de un menú de la aplicación. Un menú es una herramienta de entrada especial que permite a un usuario seleccionar comandos y abrir submenús en una lista de elementos de menú. También define lo siguiente:

-   Los identificadores de ayuda de los menús.
-   Identificadores de los menús.
-   Uso de las marcas de tipo **MFT \_ \** _ y estado de _*MFS \_ \**_ . Para obtener más información sobre estas marcas, consulte la estructura [_ *MENUITEMINFO* *](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="MENUITEM"></span><span id="menuitem"></span>[**OBJETOS**](menuitem-statement.md)
</dt> <dd>

Define un elemento de menú.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

Cadena que contiene el texto del elemento de menú. Para obtener más información, vea [**MenuItem**](menuitem-statement.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*sesión*
</dt> <dd>

Expresión numérica que indica el identificador del elemento de menú.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*automáticamente*
</dt> <dd>

Expresión numérica que indica el tipo de elemento de menú para usar los valores de tipo de MFT predefinidos \_ \* , incluya la siguiente instrucción en el archivo. RC:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*State*
</dt> <dd>

Expresión numérica que indica el estado del elemento de menú para usar los valores de estado de la MFS predefinidos \_ \* , incluya la siguiente instrucción en su. Archivo RC:`#include "winuser.h"`

</dd> </dl> </dd> <dt>

<span id="POPUP"></span><span id="popup"></span>[**EMERGENTE**](popup-resource.md)
</dt> <dd>

Define un elemento de menú que tiene un submenú asociado a él.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

Cadena que contiene el texto del elemento de menú.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*sesión*
</dt> <dd>

Expresión numérica que indica el identificador del elemento de menú.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*automáticamente*
</dt> <dd>

Expresión numérica que indica el tipo de elemento de menú para usar los valores de tipo de MFT predefinidos \_ \* , incluya la siguiente instrucción en su. Archivo RC:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*State*
</dt> <dd>

Expresión numérica que indica el estado del elemento de menú para usar los valores de estado de la MFS predefinidos \_ \* , incluya la siguiente instrucción en el archivo. RC:`#include "winuser.h"`

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*
</dt> <dd>

Expresión numérica que indica el identificador usado para identificar el menú durante el procesamiento de la [**\_ ayuda de WM**](../shell/wm-help.md) .

</dd> </dl> </dd> <dt>

<span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*
</dt> <dd>

Contiene cualquier combinación de las instrucciones [**MenuItem**](menuitem-statement.md) y [**popup**](popup-resource.md) .

</dd> </dl>

Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores. Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).

## <a name="remarks"></a>Observaciones

Las operaciones aritméticas y booleanas válidas que se pueden incluir en cualquiera de las expresiones numéricas de las instrucciones de **MENUEX** son las siguientes:

-   Agregar (' + ')
-   Resta ('-')
-   Unario menos ('-')
-   Unario no (' ~ ')
-   Y (' & ')
-   O (' \| ')

## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de los menús](./using-menus.md)
</dt> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**SUS**](characteristics-statement.md)
</dt> <dt>

[**DIÁLOGO**](dialog-resource.md)
</dt> <dt>

[**MÓDULO**](language-statement.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**OBJETOS**](menuitem-statement.md)
</dt> <dt>

[**EMERGENTE**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versión**](version-statement.md)
</dt> </dl>

 

 
