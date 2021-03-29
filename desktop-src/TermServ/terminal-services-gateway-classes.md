---
title: Clases de puerta de enlace de Escritorio remoto
description: El proveedor WMI de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) proporciona las siguientes clases.
ms.assetid: 482ba056-0de7-4c91-816c-dd3c926662ef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d17adca523833f3418661cd3f9851d7c814cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778828"
---
# <a name="remote-desktop-gateway-classes"></a><span data-ttu-id="9baf8-103">Clases de puerta de enlace de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9baf8-103">Remote Desktop Gateway classes</span></span>

<span data-ttu-id="9baf8-104">El proveedor WMI de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) proporciona las siguientes clases.</span><span class="sxs-lookup"><span data-stu-id="9baf8-104">The Remote Desktop Gateway (RD Gateway) WMI provider provides the following classes.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9baf8-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9baf8-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="9baf8-106">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="9baf8-106">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dd>

<span data-ttu-id="9baf8-107">Representa una conexión desde un equipo cliente a un servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="9baf8-107">Represents a connection from a client computer to a RD Gateway server.</span></span>

</dd> <dt>

[<span data-ttu-id="9baf8-108">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="9baf8-108">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dd>

<span data-ttu-id="9baf8-109">Describe una Escritorio remoto Directiva de autorización de conexión (CAP de RD).</span><span class="sxs-lookup"><span data-stu-id="9baf8-109">Describes a Remote Desktop connection authorization policy (RD CAP).</span></span> <span data-ttu-id="9baf8-110">Las Cap de RD se usan para determinar si un usuario puede conectarse al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="9baf8-110">RD CAPs are used to determine whether a user is allowed to connect to the RD Gateway server.</span></span>

</dd> <dt>

[<span data-ttu-id="9baf8-111">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="9baf8-111">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dd>

<span data-ttu-id="9baf8-112">Describe un conjunto de servidores de equilibrio de carga de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="9baf8-112">Describes a set of RD Gateway load-balancing servers.</span></span> <span data-ttu-id="9baf8-113">Se usan para equilibrar la carga de las conexiones de puerta de enlace de escritorio remoto entre varios servidores.</span><span class="sxs-lookup"><span data-stu-id="9baf8-113">These are used to load balance RD Gateway connections across multiple servers.</span></span>

</dd> <dt>

[<span data-ttu-id="9baf8-114">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="9baf8-114">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dd>

<span data-ttu-id="9baf8-115">Describe un servidor Servicio de autenticación remota telefónica de usuario (RADIUS), que tiene un conjunto de Servicios de Escritorio remoto directivas de autorización de conexión (Cap de RD).</span><span class="sxs-lookup"><span data-stu-id="9baf8-115">Describes a Remote Authentication Dial-In User Service (RADIUS) server, which has a set of Remote Desktop Services connection authorization policies (RD CAPs).</span></span>

</dd> <dt>

[<span data-ttu-id="9baf8-116">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="9baf8-116">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dd>

<span data-ttu-id="9baf8-117">Describe una Escritorio remoto Directiva de autorización de recursos (RAP de RD).</span><span class="sxs-lookup"><span data-stu-id="9baf8-117">Describes a Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="9baf8-118">Una RAP de RD se usa para decidir si un usuario está autorizado para conectarse a un recurso especificado a través de la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="9baf8-118">An RD RAP is used to decide whether a user is authorized to connect to a specified resource through RD Gateway.</span></span>

</dd> <dt>

[<span data-ttu-id="9baf8-119">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="9baf8-119">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dd>

<span data-ttu-id="9baf8-120">Describe un grupo de recursos, que asigna un conjunto de recursos (nombres de equipo) a una sola entidad.</span><span class="sxs-lookup"><span data-stu-id="9baf8-120">Describes a resource group, which maps a set of resources (computer names) to a single entity.</span></span>

</dd> <dt>

[<span data-ttu-id="9baf8-121">**Win32 \_ TSGatewayServer**</span><span class="sxs-lookup"><span data-stu-id="9baf8-121">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> <dd>

<span data-ttu-id="9baf8-122">Se usa para las operaciones específicas del servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="9baf8-122">Used for RD Gateway server-specific operations.</span></span>

</dd> <dt>

[<span data-ttu-id="9baf8-123">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="9baf8-123">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dd>

<span data-ttu-id="9baf8-124">Proporciona métodos y propiedades para ver y configurar las opciones del servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="9baf8-124">Provides methods and properties to view and configure RD Gateway server settings.</span></span>

</dd> </dl>

 

 




