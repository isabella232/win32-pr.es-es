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
# <a name="defining-names-for-the-preprocessor"></a><span data-ttu-id="a11c5-103">Definir nombres para el preprocesador</span><span class="sxs-lookup"><span data-stu-id="a11c5-103">Defining Names for the Preprocessor</span></span>

<span data-ttu-id="a11c5-104">Puede especificar la compilación condicional en un script, en función de si se define un nombre en la línea de comandos RC con la opción **/d** , o en el archivo o en un archivo de inclusión con la directiva [**\# define**](-define.md) .</span><span class="sxs-lookup"><span data-stu-id="a11c5-104">You can specify conditional compilation in a script, based on whether a name is defined on the RC command line with the **/d** option, or in the file or an include file with the [**\#define**](-define.md) directive.</span></span>

<span data-ttu-id="a11c5-105">Por ejemplo, supongamos que la aplicación tiene un menú emergente que solo debe aparecer con versiones de depuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a11c5-105">For example, suppose your application has a pop-up menu that should appear only with debugging versions of the application.</span></span> <span data-ttu-id="a11c5-106">Al compilar la aplicación para su uso normal, el menú no se incluye.</span><span class="sxs-lookup"><span data-stu-id="a11c5-106">When you compile the application for normal use, the menu is not included.</span></span> <span data-ttu-id="a11c5-107">En el ejemplo siguiente se muestran las instrucciones que se pueden agregar al archivo de definición de recursos para definir un menú Depurar:</span><span class="sxs-lookup"><span data-stu-id="a11c5-107">The following example shows the statements that can be added to the resource-definition file to define a Debug menu:</span></span>

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

<span data-ttu-id="a11c5-108">Al compilar recursos para una versión de depuración de la aplicación, puede incluir el menú Depurar mediante el comando siguiente:</span><span class="sxs-lookup"><span data-stu-id="a11c5-108">When compiling resources for a debugging version of the application, you could include the Debug menu by using the following command:</span></span>

<span data-ttu-id="a11c5-109">**RC-d depuración MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="a11c5-109">**rc -d DEBUG myapp.rc**</span></span>

<span data-ttu-id="a11c5-110">Para compilar recursos para una versión normal de la aplicación, uno que no incluya el menú Depurar, podría usar el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="a11c5-110">To compile resources for a normal version of the application?one that does not include the Debug menu?you could use the following command:</span></span>

<span data-ttu-id="a11c5-111">**RC MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="a11c5-111">**rc myapp.rc**</span></span>

 

 




