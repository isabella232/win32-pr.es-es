---
title: Instrucción MENUITEM
description: Define un elemento de menú.
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- Menús de instrucción MENUITEM y otros recursos
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45bca50025e1c9136c22166d6d3f758c5c9b5819a9328d33d375195285f1d4f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092195"
---
# <a name="menuitem-statement"></a>Instrucción MENUITEM

Define un elemento de menú.

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Texto*
</dt> <dd>

Nombre del elemento de menú.

La cadena puede contener los caracteres de escape **\\ t** **\\ y**. El **\\ carácter t** inserta una pestaña en la cadena y se usa para alinear texto en columnas. Los caracteres de tabulación solo se deben usar en los menús, no en las barras de menú. (Para obtener información sobre los menús, vea [**Recursos POPUP).**](popup-resource.md) El **\\ carácter alinea** todo el texto que le sigue se vacía directamente en la barra de menús o en el menú emergente.

</dd> <dt>

<span id="result"></span><span id="RESULT"></span>*Resultado*
</dt> <dd>

Número que especifica el resultado generado cuando el usuario selecciona el elemento de menú. Este parámetro toma un valor entero. Los resultados del elemento de menú siempre son enteros; cuando el usuario hace clic en el nombre del elemento de menú, el resultado se envía a la ventana que posee el menú.

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*
</dt> <dd>

Apariencia del elemento de menú. Este parámetro opcional toma una o varias de las siguientes opciones de menú redefinidos, separadas por comas o espacios.



| Opción           | Descripción                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Comprobado**      | El elemento de menú tiene una marca de verificación junto a él.                                                                                                                                |
| **Gris**       | El elemento de menú está inicialmente inactivo y aparece en el menú en gris o en un tono claro del color de texto del menú. Esta opción no se puede usar con la **opción INACTIVE.** |
| **Ayuda**         | Identifica un elemento de ayuda. Esta opción no tiene ningún efecto en la apariencia del elemento de menú.                                                                                 |
| **Inactivo**     | Se muestra el elemento de menú, pero no se puede seleccionar. Esta opción no se puede usar con la **opción GRAYED.**                                                              |
| **MENUBARBREAK** | Igual que **MENUBREAK,** salvo que para los menús emergentes, separa la nueva columna de la columna anterior con una línea vertical.                                             |
| **MENUBREAK**    | Coloca el elemento de menú en una nueva línea para los elementos estáticos de la barra de menús. En el caso de los menús, coloca el elemento de menú en una nueva columna sin ninguna línea divisora entre las columnas.           |



 

</dd> <dt>

<span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MENUITEM SEPARATOR**
</dt> <dd>

El **formulario MENUITEM SEPARATOR** de la instrucción **MENUITEM** crea un elemento de menú inactivo que actúa como barra divisora entre dos elementos de menú activos de un menú.

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de las **instrucciones MENUITEM** y **MENUITEM SEPARATOR:**

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Menú**](menu-resource.md)
</dt> <dt>

[**Popup**](popup-resource.md)
</dt> </dl>

 

 




