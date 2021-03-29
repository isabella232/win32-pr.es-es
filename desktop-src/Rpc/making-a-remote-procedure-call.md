---
title: Realización de una llamada a procedimiento remoto
description: Una vez que el programa cliente de las aplicaciones distribuidas que utiliza identificadores de enlace explícitos tiene un identificador de enlace, puede ejecutar procedimientos remotos.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- RPC llamada a procedimiento remoto, tareas, realizar una llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97095d7eda8227f2369f5e3776faf8ce04c22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772720"
---
# <a name="making-a-remote-procedure-call"></a><span data-ttu-id="fe089-104">Realización de una llamada a procedimiento remoto</span><span class="sxs-lookup"><span data-stu-id="fe089-104">Making a Remote Procedure Call</span></span>

<span data-ttu-id="fe089-105">Una vez que el programa cliente de las aplicaciones distribuidas que utiliza identificadores de enlace explícitos tiene un identificador de enlace, puede ejecutar procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="fe089-105">Once the client program of distributed applications that uses explicit binding handles has a binding handle, it can execute remote procedures.</span></span>

<span data-ttu-id="fe089-106">Microsoft RPC también ofrece identificadores de enlace personalizados, identificadores de enlace implícitos y controladores de enlace automáticos.</span><span class="sxs-lookup"><span data-stu-id="fe089-106">Microsoft RPC also offers custom binding handles, implicit binding handles, and automatic binding handles.</span></span> <span data-ttu-id="fe089-107">Estos identificadores de enlace ofrecen a los programas de cliente y servidor distintos niveles de control sobre el proceso de ejecución de procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="fe089-107">These binding handles offer client and server programs different levels of control over the process of executing remote procedures.</span></span> <span data-ttu-id="fe089-108">Para obtener más información sobre los diferentes tipos de identificadores y la flexibilidad que ofrecen, vea [enlazar y controlar](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="fe089-108">For details on different handle types and the flexibility they offer, see [Binding and Handles](binding-and-handles.md).</span></span>

<span data-ttu-id="fe089-109">Para ejecutar la llamada al procedimiento de forma remota, llame a la función de código auxiliar del lado cliente de la misma manera que se llama a cualquier función de C.</span><span class="sxs-lookup"><span data-stu-id="fe089-109">To execute the procedure call remotely, call the client-side stub function in the same manner any C function is called.</span></span>

 

 




