---
title: Generar un archivo DLL de proxy y una biblioteca de tipos desde un solo archivo IDL
description: Puede usar un solo archivo IDL para generar el código auxiliar del proxy y los archivos de encabezado para calcular las referencias del código, y una biblioteca de tipos.
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL, tareas, generar un archivo DLL de proxy y una biblioteca de tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81001bba7aeff416e765291d3e6660b705919a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076096"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a><span data-ttu-id="dbc84-104">Generar un archivo DLL de proxy y una biblioteca de tipos desde un solo archivo IDL</span><span class="sxs-lookup"><span data-stu-id="dbc84-104">Generating a Proxy DLL and a Type Library from a Single IDL File</span></span>

<span data-ttu-id="dbc84-105">Puede usar un solo archivo IDL para generar el código auxiliar del proxy y los archivos de encabezado para calcular las referencias del código, y una biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="dbc84-105">You can use a single IDL file to generate both the proxy stubs and header files for marshaling code, and a type library.</span></span> <span data-ttu-id="dbc84-106">Para ello, defina una interfaz fuera del bloque de biblioteca y, a continuación, haga referencia a esa interfaz desde dentro del bloque de biblioteca, como se muestra en este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="dbc84-106">You do this by defining an interface outside the library block and then referencing that interface from inside the library block, as shown in this example:</span></span>

``` syntax
//file: AllKnown.idl

[
    object, uuid(. . .), <other interface attributes>
]
interface IKnown : IUnknown 
{
    import "unknwn.idl";
    <declarations, etc. for IKnown interface go here>
};

[
    <library attributes>
]
library KnownLibrary 
{

    //reference interface IKnown:
    interface IKnown;

    //or create a new class:
    [
        <coclass attributes>
    ] 
    coclass KnowMore 
    {
       interface IKnown;
    };
};
```

<span data-ttu-id="dbc84-107">Para obtener más información, vea [serialización de tipos de datos OLE](marshaling-ole-data-types.md) y [archivos adicionales necesarios para generar una biblioteca de tipos](additional-files-required-to-generate-a-type-library-2.md).</span><span class="sxs-lookup"><span data-stu-id="dbc84-107">For more information, see [Marshaling OLE Data Types](marshaling-ole-data-types.md) and [Additional Files Required To Generate a Type Library](additional-files-required-to-generate-a-type-library-2.md).</span></span>

 

 




