---
title: Punteros y RPC
description: Es muy eficaz usar punteros como parámetros de la función de C.
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbacce89046e2808acad539d19bbdcfeb1bc99c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903720"
---
# <a name="pointers-and-rpc"></a><span data-ttu-id="c0a61-103">Punteros y RPC</span><span class="sxs-lookup"><span data-stu-id="c0a61-103">Pointers and RPC</span></span>

<span data-ttu-id="c0a61-104">Es muy eficaz usar punteros como parámetros de la función de C.</span><span class="sxs-lookup"><span data-stu-id="c0a61-104">It is very efficient to use pointers as C-function parameters.</span></span> <span data-ttu-id="c0a61-105">El puntero solo cuesta unos pocos bytes y se puede usar para tener acceso a una gran cantidad de memoria.</span><span class="sxs-lookup"><span data-stu-id="c0a61-105">The pointer costs only a few bytes and can be used to access a large amount of memory.</span></span> <span data-ttu-id="c0a61-106">Sin embargo, en una aplicación distribuida, los procedimientos de cliente y servidor residen en diferentes espacios de direcciones: pueden estar en equipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="c0a61-106">However, in a distributed application, the client and server procedures reside in different address spaces—they can be on different computers.</span></span> <span data-ttu-id="c0a61-107">Por lo tanto, el cliente y el servidor no suelen tener acceso al mismo espacio de memoria.</span><span class="sxs-lookup"><span data-stu-id="c0a61-107">Therefore, the client and the server usually do not have access to the same memory space.</span></span>

<span data-ttu-id="c0a61-108">Cuando uno de los parámetros del procedimiento remoto es un puntero a un objeto, el cliente debe transmitir una copia de ese objeto y su puntero al servidor.</span><span class="sxs-lookup"><span data-stu-id="c0a61-108">When one of the remote procedure's parameters is a pointer to an object, the client must transmit a copy of that object and its pointer to the server.</span></span> <span data-ttu-id="c0a61-109">Si el procedimiento remoto modifica el objeto a través de su puntero, el servidor devuelve el puntero y su copia modificada.</span><span class="sxs-lookup"><span data-stu-id="c0a61-109">If the remote procedure modifies the object through its pointer, the server returns the pointer and its modified copy.</span></span>

<span data-ttu-id="c0a61-110">MIDL ofrece atributos de puntero para minimizar la cantidad de sobrecarga necesaria y el tamaño de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c0a61-110">MIDL offers pointer attributes to minimize the amount of required overhead and the size of your application.</span></span> <span data-ttu-id="c0a61-111">En esta sección se describen el propósito y los usos de los atributos de puntero de MIDL.</span><span class="sxs-lookup"><span data-stu-id="c0a61-111">This section discusses the purpose and uses of MIDL pointer attributes.</span></span> <span data-ttu-id="c0a61-112">También se muestra información sobre el control de puntero en las aplicaciones RPC.</span><span class="sxs-lookup"><span data-stu-id="c0a61-112">It also presents information on pointer handling in RPC applications.</span></span> <span data-ttu-id="c0a61-113">Se divide en los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="c0a61-113">It is divided into the following topics:</span></span>

-   [<span data-ttu-id="c0a61-114">Tipos de punteros</span><span class="sxs-lookup"><span data-stu-id="c0a61-114">Kinds of Pointers</span></span>](kinds-of-pointers.md)
-   [<span data-ttu-id="c0a61-115">Punteros y asignación de memoria</span><span class="sxs-lookup"><span data-stu-id="c0a61-115">Pointers and Memory Allocation</span></span>](pointers-and-memory-allocation.md)
-   [<span data-ttu-id="c0a61-116">Tipos de puntero predeterminados</span><span class="sxs-lookup"><span data-stu-id="c0a61-116">Default Pointer Types</span></span>](default-pointer-types.md)
-   [<span data-ttu-id="c0a61-117">Herencia de tipos de atributos de puntero</span><span class="sxs-lookup"><span data-stu-id="c0a61-117">Pointer-Attribute Type Inheritance</span></span>](pointer-attribute-type-inheritance.md)

 

 




