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
# <a name="sample-resource-definition-file"></a><span data-ttu-id="48e3c-103">Archivo de Resource-Definition de ejemplo</span><span class="sxs-lookup"><span data-stu-id="48e3c-103">Sample Resource-Definition File</span></span>

<span data-ttu-id="48e3c-104">En el ejemplo siguiente se muestra un archivo de script que define los recursos de una aplicación denominada Shapes:</span><span class="sxs-lookup"><span data-stu-id="48e3c-104">The following example shows a script file that defines the resources for an application named Shapes:</span></span>

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

<span data-ttu-id="48e3c-105">La instrucción de [**cursor**](cursor-resource.md) nombra el recurso de cursor de la aplicación ShapesCursor y especifica las formas de archivo de cursor. CUR, que contiene la imagen de ese cursor.</span><span class="sxs-lookup"><span data-stu-id="48e3c-105">The [**CURSOR**](cursor-resource.md) statement names the application's cursor resource ShapesCursor and specifies the cursor file SHAPES.CUR, which contains the image for that cursor.</span></span>

<span data-ttu-id="48e3c-106">La instrucción [**Icon**](icon-resource.md) nombra el recurso de icono de la aplicación ShapesIcon y especifica las formas de archivo de icono. ICO, que contiene la imagen de ese icono.</span><span class="sxs-lookup"><span data-stu-id="48e3c-106">The [**ICON**](icon-resource.md) statement names the application's icon resource ShapesIcon and specifies the icon file SHAPES.ICO, which contains the image for that icon.</span></span>

<span data-ttu-id="48e3c-107">La instrucción de [**menú**](menu-resource.md) define un menú de la aplicación denominado **ShapesMenu**, un menú emergente con cinco elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="48e3c-107">The [**MENU**](menu-resource.md) statement defines an application menu named **ShapesMenu**, a pop-up menu with five menu items.</span></span>

<span data-ttu-id="48e3c-108">El cuerpo de la definición de menú, incluido entre las llaves, o las palabras clave **Begin** y **End** , especifica cada elemento de menú y el identificador de menú que se devuelve cuando el usuario selecciona ese elemento.</span><span class="sxs-lookup"><span data-stu-id="48e3c-108">The body of the menu definition, enclosed by the curly braces, or the **BEGIN** and **END** keywords, specifies each menu item and the menu identifier that is returned when the user selects that item.</span></span> <span data-ttu-id="48e3c-109">Por ejemplo, el primer elemento del menú, **Clear**, devuelve el identificador de menú \_ sin cifrar cuando el usuario lo selecciona.</span><span class="sxs-lookup"><span data-stu-id="48e3c-109">For example, the first item on the menu, **Clear**, returns the menu identifier ID\_CLEAR when the user selects it.</span></span> <span data-ttu-id="48e3c-110">Los identificadores de menú se definen en el archivo de encabezado de la aplicación, SHAPEs. H.</span><span class="sxs-lookup"><span data-stu-id="48e3c-110">The menu identifiers are defined in the application header file, SHAPES.H.</span></span>

 

 




