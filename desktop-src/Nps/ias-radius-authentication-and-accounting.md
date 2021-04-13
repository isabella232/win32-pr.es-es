---
title: Autenticación, autorización y cuentas RADIUS
description: NPS es totalmente compatible con el protocolo Servicio de autenticación remota telefónica de usuario (RADIUS). El protocolo RADIUS es el estándar de facto para la autenticación de usuarios remotos y se documenta en RFC 2865 y RFC 2866.
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce45bbc6e4802ed5137849a5b22520c8a4badbb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421090"
---
# <a name="radius-authentication-authorization-and-accounting"></a><span data-ttu-id="fac3b-104">Autenticación, autorización y cuentas RADIUS</span><span class="sxs-lookup"><span data-stu-id="fac3b-104">RADIUS Authentication, Authorization, and Accounting</span></span>

> [!Note]  
> <span data-ttu-id="fac3b-105">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fac3b-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="fac3b-106">El contenido de este tema se aplica a IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="fac3b-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="fac3b-107">En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.</span><span class="sxs-lookup"><span data-stu-id="fac3b-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="fac3b-108">NPS es totalmente compatible con el protocolo Servicio de autenticación remota telefónica de usuario (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="fac3b-108">NPS fully supports the Remote Authentication Dial-In User Service (RADIUS) protocol.</span></span> <span data-ttu-id="fac3b-109">El protocolo RADIUS es el estándar de facto para la autenticación de usuarios remotos y se documenta en [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) y [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="fac3b-109">The RADIUS protocol is the de facto standard for remote user authentication and it is documented in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) and [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

## <a name="radius-authentication-and-authorization"></a><span data-ttu-id="fac3b-110">Autenticación y autorización RADIUS</span><span class="sxs-lookup"><span data-stu-id="fac3b-110">RADIUS Authentication and Authorization</span></span>

<span data-ttu-id="fac3b-111">En el diagrama siguiente se muestra un cliente de autenticación ("usuario") que se conecta a un servidor de acceso a la red (NAS) a través de una conexión de acceso telefónico mediante el Protocolo punto a punto (PPP).</span><span class="sxs-lookup"><span data-stu-id="fac3b-111">The following diagram shows an authenticating client ("User") connecting to a Network Access Server (NAS) over a dial-up connection, using the Point-to-Point Protocol (PPP).</span></span> <span data-ttu-id="fac3b-112">Para autenticar al usuario, el NAS se pone en contacto con un servidor remoto que ejecuta NPS.</span><span class="sxs-lookup"><span data-stu-id="fac3b-112">In order to authenticate the User, the NAS contacts a remote server running NPS.</span></span> <span data-ttu-id="fac3b-113">El NAS y el servidor NPS se comunican mediante el protocolo RADIUS.</span><span class="sxs-lookup"><span data-stu-id="fac3b-113">The NAS and the NPS server communicate using the RADIUS protocol.</span></span>

![autenticación de usuario remoto](images/ias01.png)

<span data-ttu-id="fac3b-115">Un NAS funciona como cliente de un servidor o servidores que admiten el protocolo RADIUS.</span><span class="sxs-lookup"><span data-stu-id="fac3b-115">A NAS operates as a client of a server or servers that support the RADIUS protocol.</span></span> <span data-ttu-id="fac3b-116">Los servidores que admiten el protocolo RADIUS se conocen normalmente como servidores RADIUS.</span><span class="sxs-lookup"><span data-stu-id="fac3b-116">Servers that support the RADIUS protocol are generally referred to as the RADIUS servers.</span></span> <span data-ttu-id="fac3b-117">El cliente RADIUS, es decir, el servidor NAS, pasa información sobre el usuario a los servidores RADIUS designados y, a continuación, actúa en la respuesta que los servidores devuelven.</span><span class="sxs-lookup"><span data-stu-id="fac3b-117">The RADIUS client, that is, the NAS, passes information about the User to designated RADIUS servers, and then acts on the response that the servers return.</span></span> <span data-ttu-id="fac3b-118">La solicitud enviada por el NAS al servidor RADIUS para autenticar al usuario suele denominarse "solicitud de autenticación".</span><span class="sxs-lookup"><span data-stu-id="fac3b-118">The request sent by the NAS to the RADIUS server in order to authenticate the User is generally called an "authentication request."</span></span>

<span data-ttu-id="fac3b-119">Si un servidor RADIUS autentica el usuario correctamente, el servidor RADIUS devuelve la información de configuración al NAS para que pueda proporcionar el servicio de red al usuario.</span><span class="sxs-lookup"><span data-stu-id="fac3b-119">If a RADIUS server authenticates the User successfully, the RADIUS server returns configuration information to the NAS so that it can provide network service to the user.</span></span> <span data-ttu-id="fac3b-120">Esta información de configuración se compone de "autorizaciones" y contiene, entre otras, el tipo de servicio NAS que puede proporcionar al usuario (por ejemplo, PPP o Telnet).</span><span class="sxs-lookup"><span data-stu-id="fac3b-120">This configuration information is composed of "authorizations" and contains, among others, the type of service NAS may provide to the User (for example, PPP, or telnet).</span></span>

<span data-ttu-id="fac3b-121">Mientras el servidor RADIUS está procesando la solicitud de autenticación, puede realizar funciones de autorización como comprobar el número de teléfono del usuario y comprobar si el usuario ya tiene una sesión en curso.</span><span class="sxs-lookup"><span data-stu-id="fac3b-121">While the RADIUS server is processing the authentication request, it can perform authorization functions such as verifying the user's telephone number and checking whether the user already has a session in progress.</span></span> <span data-ttu-id="fac3b-122">El servidor RADIUS puede determinar si el usuario ya tiene una sesión en curso poniéndose en contacto con un servidor de estado.</span><span class="sxs-lookup"><span data-stu-id="fac3b-122">The RADIUS server can determine whether the user already has a session in progress by contacting a state server.</span></span>

<span data-ttu-id="fac3b-123">Para obtener más información sobre la autenticación y autorización RADIUS, consulte [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).</span><span class="sxs-lookup"><span data-stu-id="fac3b-123">For more information on RADIUS authentication and authorization, see [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).</span></span>

## <a name="radius-accounting"></a><span data-ttu-id="fac3b-124">Cuentas RADIUS</span><span class="sxs-lookup"><span data-stu-id="fac3b-124">RADIUS Accounting</span></span>

<span data-ttu-id="fac3b-125">El servidor RADIUS también recopila una gran variedad de información enviada por el NAS que se puede usar para la contabilidad y para informar sobre la actividad de la red.</span><span class="sxs-lookup"><span data-stu-id="fac3b-125">The RADIUS server also collects a variety of information sent by the NAS that can be used for accounting and for reporting on network activity.</span></span> <span data-ttu-id="fac3b-126">El cliente RADIUS envía información a los servidores RADIUS designados cuando el usuario inicia sesión y cierra la sesión.</span><span class="sxs-lookup"><span data-stu-id="fac3b-126">The RADIUS client sends information to designated RADIUS servers when the User logs on and logs off.</span></span> <span data-ttu-id="fac3b-127">El cliente RADIUS puede enviar información de uso adicional periódicamente mientras la sesión está en curso.</span><span class="sxs-lookup"><span data-stu-id="fac3b-127">The RADIUS client may send additional usage information on a periodic basis while the session is in progress.</span></span> <span data-ttu-id="fac3b-128">Las solicitudes enviadas por el cliente al servidor para registrar la información de inicio y cierre de sesión y uso se suelen denominar "solicitudes de contabilidad".</span><span class="sxs-lookup"><span data-stu-id="fac3b-128">The requests sent by the client to the server to record logon/logoff and usage information are generally called "accounting requests."</span></span>

<span data-ttu-id="fac3b-129">Para obtener más información sobre las cuentas RADIUS, consulte [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="fac3b-129">For more information on RADIUS accounting, see [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

## <a name="radius-proxy"></a><span data-ttu-id="fac3b-130">Proxy RADIUS</span><span class="sxs-lookup"><span data-stu-id="fac3b-130">RADIUS Proxy</span></span>

<span data-ttu-id="fac3b-131">Un servidor RADIUS puede actuar como cliente proxy para otros servidores RADIUS.</span><span class="sxs-lookup"><span data-stu-id="fac3b-131">A RADIUS server can act as a proxy client to other RADIUS servers.</span></span> <span data-ttu-id="fac3b-132">En estos casos, el servidor RADIUS contactado por el NAS pasa la solicitud de autenticación o de cuentas a otro servidor RADIUS que realmente realiza la autenticación o la tarea de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="fac3b-132">In these cases, the RADIUS server contacted by the NAS passes the authentication or accounting request to another RADIUS server that actually performs the authentication or the accounting task.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fac3b-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fac3b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fac3b-134">Servicio de autenticación de Internet y servidor de directivas de redes</span><span class="sxs-lookup"><span data-stu-id="fac3b-134">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="fac3b-135">Paquetes de cuentas RADIUS</span><span class="sxs-lookup"><span data-stu-id="fac3b-135">RADIUS Accounting Packets</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="fac3b-136">Trabajar con un servidor de estado</span><span class="sxs-lookup"><span data-stu-id="fac3b-136">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 