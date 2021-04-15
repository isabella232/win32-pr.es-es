---
title: MENUITEM (instrucción)
description: Define un elemento de menú.
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- Menús de instrucciones MENUITEM y otros recursos
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2051b326b2f2f37c9e24e03bcb5e5116cf290a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105665763"
---
# <a name="menuitem-statement"></a>MENUITEM (instrucción)

Define un elemento de menú.

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*negrita*
</dt> <dd>

Nombre del elemento de menú.

La cadena puede contener los caracteres de escape **\\ t** y **\\ a**. El carácter **\\ t** inserta una tabulación en la cadena y se usa para alinear el texto en las columnas. Los caracteres de tabulación solo se deben usar en menús, no en barras de menús. (Para obtener información sobre los menús, vea [**elemento popup**](popup-resource.md)). El carácter **\\ a** alinea todo el texto que sigue a su derecha en la barra de menús o en el menú emergente.

</dd> <dt>

<span id="result"></span><span id="RESULT"></span>*da*
</dt> <dd>

Número que especifica el resultado generado cuando el usuario selecciona el elemento de menú. Este parámetro toma un valor entero. Los resultados de los elementos de menú siempre son enteros; Cuando el usuario hace clic en el nombre del elemento de menú, el resultado se envía a la ventana que posee el menú.

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*
</dt> <dd>

Apariencia del elemento de menú. Este parámetro opcional toma una o varias de las siguientes opciones de menú redefinidas, separadas por comas o espacios.



| Opción           | Descripción                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **INCORPORA**      | El elemento de menú tiene una marca de verificación junto a él.                                                                                                                                |
| **ATENUADO**       | El elemento de menú está inicialmente inactivo y aparece en el menú en gris o en una sombra iluminada del color del texto de menú. Esta opción no se puede usar con la opción **inactiva** . |
| **Ayuda**         | Identifica un elemento de ayuda. Esta opción no tiene ningún efecto en la apariencia del elemento de menú.                                                                                 |
| **INACTIVA**     | Se muestra el elemento de menú, pero no se puede seleccionar. Esta opción no se puede usar con la opción **atenuada** .                                                              |
| **MENUBARBREAK** | Igual que **MENUBREAK** , excepto en el caso de los menús emergentes, separa la nueva columna de la antigua con una línea vertical.                                             |
| **MENUBREAK**    | Coloca el elemento de menú en una nueva línea para los elementos de barra de menús estáticos. En los menús, coloca el elemento de menú en una nueva columna sin ninguna línea dividida entre las columnas.           |



 

</dd> <dt>

<span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**SEPARADOR MENUITEM**
</dt> <dd>

La forma del **SEparador MenuItem** de la instrucción **MenuItem** crea un elemento de menú inactivo que sirve como barra divisoria entre dos elementos de menú activos en un menú.

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de las instrucciones de **SEparador** **MenuItem** y MenuItem:

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**EMERGENTE**](popup-resource.md)
</dt> </dl>

 

 




