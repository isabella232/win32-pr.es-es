---
description: Los orígenes principales de los procedimientos de instalación son el kit de recursos del sistema operativo de destino, la documentación de la aplicación y las instrucciones del proveedor de servicios. En el caso de los proveedores de servicios de Microsoft, el kit de recursos adecuado contiene instrucciones.
ms.assetid: a94023ac-5226-4a51-a08b-c53d08260710
title: Instalación (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446510c3d92431188bcff50842b15c200cc5d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677611"
---
# <a name="installation-telephony-api"></a><span data-ttu-id="d88fe-104">Instalación (API de telefonía)</span><span class="sxs-lookup"><span data-stu-id="d88fe-104">Installation (Telephony API)</span></span>

<span data-ttu-id="d88fe-105">Los orígenes principales de los procedimientos de instalación son el kit de recursos del sistema operativo de destino, la documentación de la aplicación y las instrucciones del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="d88fe-105">The primary sources for installation procedures are the Resource Kit for the target operating system, application documentation, and service provider instructions.</span></span> <span data-ttu-id="d88fe-106">En el caso de los proveedores de servicios de Microsoft, el kit de recursos adecuado contiene instrucciones.</span><span class="sxs-lookup"><span data-stu-id="d88fe-106">For Microsoft service providers, the appropriate resource kit contains instructions.</span></span>

<span data-ttu-id="d88fe-107">El proceso de instalación debe incluir la lista de "servicio de telefonía" como dependencia.</span><span class="sxs-lookup"><span data-stu-id="d88fe-107">The installation process must include listing "Telephony Service" as dependency.</span></span>

<span data-ttu-id="d88fe-108">Si una aplicación o un proveedor de servicios utiliza el registro para el almacenamiento de datos privados persistentes, la información no se debe colocar en la sección de TAPI del registro.</span><span class="sxs-lookup"><span data-stu-id="d88fe-108">If an application or service provider uses the registry for storage of persistent private data, the information must not be placed in TAPI's section of the registry.</span></span> <span data-ttu-id="d88fe-109">No se garantiza que el formato de esta sección se mantenga en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="d88fe-109">The format of this section is not guaranteed to be maintained in future versions.</span></span>

 

 



