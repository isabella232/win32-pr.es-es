---
title: Registro con servidor de directivas de redes
description: Registro con servidor de directivas de redes
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5117ce15731ea656913b47525387a48a39aa414c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359208"
---
# <a name="logging-with-network-policy-server"></a><span data-ttu-id="09c00-103">Registro con servidor de directivas de redes</span><span class="sxs-lookup"><span data-stu-id="09c00-103">Logging With Network Policy Server</span></span>

> [!Note]  
> <span data-ttu-id="09c00-104">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="09c00-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="09c00-105">El contenido de este tema se aplica a IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="09c00-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="09c00-106">En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.</span><span class="sxs-lookup"><span data-stu-id="09c00-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="09c00-107">En la tabla siguiente se describen solo los aspectos más importantes de los paquetes de cuentas RADIUS.</span><span class="sxs-lookup"><span data-stu-id="09c00-107">The following table describes only the most important aspects of the RADIUS accounting packets.</span></span> <span data-ttu-id="09c00-108">El documento de solicitud de comentarios de cuentas de RADIUS ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) proporciona información detallada sobre estos paquetes.</span><span class="sxs-lookup"><span data-stu-id="09c00-108">The RADIUS Accounting Request for Comments document ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) provides detailed information on these packets.</span></span>

<span data-ttu-id="09c00-109">Los paquetes de cuentas RADIUS se pueden dividir en las siguientes categorías.</span><span class="sxs-lookup"><span data-stu-id="09c00-109">RADIUS accounting packets can be divided into the following categories.</span></span>



| <span data-ttu-id="09c00-110">Paquete de cuentas</span><span class="sxs-lookup"><span data-stu-id="09c00-110">Accounting packet</span></span>  | <span data-ttu-id="09c00-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="09c00-111">Description</span></span>                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09c00-112">Accounting-On</span><span class="sxs-lookup"><span data-stu-id="09c00-112">Accounting-On</span></span>      | <span data-ttu-id="09c00-113">Lo envía el servidor de acceso a la red (NAS) para indicar que se ha reiniciado.</span><span class="sxs-lookup"><span data-stu-id="09c00-113">Sent by the Network Access Server (NAS) to indicate that it has restarted.</span></span><br/> <span data-ttu-id="09c00-114">Contiene el identificador de NAS/IPAddress.</span><span class="sxs-lookup"><span data-stu-id="09c00-114">Contains nas-identifier/ipaddress.</span></span><br/>                                                                                        |
| <span data-ttu-id="09c00-115">Accounting-Off</span><span class="sxs-lookup"><span data-stu-id="09c00-115">Accounting-Off</span></span>     | <span data-ttu-id="09c00-116">Enviado por el NAS para indicar que se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="09c00-116">Sent by the NAS to indicate that it is being shutdown.</span></span><br/> <span data-ttu-id="09c00-117">Contiene el identificador de NAS/IPAddress.</span><span class="sxs-lookup"><span data-stu-id="09c00-117">Contains nas-identifier/ipaddress.</span></span><br/>                                                                                                            |
| <span data-ttu-id="09c00-118">Accounting-Start</span><span class="sxs-lookup"><span data-stu-id="09c00-118">Accounting-Start</span></span>   | <span data-ttu-id="09c00-119">Enviado por el NAS, después de que el usuario se haya autenticado y autorizado, para indicar el inicio de una sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="09c00-119">Sent by the NAS, after the user was authenticated and authorized, to indicate the start of a user session.</span></span> <br/> <span data-ttu-id="09c00-120">Contiene userid, NAS-Identifier/IPAddress, además de otra información recibida del NAS.</span><span class="sxs-lookup"><span data-stu-id="09c00-120">Contains userid, nas-identifier/ipaddress, plus other information received from the NAS.</span></span><br/> |
| <span data-ttu-id="09c00-121">Accounting-Stop</span><span class="sxs-lookup"><span data-stu-id="09c00-121">Accounting-Stop</span></span>    | <span data-ttu-id="09c00-122">Enviado por el NAS para indicar el final de una sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="09c00-122">Sent by the NAS to indicate the end of a user session.</span></span><br/> <span data-ttu-id="09c00-123">Contiene userid, NAS-Identifier/IPAddress, además de otra información recibida del NAS.</span><span class="sxs-lookup"><span data-stu-id="09c00-123">Contains userid, nas-identifier/ipaddress, plus other information received from the NAS.</span></span><br/>                                                      |
| <span data-ttu-id="09c00-124">Accounting-Interim</span><span class="sxs-lookup"><span data-stu-id="09c00-124">Accounting-Interim</span></span> | <span data-ttu-id="09c00-125">Se puede enviar periódicamente por el NAS para cada usuario que ha iniciado sesión en el NAS.</span><span class="sxs-lookup"><span data-stu-id="09c00-125">Could be sent periodically by the NAS for each user that is logged on at the NAS.</span></span> <br/> <span data-ttu-id="09c00-126">Esta característica se admite generalmente en las versiones más recientes de NAS.</span><span class="sxs-lookup"><span data-stu-id="09c00-126">This feature is generally supported in newer versions of NAS.</span></span><br/>                                                     |



 

<span data-ttu-id="09c00-127">Es importante tener en cuenta los siguientes problemas a la hora de recopilar información de cuentas disponible a través de RADIUS:</span><span class="sxs-lookup"><span data-stu-id="09c00-127">The following issues are important to consider when collecting accounting information made available through RADIUS:</span></span>

-   <span data-ttu-id="09c00-128">En raras ocasiones, es posible que los paquetes se pierdan durante la transmisión y que nunca lleguen al servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="09c00-128">In rare cases, packets could be lost during transmission and may never reach the RADIUS server.</span></span>
-   <span data-ttu-id="09c00-129">No se notifica al servidor RADIUS si el NAS se anula.</span><span class="sxs-lookup"><span data-stu-id="09c00-129">The RADIUS server is not notified if the NAS aborts.</span></span>
-   <span data-ttu-id="09c00-130">ISDN admite varias sesiones y cada sesión genera un par de paquetes de inicio y detención de cuentas.</span><span class="sxs-lookup"><span data-stu-id="09c00-130">ISDN supports multiple sessions and each session generates an Accounting-Start/-Stop pair of packets.</span></span> <span data-ttu-id="09c00-131">Hay un atributo de contabilidad denominado identificador de varias sesiones que identifica claramente estos paquetes de varias sesiones.</span><span class="sxs-lookup"><span data-stu-id="09c00-131">There is an accounting attribute called multi-session identifier that clearly identifies such multi-session packets.</span></span> <span data-ttu-id="09c00-132">Busque el identificador de varias sesiones además del identificador de sesión para calcular el número de sesiones.</span><span class="sxs-lookup"><span data-stu-id="09c00-132">Check for the multi-session identifier in addition to the session identifier to calculate the number of sessions.</span></span>

## <a name="requests-logged-by-nps"></a><span data-ttu-id="09c00-133">Solicitudes registradas por NPS</span><span class="sxs-lookup"><span data-stu-id="09c00-133">Requests Logged by NPS</span></span>

<span data-ttu-id="09c00-134">De forma predeterminada, NPS no registra ningún dato.</span><span class="sxs-lookup"><span data-stu-id="09c00-134">By default, NPS does not log any data.</span></span> <span data-ttu-id="09c00-135">NPS se puede configurar mediante la interfaz de usuario de NPS (NPS. msc) para registrar las siguientes solicitudes.</span><span class="sxs-lookup"><span data-stu-id="09c00-135">NPS can be configured, using the NPS user interface (nps.msc), to log the following requests.</span></span>



| <span data-ttu-id="09c00-136">Paquete registrado</span><span class="sxs-lookup"><span data-stu-id="09c00-136">Logged packet</span></span>          | <span data-ttu-id="09c00-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="09c00-137">Description</span></span>                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09c00-138">Solicitud de cuentas</span><span class="sxs-lookup"><span data-stu-id="09c00-138">Accounting Request</span></span>     | <span data-ttu-id="09c00-139">Cualquiera de los paquetes de cuentas descritos en la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="09c00-139">Any of the accounting packets described in the previous table.</span></span><br/>                                                                    |
| <span data-ttu-id="09c00-140">Solicitud de autenticación</span><span class="sxs-lookup"><span data-stu-id="09c00-140">Authentication Request</span></span> | <span data-ttu-id="09c00-141">Enviado por el NAS en nombre del usuario que se conecta.</span><span class="sxs-lookup"><span data-stu-id="09c00-141">Sent by the NAS on behalf of the connecting user.</span></span><br/> <span data-ttu-id="09c00-142">Las entradas del registro solo contienen atributos entrantes.</span><span class="sxs-lookup"><span data-stu-id="09c00-142">The log entries contain only incoming attributes.</span></span><br/>                    |
| <span data-ttu-id="09c00-143">Aceptación de autenticación</span><span class="sxs-lookup"><span data-stu-id="09c00-143">Authentication Accept</span></span>  | <span data-ttu-id="09c00-144">Lo envía NPS para indicar que se debe aceptar la conexión de usuario.</span><span class="sxs-lookup"><span data-stu-id="09c00-144">Sent by NPS to indicate that the user connection should be accepted.</span></span><br/> <span data-ttu-id="09c00-145">Las entradas del registro solo contienen atributos de salida.</span><span class="sxs-lookup"><span data-stu-id="09c00-145">The log entries contain only outgoing attributes.</span></span><br/> |
| <span data-ttu-id="09c00-146">Rechazo de autenticación</span><span class="sxs-lookup"><span data-stu-id="09c00-146">Authentication Reject</span></span>  | <span data-ttu-id="09c00-147">Lo envía NPS para indicar que se debe rechazar la conexión de usuario.</span><span class="sxs-lookup"><span data-stu-id="09c00-147">Sent by NPS to indicate that the user connection should be rejected.</span></span><br/> <span data-ttu-id="09c00-148">Las entradas del registro solo contienen atributos de salida.</span><span class="sxs-lookup"><span data-stu-id="09c00-148">The log entries contain only outgoing attributes.</span></span><br/> |



 

<span data-ttu-id="09c00-149">Los datos registrados por NPS pueden ir a un archivo de texto en el servidor NPS o a una base de datos SQL central.</span><span class="sxs-lookup"><span data-stu-id="09c00-149">Data logged by NPS can go to a text file on the NPS server or to a central SQL database.</span></span> <span data-ttu-id="09c00-150">Para obtener más información sobre el registro de SQL de NPS, consulte [programación de SQL](sql-programmability.md).</span><span class="sxs-lookup"><span data-stu-id="09c00-150">For more information on NPS SQL logging, see [SQL Programmability](sql-programmability.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="09c00-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09c00-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09c00-152">Servicio de autenticación de Internet y servidor de directivas de redes</span><span class="sxs-lookup"><span data-stu-id="09c00-152">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="09c00-153">Autenticación, autorización y cuentas RADIUS</span><span class="sxs-lookup"><span data-stu-id="09c00-153">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="09c00-154">Trabajar con un servidor de estado</span><span class="sxs-lookup"><span data-stu-id="09c00-154">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

