---
description: Limitaciones del programa de ejemplo
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Limitaciones del programa de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1fde65fa1870ac3ed118bd7c9f95c6add5192f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668031"
---
# <a name="example-program-limitations"></a><span data-ttu-id="ad77d-103">Limitaciones del programa de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad77d-103">Example Program Limitations</span></span>

<span data-ttu-id="ad77d-104">Los principios de una buena práctica de programación no se siguen siempre en estos programas de ejemplo para proporcionar código más conciso y más legible.</span><span class="sxs-lookup"><span data-stu-id="ad77d-104">Principles of good programming practice are not always followed in these sample programs in order to provide more concise, more readable code.</span></span> <span data-ttu-id="ad77d-105">En concreto:</span><span class="sxs-lookup"><span data-stu-id="ad77d-105">In particular:</span></span>

-   <span data-ttu-id="ad77d-106">Solo se muestran las respuestas de error limitadas.</span><span class="sxs-lookup"><span data-stu-id="ad77d-106">Only limited error responses are shown.</span></span> <span data-ttu-id="ad77d-107">Los programas de trabajo siempre deben comprobar los códigos de error devueltos y realizar las acciones adecuadas cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="ad77d-107">Working programs should always check returned error codes and perform appropriate actions when an error is encountered.</span></span>
-   <span data-ttu-id="ad77d-108">Solo se lleva a cabo la administración de memoria y recursos limitados.</span><span class="sxs-lookup"><span data-stu-id="ad77d-108">Only limited memory and resource management is done.</span></span> <span data-ttu-id="ad77d-109">En los programas de trabajo, todas las claves y los [*valores hash*](../secgloss/h-gly.md) deben destruirse, se debe liberar toda la memoria asignada, se deben cerrar todos los archivos y se deben liberar todos los identificadores.</span><span class="sxs-lookup"><span data-stu-id="ad77d-109">In working programs, all keys and [*hashes*](../secgloss/h-gly.md) should be destroyed, all allocated memory should be freed, all files should be closed, and all handles should be released.</span></span> <span data-ttu-id="ad77d-110">Estos programas de ejemplo solo proporcionan demostraciones limitadas del uso de funciones que realizan estas tareas.</span><span class="sxs-lookup"><span data-stu-id="ad77d-110">These example programs provide only limited demonstrations of the use of functions that perform these tasks.</span></span> <span data-ttu-id="ad77d-111">Estos programas de ejemplo no realizan ninguna tarea de administración de recursos ni memoria en el caso de la finalización del programa debido a errores.</span><span class="sxs-lookup"><span data-stu-id="ad77d-111">These example programs perform no memory or resource management tasks in the case of program termination due to errors.</span></span>

 

 
