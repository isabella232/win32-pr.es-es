---
title: Definir nombres para el preprocesador
description: Puede especificar la compilación condicional en un script, en función de si se define un nombre en la línea de comandos RC con la opción/d, o en el archivo o en un archivo de inclusión con la Directiva \ define.
ms.assetid: bc72911e-2aca-46a4-b6c1-60cc8ed7d82f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64b339959ace5a70d83fa8ee8beb615f1bc5ce4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356796"
---
# <a name="defining-names-for-the-preprocessor"></a>Definir nombres para el preprocesador

Puede especificar la compilación condicional en un script, en función de si se define un nombre en la línea de comandos RC con la opción **/d** , o en el archivo o en un archivo de inclusión con la directiva [**\# define**](-define.md) .

Por ejemplo, supongamos que la aplicación tiene un menú emergente que solo debe aparecer con versiones de depuración de la aplicación. Al compilar la aplicación para su uso normal, el menú no se incluye. En el ejemplo siguiente se muestran las instrucciones que se pueden agregar al archivo de definición de recursos para definir un menú Depurar:

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

**RC-d depuración MyApp. RC**

Para compilar recursos para una versión normal de la aplicación, uno que no incluya el menú Depurar, podría usar el siguiente comando:

**RC MyApp. RC**

 

 




