---
title: Macros predefinidas
description: RC no admite las macros predefinidas de ANSI C ( \_ \_ Date \_ \_ , \_ \_ file \_ \_ , \_ \_ line \_ \_ , \_ \_ stdc \_ \_ , \_ \_ Time \_ \_ , \_ \_ timestamp \_ \_ ). Por lo tanto, no puede incluir estas macros en los archivos de encabezado que incluirá en el script de recursos.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 351674bc86ab56753bb49dba9e65edd97a7b1a04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148794"
---
# <a name="predefined-macros"></a><span data-ttu-id="d6a10-104">Macros predefinidas</span><span class="sxs-lookup"><span data-stu-id="d6a10-104">Predefined Macros</span></span>

<span data-ttu-id="d6a10-105">RC no admite las macros predefinidas de ANSI C (**\_ \_ Date \_ \_**, **\_ \_ file \_ \_**, **\_ \_ line \_ \_**, **\_ \_ stdc \_ \_**, **\_ \_ Time \_ , TIMESTAMP \_** **\_ \_ ). \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6a10-105">RC does not support the ANSI C predefined macros (**\_\_DATE\_\_**, **\_\_FILE\_\_**, **\_\_LINE\_\_**, **\_\_STDC\_\_**, **\_\_TIME\_\_**, **\_\_TIMESTAMP\_\_**).</span></span> <span data-ttu-id="d6a10-106">Por lo tanto, no puede incluir estas macros en los archivos de encabezado que incluirá en el script de recursos.</span><span class="sxs-lookup"><span data-stu-id="d6a10-106">Therefore, you cannot include these macros in header files that you will include in your resource script.</span></span>

<span data-ttu-id="d6a10-107">RC define RC \_ invocado, lo que permite compilar condicionalmente partes de los archivos de encabezado, dependiendo de si el compilador es el compilador de C o el compilador de RC.</span><span class="sxs-lookup"><span data-stu-id="d6a10-107">RC does define RC\_INVOKED, which enables you conditionally compile portions of your header files, depending on whether the compiler is your C compiler or the RC compiler.</span></span> <span data-ttu-id="d6a10-108">Esto es importante porque el compilador RC admite solo un subconjunto de las instrucciones compatibles con un compilador de C.</span><span class="sxs-lookup"><span data-stu-id="d6a10-108">This is important because the RC compiler supports only a subset of the statements a C compiler would support.</span></span>

<span data-ttu-id="d6a10-109">Para compilar condicionalmente el código con el compilador RC, el código envolvente que RC no puede compilar con \# ifndef RC \_ Invoke y **\# endif**.</span><span class="sxs-lookup"><span data-stu-id="d6a10-109">To conditionally compile your code with the RC compiler, surround code that RC cannot compile with \#ifndef RC\_INVOKED and **\#endif**.</span></span>

<span data-ttu-id="d6a10-110">El siguiente ejemplo se toma de los ejemplos del SDK de.</span><span class="sxs-lookup"><span data-stu-id="d6a10-110">The following example is taken from the SDK samples.</span></span> <span data-ttu-id="d6a10-111">Muestra cómo crear un archivo de encabezado que se puede compilar de forma condicional.</span><span class="sxs-lookup"><span data-stu-id="d6a10-111">It demonstrates how to create a header file that can be compiled conditionally.</span></span>

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




