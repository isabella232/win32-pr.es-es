---
title: Publicación con la resolución de & de registro de Windows Sockets
description: Los servicios de Windows Sockets pueden usar las API de registro y resolución (RnR) para publicar servicios y buscar servicios publicados con RnR.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Registro y resolución de Windows Sockets AD, publicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e722d83447bd97e3964a9a0cc85df45ffd27faba
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/04/2019
ms.locfileid: "104487207"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a><span data-ttu-id="1dd47-104">Publicación con la resolución de & de registro de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="1dd47-104">Publishing with Windows Sockets Registration & Resolution</span></span>

<span data-ttu-id="1dd47-105">Los servicios de Windows Sockets pueden usar las API de registro y resolución (RnR) para publicar servicios y buscar servicios publicados con RnR.</span><span class="sxs-lookup"><span data-stu-id="1dd47-105">Windows Sockets services can use the Registration and Resolution (RnR) APIs to publish services and look up services published with RnR.</span></span> <span data-ttu-id="1dd47-106">La publicación de RnR se produce en dos pasos.</span><span class="sxs-lookup"><span data-stu-id="1dd47-106">RnR publication occurs in two steps.</span></span> <span data-ttu-id="1dd47-107">En el primer paso se instala una clase de servicio que asocia un GUID con un nombre para el servicio.</span><span class="sxs-lookup"><span data-stu-id="1dd47-107">The first step installs a service class that associates a GUID with a name for the service.</span></span> <span data-ttu-id="1dd47-108">La clase de servicio puede contener datos de configuración específicos del servicio.</span><span class="sxs-lookup"><span data-stu-id="1dd47-108">The service class can hold service-specific configuration data.</span></span> <span data-ttu-id="1dd47-109">Después, los servicios pueden publicarse como instancias de la clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="1dd47-109">Services can then publish themselves as instances of the service class.</span></span> <span data-ttu-id="1dd47-110">Cuando se publican, los clientes pueden consultar el servicio de directorio en busca de instancias de una clase determinada mediante las API de RnR y seleccionar una instancia de a la que enlazar.</span><span class="sxs-lookup"><span data-stu-id="1dd47-110">When published, clients can query the directory service for instances of a given class using the RnR APIs and select an instance to bind to.</span></span> <span data-ttu-id="1dd47-111">Cuando ya no se necesita una clase, se puede quitar.</span><span class="sxs-lookup"><span data-stu-id="1dd47-111">When a class is no longer required, it can be removed.</span></span>

 

 




