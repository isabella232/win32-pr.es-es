---
description: La clase CMSPThread implementa el subproceso de trabajo de los MSP.
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: CMSPThread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a12b71668e81688b5de7f41e188a51b88944d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678362"
---
# <a name="cmspthread"></a><span data-ttu-id="3c5d2-103">CMSPThread</span><span class="sxs-lookup"><span data-stu-id="3c5d2-103">CMSPThread</span></span>

<span data-ttu-id="3c5d2-104">La clase **CMSPThread** implementa el subproceso de trabajo de MSP.</span><span class="sxs-lookup"><span data-stu-id="3c5d2-104">The **CMSPThread** class implements the MSP's worker thread.</span></span> <span data-ttu-id="3c5d2-105">Las clases base utilizan este subproceso de trabajo para varios propósitos.</span><span class="sxs-lookup"><span data-stu-id="3c5d2-105">The base classes use this worker thread for a number of purposes.</span></span> <span data-ttu-id="3c5d2-106">Se proporciona un mecanismo de elementos de trabajo genéricos y ligeros para permitir que el MSP derivado use este subproceso para sus propios elementos de trabajo sincrónicos o asincrónicos, lo que sea posible.</span><span class="sxs-lookup"><span data-stu-id="3c5d2-106">A generic and lightweight work item mechanism is provided to allow the derived MSP to use this thread for its own synchronous or asynchronous work items, whatever they may be.</span></span> <span data-ttu-id="3c5d2-107">El subproceso también bombea mensajes y admite el control de APC (aunque APC no se usan en las clases base).</span><span class="sxs-lookup"><span data-stu-id="3c5d2-107">The thread also pumps messages and supports handling of APCs (although APCs are not used in the base classes).</span></span>

<span data-ttu-id="3c5d2-108">Cuando hay varias direcciones similares (es decir, cuando se crea una instancia de la misma implementación MSP del mismo archivo DLL varias veces), la clase de subproceso garantiza la escalabilidad mediante el uso automático de un único subproceso para todas las direcciones.</span><span class="sxs-lookup"><span data-stu-id="3c5d2-108">When multiple like addresses are present (that is, when the same MSP implementation from the same DLL is instantiated multiple times), the thread class ensures scalability by automatically using a single thread for all the addresses.</span></span> <span data-ttu-id="3c5d2-109">La interfaz a la clase de subproceso es de tal modo que la implementación de MSP puede pensar en la clase de subproceso como un subproceso privado y no necesita preocuparse por las demás direcciones que pueden compartirla.</span><span class="sxs-lookup"><span data-stu-id="3c5d2-109">The interface to the thread class is such that the MSP implementation can think of the thread class as a private thread and need not care about the other addresses that may be sharing it.</span></span>

<span data-ttu-id="3c5d2-110">Definido en MSPthrd. h.</span><span class="sxs-lookup"><span data-stu-id="3c5d2-110">Defined in MSPthrd.h.</span></span>

 

 



