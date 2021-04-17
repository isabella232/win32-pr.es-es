---
title: Tipos de datos en el cuerpo de la interfaz
description: El cuerpo de la interfaz, que se incluye entre llaves (), contiene los tipos de datos que se utilizarán en las llamadas a procedimientos remotos y prototipos para las funciones que se ejecutarán de forma remota.
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- interfaces MIDL, tipos de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bdbbb90c4cbecd4a6a4e3cc74ba9775772dd0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685498"
---
# <a name="data-types-in-the-interface-body"></a><span data-ttu-id="abcd9-104">Tipos de datos en el cuerpo de la interfaz</span><span class="sxs-lookup"><span data-stu-id="abcd9-104">Data Types in the Interface Body</span></span>

<span data-ttu-id="abcd9-105">El cuerpo de la interfaz, que se incluye entre llaves ({}), contiene los tipos de datos que se utilizarán en las llamadas a procedimientos remotos y prototipos para las funciones que se ejecutarán de forma remota.</span><span class="sxs-lookup"><span data-stu-id="abcd9-105">The interface body, which is enclosed in braces ({ }), contains the data types that will be used in remote procedure calls and prototypes for the functions that will be executed remotely.</span></span> <span data-ttu-id="abcd9-106">Un cuerpo de la interfaz puede contener importaciones, pragmas, declaraciones de constantes, declaraciones de tipos y declaraciones de función.</span><span class="sxs-lookup"><span data-stu-id="abcd9-106">An interface body can contain imports, pragmas, constant declarations, type declarations, and function declarations.</span></span> <span data-ttu-id="abcd9-107">Excepto en el modo de compatibilidad de OSF, el compilador MIDL también permite declaraciones implícitas en forma de definiciones de variables.</span><span class="sxs-lookup"><span data-stu-id="abcd9-107">Except in OSF-compatibility mode, the MIDL compiler also allows implicit declarations in the form of variable definitions.</span></span>

<span data-ttu-id="abcd9-108">Tenga en cuenta que la especificación de OSF-DCE para las interfaces RPC no permite varias interfaces en un solo archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="abcd9-108">Note that the OSF-DCE specification for RPC interfaces does not allow multiple interfaces in a single IDL file.</span></span> <span data-ttu-id="abcd9-109">Por lo tanto, si está compilando el modo de compatibilidad de OSF de MIDL ( [**/OSF**](-osf.md)), el archivo IDL solo puede contener una interfaz.</span><span class="sxs-lookup"><span data-stu-id="abcd9-109">Therefore, if you are compiling in MIDL's OSF-compatibility mode ( [**/osf**](-osf.md)), your IDL file can contain only one interface.</span></span>

<span data-ttu-id="abcd9-110">Para obtener información detallada sobre el uso del compilador MIDL para generar bibliotecas de tipos, vea [generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md).</span><span class="sxs-lookup"><span data-stu-id="abcd9-110">For details on using the MIDL compiler to produce type libraries, see [Generating a Type Library with MIDL](generating-a-type-library-with-midl-2.md).</span></span>

<span data-ttu-id="abcd9-111">En Microsoft RPC, un archivo IDL puede contener varias interfaces y estas interfaces se pueden declarar hacia delante (dentro del archivo IDL que las define).</span><span class="sxs-lookup"><span data-stu-id="abcd9-111">In Microsoft RPC, an IDL file can contain multiple interfaces and these interfaces can be forward declared (within the IDL file that defines them).</span></span> <span data-ttu-id="abcd9-112">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="abcd9-112">For example:</span></span>

``` syntax
interface ITwo; //forward declaration
interface IOne 
{
...uses ITwo...
}
interface ITwo 
{
...uses IOne...
}
```

 

 




