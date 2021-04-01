---
title: Agregar controladores dentro de una aplicación
description: Agregar controladores dentro de una aplicación
ms.assetid: cd9bd0a8-652b-440b-a197-81e20a9d71f1
keywords:
- Administrador de compresión de audio (ACM), agregar controladores
- ACM (Administrador de compresión de audio), agregar controladores
- Ejemplos de ACM, agregar controladores
- agregar controladores
- acmDriverAdd función)
- Controladores globales
- Controladores locales
- Administrador de compresión de audio (ACM), controladores globales
- ACM (Administrador de compresión de audio), controladores globales
- Administrador de compresión de audio (ACM), controladores locales
- ACM (Administrador de compresión de audio), controladores locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bf7bded89b778f271599d5ce0f8d7f7bd5f72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075738"
---
# <a name="adding-drivers-within-an-application"></a><span data-ttu-id="5b7b3-114">Agregar controladores dentro de una aplicación</span><span class="sxs-lookup"><span data-stu-id="5b7b3-114">Adding Drivers Within an Application</span></span>

<span data-ttu-id="5b7b3-115">Si necesita que la aplicación implemente sus propias rutinas de compresión internamente, la aplicación puede agregar controladores a ACM mediante una llamada a la función [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) .</span><span class="sxs-lookup"><span data-stu-id="5b7b3-115">If you need your application to implement its own compression routines internally, the application can add drivers to the ACM by calling the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function.</span></span> <span data-ttu-id="5b7b3-116">La aplicación implementa el controlador proporcionando una función que se ajusta al prototipo [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) .</span><span class="sxs-lookup"><span data-stu-id="5b7b3-116">The application implements the driver by providing a function that conforms to the [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) prototype.</span></span> <span data-ttu-id="5b7b3-117">Una vez que la aplicación ha agregado el controlador, la aplicación puede usar el controlador a través de ACM, ya que usaría cualquier otro controlador.</span><span class="sxs-lookup"><span data-stu-id="5b7b3-117">After the application has added the driver, the application can use the driver through the ACM as it would use any other driver.</span></span>

<span data-ttu-id="5b7b3-118">ACM trata los controladores como globales o locales.</span><span class="sxs-lookup"><span data-stu-id="5b7b3-118">The ACM treats drivers as either global or local.</span></span> <span data-ttu-id="5b7b3-119">Una aplicación especifica si se debe agregar un controlador como global o local cuando llama a **acmDriverAdd**.</span><span class="sxs-lookup"><span data-stu-id="5b7b3-119">An application specifies whether a driver should be added as global or local when it calls **acmDriverAdd**.</span></span> <span data-ttu-id="5b7b3-120">Hay dos diferencias entre los controladores globales y locales:</span><span class="sxs-lookup"><span data-stu-id="5b7b3-120">There are two differences between global and local drivers:</span></span>

-   <span data-ttu-id="5b7b3-121">Los controladores agregados como controladores globales no se comparten con otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5b7b3-121">Drivers added as global drivers are not shared with other applications.</span></span>
-   <span data-ttu-id="5b7b3-122">Una aplicación puede modificar directamente la prioridad de un controlador global (pero no un controlador local) mediante una llamada a la función [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) .</span><span class="sxs-lookup"><span data-stu-id="5b7b3-122">An application can directly alter the priority of a global driver (but not a local driver) by calling the [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) function.</span></span> <span data-ttu-id="5b7b3-123">ACM realiza una búsqueda prioritaria al buscar un controlador adecuado para proporcionar una implementación de una llamada de función.</span><span class="sxs-lookup"><span data-stu-id="5b7b3-123">The ACM conducts a prioritized search when seeking an appropriate driver to provide an implementation of a function call.</span></span> <span data-ttu-id="5b7b3-124">ACM siempre proporciona a los controladores locales mayor prioridad que los controladores globales.</span><span class="sxs-lookup"><span data-stu-id="5b7b3-124">The ACM always gives local drivers higher priority than global drivers.</span></span> <span data-ttu-id="5b7b3-125">El controlador local agregado más recientemente tiene la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="5b7b3-125">The most recently added local driver has highest priority.</span></span>

 

 




