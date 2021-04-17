---
description: Tanto los proveedores de C++ como las aplicaciones cliente deben realizar muchas de las mismas operaciones para mantener la seguridad de WMI.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Protección de clientes y proveedores de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac93ee88f710bf17a2b6199b3a9b2e89279b4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706086"
---
# <a name="securing-c-clients-and-providers"></a><span data-ttu-id="7277a-103">Protección de clientes y proveedores de C++</span><span class="sxs-lookup"><span data-stu-id="7277a-103">Securing C++ Clients and Providers</span></span>

<span data-ttu-id="7277a-104">Tanto los proveedores de C++ como las aplicaciones cliente deben realizar muchas de las mismas operaciones para mantener la seguridad de WMI.</span><span class="sxs-lookup"><span data-stu-id="7277a-104">Both C++ providers and client applications must perform many of the same operations to maintain WMI security.</span></span>

<span data-ttu-id="7277a-105">Las aplicaciones cliente deben establecer los niveles de [suplantación](setting-the-default-process-security-level-using-c-.md) y [autenticación](setting-authentication-in-wmi.md) de DCOM correctamente al conectarse a WMI.</span><span class="sxs-lookup"><span data-stu-id="7277a-105">Client applications must set DCOM [impersonation](setting-the-default-process-security-level-using-c-.md) and [authentication](setting-authentication-in-wmi.md) levels correctly when connecting to WMI.</span></span> <span data-ttu-id="7277a-106">Las devoluciones de llamada de [llamadas asincrónicas](setting-security-on-an-asynchronous-call.md) tienen riesgos de seguridad, por lo que las aplicaciones cliente deben [realizar comprobaciones de acceso](performing-access-checks.md) para asegurarse de que la devolución de llamada proviene de un origen de confianza.</span><span class="sxs-lookup"><span data-stu-id="7277a-106">Callbacks from [asynchronous calls](setting-security-on-an-asynchronous-call.md) have security risks, so client applications must [perform access checks](performing-access-checks.md) to ensure the callback is from a trusted source.</span></span> <span data-ttu-id="7277a-107">Los clientes necesitan proteger a los [consumidores de eventos temporales y permanentes](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="7277a-107">Clients need to secure both [temporary and permanent event consumers](securing-wmi-events.md).</span></span>

<span data-ttu-id="7277a-108">Un proveedor puede [realizar comprobaciones de acceso](performing-access-checks.md) para asegurarse de que los clientes adecuados solo tienen acceso a los recursos que crea.</span><span class="sxs-lookup"><span data-stu-id="7277a-108">A provider may [perform access checks](performing-access-checks.md) to ensure that the resources it creates are only accessed by appropriate clients.</span></span>

<span data-ttu-id="7277a-109">Tanto los proveedores como los clientes también pueden establecer la seguridad en una conexión de [proxy específica](setting-the-security-on-iwbemservices-and-other-proxies.md) .</span><span class="sxs-lookup"><span data-stu-id="7277a-109">Both providers and clients also can set the security on a [specific proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) connection.</span></span> <span data-ttu-id="7277a-110">Ambos también pueden habilitar los [privilegios](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="7277a-110">Both can also enable [privileges](executing-privileged-operations.md).</span></span> <span data-ttu-id="7277a-111">Un proveedor de eventos debe asegurarse de que el consumidor del cliente tenga privilegios para [recibir un evento solicitado](providing-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="7277a-111">An event provider must ensure that the client consumer has privileges to [receive a requested event](providing-events-securely.md).</span></span>

<span data-ttu-id="7277a-112">Es posible que un cliente o un proveedor necesiten realizar una conexión remota que requiera un servicio de autenticación diferente, NTLM en lugar de Kerberos, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="7277a-112">Either a client or provider may need to make a remote connection that requires a different authentication service, NTLM instead of Kerberos for example.</span></span>

 

 



