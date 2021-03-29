---
description: El conjunto de herramientas de configuración de seguridad de Microsoft es un conjunto de herramientas de Microsoft Management Console (MMC) que simplifican la configuración y el análisis de la seguridad del sistema.
ms.assetid: c6558789-84eb-4998-a2c1-725d8a64d255
title: Datos adjuntos de seguridad del servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47cdd0ca3799615125900a3ae6b0b78c26f4abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360217"
---
# <a name="service-security-attachments"></a><span data-ttu-id="13b97-103">Datos adjuntos de seguridad del servicio</span><span class="sxs-lookup"><span data-stu-id="13b97-103">Service Security Attachments</span></span>

<span data-ttu-id="13b97-104">El conjunto de herramientas de configuración de seguridad de Microsoft es un conjunto de herramientas de Microsoft Management Console (MMC) que simplifican la configuración y el análisis de la seguridad del sistema.</span><span class="sxs-lookup"><span data-stu-id="13b97-104">The Microsoft Security Configuration tool set is a set of Microsoft Management Console (MMC) tools that simplify configuration and analysis of system security.</span></span> <span data-ttu-id="13b97-105">Sin embargo, algunos servicios tienen necesidades de configuración especializadas que van más allá de la configuración de seguridad proporcionada por el conjunto de herramientas estándar.</span><span class="sxs-lookup"><span data-stu-id="13b97-105">Some services, however, have specialized configuration needs that go beyond the security settings provided by the standard tool set.</span></span> <span data-ttu-id="13b97-106">Para controlar esas necesidades, puede extender la funcionalidad del conjunto de herramientas escribiendo datos adjuntos que controlan las tareas de seguridad específicas del servicio.</span><span class="sxs-lookup"><span data-stu-id="13b97-106">To handle those needs, you can extend the functionality of the tool set by writing an attachment that handles the service-specific security tasks.</span></span>

<span data-ttu-id="13b97-107">Por ejemplo, el administrador de trabajos de impresión es un servicio de Windows NT que define objetos privados, que deben protegerse, por ejemplo, impresoras.</span><span class="sxs-lookup"><span data-stu-id="13b97-107">For example, Spooler is a Windows NT service that defines private objects, which need to be secured, for example, printers.</span></span> <span data-ttu-id="13b97-108">Esta funcionalidad no está controlada por el conjunto de herramientas estándar y, por tanto, requiere un dato adjunto para controlar la configuración y el análisis de los objetos de impresora.</span><span class="sxs-lookup"><span data-stu-id="13b97-108">This functionality is not handled by the standard tool set and thus requires an attachment to handle configuration and analysis of printer objects.</span></span> <span data-ttu-id="13b97-109">La configuración de los parámetros de seguridad generales, como la Directiva de invocación de servicio, todavía se controla mediante el conjunto de herramientas de configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="13b97-109">Configuration of general security parameters, such as the service invocation policy, is still handled by the Security Configuration tool set.</span></span>

<span data-ttu-id="13b97-110">Los datos adjuntos del servicio de seguridad amplían la funcionalidad del conjunto de herramientas de configuración de seguridad para admitir configuraciones específicas del servicio.</span><span class="sxs-lookup"><span data-stu-id="13b97-110">Security service attachments extend the functionality of the Security Configuration tool set to support service-specific configurations.</span></span>

<span data-ttu-id="13b97-111">Los datos adjuntos tienen dos componentes:</span><span class="sxs-lookup"><span data-stu-id="13b97-111">An attachment has two components:</span></span>

-   <span data-ttu-id="13b97-112">Extensión del complemento MMC que implementa la interfaz de usuario de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="13b97-112">An MMC snap-in extension that implements the attachment user interface.</span></span>
-   <span data-ttu-id="13b97-113">Motor de datos adjuntos que procesa tareas de análisis y configuración de seguridad específicas del servicio.</span><span class="sxs-lookup"><span data-stu-id="13b97-113">An attachment engine that processes service-specific security configuration and analysis tasks.</span></span>

<span data-ttu-id="13b97-114">Los complementos de configuración de seguridad hospedan la extensión del complemento de datos adjuntos. Se trata de complementos de MMC que proporcionan al usuario interfaces para configurar y analizar la configuración de seguridad general de un servicio.</span><span class="sxs-lookup"><span data-stu-id="13b97-114">The attachment snap-in extension is hosted by the Security Configuration snap-ins. These are MMC snap-ins that provide the user with interfaces to configure and analyze the general security settings for a service.</span></span> <span data-ttu-id="13b97-115">La configuración específica del servicio se configura mediante la extensión del complemento de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="13b97-115">Service-specific settings are configured using the attachment snap-in extension.</span></span>

<span data-ttu-id="13b97-116">Cuando el usuario cambia una opción de configuración, los complementos de configuración de seguridad almacenan la nueva información y, a continuación, pasan la solicitud al motor de configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="13b97-116">When the user changes a configuration setting, the Security Configuration snap-ins store the new information and then pass the request to the Security Configuration Engine.</span></span> <span data-ttu-id="13b97-117">El motor procesa la solicitud y establece el servicio en la nueva configuración.</span><span class="sxs-lookup"><span data-stu-id="13b97-117">The Engine processes the request and sets the service to the new configuration.</span></span> <span data-ttu-id="13b97-118">Si la solicitud afecta a una configuración de seguridad estándar, la administra el motor.</span><span class="sxs-lookup"><span data-stu-id="13b97-118">If the request affects a standard security setting, it is handled by the Engine.</span></span> <span data-ttu-id="13b97-119">Si la solicitud es específica del servicio, el motor llama al motor de datos adjuntos adecuado para administrar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="13b97-119">If the request is service-specific, the Engine calls the appropriate attachment engine to handle the request.</span></span>

<span data-ttu-id="13b97-120">En la ilustración siguiente se muestra cómo funcionan el motor de datos adjuntos y la extensión del complemento en el marco del conjunto de herramientas de configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="13b97-120">The following illustration shows how the attachment engine and snap-in extension work within the framework of the Security Configuration tool set.</span></span>

![complemento y motor de datos adjuntos](images/model1a.png)

<span data-ttu-id="13b97-122">Para obtener más información sobre el uso del conjunto de herramientas de configuración de seguridad de Microsoft, busque configuración de seguridad con el motor de búsqueda preferido.</span><span class="sxs-lookup"><span data-stu-id="13b97-122">For more information about using the Microsoft Security Configuration tool set, search for Security Configuration using your preferred search engine.</span></span>

 

 



