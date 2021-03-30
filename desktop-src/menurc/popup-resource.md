---
title: Recurso POPUP
description: Define un elemento de menú que puede contener elementos de menú y submenús.
ms.assetid: afca21c7-605e-4354-b6ec-576b81389b69
keywords:
- Menús EMERGENTEs de recursos y otros recursos
topic_type:
- apiref
api_name:
- POPUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c7a1af3bd8ed9aae8908aa7ff926a3f4799ee5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148925"
---
# <a name="popup-resource"></a>Recurso POPUP

Define un elemento de menú que puede contener elementos de menú y submenús.

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*negrita*
</dt> <dd>

Cadena que contiene el nombre del menú. Esta cadena se debe incluir entre comillas dobles (**"**).

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*
</dt> <dd>

Este parámetro especifica las opciones de menú redefinidas que especifican la apariencia del elemento de menú. Este parámetro opcional puede ser uno o varios de los siguientes.



| Opción           | Descripción                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **INCORPORA**      | El elemento de menú tiene una marca de verificación junto a él. Esta opción no es válida para un menú de nivel superior.                                                                                 |
| **ATENUADO**       | El elemento de menú está inicialmente inactivo y aparece en el menú en gris o en una sombra iluminada del color del texto de menú. Esta opción no se puede usar con la opción **inactiva** . |
| **Ayuda**         | Identifica un elemento de ayuda. El elemento de menú se coloca en la posición más a la derecha en la barra de menús.                                                                            |
| **INACTIVA**     | Se muestra el elemento de menú, pero no se puede seleccionar. Esta opción no se puede usar con la opción **atenuada** .                                                              |
| **MENUBARBREAK** | Igual que **MENUBREAK** , excepto en el caso de los menús emergentes, separa la nueva columna de la antigua con una línea vertical.                                             |
| **MENUBREAK**    | Coloca el elemento de menú en una nueva línea para los elementos de barra de menús estáticos. En los menús, coloca el elemento de menú en una nueva columna sin ninguna línea dividida entre las columnas.           |



 

</dd> </dl>

Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores. Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se muestra el uso de la instrucción **popup** :

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

[**MENU**](menu-resource.md)
</dt> <dt>

[**OBJETOS**](menuitem-statement.md)
</dt> </dl>

 

 




