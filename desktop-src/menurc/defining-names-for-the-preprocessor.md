---
title: Definición de nombres para el preprocesador
description: Puede especificar la compilación condicional en un script, en función de si se define un nombre en la línea de comandos RC con la opción /d, en el archivo o en un archivo de incluir con la directiva \define.
ms.assetid: bc72911e-2aca-46a4-b6c1-60cc8ed7d82f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3bcf9c02b5a4da4487b0c82de8d8b0223662cb30f9529e82204fc66a3de91cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972114"
---
# <a name="defining-names-for-the-preprocessor"></a>Definición de nombres para el preprocesador

Puede especificar la compilación condicional en un script, en función de si se define un nombre en la línea de comandos RC con la opción **/d,** en el archivo o en un archivo de incluir con la [**\# directiva define.**](-define.md)

Por ejemplo, suponga que la aplicación tiene un menú emergente que solo debería aparecer con las versiones de depuración de la aplicación. Al compilar la aplicación para su uso normal, el menú no se incluye. En el ejemplo siguiente se muestran las instrucciones que se pueden agregar al archivo de definición de recursos para definir un menú Depurar:

``` syntax
#include <windows.h>

MainMenu MENU
{
    //. . .
#ifdef DEBUG
    POPUP "&Debug"
    {
        MENUITEM "&Memory usage", ID_MEMORY
        MENUITEM "&Walk data heap", ID_WALK_HEAP
    }
#endif
}
```

Al compilar recursos para una versión de depuración de la aplicación, puede incluir el menú Depurar mediante el comando siguiente:

**rc -d DEBUG myapp.rc**

Para compilar recursos para una versión normal de la aplicación?, ¿una que no incluya el menú Depurar?, puede usar el siguiente comando:

**rc myapp.rc**

 

 




