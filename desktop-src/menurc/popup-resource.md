---
title: Recurso POPUP
description: Define un elemento de menú que puede contener elementos de menú y submenús.
ms.assetid: afca21c7-605e-4354-b6ec-576b81389b69
keywords:
- Menús de recursos POPUP y otros recursos
topic_type:
- apiref
api_name:
- POPUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f134b2d5801bc5003be6f45b42d13f1668c2e684b5f63fe0aed1f2c9c0400860
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952360"
---
# <a name="popup-resource"></a>Recurso POPUP

Define un elemento de menú que puede contener elementos de menú y submenús.

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Texto*
</dt> <dd>

Cadena que contiene el nombre del menú. Esta cadena debe ir entre comillas dobles (**"**).

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*
</dt> <dd>

Este parámetro especifica opciones de menú redefinidos que especifican la apariencia del elemento de menú. Este parámetro opcional puede ser uno o varios de los siguientes.



| Opción           | Descripción                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Comprobado**      | El elemento de menú tiene una marca de verificación junto a él. Esta opción no es válida para un menú de nivel superior.                                                                                 |
| **Gris**       | El elemento de menú está inicialmente inactivo y aparece en el menú en gris o en un tono claro del color del texto del menú. Esta opción no se puede usar con la **opción INACTIVE.** |
| **Ayuda**         | Identifica un elemento de ayuda. El elemento de menú se coloca en la posición más a la derecha de la barra de menús.                                                                            |
| **Inactivo**     | Se muestra el elemento de menú, pero no se puede seleccionar. Esta opción no se puede usar con la **opción GRAYED.**                                                              |
| **MENUBARBREAK** | Igual que **MENUBREAK,** salvo que para los menús emergentes, separa la nueva columna de la columna antigua con una línea vertical.                                             |
| **MENUBREAK**    | Coloca el elemento de menú en una nueva línea para los elementos estáticos de la barra de menús. Para los menús, coloca el elemento de menú en una nueva columna sin ninguna línea divisora entre las columnas.           |



 

</dd> </dl>

Algunos atributos también se admiten por compatibilidad con versiones anteriores. Para más información, consulte [Atributos de recursos comunes.](common-resource-attributes.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la **instrucción POPUP:**

``` syntax
chem MENU
{
    POPUP "&Elements"
    {
         MENUITEM "&Oxygen", 200
         MENUITEM "&Carbon", 201, CHECKED
         MENUITEM "&Hydrogen", 202
         MENUITEM SEPARATOR
         MENUITEM "&Sulfur", 203
         MENUITEM "Ch&lorine", 204
    } 
    POPUP "&Compounds"
    {
         POPUP "&Sugars"
         {
            MENUITEM "&Glucose", 301
            MENUITEM "&Sucrose", 302, CHECKED
            MENUITEM "&Lactose", 303, MENUBREAK
            MENUITEM "&Fructose", 304
         }
         POPUP "&Acids"
         {
              "&Hydrochloric", 401
              "&Sulfuric", 402
         }
    }
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Menú**](menu-resource.md)
</dt> <dt>

[**Menuitem**](menuitem-statement.md)
</dt> </dl>

 

 




