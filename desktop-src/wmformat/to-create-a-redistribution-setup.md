---
title: Para crear una configuración de redistribución
description: Para crear una configuración de redistribución
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- SDK de Windows Media Format, redistribución de software
- Advanced Systems Format (ASF), redistribución de software
- ASF (formato de sistemas avanzados), redistribución de software
- SDK de Windows Media Format, redistribución
- Advanced Systems Format (ASF), redistribución
- ASF (formato de sistemas avanzados), redistribución
- redistribución de software, crear
- redistribución de software, WMFDist.exe
- redistribución, crear
- redistribución, WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0c2f241d8c1ad164bc14608103f423a7aba78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268705"
---
# <a name="to-create-a-redistribution-setup"></a><span data-ttu-id="12c18-114">Para crear una configuración de redistribución</span><span class="sxs-lookup"><span data-stu-id="12c18-114">To Create a Redistribution Setup</span></span>

1.  <span data-ttu-id="12c18-115">Haga que su rutina de instalación Instale los archivos de aplicación y realice la configuración necesaria antes de invocar el paquete de redistribución.</span><span class="sxs-lookup"><span data-stu-id="12c18-115">Have your setup routine install your application files and make required settings before invoking the redistribution package.</span></span>
2.  <span data-ttu-id="12c18-116">Instale WMFDist.exe.</span><span class="sxs-lookup"><span data-stu-id="12c18-116">Install WMFDist.exe.</span></span> <span data-ttu-id="12c18-117">Puede usar la marca/Q: a para realizar una instalación silenciosa y desatendida, y suprimir la interfaz de usuario de la configuración de redistribución durante la instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="12c18-117">You can use the /Q:A flag to do a quiet, unattended installation and suppress the user interface of the redistribution setup during the installation of your application.</span></span> <span data-ttu-id="12c18-118">A continuación, la rutina debe detectar si es necesario reiniciar al final.</span><span class="sxs-lookup"><span data-stu-id="12c18-118">Your routine must then detect whether restarting is needed at the end.</span></span>

    <span data-ttu-id="12c18-119">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="12c18-119">For example:</span></span>

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a><span data-ttu-id="12c18-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12c18-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12c18-121">**Redistribución de software**</span><span class="sxs-lookup"><span data-stu-id="12c18-121">**Software Redistribution**</span></span>](software-redistribution.md)
</dt> </dl>

 

 




