---
title: El modelo RPC
description: La llamada a procedimiento remoto (RPC) para los lenguajes de programación C y C++ está diseñada para ayudar a satisfacer las necesidades de los programadores que trabajan en la próxima generación de software para los sistemas operativos Windows.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- RPC llamada a procedimiento remoto, descrito, el modelo RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e72048b12329133fcc8ce4ee82bce266ed29162
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793210"
---
# <a name="the-rpc-model"></a><span data-ttu-id="e1d9c-104">El modelo RPC</span><span class="sxs-lookup"><span data-stu-id="e1d9c-104">The RPC Model</span></span>

<span data-ttu-id="e1d9c-105">La llamada a procedimiento remoto (RPC) para los lenguajes de programación C y C++ está diseñada para ayudar a satisfacer las necesidades de los programadores que trabajan en la próxima generación de software para los sistemas operativos Windows.</span><span class="sxs-lookup"><span data-stu-id="e1d9c-105">Remote Procedure Call (RPC) for the C and C++ programming languages is designed to help meet the needs of developers working on the next generation of software for Windows operating systems.</span></span>

<span data-ttu-id="e1d9c-106">RPC es un mecanismo de comunicación entre procesos (IPC) eficaz, sólido, eficiente y seguro que permite el intercambio de datos y la invocación de funciones que residen en un proceso diferente.</span><span class="sxs-lookup"><span data-stu-id="e1d9c-106">RPC is a powerful, robust, efficient, and secure interprocess communication (IPC) mechanism that enables data exchange and invocation of functionality residing in a different process.</span></span> <span data-ttu-id="e1d9c-107">Ese proceso diferente puede estar en el mismo equipo, en la red de área local o a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="e1d9c-107">That different process can be on the same machine, on the local area network, or across the Internet.</span></span> <span data-ttu-id="e1d9c-108">En esta sección se explica el modelo de programación RPC y el modelo para sistemas distribuidos que se pueden implementar con RPC.</span><span class="sxs-lookup"><span data-stu-id="e1d9c-108">This section explains the RPC programming model and the model for distributed systems that can be implemented using RPC.</span></span>

<span data-ttu-id="e1d9c-109">RPC es totalmente compatible con Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e1d9c-109">RPC fully supports 64-bit Windows.</span></span> <span data-ttu-id="e1d9c-110">Hay tres tipos de procesos: procesos nativos de 32 bits, procesos nativos de 64 bits y procesos de 32 bits que se ejecutan en el emulador de proceso de 32 bits en un sistema de 64 bits (a menudo denominados procesos WOW64).</span><span class="sxs-lookup"><span data-stu-id="e1d9c-110">There are three types of processes: native 32-bit processes, native 64-bit processes, and 32-bit processes running under the 32-bit process emulator on a 64-bit system (often referred to as WOW64 processes).</span></span> <span data-ttu-id="e1d9c-111">Para obtener más información sobre WOW64, vea [ejecutar aplicaciones de 32 bits](/windows/desktop/WinProg64/running-32-bit-applications).</span><span class="sxs-lookup"><span data-stu-id="e1d9c-111">For more information about WOW64, see [Running 32-bit Applications](/windows/desktop/WinProg64/running-32-bit-applications).</span></span> <span data-ttu-id="e1d9c-112">Con RPC, los desarrolladores pueden comunicarse de forma transparente entre distintos tipos de procesos; RPC administra automáticamente las diferencias en los procesos en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e1d9c-112">Using RPC, developers can transparently communicate between different types of process; RPC automatically manages process differences behind the scenes.</span></span>

<span data-ttu-id="e1d9c-113">RPC se desarrolló inicialmente como una extensión para la RPC de OSF.</span><span class="sxs-lookup"><span data-stu-id="e1d9c-113">RPC was initially developed as an extension to OSF RPC.</span></span> <span data-ttu-id="e1d9c-114">Con la excepción de algunas de sus características avanzadas, RPC es interoperable con las implementaciones de otros proveedores de la RPC de OSF.</span><span class="sxs-lookup"><span data-stu-id="e1d9c-114">With the exception of some of its advanced features, RPC is interoperable with other vendors' implementations of OSF RPC.</span></span>

<span data-ttu-id="e1d9c-115">En esta sección también se proporciona información general sobre los componentes de RPC y su funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="e1d9c-115">This section also provides an overview of RPC components and their operation.</span></span> <span data-ttu-id="e1d9c-116">La información se presenta en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="e1d9c-116">The information is presented in the following topics:</span></span>

-   [<span data-ttu-id="e1d9c-117">Modelo de programación</span><span class="sxs-lookup"><span data-stu-id="e1d9c-117">The Programming Model</span></span>](the-programming-model.md)
-   [<span data-ttu-id="e1d9c-118">El modelo para sistemas distribuidos</span><span class="sxs-lookup"><span data-stu-id="e1d9c-118">The Model for Distributed Systems</span></span>](the-model-for-distributed-systems.md)
-   [<span data-ttu-id="e1d9c-119">Cómo funciona RPC</span><span class="sxs-lookup"><span data-stu-id="e1d9c-119">How RPC Works</span></span>](how-rpc-works.md)
-   [<span data-ttu-id="e1d9c-120">Componentes de Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="e1d9c-120">Microsoft RPC Components</span></span>](microsoft-rpc-components.md)

 

 