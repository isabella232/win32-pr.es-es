---
title: Usar la constante predefinida __midl
description: Cuando el compilador MIDL procesa los archivos IDL y ACF de entrada, \_ \_ se define MIDL de forma predeterminada y se usa para la compilación condicional con el fin de lograr la coherencia en toda la compilación.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- MIDL del compilador MIDL mediante la _midl constante predefinida
- _midl la constante MIDL predefinida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae49675b38dcc3cab2d3d41e4f48cd0637d78523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075799"
---
# <a name="using-the-__midl-predefined-constant"></a><span data-ttu-id="a84ef-105">Usar la \_ \_ constante predefinida MIDL</span><span class="sxs-lookup"><span data-stu-id="a84ef-105">Using the \_\_midl Predefined Constant</span></span>

<span data-ttu-id="a84ef-106">Cuando el compilador MIDL procesa los archivos IDL y ACF de entrada, \_ \_ se define MIDL de forma predeterminada y se usa para la compilación condicional con el fin de lograr la coherencia en toda la compilación.</span><span class="sxs-lookup"><span data-stu-id="a84ef-106">When the MIDL compiler processes the input IDL and ACF files, \_\_midl is defined by default and is used for conditional compilation to attain consistency throughout the build.</span></span> <span data-ttu-id="a84ef-107">En este caso, se usa la instrucción define en los archivos de encabezado, como la **\_ fase MIDL Pass**, y se reemplazan por una marca coherente.</span><span class="sxs-lookup"><span data-stu-id="a84ef-107">This phases out the use of define statements in the header files, such as **MIDL\_PASS**, and replaces them with a consistent flag.</span></span> <span data-ttu-id="a84ef-108">El valor de la \_ \_ constante MIDL indica la versión del compilador *Major. minor* según la fórmula *principal* \* 100 + *Minor*; por ejemplo, MIDL ver.</span><span class="sxs-lookup"><span data-stu-id="a84ef-108">The value of the \_\_midl constant indicates the compiler version *major.minor* according to the formula *major* \* 100 + *minor*; for example MIDL ver.</span></span> <span data-ttu-id="a84ef-109">6.0. x tiene el \_ \_ MIDL definido como 600.</span><span class="sxs-lookup"><span data-stu-id="a84ef-109">6.0.x has the \_\_midl defined as 600.</span></span>

<span data-ttu-id="a84ef-110">Si lo desea, puede invalidar este valor predeterminado si especifica lo siguiente en la línea de comandos: **/u \_ \_ MIDL**.</span><span class="sxs-lookup"><span data-stu-id="a84ef-110">If you choose, you can override this default by specifying the following on the command line: **/U\_\_midl**.</span></span> <span data-ttu-id="a84ef-111">Para obtener más información, consulte [**/u**](-u.md).</span><span class="sxs-lookup"><span data-stu-id="a84ef-111">For more information, see [**/U**](-u.md).</span></span>

 

 




