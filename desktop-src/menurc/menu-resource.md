---
title: Recurso MENU
description: Define el contenido de un recurso de menú. | Recurso MENU
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- Menús de recursos MENU y otros recursos
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5cdb564c7bf012255b339a13691d2ecf214a86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574741"
---
# <a name="menu-resource"></a>Recurso MENU

Define el contenido de un recurso de menú. Un recurso de menú es una colección de información que define la apariencia y la función de un menú de aplicación. Un menú es una herramienta de entrada especial que permite a un usuario seleccionar comandos y abrir submenús desde una lista de elementos de menú.

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*
</dt> <dd>

Número que identifica el menú. Este valor es una cadena única o un valor entero único de 16 bits sin signo en el intervalo de 1 a 65 535.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*
</dt> <dd>

Este parámetro puede ser cero de más de las instrucciones siguientes.



| .                                                        | Descripción                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHARACTERISTICS**](characteristics-statement.md) *dword*     | Información definida por el usuario sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**CHARACTERISTICS**](characteristics-statement.md). |
| [**Language**](language-statement.md) *Language*, *sublanguage* | Idioma del recurso. Para obtener más información, vea [**LANGUAGE**](language-statement.md).                                                                                            |
| [**VERSION**](version-statement.md) *dword*                     | Número de versión definido por el usuario para el recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**VERSION**](version-statement.md).              |



 

</dd> </dl>

Algunos atributos también se admiten por compatibilidad con versiones anteriores. Para más información, consulte [Atributos de recursos comunes.](common-resource-attributes.md)

## <a name="examples"></a>Ejemplos

A continuación se muestra un ejemplo de una instrucción **MENU** completa:

``` syntax
sample MENU
{
     MENUITEM "&Soup", 100
     MENUITEM "S&alad", 101
     POPUP "&Entree"
     {
          MENUITEM "&Fish", 200
          MENUITEM "&Chicken", 201, CHECKED
          POPUP "&Beef"
          {
               MENUITEM "&Steak", 301
               MENUITEM "&Prime Rib", 302
          }
     }
     MENUITEM "&Dessert", 103
}
```

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uso de los menús](./using-menus.md)
</dt> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**CARACTERÍSTICAS**](characteristics-statement.md)
</dt> <dt>

[**LENGUA**](language-statement.md)
</dt> <dt>

[**MENUEX**](menuex-resource.md)
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

 

 
