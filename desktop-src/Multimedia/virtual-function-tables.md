---
title: Tablas de funciones virtuales
description: Tablas de funciones virtuales
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a784a027f7e1120d8e7092aa5dd6c0f5c0e958b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651290"
---
# <a name="virtual-function-tables"></a><span data-ttu-id="9d790-103">Tablas de funciones virtuales</span><span class="sxs-lookup"><span data-stu-id="9d790-103">Virtual Function Tables</span></span>

<span data-ttu-id="9d790-104">Una tabla de funciones virtuales es una matriz de punteros a los métodos que admite un objeto.</span><span class="sxs-lookup"><span data-stu-id="9d790-104">A virtual function table is an array of pointers to the methods an object supports.</span></span> <span data-ttu-id="9d790-105">Si está utilizando C, un objeto aparece como una estructura cuyo primer miembro es un puntero a la tabla de función virtual (**lpVtbl**); es decir, el primer miembro apunta a una matriz que contiene punteros de función.</span><span class="sxs-lookup"><span data-stu-id="9d790-105">If you're using C, an object appears as a structure whose first member is a pointer to the virtual function table (**lpVtbl**); that is, the first member points to an array containing function pointers.</span></span> <span data-ttu-id="9d790-106">Todos los métodos toman un puntero a la tabla de funciones como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="9d790-106">The methods all take a pointer to the function table as the first parameter.</span></span> <span data-ttu-id="9d790-107">Por lo tanto, en el ejemplo siguiente se llama al método **Read** de un objeto **pStream** :</span><span class="sxs-lookup"><span data-stu-id="9d790-107">Thus, the following example calls the **Read** method of a **pStream** object:</span></span>


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



<span data-ttu-id="9d790-108">En C + +, el puntero a la tabla de función virtual, el puntero *this* , es implícito.</span><span class="sxs-lookup"><span data-stu-id="9d790-108">In C+ +, the pointer to the virtual function table, the *this* pointer, is implicit.</span></span> <span data-ttu-id="9d790-109">Lo siguiente es equivalente al ejemplo anterior al usar C + +:</span><span class="sxs-lookup"><span data-stu-id="9d790-109">The following is equivalent to the previous example when using C+ +:</span></span>


```C++
pStream->Read(parameters) 
 
```



 

 




