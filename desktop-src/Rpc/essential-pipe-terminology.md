---
title: Terminología de canalización esencial
description: Al igual que otros tipos de parámetros a llamadas a procedimientos remotos, las canalizaciones pueden ser \ in \ o \ out \ Parameters.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df183d18d7962ad0c63ecaa0d350006a4144f23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533405"
---
# <a name="essential-pipe-terminology"></a><span data-ttu-id="934f0-103">Terminología de canalización esencial</span><span class="sxs-lookup"><span data-stu-id="934f0-103">Essential Pipe Terminology</span></span>

<span data-ttu-id="934f0-104">Al igual que otros tipos de parámetros a llamadas a procedimientos remotos, las canalizaciones pueden ser \[ [**in**](/windows/desktop/Midl/in) \] o \[ [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="934f0-104">Like other types of parameters to remote procedure calls, pipes can be \[ [**in**](/windows/desktop/Midl/in)\] or \[ [**out**](/windows/desktop/Midl/out-idl)\] parameters.</span></span> <span data-ttu-id="934f0-105">Puesto que el servidor controla la transferencia de datos a través de una canalización, se dice que las canalizaciones con el \[  \] atributo in *extraen* datos al servidor.</span><span class="sxs-lookup"><span data-stu-id="934f0-105">Since the server controls the transfer of data through a pipe, pipes with the \[**in**\] attribute are said to *pull* data to the server.</span></span> <span data-ttu-id="934f0-106">Del mismo modo, las canalizaciones de salida *envían* datos del servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="934f0-106">Similarly, output pipes *push* data from the server to the client.</span></span> <span data-ttu-id="934f0-107">Los procedimientos que realizan la transferencia de datos se denominan *procedimiento de extracción* y el *procedimiento de inserción*, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="934f0-107">The procedures that do the data transfer are called the *pull procedure* and the *push procedure*, respectively.</span></span>

<span data-ttu-id="934f0-108">El compilador MIDL genera los procedimientos de inserción y extracción para el servidor.</span><span class="sxs-lookup"><span data-stu-id="934f0-108">The MIDL compiler generates the push and pull procedures for the server.</span></span> <span data-ttu-id="934f0-109">Además, administra la asignación de búferes de datos en la memoria.</span><span class="sxs-lookup"><span data-stu-id="934f0-109">In addition, it manages the allocation of data buffers in memory.</span></span> <span data-ttu-id="934f0-110">Sin embargo, el cliente debe proporcionar sus propios procedimientos de inserción y extracción.</span><span class="sxs-lookup"><span data-stu-id="934f0-110">However, the client must provide its own push and pull procedures.</span></span> <span data-ttu-id="934f0-111">También debe proporcionar un procedimiento para asignar los búferes de memoria utilizados por la canalización.</span><span class="sxs-lookup"><span data-stu-id="934f0-111">It must also provide a procedure for allocating the memory buffers used by the pipe.</span></span> <span data-ttu-id="934f0-112">El código auxiliar del cliente llama a estos automáticamente en el momento adecuado.</span><span class="sxs-lookup"><span data-stu-id="934f0-112">These are automatically called at the appropriate time by the client stub.</span></span> <span data-ttu-id="934f0-113">El procedimiento de asignación se denomina a menudo procedimiento de asignación o la función de asignación.</span><span class="sxs-lookup"><span data-stu-id="934f0-113">The allocation procedure is often called the alloc procedure or the alloc function.</span></span>

 

 