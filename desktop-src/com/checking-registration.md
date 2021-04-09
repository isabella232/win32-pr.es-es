---
title: Comprobando registro
description: Comprobando registro
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee215fd052ffc242900eead069a8b72fd25b31d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994043"
---
# <a name="checking-registration"></a><span data-ttu-id="c412f-103">Comprobando registro</span><span class="sxs-lookup"><span data-stu-id="c412f-103">Checking Registration</span></span>

<span data-ttu-id="c412f-104">Cada vez que se carga una aplicación, debe comprobar su registro para determinar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c412f-104">Each time an application loads, it should check its registration to determine the following:</span></span>

-   <span data-ttu-id="c412f-105">Si los CLSID están presentes en el registro.</span><span class="sxs-lookup"><span data-stu-id="c412f-105">Whether the CLSIDs are present in the registry.</span></span> <span data-ttu-id="c412f-106">Si no están presentes, la aplicación debe registrarse como la configuración original.</span><span class="sxs-lookup"><span data-stu-id="c412f-106">If they are not present, the application should register as the original setup.</span></span>
-   <span data-ttu-id="c412f-107">Si los CLSID de la aplicación están presentes en el registro pero no tienen ninguna información relacionada con OLE 2.</span><span class="sxs-lookup"><span data-stu-id="c412f-107">Whether the application's CLSIDs are present in the register but have no OLE 2-related information in them.</span></span> <span data-ttu-id="c412f-108">En este caso, la aplicación debe registrarse como la configuración original.</span><span class="sxs-lookup"><span data-stu-id="c412f-108">If this is the case, the application should register as the original setup.</span></span>
-   <span data-ttu-id="c412f-109">Si la ruta de acceso que contiene entradas del servidor ([LocalServer](localserver.md) y [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) y [InProcServer32](inprocserver32.md)y [DefaultIcon](defaulticon.md)) apunta a la ubicación en la que la aplicación está instalada actualmente.</span><span class="sxs-lookup"><span data-stu-id="c412f-109">Whether the path containing server entries ([LocalServer](localserver.md) and [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) and [InprocServer32](inprocserver32.md), and [DefaultIcon](defaulticon.md)) points to the location at which the application is currently installed.</span></span> <span data-ttu-id="c412f-110">Si la ruta de acceso no es, vuelva a escribir las entradas de ruta de acceso para que apunten a la ubicación actual.</span><span class="sxs-lookup"><span data-stu-id="c412f-110">If the path does not, rewrite the path entries to point to the current location.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c412f-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c412f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c412f-112">Registro de aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="c412f-112">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 




