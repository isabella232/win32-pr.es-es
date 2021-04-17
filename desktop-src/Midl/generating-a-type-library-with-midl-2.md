---
title: Generar una biblioteca de tipos con MIDL
description: El elemento de nivel superior de la sintaxis ODL es la instrucción Library (bloque de biblioteca).
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL, tareas, generar una biblioteca de tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85f6e8f7ea6f65bc503c08872c9199ff3d5fd828
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651374"
---
# <a name="generating-a-type-library-with-midl"></a><span data-ttu-id="131ec-104">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="131ec-104">Generating a Type Library with MIDL</span></span>

<span data-ttu-id="131ec-105">El elemento de nivel superior de la sintaxis ODL es la instrucción Library (bloque de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="131ec-105">The top-level element of the ODL syntax is the library statement (library block).</span></span> <span data-ttu-id="131ec-106">Todas las demás instrucciones ODL, con la excepción de los atributos que se aplican a la instrucción Library, deben definirse dentro del bloque de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="131ec-106">Every other ODL statement, with the exception of the attributes that are applied to the library statement, must be defined within the library block.</span></span> <span data-ttu-id="131ec-107">Cuando el compilador MIDL ve un bloque de biblioteca, genera una biblioteca de tipos prácticamente de la misma manera que en MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="131ec-107">When the MIDL compiler sees a library block, it generates a type library in much the same way that MkTypLib does.</span></span> <span data-ttu-id="131ec-108">Con algunas excepciones, descritas en [diferencias entre MIDL y MkTypLib](differences-between-midl-and-mktyplib.md), las instrucciones dentro del bloque de biblioteca deben seguir la misma sintaxis que en el lenguaje ODL y MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="131ec-108">With a few exceptions, described in [Differences Between MIDL and MKTYPLIB](differences-between-midl-and-mktyplib.md), the statements within the library block should follow the same syntax as in the ODL language and MkTypLib.</span></span>

> [!Note]  
> <span data-ttu-id="131ec-109">La herramienta Mktyplib.exe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="131ec-109">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="131ec-110">En su lugar, utilice el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="131ec-110">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="131ec-111">Puede aplicar atributos ODL a los elementos que se definen dentro o fuera del bloque de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="131ec-111">You can apply ODL attributes to elements that are defined either inside or outside the library block.</span></span> <span data-ttu-id="131ec-112">Estos atributos no tienen ningún efecto fuera del bloque de biblioteca a menos que se haga referencia al elemento al que se aplican desde dentro del bloque de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="131ec-112">These attributes have no effect outside the library block unless the element they are applied to is referenced from within the library block.</span></span> <span data-ttu-id="131ec-113">Las instrucciones dentro del bloque de biblioteca pueden hacer referencia a un elemento externo mediante su uso como un tipo base, heredando de él o haciendo referencia a él en una línea, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="131ec-113">Statements inside the library block can reference an outside element either by using it as a base type, inheriting from it, or by referencing it on a line as shown:</span></span>

``` syntax
<some IDL definitions including definitions for interface IFace and struct bar>
[<some attributes>]
library a
{
    interface IFace;
    struct this_struct;
...
};
```

<span data-ttu-id="131ec-114">Si se hace referencia a un elemento definido fuera del bloque de biblioteca dentro del bloque de biblioteca, su definición se colocará en la biblioteca de tipos generada.</span><span class="sxs-lookup"><span data-stu-id="131ec-114">If an element defined outside the library block is referenced within the library block, then its definition will be put into the generated type library.</span></span> <span data-ttu-id="131ec-115">El compilador MIDL trata las instrucciones fuera de un bloque de biblioteca como un archivo IDL típico y analiza esas instrucciones tal y como se ha hecho siempre.</span><span class="sxs-lookup"><span data-stu-id="131ec-115">The MIDL compiler treats the statements outside of a library block as a typical IDL file and parses those statements as it has always done.</span></span> <span data-ttu-id="131ec-116">Normalmente, esto significa generar códigos auxiliares de lenguaje C para una aplicación RPC.</span><span class="sxs-lookup"><span data-stu-id="131ec-116">Normally, this means generating C-language stubs for an RPC application.</span></span>

<span data-ttu-id="131ec-117">Para obtener más información sobre la sintaxis general de un archivo ODL, vea [Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax).</span><span class="sxs-lookup"><span data-stu-id="131ec-117">For more information about the general syntax for an ODL file see [ODL File Syntax](/previous-versions/windows/desktop/automat/odl-file-syntax).</span></span>

 

 