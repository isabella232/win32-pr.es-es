---
description: El sistema utiliza la información de configuración para determinar cómo iniciar el servicio.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Configuración de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5019469e17fdd0807aa101c7d1e4d6f6019da783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541123"
---
# <a name="service-configuration"></a><span data-ttu-id="81a90-103">Configuración de servicio</span><span class="sxs-lookup"><span data-stu-id="81a90-103">Service Configuration</span></span>

<span data-ttu-id="81a90-104">El sistema utiliza la información de configuración para determinar cómo iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="81a90-104">The system uses the configuration information to determine how to start the service.</span></span> <span data-ttu-id="81a90-105">La información de configuración también incluye el nombre para mostrar del servicio y su descripción.</span><span class="sxs-lookup"><span data-stu-id="81a90-105">The configuration information also includes the service display name and its description.</span></span> <span data-ttu-id="81a90-106">Por ejemplo, para el servicio DHCP, puede usar el nombre para mostrar "servicio de protocolo de configuración dinámica de host" y la descripción "proporciona direcciones de Internet para el equipo en la red".</span><span class="sxs-lookup"><span data-stu-id="81a90-106">For example, for the DHCP service, you could use the display name "Dynamic Host Configuration Protocol Service" and the description "Provides internet addresses for computer on your network."</span></span>

<span data-ttu-id="81a90-107">Para modificar la información de configuración de un objeto de servicio, un programa de configuración utiliza la función [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) o [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) .</span><span class="sxs-lookup"><span data-stu-id="81a90-107">To modify the configuration information for a service object, a configuration program uses the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) or [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function.</span></span> <span data-ttu-id="81a90-108">Para obtener un ejemplo, consulte [cambiar una configuración de servicio](changing-a-service-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="81a90-108">For an example, see [Changing a Service Configuration](changing-a-service-configuration.md).</span></span>

<span data-ttu-id="81a90-109">Para recuperar la información de configuración de un objeto de servicio, el programa de configuración utiliza la función [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) o [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) .</span><span class="sxs-lookup"><span data-stu-id="81a90-109">To retrieve the configuration information for a service object, the configuration program uses the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) or [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) function.</span></span> <span data-ttu-id="81a90-110">Para obtener un ejemplo, consulte [consultar la configuración de un servicio](querying-a-service-s-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="81a90-110">For an example, see [Querying a Service's Configuration](querying-a-service-s-configuration.md).</span></span>

<span data-ttu-id="81a90-111">Las funciones de configuración del servicio [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) y [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) admiten el uso de desencadenadores para controlar el inicio del servicio.</span><span class="sxs-lookup"><span data-stu-id="81a90-111">The [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) service configuration functions support the use of triggers to control service start.</span></span>

<span data-ttu-id="81a90-112">Para modificar el descriptor de seguridad para un objeto SCManager o un objeto de servicio, un programa de configuración utiliza la función [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="81a90-112">To modify the security descriptor for either an SCManager object or a service object, a configuration program uses the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function.</span></span> <span data-ttu-id="81a90-113">Para recuperar una copia del descriptor de seguridad, el programa de configuración utiliza la función [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="81a90-113">To retrieve a copy of the security descriptor, the configuration program uses the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81a90-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81a90-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81a90-115">Configuración de un servicio mediante SC</span><span class="sxs-lookup"><span data-stu-id="81a90-115">Configuring a Service Using SC</span></span>](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
