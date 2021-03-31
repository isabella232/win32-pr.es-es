---
title: Importación de archivos de encabezado del sistema
description: Aunque a menudo es posible usar la Directiva \ include para incluir archivos de encabezado en el archivo IDL, no se recomienda.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- importar MIDL, archivos de encabezado del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df7ca983fa21ae8e604446f0221c302c73099
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820474"
---
# <a name="importing-system-header-files"></a><span data-ttu-id="0e59f-104">Importación de archivos de encabezado del sistema</span><span class="sxs-lookup"><span data-stu-id="0e59f-104">Importing System Header Files</span></span>

<span data-ttu-id="0e59f-105">Aunque a menudo es posible usar la directiva **\# include** para incluir archivos de encabezado en el archivo IDL, no se recomienda.</span><span class="sxs-lookup"><span data-stu-id="0e59f-105">While it is often possible to use the **\#include** directive to include header files in your IDL file, it is not recommended.</span></span> <span data-ttu-id="0e59f-106">El compilador MIDL generará códigos auxiliares para todas las funciones definidas en el archivo IDL que se está compilando.</span><span class="sxs-lookup"><span data-stu-id="0e59f-106">The MIDL compiler will generate stubs for all functions defined in the IDL file being compiled.</span></span> <span data-ttu-id="0e59f-107">Normalmente, un archivo de encabezado contiene una serie de prototipos que no necesita ni quiere incluir en los archivos de código auxiliar, y un **\# incluye** de forma eficaz todas esas definiciones en el archivo IDL principal.</span><span class="sxs-lookup"><span data-stu-id="0e59f-107">Usually a header file contains a number of prototypes that you neither need nor want to include in your stub files, and a **\#include** effectively puts all those definitions into your main IDL file.</span></span> <span data-ttu-id="0e59f-108">Además, si hay tipos no utilizables definidos en el archivo de encabezado, es posible que el archivo IDL no se compile.</span><span class="sxs-lookup"><span data-stu-id="0e59f-108">Furthermore, if there are nonremotable types defined in the header file, the IDL file may not compile.</span></span>

<span data-ttu-id="0e59f-109">Hay dos formas de incluir definiciones de tipos de archivos de encabezado en un archivo IDL:</span><span class="sxs-lookup"><span data-stu-id="0e59f-109">There are two ways to include type definitions from header files in an IDL file:</span></span>

-   <span data-ttu-id="0e59f-110">Use la Directiva de [**importación**](import.md) para incluir tipos de datos definidos en un archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="0e59f-110">Use the [**import**](import.md) directive to include data types defined in a header file.</span></span> <span data-ttu-id="0e59f-111">A diferencia de la directiva **\# include** del lenguaje C, la directiva **Import** solo selecciona las definiciones de tipo y constante y omite los prototipos de procedimiento.</span><span class="sxs-lookup"><span data-stu-id="0e59f-111">Unlike the C-language **\#include** directive, the **import** directive only picks up type and constant definitions and ignores procedure prototypes.</span></span> <span data-ttu-id="0e59f-112">Este enfoque funcionará siempre que el archivo IDL principal no haga referencia a ningún tipo de no utilizables definido en el archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="0e59f-112">This approach will work as long as your main IDL file does not reference any nonremotable types defined in the header file.</span></span>
-   <span data-ttu-id="0e59f-113">Cree un archivo IDL auxiliar con una interfaz ficticia que incluya los archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="0e59f-113">Create a helper IDL file with a dummy interface that includes the header files.</span></span> <span data-ttu-id="0e59f-114">A continuación, use la Directiva de [**importación**](import.md) para incluir el archivo auxiliar.</span><span class="sxs-lookup"><span data-stu-id="0e59f-114">Then, use the [**import**](import.md) directive to include the helper file.</span></span> <span data-ttu-id="0e59f-115">De este modo, solo los [**typedef**](typedef.md)aparecerán en el código auxiliar compilado.</span><span class="sxs-lookup"><span data-stu-id="0e59f-115">In this way, only the [**typedef**](typedef.md)s will appear in the compiled stubs.</span></span> <span data-ttu-id="0e59f-116">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0e59f-116">For example:</span></span>

```syntax
//in helper.idl:
interface dummy
{ 
   #include "kitchensink.h"
   #include "system.h"
}

//in main.idl:
import "helper.idl";
```
