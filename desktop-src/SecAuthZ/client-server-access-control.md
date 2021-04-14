---
description: Una aplicación de servidor proporciona servicios a los clientes.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Access Control cliente/servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b1d349abb2d55f00b9801c9bb493437fa858eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648235"
---
# <a name="clientserver-access-control"></a><span data-ttu-id="29f4e-103">Access Control cliente/servidor</span><span class="sxs-lookup"><span data-stu-id="29f4e-103">Client/Server Access Control</span></span>

<span data-ttu-id="29f4e-104">Una aplicación de servidor proporciona servicios a los clientes.</span><span class="sxs-lookup"><span data-stu-id="29f4e-104">A server application provides services to clients.</span></span> <span data-ttu-id="29f4e-105">Por ejemplo, un servidor podría realizar los siguientes servicios en nombre de un cliente:</span><span class="sxs-lookup"><span data-stu-id="29f4e-105">For example, a server could perform the following services on behalf of a client:</span></span>

-   <span data-ttu-id="29f4e-106">Guardar y recuperar información de una base de datos privada</span><span class="sxs-lookup"><span data-stu-id="29f4e-106">Save and retrieve information from a private database</span></span>
-   <span data-ttu-id="29f4e-107">Acceder a los recursos de red</span><span class="sxs-lookup"><span data-stu-id="29f4e-107">Access network resources</span></span>
-   <span data-ttu-id="29f4e-108">Iniciar [*procesos*](/windows/desktop/SecGloss/p-gly) en el contexto de [*seguridad*](/windows/desktop/SecGloss/s-gly) del cliente en el equipo del servidor</span><span class="sxs-lookup"><span data-stu-id="29f4e-108">Start [*processes*](/windows/desktop/SecGloss/p-gly) in the client's [*security context*](/windows/desktop/SecGloss/s-gly) on the server's computer</span></span>

<span data-ttu-id="29f4e-109">Un servidor protegido controla el acceso a sus servicios.</span><span class="sxs-lookup"><span data-stu-id="29f4e-109">A protected server controls access to its services.</span></span> <span data-ttu-id="29f4e-110">Windows proporciona compatibilidad de seguridad que permite que un servidor haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="29f4e-110">Windows provides security support that enables a server to do the following:</span></span>

-   <span data-ttu-id="29f4e-111">Suplantar el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly)de un cliente, que hace que el sistema realice la mayoría de las comprobaciones de [*privilegios*](/windows/desktop/SecGloss/p-gly) y de acceso en el [*token de acceso*](/windows/desktop/SecGloss/a-gly) del cliente en lugar de en el servidor</span><span class="sxs-lookup"><span data-stu-id="29f4e-111">Impersonate a client's [*security context*](/windows/desktop/SecGloss/s-gly), which causes the system to perform most access and [*privilege*](/windows/desktop/SecGloss/p-gly) checks against the client's [*access token*](/windows/desktop/SecGloss/a-gly) rather than the server's</span></span>
-   <span data-ttu-id="29f4e-112">Iniciar una sesión de cliente en el equipo del servidor</span><span class="sxs-lookup"><span data-stu-id="29f4e-112">Log a client on to the server's computer</span></span>
-   <span data-ttu-id="29f4e-113">Conectarse a recursos de red mediante el contexto de seguridad del cliente</span><span class="sxs-lookup"><span data-stu-id="29f4e-113">Connect to network resources using the client's security context</span></span>
-   <span data-ttu-id="29f4e-114">Crear [*descriptores de seguridad*](/windows/desktop/SecGloss/s-gly) para proteger objetos privados</span><span class="sxs-lookup"><span data-stu-id="29f4e-114">Create [*security descriptors*](/windows/desktop/SecGloss/s-gly) to protect private objects</span></span>
-   <span data-ttu-id="29f4e-115">Determinar si un descriptor de seguridad permite el acceso a un cliente</span><span class="sxs-lookup"><span data-stu-id="29f4e-115">Determine whether a security descriptor allows access to a client</span></span>
-   <span data-ttu-id="29f4e-116">Determinar si un conjunto de privilegios está habilitado en el token de un cliente</span><span class="sxs-lookup"><span data-stu-id="29f4e-116">Determine whether a set of privileges are enabled in a client's token</span></span>
-   <span data-ttu-id="29f4e-117">Generar mensajes de auditoría en el registro de eventos de seguridad para registrar intentos de un cliente para obtener acceso a objetos o usar privilegios</span><span class="sxs-lookup"><span data-stu-id="29f4e-117">Generate audit messages in the security event log to record attempts by a client to access objects or use privileges</span></span>

 

 
