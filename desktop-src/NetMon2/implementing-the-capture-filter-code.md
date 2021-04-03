---
description: Después de determinar cómo organizar el filtro a través de una estructura CAPTUREFILTER, debe asignar y rellenar la estructura, que se pasa a la Monitor de red controlador a través de un BLOB de configuración.
ms.assetid: c2709da6-4d70-4abe-bab5-941053217e57
title: Implementar el código de filtro de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c407f3208a1c7720655667f78e4422b57882de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913858"
---
# <a name="implementing-the-capture-filter-code"></a><span data-ttu-id="09220-103">Implementar el código de filtro de captura</span><span class="sxs-lookup"><span data-stu-id="09220-103">Implementing the Capture Filter Code</span></span>

<span data-ttu-id="09220-104">Después de determinar cómo organizar el filtro a través de una estructura [**CAPTUREFILTER**](capturefilter.md) , debe asignar y rellenar la estructura, que se pasa a la monitor de red controlador a través de un BLOB de configuración.</span><span class="sxs-lookup"><span data-stu-id="09220-104">After you determine how to organize your filter through a [**CAPTUREFILTER**](capturefilter.md) structure, you must allocate and fill in the structure, which is then passed to the Network Monitor driver through a configuration BLOB.</span></span>

<span data-ttu-id="09220-105">Los usuarios directos de NPP agregan el filtro de captura al BLOB de configuración que se pasa a **Connect**, [**Configure**](configure.md)o ambos.</span><span class="sxs-lookup"><span data-stu-id="09220-105">Direct NPP users add the capture filter to the configuration BLOB that is passed to **Connect**, [**Configure**](configure.md), or both.</span></span> <span data-ttu-id="09220-106">Para obtener una lista de las interfaces COM que puede usar para comunicarse con el NPP, consulte [interfaces NPP](npp-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="09220-106">For a list of COM interfaces that you can use to communicate with the NPP, see [NPP Interfaces](npp-interfaces.md).</span></span>

 

 



