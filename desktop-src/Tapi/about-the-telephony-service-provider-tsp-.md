---
description: Un proveedor de servicios de telefonía (TSP) TAPI es una biblioteca de vínculos dinámicos (DLL) que admite el control de los dispositivos de comunicaciones a través de un conjunto de funciones de servicio exportadas.
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: Acerca del proveedor de servicios de telefonía (TSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5200a4291bdd91aba9f93a5552fecf4b52d24ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809242"
---
# <a name="about-the-telephony-service-provider-tsp"></a><span data-ttu-id="2c2ac-103">Acerca del proveedor de servicios de telefonía (TSP)</span><span class="sxs-lookup"><span data-stu-id="2c2ac-103">About the Telephony Service Provider (TSP)</span></span>

<span data-ttu-id="2c2ac-104">\[ Los profesionales H323 y IPConf no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2c2ac-104">\[ The H323 and IPConf TSPs are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2c2ac-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="2c2ac-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2c2ac-106">Un proveedor de servicios de telefonía (TSP) TAPI es una biblioteca de vínculos dinámicos (DLL) que admite el control de los dispositivos de comunicaciones a través de un conjunto de funciones de servicio exportadas.</span><span class="sxs-lookup"><span data-stu-id="2c2ac-106">A TAPI telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="2c2ac-107">Una aplicación TAPI usa comandos estandarizados, TAPI pasa al proveedor de servicios de telefonía y el TSP controla los comandos específicos que se deben intercambiar con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c2ac-107">A TAPI application uses standardized commands, TAPI passes in formation to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span>

<span data-ttu-id="2c2ac-108">En las siguientes secciones se describen brevemente los profesionales proporcionados con Microsoft Windows:</span><span class="sxs-lookup"><span data-stu-id="2c2ac-108">The following sections briefly describe the TSPs provided with Microsoft Windows:</span></span>

-   [<span data-ttu-id="2c2ac-109">TSP H323</span><span class="sxs-lookup"><span data-stu-id="2c2ac-109">H323 TSP</span></span>](h323-tsp.md)
-   [<span data-ttu-id="2c2ac-110">IPConf TSP</span><span class="sxs-lookup"><span data-stu-id="2c2ac-110">IPConf TSP</span></span>](ipconf-tsp.md)
-   [<span data-ttu-id="2c2ac-111">Proveedor de dispositivos de modo kernel (TSP)</span><span class="sxs-lookup"><span data-stu-id="2c2ac-111">Kernel-Mode Device Driver TSP</span></span>](kernel-mode-device-driver-tsp.md)
-   [<span data-ttu-id="2c2ac-112">TSP de proxy NDIS</span><span class="sxs-lookup"><span data-stu-id="2c2ac-112">NDIS Proxy TSP</span></span>](ndis-proxy-tsp.md)
-   [<span data-ttu-id="2c2ac-113">TSP remoto</span><span class="sxs-lookup"><span data-stu-id="2c2ac-113">Remote TSP</span></span>](remote-tsp.md)
-   [<span data-ttu-id="2c2ac-114">TSP de terceros</span><span class="sxs-lookup"><span data-stu-id="2c2ac-114">Third-Party TSP</span></span>](third-party-tsp.md)
-   [<span data-ttu-id="2c2ac-115">TSP de Unimodem</span><span class="sxs-lookup"><span data-stu-id="2c2ac-115">Unimodem TSP</span></span>](unimodem-tsp.md)

<span data-ttu-id="2c2ac-116">Para obtener información detallada, consulte el kit de recursos del sistema operativo de destino.</span><span class="sxs-lookup"><span data-stu-id="2c2ac-116">For detailed information, please see the Resource Kit for the target operating system.</span></span> <span data-ttu-id="2c2ac-117">Normalmente, el fabricante proporcionará profesionales de terceros para dispositivos de comunicaciones especializados y se instalará con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c2ac-117">Third-party TSPs for specialized communications devices will typically be provided by the manufacturer and will be installed with the device.</span></span>

<span data-ttu-id="2c2ac-118">En los temas siguientes se describe cómo crear un TSP que funcione correctamente en el entorno de telefonía de Microsoft y cómo crear un par de TSP/MSP:</span><span class="sxs-lookup"><span data-stu-id="2c2ac-118">The following topics describe how to create a TSP that will function properly within the Microsoft Telephony environment, and how to create a TSP/MSP pair:</span></span>

-   [<span data-ttu-id="2c2ac-119">Interfaz del proveedor de servicios de telefonía (TSPI)</span><span class="sxs-lookup"><span data-stu-id="2c2ac-119">Telephony Service Provider Interface (TSPI)</span></span>](telephony-service-provider-interface-tspi-.md)
-   [<span data-ttu-id="2c2ac-120">Referencia de TSPI</span><span class="sxs-lookup"><span data-stu-id="2c2ac-120">TSPI Reference</span></span>](tspi-reference.md)
-   [<span data-ttu-id="2c2ac-121">Proveedores de servicios multimedia</span><span class="sxs-lookup"><span data-stu-id="2c2ac-121">Media Service Providers</span></span>](./media-service-providers-start-page.md)

> [!Note]  
> <span data-ttu-id="2c2ac-122">Un TSP es un archivo DLL creado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2c2ac-122">A TSP is a user-created DLL.</span></span> <span data-ttu-id="2c2ac-123">Si va a crear un TSP para una plataforma de Windows de 64 bits, debe compilarlo como DLL o dll de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2c2ac-123">If you are creating a TSP for a 64-bit Windows platform, you must compile it as a 64-bit DLL or DLLs.</span></span>

 

 

 
