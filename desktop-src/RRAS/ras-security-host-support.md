---
title: Compatibilidad con el host de seguridad RAS
description: Windows NT 4,0 proporciona una manera de que un archivo DLL de seguridad RAS de terceros mejore las características de seguridad integradas de RAS. Windows 95 no proporciona esta compatibilidad.
ms.assetid: 1cbacd7f-c9b9-4fb4-b505-a4b1d1b6f632
keywords:
- Compatibilidad con hosts, RAS
- Compatibilidad del host de seguridad, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99145f80d347ccd4ee9fbf4a4cdc23ca5af373e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777275"
---
# <a name="ras-security-host-support"></a><span data-ttu-id="ac393-106">Compatibilidad con el host de seguridad RAS</span><span class="sxs-lookup"><span data-stu-id="ac393-106">RAS Security Host Support</span></span>

<span data-ttu-id="ac393-107">Windows NT 4,0 proporciona una manera de que un archivo DLL de seguridad RAS de terceros mejore las características de seguridad integradas de RAS.</span><span class="sxs-lookup"><span data-stu-id="ac393-107">Windows NT 4.0 provides a way for a third-party RAS security DLL to enhance the built-in RAS security features.</span></span> <span data-ttu-id="ac393-108">Windows 95 no proporciona esta compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="ac393-108">Windows 95 does not provide this support.</span></span>

<span data-ttu-id="ac393-109">Un servidor RAS de Windows NT/Windows 2000 proporciona mecanismos de seguridad para validar el acceso a la red de los usuarios remotos.</span><span class="sxs-lookup"><span data-stu-id="ac393-109">A Windows NT/Windows 2000 RAS server provides security mechanisms for validating the network access of remote users.</span></span> <span data-ttu-id="ac393-110">Cuando un servidor RAS recibe una llamada, valida las credenciales del usuario con la base de datos de la cuenta local o de dominio.</span><span class="sxs-lookup"><span data-stu-id="ac393-110">When a RAS server receives a call, it validates the user's credentials against the local or domain account database.</span></span> <span data-ttu-id="ac393-111">RAS también admite la seguridad de devolución de llamada, en la que el servidor RAS se cuelga y, a continuación, vuelve a llamar al usuario remoto para establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="ac393-111">RAS also supports call-back security, in which the RAS server hangs up and then calls back to the remote user to establish the connection.</span></span> <span data-ttu-id="ac393-112">En el caso de las redes en las que este nivel de seguridad no es suficiente, puede instalar un archivo DLL de seguridad RAS de terceros.</span><span class="sxs-lookup"><span data-stu-id="ac393-112">For networks in which this level of security is not enough, you can install a third-party RAS security DLL.</span></span> <span data-ttu-id="ac393-113">A continuación, el archivo DLL de seguridad puede autenticar a un usuario remoto leyendo información de seguridad de una base de datos que no sea la base de datos de cuentas de usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="ac393-113">The security DLL can then authenticate a remote user by reading security information from a database other than the standard user account database.</span></span>

<span data-ttu-id="ac393-114">Cuando el servidor RAS recibe una llamada, invoca el archivo DLL de seguridad para autenticar al usuario remoto.</span><span class="sxs-lookup"><span data-stu-id="ac393-114">When the RAS server receives a call, it invokes the security DLL to authenticate the remote user.</span></span> <span data-ttu-id="ac393-115">La compatibilidad con el host de seguridad RAS proporciona un mecanismo para que la DLL de seguridad se comunique con el usuario remoto a través de una ventana de terminal en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="ac393-115">The RAS security host support provides a mechanism for the security DLL to communicate with the remote user through a terminal window on the remote computer.</span></span> <span data-ttu-id="ac393-116">En un escenario típico, el archivo DLL de seguridad solicita el nombre de inicio de sesión del usuario remoto.</span><span class="sxs-lookup"><span data-stu-id="ac393-116">In a typical scenario, the security DLL asks for the logon name of the remote user.</span></span> <span data-ttu-id="ac393-117">A continuación, el archivo DLL utiliza su base de datos de seguridad privada para formular un desafío para enviar al terminal remoto.</span><span class="sxs-lookup"><span data-stu-id="ac393-117">The DLL then uses its private security database to formulate a challenge to send to the remote terminal.</span></span> <span data-ttu-id="ac393-118">Por ejemplo, el desafío podría ser un código que el usuario debe proporcionar como entrada para un lector Cardkey.</span><span class="sxs-lookup"><span data-stu-id="ac393-118">For example, the challenge could be a code that the user must provide as input to a cardkey reader.</span></span> <span data-ttu-id="ac393-119">A continuación, el lector Cardkey muestra una respuesta que el usuario remoto escribe en la ventana de terminal.</span><span class="sxs-lookup"><span data-stu-id="ac393-119">The cardkey reader then displays a response that the remote user types in the terminal window.</span></span> <span data-ttu-id="ac393-120">A continuación, la DLL de seguridad valida la respuesta con la información del usuario en la base de datos de seguridad privada.</span><span class="sxs-lookup"><span data-stu-id="ac393-120">The security DLL then validates the response against the user's information in the private security database.</span></span>

<span data-ttu-id="ac393-121">Si el archivo DLL de seguridad autentica al usuario remoto, el servidor RAS realiza su propia autenticación.</span><span class="sxs-lookup"><span data-stu-id="ac393-121">If the security DLL authenticates the remote user, the RAS server performs its own authentication.</span></span> <span data-ttu-id="ac393-122">Esto garantiza que la seguridad de RAS siempre autentique a un usuario remoto, incluso si hay instalado un archivo DLL de seguridad que conceda acceso a todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ac393-122">This ensures that RAS security always authenticates a remote user, even if a security DLL is installed that grants access to all users.</span></span>

> [!Note]  
> <span data-ttu-id="ac393-123">Windows NT/Windows 2000 actualmente proporciona compatibilidad de host de seguridad de RAS solo para conexiones de módem asincrónicas; no se admiten otros tipos de conexiones, como Ethernet (que no es una conexión de módem), VPN (que tampoco es una conexión de módem) o ISDN (que es sincrónico).</span><span class="sxs-lookup"><span data-stu-id="ac393-123">Windows NT/Windows 2000 currently provides RAS security host support only for asynchronous modem connections; other types of connections such as Ethernet (which is not a modem connection), VPN (which is also not a modem connection), or ISDN (which is synchronous), are not supported.</span></span>

 

 

 




