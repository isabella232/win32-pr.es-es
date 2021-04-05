---
title: Usuario interactivo
description: El usuario interactivo es el usuario que ha iniciado sesión actualmente en el equipo en el que se ejecuta el servidor COM.
ms.assetid: 6d43842c-0ad1-4563-b50c-5024bda480f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7fc8aeb5fd9674c09b40f6c46e4e173f5965a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359435"
---
# <a name="interactive-user"></a><span data-ttu-id="347aa-103">Usuario interactivo</span><span class="sxs-lookup"><span data-stu-id="347aa-103">Interactive User</span></span>

<span data-ttu-id="347aa-104">El *usuario interactivo* es el usuario que ha iniciado sesión actualmente en el equipo en el que se ejecuta el servidor com.</span><span class="sxs-lookup"><span data-stu-id="347aa-104">The *interactive user* is the user that is currently logged on to the computer where the COM server is running.</span></span> <span data-ttu-id="347aa-105">Si la identidad se establece para ser el usuario interactivo, todos los clientes usan la misma instancia del servidor si el servidor registra su generador de clases como multiuso.</span><span class="sxs-lookup"><span data-stu-id="347aa-105">If the identity is set to be the interactive user, all clients use the same instance of the server if the server registers its class factory as multi-use.</span></span> <span data-ttu-id="347aa-106">Si ningún usuario ha iniciado sesión, el servidor no se ejecutará.</span><span class="sxs-lookup"><span data-stu-id="347aa-106">If no user is logged on, the server will not run.</span></span> <span data-ttu-id="347aa-107">Si el servidor tiene una interfaz gráfica de usuario (GUI) que el cliente debe ver, debe usar el usuario interactivo para la identidad del servidor.</span><span class="sxs-lookup"><span data-stu-id="347aa-107">If the server has a graphical user interface (GUI) that the client needs to see, you should use interactive user for the server's identity.</span></span> <span data-ttu-id="347aa-108">Sin embargo, la elección de esta identidad conlleva algunos riesgos de seguridad porque el servidor se ejecuta bajo la identidad del usuario que ha iniciado sesión sin el conocimiento o consentimiento del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="347aa-108">However, choosing this identity carries some security risks because the server runs under the identity of the logged on user without the logged on user's knowledge or consent.</span></span> <span data-ttu-id="347aa-109">Además, una aplicación de servicio no puede mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="347aa-109">In addition, a service application cannot display a user interface.</span></span> <span data-ttu-id="347aa-110">Para obtener más información, vea [servicios interactivos](/windows/desktop/Services/interactive-services).</span><span class="sxs-lookup"><span data-stu-id="347aa-110">For more information, see [Interactive Services](/windows/desktop/Services/interactive-services).</span></span>

<span data-ttu-id="347aa-111">Si un servidor COM está configurado para ejecutarse como usuario interactivo, en un entorno de Terminal Services, el servidor se iniciará en la sesión interactiva que coincide con la identidad de usuario del cliente.</span><span class="sxs-lookup"><span data-stu-id="347aa-111">If a COM server is configured to run as the interactive user, in a terminal services environment, the server will be launched in the interactive session that matches the client's user identity.</span></span> <span data-ttu-id="347aa-112">Sin embargo, la aplicación cliente puede utilizar el moniker de sesión para hacer referencia a un objeto proporcionado por el servidor en una sesión que no coincide con la identidad del cliente.</span><span class="sxs-lookup"><span data-stu-id="347aa-112">However, the client application can use the session moniker to reference an object provided by the server in a session that does not match the client identity.</span></span> <span data-ttu-id="347aa-113">Cuando se usa, la aplicación cliente puede especificar cualquier sesión, en cuyo caso el servidor se ejecutará como el usuario propietario de la sesión, no el usuario que inicia.</span><span class="sxs-lookup"><span data-stu-id="347aa-113">When this is used, the client application can specify any session, in which case the server will run as the user who owns the session, not the launching user.</span></span> <span data-ttu-id="347aa-114">Los permisos de acceso predeterminados en este escenario no permitirán que el usuario iniciador llame a métodos en el servidor.</span><span class="sxs-lookup"><span data-stu-id="347aa-114">The default access permissions in this scenario would not allow the launching user to call methods on the server.</span></span> <span data-ttu-id="347aa-115">Sin embargo, quedan los siguientes riesgos de seguridad:</span><span class="sxs-lookup"><span data-stu-id="347aa-115">However, the following security risks remain:</span></span>

-   <span data-ttu-id="347aa-116">Si el servidor COM expone interfaces que no están controladas por COM, como puertos TCP, canalizaciones con nombre, puertos LPC, secciones de memoria compartida, etc., el usuario que inicia la podría usar para influir en el servidor.</span><span class="sxs-lookup"><span data-stu-id="347aa-116">If the COM server exposes interfaces that are not controlled by COM, such as TCP ports, named pipes, LPC ports, shared memory sections, and so on, these could be used by the launching user to influence the server.</span></span> <span data-ttu-id="347aa-117">Los objetos COM configurados para ejecutarse como usuario interactivo deben reducir esta superficie de ataque lo máximo posible.</span><span class="sxs-lookup"><span data-stu-id="347aa-117">COM objects configured to run as the interactive user should reduce this attack surface as much as possible.</span></span>
-   <span data-ttu-id="347aa-118">Los objetos COM son gratuitos para establecer sus propios permisos de acceso.</span><span class="sxs-lookup"><span data-stu-id="347aa-118">COM objects are free to set their own access permissions.</span></span> <span data-ttu-id="347aa-119">Si el objeto establece permisos de acceso, ya sea en su registro de AppID o llamando a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), para permitir el acceso de usuario inicial, el usuario podría iniciar el servidor para ejecutarse como otro usuario y, a continuación, tener acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="347aa-119">If the object sets access permissions, either in its AppID registration or by calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), to allow the launching user access, the user would be able to launch the server to run as another user, then access the object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="347aa-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="347aa-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="347aa-121">Identidad de la aplicación</span><span class="sxs-lookup"><span data-stu-id="347aa-121">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="347aa-122">Iniciando usuario</span><span class="sxs-lookup"><span data-stu-id="347aa-122">Launching User</span></span>](launching-user.md)
</dt> <dt>

[<span data-ttu-id="347aa-123">Identidad de servicio</span><span class="sxs-lookup"><span data-stu-id="347aa-123">Service Identity</span></span>](service-identity.md)
</dt> <dt>

[<span data-ttu-id="347aa-124">Usuario especificado</span><span class="sxs-lookup"><span data-stu-id="347aa-124">Specified User</span></span>](specified-user.md)
</dt> </dl>

 

 