---
title: Proxy de aplicación web
description: Proxy de aplicación web
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220ac5f52a8f5130cdb6fb21649ff302e6693b1b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104149686"
---
# <a name="web-application-proxy"></a><span data-ttu-id="5fbe0-103">Proxy de aplicación web</span><span class="sxs-lookup"><span data-stu-id="5fbe0-103">Web Application Proxy</span></span>

## <a name="platform"></a><span data-ttu-id="5fbe0-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="5fbe0-104">Platform</span></span>

<span data-ttu-id="5fbe0-105">**Servidores:** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5fbe0-105">**Servers -** Windows Server 2012 R2</span></span>  






## <a name="description"></a><span data-ttu-id="5fbe0-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fbe0-106">Description</span></span>

<span data-ttu-id="5fbe0-107">En Windows Server 2012 R2, se ha agregado un nuevo servicio denominado proxy de aplicación web en el rol de acceso remoto que permite a los administradores publicar aplicaciones para el acceso externo.</span><span class="sxs-lookup"><span data-stu-id="5fbe0-107">In Windows Server 2012 R2, we added a new service called the Web Application Proxy under the Remote Access role that allows administrators to publish applications for external access.</span></span> <span data-ttu-id="5fbe0-108">Este servicio actúa como proxy inverso y como proxy de Servicios de federación de Active Directory (AD FS) (AD FS).</span><span class="sxs-lookup"><span data-stu-id="5fbe0-108">This service acts as a reverse proxy and as an Active Directory Federation Services (AD FS) proxy.</span></span> <span data-ttu-id="5fbe0-109">De hecho, este servicio reemplaza el servicio de proxy de AD FS como se conocía en Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5fbe0-109">In fact, this service replaces the AD FS proxy service as it was known in Windows Server 2012.</span></span>

<span data-ttu-id="5fbe0-110">Con el proxy de aplicación Web, una organización puede hacer que los recursos web locales estén disponibles para el acceso externo al mismo tiempo que administra el riesgo de este acceso mediante el control de las directivas de autenticación y autorización en el AD FS.</span><span class="sxs-lookup"><span data-stu-id="5fbe0-110">With the Web Application Proxy, an organization can make on-premises web resources available for external access while at the same time managing the risk of this access by controlling authentication and authorization policies on the AD FS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="5fbe0-111">Manifestación</span><span class="sxs-lookup"><span data-stu-id="5fbe0-111">Manifestation</span></span>

<span data-ttu-id="5fbe0-112">El servicio de proxy de AD FS ya no se encuentra en el rol de Servicios de federación de Active Directory (AD FS) (AD FS), pero se ha reemplazado por el proxy de aplicación web en el rol de acceso remoto.</span><span class="sxs-lookup"><span data-stu-id="5fbe0-112">The AD FS proxy service is no longer under the Active Directory Federation Services role (AD FS), but has been replaced by the Web Application Proxy under the Remote Access role.</span></span> <span data-ttu-id="5fbe0-113">Esto representa una expansión del servicio de proxy de AD FS mediante la inclusión de la funcionalidad de proxy inverso para la publicación de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5fbe0-113">This represents an expansion of the AD FS proxy service by including reverse proxy functionality for application publishing.</span></span>

## <a name="solution"></a><span data-ttu-id="5fbe0-114">Solución</span><span class="sxs-lookup"><span data-stu-id="5fbe0-114">Solution</span></span>

<span data-ttu-id="5fbe0-115">Para tener acceso al proxy de aplicación Web, los administradores pueden ir a Administrador del servidor y agregar un nuevo rol o servicio de rol.</span><span class="sxs-lookup"><span data-stu-id="5fbe0-115">To access the Web Application Proxy, administrators can go to Server Manager and add a new role/role service.</span></span> <span data-ttu-id="5fbe0-116">El administrador encontrará el proxy de aplicación web en el rol de acceso remoto.</span><span class="sxs-lookup"><span data-stu-id="5fbe0-116">The administrator will find the Web Application Proxy under the Remote Access role.</span></span>

## <a name="resources"></a><span data-ttu-id="5fbe0-117">Recursos</span><span class="sxs-lookup"><span data-stu-id="5fbe0-117">Resources</span></span>

-   <span data-ttu-id="5fbe0-118">[Guía de soluciones](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="5fbe0-118">[Solution guide](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))</span></span>

 

 