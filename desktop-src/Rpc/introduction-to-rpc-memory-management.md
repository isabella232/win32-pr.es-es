---
title: Introducción a la administración de memoria RPC
description: Introducción a la administración de memoria de la llamada a procedimiento remoto (RPC).
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ac4b6aecb2fd78448ebe31c72587fafb8f6fde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359283"
---
# <a name="introduction-to-rpc-memory-management"></a><span data-ttu-id="26160-103">Introducción a la administración de memoria RPC</span><span class="sxs-lookup"><span data-stu-id="26160-103">Introduction to RPC Memory Management</span></span>

<span data-ttu-id="26160-104">En el contexto de RPC, la administración de memoria implica:</span><span class="sxs-lookup"><span data-stu-id="26160-104">In the context of RPC, memory management involves:</span></span>

-   <span data-ttu-id="26160-105">Asignar y desasignar la memoria necesaria para simular un solo espacio de direcciones conceptual entre el cliente y el servidor en los diferentes espacios de direcciones de los subprocesos del cliente y del servidor.</span><span class="sxs-lookup"><span data-stu-id="26160-105">Allocating and deallocating the memory needed to simulate a single conceptual address space between the client and the server in the different address spaces of the client and server's threads.</span></span>
-   <span data-ttu-id="26160-106">Determinar qué componente de software es responsable de administrar la memoria, la aplicación o el código auxiliar generado por MIDL.</span><span class="sxs-lookup"><span data-stu-id="26160-106">Determining which software component is responsible for managing memory — the application or the MIDL-generated stub.</span></span>
-   <span data-ttu-id="26160-107">Seleccionar atributos MIDL que afectan a la administración de memoria: atributos direccionales, atributos de puntero, atributos de matriz y atributos ACF \[ [ \_ recuento de bytes](/windows/desktop/Midl/byte-count) \] , \[ [asignación](/windows/desktop/Midl/allocate) \] y \[ [habilitar \_ asignación](/windows/desktop/Midl/enable-allocate) \] .</span><span class="sxs-lookup"><span data-stu-id="26160-107">Selecting MIDL attributes that affect memory management: directional attributes, pointer attributes, array attributes, and the ACF attributes \[ [byte\_count](/windows/desktop/Midl/byte-count)\], \[ [allocate](/windows/desktop/Midl/allocate)\], and \[ [enable\_allocate](/windows/desktop/Midl/enable-allocate)\].</span></span>

<span data-ttu-id="26160-108">Cuando un programa llama a una función o un procedimiento en su espacio de direcciones, la administración de la memoria es más sencilla que en una aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="26160-108">When a program calls a function or procedure in its address space, memory management is more straightforward than in a distributed application.</span></span> <span data-ttu-id="26160-109">En el siguiente diagrama se muestra un árbol binario.</span><span class="sxs-lookup"><span data-stu-id="26160-109">To illustrate, the following diagram depicts a binary tree.</span></span> <span data-ttu-id="26160-110">Para pasar esta estructura de datos a un procedimiento en su espacio de direcciones, un programa simplemente pasa un puntero a la raíz del árbol.</span><span class="sxs-lookup"><span data-stu-id="26160-110">To pass this data structure to a procedure in its address space, a program simply passes a pointer to the root of the tree.</span></span>

![un árbol binario, con punteros para estructurar los datos alojados en la raíz del árbol.](images/bintree.png)

<span data-ttu-id="26160-112">Las aplicaciones RPC cliente/servidor comparten datos entre dos espacios de memoria distintos.</span><span class="sxs-lookup"><span data-stu-id="26160-112">Client/server RPC applications share data across two different memory spaces.</span></span> <span data-ttu-id="26160-113">Estos espacios de memoria pueden estar o no en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="26160-113">These memory spaces may or may not be on the same computer.</span></span> <span data-ttu-id="26160-114">En cualquier caso, el cliente y el servidor no tienen acceso directo al espacio de memoria de los demás.</span><span class="sxs-lookup"><span data-stu-id="26160-114">Either way, the client and server have no direct access to each other's memory space.</span></span> <span data-ttu-id="26160-115">RPC depende de la capacidad de simular el espacio de direcciones del programa cliente en el espacio de direcciones del programa de servidor.</span><span class="sxs-lookup"><span data-stu-id="26160-115">RPC depends on the ability to simulate the client program's address space in the server program's address space.</span></span> <span data-ttu-id="26160-116">También debe devolver datos, incluidos los datos nuevos y modificados, del servidor a la memoria del cliente.</span><span class="sxs-lookup"><span data-stu-id="26160-116">It must also return data, including new and changed data, from the server to the client memory.</span></span>

<span data-ttu-id="26160-117">En casos como el árbol binario representado en el diagrama anterior, no basta con pasar un puntero al nodo raíz a un procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="26160-117">In cases such as the binary tree depicted in the preceding diagram, it is not sufficient to pass a pointer to the root node to a remote procedure.</span></span> <span data-ttu-id="26160-118">El programa o el código auxiliar debe pasar el árbol completo al espacio de direcciones del servidor para que el procedimiento remoto opere en él.</span><span class="sxs-lookup"><span data-stu-id="26160-118">Either the program or the stubs must pass the entire tree to the server's address space for the remote procedure to operate on it.</span></span>

 

 