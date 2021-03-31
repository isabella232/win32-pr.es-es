---
description: COM+ incorpora apartamentos neutros para simplificar la programación en entornos multiproceso. El apartamento neutro es el modelo preferido para COM+ para los componentes sin interfaz de usuario.
ms.assetid: 679742af-7c04-4b0e-822a-a43e1aafa936
title: Apartamentos neutros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac3bdff2670e4f99ad94af20278eaca6a38861e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423336"
---
# <a name="neutral-apartments"></a><span data-ttu-id="f1c36-104">Apartamentos neutros</span><span class="sxs-lookup"><span data-stu-id="f1c36-104">Neutral Apartments</span></span>

<span data-ttu-id="f1c36-105">COM+ incorpora apartamentos neutros para simplificar la programación en entornos multiproceso.</span><span class="sxs-lookup"><span data-stu-id="f1c36-105">COM+ introduces neutral apartments to simplify programming in multithreaded environments.</span></span> <span data-ttu-id="f1c36-106">El apartamento neutro es el modelo preferido para COM+ para los componentes sin interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f1c36-106">The neutral apartment is the preferred model for COM+ for components with no user interface.</span></span>

<span data-ttu-id="f1c36-107">En el pasado, para evitar cuellos de botella, los desarrolladores de COM+ que requieran la escalabilidad del servidor tenían que implementar componentes de subprocesamiento libre. sin embargo, los modelos de subprocesamiento libre son complicados de implementar porque deben tratar el acceso de interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="f1c36-107">In the past, to prevent bottlenecks, COM+ developers requiring server scalability had to implement free-threaded components; however, free-threading models are complicated to implement because they must deal with interlocking access.</span></span> <span data-ttu-id="f1c36-108">En apartamentos neutros, los objetos siguen las instrucciones para apartamentos multiproceso pero se pueden ejecutar en cualquier tipo de subproceso.</span><span class="sxs-lookup"><span data-stu-id="f1c36-108">In neutral apartments, objects follow the guidelines for multithreaded apartments but can execute on any kind of thread.</span></span> <span data-ttu-id="f1c36-109">Cuando un subproceso se ejecuta en un apartamento neutro, se recibe el contexto del objeto sin que se produzca un cambio de subproceso.</span><span class="sxs-lookup"><span data-stu-id="f1c36-109">When a thread is running in a neutral apartment, the object's context is received without causing a thread switch.</span></span>

<span data-ttu-id="f1c36-110">Cada proceso solo puede tener un apartamento neutro.</span><span class="sxs-lookup"><span data-stu-id="f1c36-110">Each process can have only one neutral apartment.</span></span> <span data-ttu-id="f1c36-111">Para seleccionar un apartamento neutro, utilice la siguiente configuración del registro:</span><span class="sxs-lookup"><span data-stu-id="f1c36-111">To select a neutral apartment, use the following registry setting:</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         ThreadingModel = Neutral
```

<span data-ttu-id="f1c36-112">Los componentes que tienen interfaces de usuario deben seguir usando apartamentos de un solo subproceso como modelo preferido.</span><span class="sxs-lookup"><span data-stu-id="f1c36-112">Components that have user interfaces should continue to use single-threaded apartments as the preferred model.</span></span> <span data-ttu-id="f1c36-113">Para seleccionar un contenedor uniproceso, utilice la siguiente configuración del registro:</span><span class="sxs-lookup"><span data-stu-id="f1c36-113">To select a single-threaded apartment, use the following registry setting:</span></span>

<span data-ttu-id="f1c36-114">**ThreadingModel** = Apartamento</span><span class="sxs-lookup"><span data-stu-id="f1c36-114">**ThreadingModel** = Apartment</span></span>

 

 



