---
title: Trabajar con un servidor de estado
description: NPS realiza la autenticación mediante una base de datos que está configurada en el sitio del servidor NPS.
ms.assetid: 8313ba91-5ed1-44d0-80db-cfb82c641100
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d79ff46802d53109c7bb8b40fe3a2db2480949e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685736"
---
# <a name="working-with-a-state-server"></a><span data-ttu-id="e97a3-103">Trabajar con un servidor de estado</span><span class="sxs-lookup"><span data-stu-id="e97a3-103">Working With a State Server</span></span>

> [!Note]  
> <span data-ttu-id="e97a3-104">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e97a3-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="e97a3-105">El contenido de este tema se aplica a IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="e97a3-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="e97a3-106">En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.</span><span class="sxs-lookup"><span data-stu-id="e97a3-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="e97a3-107">NPS realiza la autenticación mediante una base de datos que está configurada en el sitio del servidor NPS.</span><span class="sxs-lookup"><span data-stu-id="e97a3-107">NPS performs authentication using a database that is configured at the NPS server site.</span></span> <span data-ttu-id="e97a3-108">Esta base de datos de autenticación podría ser la base de datos de usuario de un dominio de Windows o podría dibujarse en la información de usuario obtenida del Active Directory de Windows.</span><span class="sxs-lookup"><span data-stu-id="e97a3-108">This authentication database could be the user database for a Windows Domain or it could draw upon the user information obtained from the Windows Active Directory.</span></span> <span data-ttu-id="e97a3-109">En el diagrama siguiente se muestra una configuración típica que muestra cómo interactúa NPS con las bases de datos de autenticación, como una base de datos de usuario de dominio de Windows o Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e97a3-109">The following diagram illustrates a typical configuration that shows how NPS interacts with authentication databases such as a Windows Domain user database or Active Directory.</span></span> <span data-ttu-id="e97a3-110">En el diagrama también se muestra cómo NPS puede interactuar con un servidor de estado proporcionado por terceros.</span><span class="sxs-lookup"><span data-stu-id="e97a3-110">The diagram also shows how NPS could interact with a state server that is provided by a third party.</span></span> <span data-ttu-id="e97a3-111">El propósito principal de un servidor de estado es limitar el número de sesiones de inicio de sesión simultáneas que puede ejecutar un solo usuario.</span><span class="sxs-lookup"><span data-stu-id="e97a3-111">The primary purpose of a state server is to limit the number of simultaneous logon sessions a single user can run.</span></span>

![interacción de NPS con el servidor de estado y las bases de datos de autenticación](images/ias02.png)

<span data-ttu-id="e97a3-113">Hay dos puntos de interacción entre NPS y el servidor de estado.</span><span class="sxs-lookup"><span data-stu-id="e97a3-113">There are two points of interaction between NPS and the state server.</span></span> <span data-ttu-id="e97a3-114">Una interacción tiene lugar cuando NPS recibe una solicitud de autenticación del NAS.</span><span class="sxs-lookup"><span data-stu-id="e97a3-114">One interaction takes place when NPS receives an authentication request from the NAS.</span></span> <span data-ttu-id="e97a3-115">El servidor de estado proporciona información de su base de datos para determinar si se debe aceptar o denegar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e97a3-115">The state server provides information from its database to determine whether to accept or deny the request.</span></span> <span data-ttu-id="e97a3-116">La otra interacción tiene lugar cuando NPS recibe solicitudes de cuentas del NAS.</span><span class="sxs-lookup"><span data-stu-id="e97a3-116">The other interaction takes place when NPS receives accounting requests from the NAS.</span></span> <span data-ttu-id="e97a3-117">El servidor de estado usa la información de estas solicitudes de cuentas para actualizar su base de datos.</span><span class="sxs-lookup"><span data-stu-id="e97a3-117">The state server uses the information form these accounting requests to update its database.</span></span>

<span data-ttu-id="e97a3-118">Para obtener más información sobre los servidores de estado, vea:</span><span class="sxs-lookup"><span data-stu-id="e97a3-118">For more information on state servers see:</span></span>

-   [<span data-ttu-id="e97a3-119">Consideraciones sobre el diseño del servidor de estado</span><span class="sxs-lookup"><span data-stu-id="e97a3-119">State Server Design Considerations</span></span>](/windows/desktop/Nps/ias-state-server-design-considerations)

## <a name="related-topics"></a><span data-ttu-id="e97a3-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e97a3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e97a3-121">Servicio de autenticación de Internet y servidor de directivas de redes</span><span class="sxs-lookup"><span data-stu-id="e97a3-121">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="e97a3-122">Autenticación, autorización y cuentas RADIUS</span><span class="sxs-lookup"><span data-stu-id="e97a3-122">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="e97a3-123">Registro con servidor de directivas de redes</span><span class="sxs-lookup"><span data-stu-id="e97a3-123">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> </dl>

 

 