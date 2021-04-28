---
description: 'Microsoft Message Queuing (MSMQ): eliminación del servicio de soporte técnico de cliente de Windows 2000'
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: 'Microsoft Message Queuing (MSMQ): eliminación del servicio de soporte técnico de cliente de Windows 2000'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be68d40271153567bdaf6b04d73218aaf3d3977
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088153"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a><span data-ttu-id="6139d-103">Microsoft Message Queuing (MSMQ): eliminación del servicio de soporte técnico de cliente de Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6139d-103">Microsoft Message Queuing (MSMQ) - Removal of Windows 2000 Client Support Service</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="6139d-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="6139d-104">Affected Platforms</span></span>

<span data-ttu-id="6139d-105">**Servidores:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6139d-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="6139d-106">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="6139d-106">Feature Impact</span></span>

 <span data-ttu-id="6139d-107">**Gravedad:** alta</span><span class="sxs-lookup"><span data-stu-id="6139d-107">**Severity** - High</span></span>  
<span data-ttu-id="6139d-108">**Frecuencia:** baja</span><span class="sxs-lookup"><span data-stu-id="6139d-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="6139d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6139d-109">Description</span></span>

<span data-ttu-id="6139d-110">El servicio de soporte técnico de cliente de Windows 2000 es un componente opcional de Message Queuing Server que puede instalar en un equipo de controlador de dominio de Windows 2003 o Windows 2008.</span><span class="sxs-lookup"><span data-stu-id="6139d-110">The Windows 2000 Client Support Service is an optional component of the Message Queuing Server that you can install on a Windows 2003 or Windows 2008 domain controller machine.</span></span> <span data-ttu-id="6139d-111">Este servicio permite que los clientes de Windows 2000 funcionen en un modo integrado de dominio con cualquier servidor de Message Queuing instalado en equipos con Windows 2003/2008.</span><span class="sxs-lookup"><span data-stu-id="6139d-111">This service allows Windows 2000 clients to operate in a domain-integrated mode with any Message Queuing server installed on Windows 2003/2008 machines.</span></span> <span data-ttu-id="6139d-112">Los clientes de MSMQ que funcionan en Windows XP hacia arriba no necesitan este servicio.</span><span class="sxs-lookup"><span data-stu-id="6139d-112">MSMQ Clients operating on Windows XP upwards do not need this service.</span></span>

### <a name="manifestation-of-impact"></a><span data-ttu-id="6139d-113">Demostración de impacto</span><span class="sxs-lookup"><span data-stu-id="6139d-113">Manifestation of Impact</span></span>

<span data-ttu-id="6139d-114">Este cambio afecta a Windows 2000 al interoperar en un dominio de Windows 7 donde todos los controladores de dominio son Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="6139d-114">This change impacts Windows 2000 when interoperating in a Windows 7 domain where all domain controllers are Windows Server 2008 R2.</span></span> <span data-ttu-id="6139d-115">Si un cliente actualiza al dominio de Windows 7, las aplicaciones MSMQ existentes en cualquier máquina Windows 2000 del dominio no podrán funcionar en un modo integrado de dominio a menos que estos clientes actualicen a una versión superior de Windows.</span><span class="sxs-lookup"><span data-stu-id="6139d-115">If a customer upgrades to the Windows 7 domain, the existing MSMQ applications on any Windows 2000 machines in the domain will not be able to operate in a domain-integrated mode unless these clients upgrade to a higher Windows version.</span></span>

### <a name="mitigation"></a><span data-ttu-id="6139d-116">Mitigación</span><span class="sxs-lookup"><span data-stu-id="6139d-116">Mitigation</span></span>

<span data-ttu-id="6139d-117">Los usuarios que tienen equipos cliente de Windows 2000 en un dominio de Windows 7 pueden configurar un controlador de dominio de Windows 2003/2008 en el dominio e instalar el servicio de soporte técnico de cliente de MSMQ Windows 2000 en este controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="6139d-117">Users who have Windows 2000 Client machines on a Windows 7 domain can configure a Windows 2003/2008 domain controller in the domain and install the MSMQ Windows 2000 Client Support Service on this domain controller.</span></span>

### <a name="leveraging-feature-capabilities"></a><span data-ttu-id="6139d-118">Aprovechamiento de las funcionalidades de características</span><span class="sxs-lookup"><span data-stu-id="6139d-118">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="6139d-119">Los usuarios que tienen equipos cliente de Windows 2000 que ejecutan MSMQ deben actualizar a una versión superior de Windows para aprovechar las ventajas de la implementación basada en Active Directory del servidor MSMQ.</span><span class="sxs-lookup"><span data-stu-id="6139d-119">Users who have Windows 2000 Client machines running MSMQ should upgrade to a higher Windows version in order to take advantage of the Active Directory-based implementation of the MSMQ Server.</span></span>

### <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="6139d-120">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="6139d-120">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="6139d-121">Los usuarios que tienen equipos cliente de Windows 2000 que ejecutan MSMQ en un dominio de Windows 7 con uno o varios controladores de dominio de nivel inferior deben comprobar que sus aplicaciones son funcionales en este dominio mixto.</span><span class="sxs-lookup"><span data-stu-id="6139d-121">Users who have Windows 2000 Client machines running MSMQ on a Windows 7 domain with one or more down-level domain controllers should verify that their applications are functional on this mixed domain.</span></span>

 

 



