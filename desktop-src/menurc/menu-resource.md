---
title: Recurso de menú
description: Define el contenido de un recurso de menú. | Recurso de menú
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- Menús de recursos de menú y otros recursos
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5cdb564c7bf012255b339a13691d2ecf214a86
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717516"
---
# <a name="menu-resource"></a>Recurso de menú

Define el contenido de un recurso de menú. Un recurso de menú es una colección de información que define la apariencia y la función de un menú de la aplicación. Un menú es una herramienta de entrada especial que permite a un usuario seleccionar comandos y abrir submenús en una lista de elementos de menú.

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*
</dt> <dd>

Número que identifica el menú. Este valor es una cadena única o un valor entero de 16 bits sin signo único en el intervalo de 1 a 65.535.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instrucciones opcionales*
</dt> <dd>

Este parámetro puede ser cero de las siguientes instrucciones.



| .                                                        | Descripción                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Características**](characteristics-statement.md) *DWORD*     | Información definida por el usuario sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**características**](characteristics-statement.md). |
| [](language-statement.md) *Idioma* del idioma, *subidioma* | Idioma del recurso. Para obtener más información, vea [**Language**](language-statement.md).                                                                                            |
| [**Versión**](version-statement.md) *DWORD*                     | Número de versión definido por el usuario para el recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**versión**](version-statement.md).              |



 

</dd> </dl>

Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores. Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).

## <a name="examples"></a>Ejemplos

El siguiente es un ejemplo de una instrucción de **menú** completa:

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

## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de los menús](./using-menus.md)
</dt> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**SUS**](characteristics-statement.md)
</dt> <dt>

[**MÓDULO**](language-statement.md)
</dt> <dt>

[**MENUEX**](menuex-resource.md)
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

 

 
