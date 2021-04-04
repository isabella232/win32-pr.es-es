---
title: Archivo de Resource-Definition de ejemplo
description: Archivo de script de ejemplo que define los recursos de una aplicación denominada Shapes.
ms.assetid: 0362b1be-7671-4685-8eb8-bff502224939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e6a870b4b63b0e88e5ddcd069e8318e4bdb750
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076063"
---
# <a name="sample-resource-definition-file"></a>Archivo de Resource-Definition de ejemplo

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

La instrucción de [**cursor**](cursor-resource.md) nombra el recurso de cursor de la aplicación ShapesCursor y especifica las formas de archivo de cursor. CUR, que contiene la imagen de ese cursor.

La instrucción [**Icon**](icon-resource.md) nombra el recurso de icono de la aplicación ShapesIcon y especifica las formas de archivo de icono. ICO, que contiene la imagen de ese icono.

La instrucción de [**menú**](menu-resource.md) define un menú de la aplicación denominado **ShapesMenu**, un menú emergente con cinco elementos de menú.

El cuerpo de la definición de menú, incluido entre las llaves, o las palabras clave **Begin** y **End** , especifica cada elemento de menú y el identificador de menú que se devuelve cuando el usuario selecciona ese elemento. Por ejemplo, el primer elemento del menú, **Clear**, devuelve el identificador de menú \_ sin cifrar cuando el usuario lo selecciona. Los identificadores de menú se definen en el archivo de encabezado de la aplicación, SHAPEs. H.

 

 




