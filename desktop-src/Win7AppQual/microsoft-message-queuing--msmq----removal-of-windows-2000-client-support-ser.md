---
description: .
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: 'Microsoft Message Queuing (MSMQ): quitar el servicio de compatibilidad con clientes de Windows 2000'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54688ee4ad24eb691c95e4d70ce0acb881e212eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083176"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a><span data-ttu-id="cee48-103">Microsoft Message Queuing (MSMQ): quitar el servicio de compatibilidad con clientes de Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cee48-103">Microsoft Message Queuing (MSMQ) - Removal of Windows 2000 Client Support Service</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="cee48-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="cee48-104">Affected Platforms</span></span>

<span data-ttu-id="cee48-105">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cee48-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="cee48-106">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="cee48-106">Feature Impact</span></span>

 <span data-ttu-id="cee48-107">**Gravedad** alta</span><span class="sxs-lookup"><span data-stu-id="cee48-107">**Severity** - High</span></span>  
<span data-ttu-id="cee48-108">**Frecuencia** : baja</span><span class="sxs-lookup"><span data-stu-id="cee48-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="cee48-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cee48-109">Description</span></span>

<span data-ttu-id="cee48-110">El servicio de soporte técnico de cliente de Windows 2000 es un componente opcional del servidor de Message Queue Server que puede instalar en un equipo de controlador de dominio de Windows 2003 o Windows 2008.</span><span class="sxs-lookup"><span data-stu-id="cee48-110">The Windows 2000 Client Support Service is an optional component of the Message Queuing Server that you can install on a Windows 2003 or Windows 2008 domain controller machine.</span></span> <span data-ttu-id="cee48-111">Este servicio permite a los clientes de Windows 2000 funcionar en un modo integrado en el dominio con cualquier servidor de Message Queue Server instalado en máquinas con Windows 2003/2008.</span><span class="sxs-lookup"><span data-stu-id="cee48-111">This service allows Windows 2000 clients to operate in a domain-integrated mode with any Message Queuing server installed on Windows 2003/2008 machines.</span></span> <span data-ttu-id="cee48-112">Los clientes MSMQ que operan en Windows XP en adelante no necesitan este servicio.</span><span class="sxs-lookup"><span data-stu-id="cee48-112">MSMQ Clients operating on Windows XP upwards do not need this service.</span></span>

### <a name="manifestation-of-impact"></a><span data-ttu-id="cee48-113">Manifiesto de impacto</span><span class="sxs-lookup"><span data-stu-id="cee48-113">Manifestation of Impact</span></span>

<span data-ttu-id="cee48-114">Este cambio afecta a Windows 2000 al interoperar en un dominio de Windows 7 donde todos los controladores de dominio son Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="cee48-114">This change impacts Windows 2000 when interoperating in a Windows 7 domain where all domain controllers are Windows Server 2008 R2.</span></span> <span data-ttu-id="cee48-115">Si un cliente se actualiza al dominio de Windows 7, las aplicaciones MSMQ existentes en cualquier equipo con Windows 2000 del dominio no podrán funcionar en un modo integrado en el dominio a menos que estos clientes actualicen a una versión posterior de Windows.</span><span class="sxs-lookup"><span data-stu-id="cee48-115">If a customer upgrades to the Windows 7 domain, the existing MSMQ applications on any Windows 2000 machines in the domain will not be able to operate in a domain-integrated mode unless these clients upgrade to a higher Windows version.</span></span>

### <a name="mitigation"></a><span data-ttu-id="cee48-116">Mitigación</span><span class="sxs-lookup"><span data-stu-id="cee48-116">Mitigation</span></span>

<span data-ttu-id="cee48-117">Los usuarios que tienen equipos cliente de Windows 2000 en un dominio de Windows 7 pueden configurar un controlador de dominio de Windows 2003/2008 en el dominio e instalar el servicio de soporte técnico de cliente de Windows 2000 MSMQ en este controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="cee48-117">Users who have Windows 2000 Client machines on a Windows 7 domain can configure a Windows 2003/2008 domain controller in the domain and install the MSMQ Windows 2000 Client Support Service on this domain controller.</span></span>

### <a name="leveraging-feature-capabilities"></a><span data-ttu-id="cee48-118">Aprovechar las capacidades de características</span><span class="sxs-lookup"><span data-stu-id="cee48-118">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="cee48-119">Los usuarios que tienen equipos cliente de Windows 2000 con MSMQ deben actualizarse a una versión posterior de Windows para poder aprovechar la implementación basada en Active Directory del servidor de MSMQ.</span><span class="sxs-lookup"><span data-stu-id="cee48-119">Users who have Windows 2000 Client machines running MSMQ should upgrade to a higher Windows version in order to take advantage of the Active Directory-based implementation of the MSMQ Server.</span></span>

### <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="cee48-120">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="cee48-120">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="cee48-121">Los usuarios que tienen equipos cliente de Windows 2000 con MSMQ en un dominio de Windows 7 con uno o más controladores de dominio de nivel inferior deben comprobar que sus aplicaciones son funcionales en este dominio mixto.</span><span class="sxs-lookup"><span data-stu-id="cee48-121">Users who have Windows 2000 Client machines running MSMQ on a Windows 7 domain with one or more down-level domain controllers should verify that their applications are functional on this mixed domain.</span></span>

 

 



