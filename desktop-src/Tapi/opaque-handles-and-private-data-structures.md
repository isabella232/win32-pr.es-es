---
description: Los identificadores opacos se usan en TSPI para hacer referencia a las estructuras de datos que representan las líneas, los teléfonos y los aspectos de la llamada.
ms.assetid: aa1742aa-6cd4-461a-ad92-972eefcf637f
title: Controladores opacos y estructuras de datos privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd8c7b911de5f85f84b56a8e25e28eb805c5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001317"
---
# <a name="opaque-handles-and-private-data-structures"></a><span data-ttu-id="9b22d-103">Controladores opacos y estructuras de datos privadas</span><span class="sxs-lookup"><span data-stu-id="9b22d-103">Opaque Handles and Private Data Structures</span></span>

<span data-ttu-id="9b22d-104">Los identificadores opacos se usan en TSPI para hacer referencia a las estructuras de datos que representan las líneas, los teléfonos y los aspectos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9b22d-104">Opaque handles are used in TSPI to refer to the data structures representing lines, phones, and call appearances.</span></span> <span data-ttu-id="9b22d-105">Aparecen como parámetros de la mayoría de las funciones y devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="9b22d-105">These appear as parameters to most of the functions and callbacks.</span></span> <span data-ttu-id="9b22d-106">Hay pocas funciones que hacen referencia al dispositivo con un identificador de dispositivo en lugar de un identificador opaco.</span><span class="sxs-lookup"><span data-stu-id="9b22d-106">There are few functions that refer to the device using a device identifier instead of an opaque handle.</span></span> <span data-ttu-id="9b22d-107">En tal caso, la referencia es al propio dispositivo en lugar de a una estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="9b22d-107">In such a case, the reference is to the device itself rather than to a data structure.</span></span> <span data-ttu-id="9b22d-108">Las funciones que funcionan de esta manera son normalmente las llamadas a los tiempos de inicialización tempranas antes de que se creen las estructuras de datos y se intercambien los identificadores opacos.</span><span class="sxs-lookup"><span data-stu-id="9b22d-108">Functions that work in this fashion are typically those called at early initialization times before data structures are created and opaque handles are exchanged.</span></span>

<span data-ttu-id="9b22d-109">El proveedor de servicios debe decidir cómo interpretar estos identificadores.</span><span class="sxs-lookup"><span data-stu-id="9b22d-109">The service provider must decide how to interpret these handles.</span></span> <span data-ttu-id="9b22d-110">Un proveedor de servicios suele usar el puntero a su estructura de datos o al índice en una matriz de estructuras de datos como su identificador opaco.</span><span class="sxs-lookup"><span data-stu-id="9b22d-110">A service provider typically uses the pointer to its data structure or to the index into an array of data structures as its opaque handle.</span></span> <span data-ttu-id="9b22d-111">La única restricción es que el proveedor de servicios no puede usar el valor 0 como [HDRVLINE](hdrvline.md), HDRVCALL o [HDRVPHONE](hdrvphone.md).</span><span class="sxs-lookup"><span data-stu-id="9b22d-111">The only restriction is that the service provider cannot use the value 0 as an [HDRVLINE](hdrvline.md), HDRVCALL, or [HDRVPHONE](hdrvphone.md).</span></span> <span data-ttu-id="9b22d-112">El valor 0 o **null** para un identificador tiene un significado especial en algunas operaciones.</span><span class="sxs-lookup"><span data-stu-id="9b22d-112">The value 0 or **NULL** for a handle has a special meaning in some operations.</span></span>

 

 



