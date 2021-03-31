---
title: Redistribución de software
description: Redistribución de software
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- SDK de Windows Media Format, redistribución de software
- Advanced Systems Format (ASF), redistribución de software
- ASF (formato de sistemas avanzados), redistribución de software
- SDK de Windows Media Format, redistribución
- Advanced Systems Format (ASF), redistribución
- ASF (formato de sistemas avanzados), redistribución
- redistribución de software, acerca de
- redistribución, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d51f332f5b0e038293a1dbe1dbf59015931d67e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775012"
---
# <a name="software-redistribution"></a><span data-ttu-id="3d94a-111">Redistribución de software</span><span class="sxs-lookup"><span data-stu-id="3d94a-111">Software Redistribution</span></span>

<span data-ttu-id="3d94a-112">La inclusión del software Windows Media Format en una configuración de aplicación se conoce como redistribución.</span><span class="sxs-lookup"><span data-stu-id="3d94a-112">The inclusion of Windows Media Format software in an application setup is known as redistribution.</span></span> <span data-ttu-id="3d94a-113">El SDK de Windows Media Format incluye un paquete de instalación que se puede incluir con la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d94a-113">The Windows Media Format SDK includes an installation package which can be included with your application setup.</span></span> <span data-ttu-id="3d94a-114">El paquete de instalación es un archivo ejecutable denominado wmfdist95.exe.</span><span class="sxs-lookup"><span data-stu-id="3d94a-114">The installation package is an executable file named wmfdist95.exe.</span></span> <span data-ttu-id="3d94a-115">Al instalar el SDK de Windows Media Format, el paquete de instalación se copia en la \\ carpeta Redist del directorio de instalación (c: \\ wmsdk wmfsdk de \\ forma predeterminada).</span><span class="sxs-lookup"><span data-stu-id="3d94a-115">When you install the Windows Media Format SDK, the installation package is copied to the \\Redist folder of the install directory (c:\\wmsdk\\wmfsdk by default).</span></span>

<span data-ttu-id="3d94a-116">En las secciones siguientes se proporcionan procedimientos y otra información para la configuración de la redistribución de software.</span><span class="sxs-lookup"><span data-stu-id="3d94a-116">The following sections provide procedures and other information for software redistribution setup.</span></span>



| <span data-ttu-id="3d94a-117">Sección</span><span class="sxs-lookup"><span data-stu-id="3d94a-117">Section</span></span>                                                                            | <span data-ttu-id="3d94a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d94a-118">Description</span></span>                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d94a-119">Para crear una configuración de redistribución</span><span class="sxs-lookup"><span data-stu-id="3d94a-119">To Create a Redistribution Setup</span></span>](to-create-a-redistribution-setup.md)           | <span data-ttu-id="3d94a-120">Describe el procedimiento para crear una instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d94a-120">Describes the procedure for creating an application setup.</span></span>                                                                                                                       |
| [<span data-ttu-id="3d94a-121">Detección del estado de la instalación</span><span class="sxs-lookup"><span data-stu-id="3d94a-121">Detecting Setup Status</span></span>](detecting-setup-status.md)                               | <span data-ttu-id="3d94a-122">Proporciona código de ejemplo que comprueba el estado de la instalación del registro para determinar si es necesario instalar el paquete de redistribución.</span><span class="sxs-lookup"><span data-stu-id="3d94a-122">Provides example code that checks the registry for installation status to determine whether the redistribution package needs to be installed.</span></span>                                    |
| [<span data-ttu-id="3d94a-123">Código de ejemplo para la configuración de redistribución</span><span class="sxs-lookup"><span data-stu-id="3d94a-123">Example Code for Redistribution Setup</span></span>](example-code-for-redistribution-setup.md) | <span data-ttu-id="3d94a-124">Proporciona código de ejemplo que se puede usar en la rutina de instalación para ejecutar los paquetes de redistribución en modo silencioso y notificar a la rutina de configuración cuando se debe reiniciar el equipo.</span><span class="sxs-lookup"><span data-stu-id="3d94a-124">Provides example code that can be used in your setup routine to run the redistribution packages in quiet mode and notify your setup routine when the computer must be restarted.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3d94a-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3d94a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d94a-126">**Consideraciones del proyecto**</span><span class="sxs-lookup"><span data-stu-id="3d94a-126">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




