---
title: Información de error extendida para el usuario
description: Si hay disponible información de error ampliada, los componentes que participan en la creación de la información de error extendida deben facilitar la búsqueda del problema.
ms.assetid: 10c54f53-f449-4e7d-ba84-7b000beaee22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f52e45e3f181c5aaa0db196f9ce791581cc38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903553"
---
# <a name="extended-error-information-for-the-user"></a><span data-ttu-id="bbd8b-103">Información de error extendida para el usuario</span><span class="sxs-lookup"><span data-stu-id="bbd8b-103">Extended Error Information for the User</span></span>

<span data-ttu-id="bbd8b-104">Si hay disponible información de error ampliada, los componentes que participan en la creación de la información de error extendida deben facilitar la búsqueda del problema.</span><span class="sxs-lookup"><span data-stu-id="bbd8b-104">If extended error information is available, the components participating in the creation of the extended error information must make it easy to find the problem.</span></span> <span data-ttu-id="bbd8b-105">El primer paso es revisar el último registro de error extendido y determinar en qué equipo y qué proceso se originó el problema.</span><span class="sxs-lookup"><span data-stu-id="bbd8b-105">The first step is to review the last extended error record, and determine on which computer and which process the problem originated.</span></span> <span data-ttu-id="bbd8b-106">Esta suele ser la causa del error de RPC \_ S \_ \* .</span><span class="sxs-lookup"><span data-stu-id="bbd8b-106">This is often the cause of the RPC\_S\_\* error.</span></span> <span data-ttu-id="bbd8b-107">Busque la ubicación de detección y determine el significado de los parámetros de esta ubicación de detección.</span><span class="sxs-lookup"><span data-stu-id="bbd8b-107">Find the detection location, and determine what the parameters for this detection location mean.</span></span> <span data-ttu-id="bbd8b-108">Normalmente, indican un error en una llamada de función o en una comprobación determinada.</span><span class="sxs-lookup"><span data-stu-id="bbd8b-108">Usually they indicate a failure of a function call or particular check.</span></span> <span data-ttu-id="bbd8b-109">A partir de ahí, determine por qué se produce un error en la función o comprobación y tome medidas correctivas.</span><span class="sxs-lookup"><span data-stu-id="bbd8b-109">From there, determine why the function or check fails, and take corrective action.</span></span>

<span data-ttu-id="bbd8b-110">Los registros antes del último registro indican la ruta de acceso en la que llegó el error y, por lo general, sirven como comprobación de validez en lugar de una solución alternativa en el proceso de solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="bbd8b-110">The records before the last record indicate the path by which the error arrived, and generally serve as a sanity check rather than an aide in the troubleshooting process.</span></span>

 

 




