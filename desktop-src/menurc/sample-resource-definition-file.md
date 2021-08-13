---
title: Archivo de Resource-Definition ejemplo
description: Archivo de script de ejemplo que define los recursos de una aplicación denominada Shapes.
ms.assetid: 0362b1be-7671-4685-8eb8-bff502224939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141258148b4e7a21d625a44b7f03d5e383c318d10447e050891f32b397c4283d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119226005"
---
# <a name="sample-resource-definition-file"></a>Archivo de Resource-Definition ejemplo

En el ejemplo siguiente se muestra un archivo de script que define los recursos de una aplicación denominada Shapes:

``` syntax
#include "shapes.h"

ShapesCursor  CURSOR  SHAPES.CUR
ShapesIcon    ICON    SHAPES.ICO

ShapesMenu MENU
{
    POPUP "&Shape"
    {
        MENUITEM "&Clear", ID_CLEAR
        MENUITEM "&Rectangle", ID_RECT
        MENUITEM "&Triangle", ID_TRIANGLE
        MENUITEM "&Star", ID_STAR
        MENUITEM "&Ellipse", ID_ELLIPSE
    }
}
```

La [**instrucción CURSOR**](cursor-resource.md) asigna el nombre ShapesCursor al recurso de cursor de la aplicación y especifica el archivo de cursor SHAPES. CUR, que contiene la imagen de ese cursor.

La [**instrucción ICON**](icon-resource.md) nombra el recurso de icono de la aplicación ShapesIcon y especifica el archivo de icono SHAPES. ICO, que contiene la imagen de ese icono.

La [**instrucción MENU**](menu-resource.md) define un menú de aplicación denominado **ShapesMenu**, un menú emergente con cinco elementos de menú.

El cuerpo de la definición de menú, entre llaves o las palabras clave **BEGIN** y **END,** especifica cada elemento de menú y el identificador de menú que se devuelve cuando el usuario selecciona ese elemento. Por ejemplo, el primer elemento del menú, **Borrar**, devuelve el identificador de menú \_ CLEAR cuando el usuario lo selecciona. Los identificadores de menú se definen en el archivo de encabezado de aplicación, SHAPES.H.

 

 




