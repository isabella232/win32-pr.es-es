---
description: La \_ opción de socket de nivel de protección IPv6 \_ permite a los desarrolladores colocar restricciones de acceso en sockets IPv6.
ms.assetid: bfb934b3-1e86-431f-a21c-880048d32d35
title: IPV6_PROTECTION_LEVEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2a8dd70bb1fb5b21f74f8939f11da0d9e2a3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696375"
---
# <a name="ipv6_protection_level"></a><span data-ttu-id="4c838-103">\_Nivel de protección IPv6 \_</span><span class="sxs-lookup"><span data-stu-id="4c838-103">IPV6\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="4c838-104">La \_ opción de socket de nivel de protección IPv6 \_ permite a los desarrolladores colocar restricciones de acceso en sockets IPv6.</span><span class="sxs-lookup"><span data-stu-id="4c838-104">The IPV6\_PROTECTION\_LEVEL socket option enables developers to place access restrictions on IPv6 sockets.</span></span> <span data-ttu-id="4c838-105">Estas restricciones permiten que una aplicación que se ejecuta en una LAN privada se fortalezca de forma sencilla frente a ataques externos.</span><span class="sxs-lookup"><span data-stu-id="4c838-105">Such restrictions enable an application running on a private LAN to simply and robustly harden itself against external attacks.</span></span> <span data-ttu-id="4c838-106">La \_ \_ opción de socket de nivel de protección IPv6 amplía o reduce el ámbito de un socket de escucha, lo que permite el acceso no restringido de usuarios públicos y privados cuando sea adecuado, o restringiendo el acceso únicamente al mismo sitio, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="4c838-106">The IPV6\_PROTECTION\_LEVEL socket option widens or narrows the scope of a listening socket, enabling unrestricted access from public and private users when appropriate, or restricting access only to the same site, as required.</span></span>

<span data-ttu-id="4c838-107">El \_ nivel de protección IPv6 \_ tiene actualmente tres niveles de protección definidos.</span><span class="sxs-lookup"><span data-stu-id="4c838-107">IPV6\_PROTECTION\_LEVEL currently has three defined protection levels.</span></span>



| <span data-ttu-id="4c838-108">Nivel de protección</span><span class="sxs-lookup"><span data-stu-id="4c838-108">Protection level</span></span>                                                                                                                                 | <span data-ttu-id="4c838-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c838-109">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c838-110"><span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>nivel de protección no \_ \_ restringido</span><span class="sxs-lookup"><span data-stu-id="4c838-110"><span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>PROTECTION\_LEVEL\_UNRESTRICTED</span></span><br/>       | <span data-ttu-id="4c838-111">Lo usan las aplicaciones diseñadas para funcionar a través de Internet, incluidas las aplicaciones que aprovechan las capacidades transversales NAT de IPv6 integradas en Windows (por ejemplo, Teredo).</span><span class="sxs-lookup"><span data-stu-id="4c838-111">Used by applications designed to operate across the Internet, including applications taking advantage of IPv6 NAT traversal capabilities built into Windows (Teredo, for example).</span></span> <span data-ttu-id="4c838-112">Estas aplicaciones pueden eludir los firewalls de IPv4, lo que hace necesario protegerlas frente a los ataques por Internet dirigidos al puerto abierto.</span><span class="sxs-lookup"><span data-stu-id="4c838-112">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span><br/> |
| <span data-ttu-id="4c838-113"><span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>nivel de protección \_ \_ EDGERESTRICTED</span><span class="sxs-lookup"><span data-stu-id="4c838-113"><span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>PROTECTION\_LEVEL\_EDGERESTRICTED</span></span><br/> | <span data-ttu-id="4c838-114">Lo usan las aplicaciones diseñadas para funcionar a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="4c838-114">Used by applications designed to operate across the Internet.</span></span> <span data-ttu-id="4c838-115">Esta configuración no permite el cruce seguro de NAT mediante la implementación de Teredo de Windows.</span><span class="sxs-lookup"><span data-stu-id="4c838-115">This setting does not allow NAT traversal using the Windows Teredo implementation.</span></span> <span data-ttu-id="4c838-116">Estas aplicaciones pueden eludir los firewalls de IPv4, lo que hace necesario protegerlas frente a los ataques por Internet dirigidos al puerto abierto.</span><span class="sxs-lookup"><span data-stu-id="4c838-116">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span><br/>                                   |
| <span data-ttu-id="4c838-117"><span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>nivel de protección \_ \_ restringido</span><span class="sxs-lookup"><span data-stu-id="4c838-117"><span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>PROTECTION\_LEVEL\_RESTRICTED</span></span><br/>             | <span data-ttu-id="4c838-118">Lo usan las aplicaciones de intranet que no implementan escenarios de Internet.</span><span class="sxs-lookup"><span data-stu-id="4c838-118">Used by intranet applications that do not implement Internet scenarios.</span></span> <span data-ttu-id="4c838-119">Estas aplicaciones no se suelen probar ni proteger frente a los ataques por Internet.</span><span class="sxs-lookup"><span data-stu-id="4c838-119">These applications are generally not tested or hardened against Internet-style attacks.</span></span><br/> <span data-ttu-id="4c838-120">Este valor limitará el tráfico recibido a las direcciones locales de vínculo.</span><span class="sxs-lookup"><span data-stu-id="4c838-120">This setting will limit the received traffic to link-local only.</span></span><br/>                                                                             |



 

<span data-ttu-id="4c838-121">En el ejemplo de código siguiente se proporcionan los valores definidos para cada uno de ellos:</span><span class="sxs-lookup"><span data-stu-id="4c838-121">The following code example provides the defined values for each:</span></span>

``` syntax
#define PROTECTION_LEVEL_UNRESTRICTED   10  /* for peer-to-peer apps */
#define PROTECTION_LEVEL_EDGERESTRICTED 20  /* Same as unrestricted, except for Teredo  */
#define PROTECTION_LEVEL_RESTRICTED     30  /* for Intranet apps     */
```

<span data-ttu-id="4c838-122">Estos valores son mutuamente excluyentes y no se pueden combinar en una [**sola llamada**](/windows/desktop/api/winsock/nf-winsock-setsockopt) a la función de un solo valor.</span><span class="sxs-lookup"><span data-stu-id="4c838-122">These values are mutually exclusive, and cannot be combined in a single [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function call.</span></span> <span data-ttu-id="4c838-123">Otros valores para esta opción de socket están reservados.</span><span class="sxs-lookup"><span data-stu-id="4c838-123">Other values for this socket option are reserved.</span></span> <span data-ttu-id="4c838-124">Estos niveles de protección solo se aplican a las conexiones entrantes.</span><span class="sxs-lookup"><span data-stu-id="4c838-124">These protection levels apply only to incoming connections.</span></span> <span data-ttu-id="4c838-125">El establecimiento de esta opción de Socket no tiene ningún efecto en las conexiones o los paquetes salientes.</span><span class="sxs-lookup"><span data-stu-id="4c838-125">Setting this socket option has no effect on outbound packets or connections.</span></span>

<span data-ttu-id="4c838-126">En Windows 7 y Windows Server 2008 R2, el valor predeterminado para el \_ nivel de protección IPv6 \_ es no especificado y el **nivel de protección \_ \_ predeterminado** está definido en-1, un valor no válido para el \_ nivel de protección IPv6 \_ .</span><span class="sxs-lookup"><span data-stu-id="4c838-126">On Windows 7 and Windows Server 2008 R2, the default value for IPV6\_PROTECTION\_LEVEL is unspecified and **PROTECTION\_LEVEL\_DEFAULT** is defined to -1, an illegal value for IPV6\_PROTECTION\_LEVEL.</span></span>

<span data-ttu-id="4c838-127">En Windows Vista y Windows Server 2008, el valor predeterminado para el \_ nivel de protección IPv6 \_ es **nivel de protección no \_ \_ restringido** y el **nivel de protección \_ \_ predeterminado** está definido en-1, un valor no válido para el \_ nivel de protección IPv6 \_ .</span><span class="sxs-lookup"><span data-stu-id="4c838-127">On Windows Vista and Windows Server 2008, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED** and **PROTECTION\_LEVEL\_DEFAULT** is defined to -1, an illegal value for IPV6\_PROTECTION\_LEVEL.</span></span>

<span data-ttu-id="4c838-128">En Windows Server 2003 y Windows XP, el valor predeterminado del nivel de protección IPV6 es el nivel de \_ \_ **protección \_ \_ EDGERESTRICTED** y el nivel de **protección \_ \_ predeterminado** se define como **nivel de protección \_ \_ EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="4c838-128">On Windows Server 2003 and Windows XP, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_EDGERESTRICTED** and **PROTECTION\_LEVEL\_DEFAULT** is defined to be **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>

> [!Note]  
> <span data-ttu-id="4c838-129">La \_ opción de socket de nivel de protección IPv6 \_ debe establecerse antes de enlazar el socket.</span><span class="sxs-lookup"><span data-stu-id="4c838-129">The IPV6\_PROTECTION\_LEVEL socket option should be set before the socket is bound.</span></span> <span data-ttu-id="4c838-130">De lo contrario, los paquetes recibidos entre [**las llamadas de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) y el tipo de llamada se ajustarán al **nivel de protección \_ \_ EDGERESTRICTED** y se pueden entregar a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4c838-130">Otherwise, packets received between [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) calls will conform to **PROTECTION\_LEVEL\_EDGERESTRICTED**, and may be delivered to the application.</span></span>

 

<span data-ttu-id="4c838-131">En la tabla siguiente se describe el efecto de aplicar cada nivel de protección a un socket de escucha.</span><span class="sxs-lookup"><span data-stu-id="4c838-131">The following table describes the effect of applying each protection level to a listening socket.</span></span>

<span data-ttu-id="4c838-132">Nivel de protección</span><span class="sxs-lookup"><span data-stu-id="4c838-132">Protection level</span></span>

<span data-ttu-id="4c838-133">Tráfico entrante permitido</span><span class="sxs-lookup"><span data-stu-id="4c838-133">Incoming traffic permitted</span></span>

<span data-ttu-id="4c838-134">Mismo sitio</span><span class="sxs-lookup"><span data-stu-id="4c838-134">Same site</span></span>

<span data-ttu-id="4c838-135">Externo</span><span class="sxs-lookup"><span data-stu-id="4c838-135">External</span></span>

<span data-ttu-id="4c838-136">NAT transversal (Teredo)</span><span class="sxs-lookup"><span data-stu-id="4c838-136">NAT traversal (Teredo)</span></span>

<span data-ttu-id="4c838-137">nivel de protección \_ \_ restringido</span><span class="sxs-lookup"><span data-stu-id="4c838-137">PROTECTION\_LEVEL\_RESTRICTED</span></span>

<span data-ttu-id="4c838-138">Sí</span><span class="sxs-lookup"><span data-stu-id="4c838-138">Yes</span></span>

<span data-ttu-id="4c838-139">No</span><span class="sxs-lookup"><span data-stu-id="4c838-139">No</span></span>

<span data-ttu-id="4c838-140">No</span><span class="sxs-lookup"><span data-stu-id="4c838-140">No</span></span>

<span data-ttu-id="4c838-141">nivel de protección \_ \_ EDGERESTRICTED</span><span class="sxs-lookup"><span data-stu-id="4c838-141">PROTECTION\_LEVEL\_EDGERESTRICTED</span></span>

<span data-ttu-id="4c838-142">Sí</span><span class="sxs-lookup"><span data-stu-id="4c838-142">Yes</span></span>

<span data-ttu-id="4c838-143">Sí</span><span class="sxs-lookup"><span data-stu-id="4c838-143">Yes</span></span>

<span data-ttu-id="4c838-144">No</span><span class="sxs-lookup"><span data-stu-id="4c838-144">No</span></span>

<span data-ttu-id="4c838-145">nivel de protección no \_ \_ restringido</span><span class="sxs-lookup"><span data-stu-id="4c838-145">PROTECTION\_LEVEL\_UNRESTRICTED</span></span>

<span data-ttu-id="4c838-146">Sí</span><span class="sxs-lookup"><span data-stu-id="4c838-146">Yes</span></span>

<span data-ttu-id="4c838-147">Sí</span><span class="sxs-lookup"><span data-stu-id="4c838-147">Yes</span></span>

<span data-ttu-id="4c838-148">Sí</span><span class="sxs-lookup"><span data-stu-id="4c838-148">Yes</span></span>



 

<span data-ttu-id="4c838-149">En la tabla anterior, la **misma** columna de sitio es una combinación de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4c838-149">In the table above, the **Same site** column is a combination of the following:</span></span>

-   <span data-ttu-id="4c838-150">Vincular direcciones locales</span><span class="sxs-lookup"><span data-stu-id="4c838-150">Link local addresses</span></span>
-   <span data-ttu-id="4c838-151">Direcciones locales del sitio</span><span class="sxs-lookup"><span data-stu-id="4c838-151">Site Local addresses</span></span>
-   <span data-ttu-id="4c838-152">Direcciones globales conocidas para pertenecer al mismo sitio (que coincide con la tabla de prefijo del sitio)</span><span class="sxs-lookup"><span data-stu-id="4c838-152">Global addresses known to belong to the same site (matching the site prefix table)</span></span>

<span data-ttu-id="4c838-153">En Windows 7 y Windows Server 2008 R2, el valor predeterminado del \_ nivel de protección IPv6 \_ no está especificado.</span><span class="sxs-lookup"><span data-stu-id="4c838-153">On Windows 7 and Windows Server 2008 R2, the default value for IPV6\_PROTECTION\_LEVEL is unspecified.</span></span> <span data-ttu-id="4c838-154">Si no hay ningún software de Firewall compatible con el recorrido perimetral instalado en el equipo local (Firewall de Windows está deshabilitado o hay otro Firewall instalado que omite el tráfico Teredo), recibirá el tráfico Teredo solo si establece la \_ opción de socket de nivel de protección IPv6 en el nivel de protección no \_ **\_ \_ restringido**.</span><span class="sxs-lookup"><span data-stu-id="4c838-154">If there is no edge-traversal aware firewall software installed on the local computer (Windows firewall is disabled or some other firewall is installed that ignores Teredo traffic), you will receive Teredo traffic only if you set the IPV6\_PROTECTION\_LEVEL socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="4c838-155">Sin embargo, el Firewall de Windows o cualquier directiva de Firewall compatible con el recorrido perimetral puede omitir esta opción en función de la configuración de directivas del firewall.</span><span class="sxs-lookup"><span data-stu-id="4c838-155">However, Windows firewall or any edge-traversal aware firewall policy may ignore this option based on policy settings for the firewall.</span></span> <span data-ttu-id="4c838-156">Al establecer esta opción de socket en el **nivel de protección no \_ \_ restringido**, la aplicación está comunicando su intención explícita de recibir tráfico recorrido por el perímetro por el firewall del host instalado en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="4c838-156">By setting this socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**, the application is communicating its explicit intent to receive edge traversed traffic by the host firewall installed on the local machine.</span></span> <span data-ttu-id="4c838-157">Por tanto, si hay un firewall de host compatible con el recorrido perimetral instalado, tendrá la decisión final de aceptar un paquete.</span><span class="sxs-lookup"><span data-stu-id="4c838-157">So if there is an edge-traversal aware host firewall installed, it will have the final decision on accepting a packet.</span></span> <span data-ttu-id="4c838-158">De forma predeterminada, sin ningún conjunto de opciones de socket:</span><span class="sxs-lookup"><span data-stu-id="4c838-158">By default, without any socket option set:</span></span>

-   <span data-ttu-id="4c838-159">o si firewall de Windows está habilitado (u otro Firewall de host compatible con el recorrido perimetral está instalado) en el equipo local, se observará lo que se aplique.</span><span class="sxs-lookup"><span data-stu-id="4c838-159">o If Windows firewall is enabled (or another edge-traversal aware host firewall is installed) on the local computer, whatever it enforces will be observed.</span></span> <span data-ttu-id="4c838-160">El firewall del host con reconocimiento perimetral típico bloqueará el tráfico Teredo de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4c838-160">Typical edge-traversal aware host firewall will block Teredo traffic by default.</span></span> <span data-ttu-id="4c838-161">Por lo tanto, las aplicaciones observarán el valor predeterminado como si fuera el **nivel de protección \_ \_ EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="4c838-161">Therefore applications will observe the default as if it was **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>
-   <span data-ttu-id="4c838-162">o si firewall de Windows no está habilitado y ningún otro Firewall de host compatible con el recorrido perimetral está instalado en el sistema local, el valor predeterminado será **nivel de protección \_ \_ EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="4c838-162">o If Windows firewall is not enabled and no other edge-traversal aware host firewall is installed on the local system, the default will be **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>

<span data-ttu-id="4c838-163">En Windows Vista y Windows Server 2008, el valor predeterminado para el \_ nivel de protección IPv6 \_ es **nivel de protección no \_ \_ restringido**.</span><span class="sxs-lookup"><span data-stu-id="4c838-163">On Windows Vista and Windows Server 2008, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="4c838-164">Pero el valor efectivo depende de si firewall de Windows está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4c838-164">But the effective value depends on whether Windows firewall is enabled.</span></span> <span data-ttu-id="4c838-165">El Firewall de Windows es compatible con el recorrido perimetral (compatible con Teredo), independientemente del valor que se haya establecido para el \_ nivel de protección IPv6 \_ y se omite si el nivel de protección IPv6 \_ \_ es nivel de **protección no \_ \_ restringido**.</span><span class="sxs-lookup"><span data-stu-id="4c838-165">The Windows firewall is edge-traversal aware (Teredo aware), no matter what value is set for the IPV6\_PROTECTION\_LEVEL and ignores if IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="4c838-166">Por lo tanto, el valor efectivo depende de la Directiva de Firewall.</span><span class="sxs-lookup"><span data-stu-id="4c838-166">So the effective value depends on the firewall policy.</span></span> <span data-ttu-id="4c838-167">Cuando Firewall de Windows está deshabilitado y ningún otro Firewall compatible con el recorrido perimetral está instalado en el equipo local, el valor predeterminado para el \_ nivel de protección IPv6 \_ es nivel de **protección no \_ \_ restringido**.</span><span class="sxs-lookup"><span data-stu-id="4c838-167">When Windows firewall is disabled and no other edge-traversal aware firewall is installed on the local computer, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span>

<span data-ttu-id="4c838-168">En Windows Server 2003 y Windows XP, el valor predeterminado para el \_ nivel de protección IPv6 \_ es el nivel de **protección \_ \_ EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="4c838-168">On Windows Server 2003 and Windows XP, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span> <span data-ttu-id="4c838-169">A menos que haya establecido la \_ opción de socket de nivel de protección IPv6 \_ en el nivel de **protección no \_ \_ restringido**, no recibirá ningún tráfico Teredo.</span><span class="sxs-lookup"><span data-stu-id="4c838-169">Unless you have set the IPV6\_PROTECTION\_LEVEL socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**, you would not receive any Teredo traffic.</span></span>

<span data-ttu-id="4c838-170">Según el nivel de protección de IPV6 \_ \_ , es posible que una aplicación que requiera tráfico no solicitado de Internet no pueda recibir tráfico no solicitado.</span><span class="sxs-lookup"><span data-stu-id="4c838-170">Depending on the IPV6\_PROTECTION\_LEVEL, an application that requires unsolicited traffic from the Internet may not be capable of receiving unsolicited traffic.</span></span> <span data-ttu-id="4c838-171">Sin embargo, estos requisitos no son necesarios para recibir tráfico solicitado a través de la interfaz Teredo de Windows.</span><span class="sxs-lookup"><span data-stu-id="4c838-171">However, these requirements are not necessary for receiving solicited traffic over the Windows Teredo interface.</span></span> <span data-ttu-id="4c838-172">Para obtener más información sobre la interacción con Teredo, consulte [recibir tráfico solicitado a través de Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).</span><span class="sxs-lookup"><span data-stu-id="4c838-172">For more details on the interaction with Teredo, see [Receiving Solicited Traffic Over Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).</span></span>

<span data-ttu-id="4c838-173">Cuando se rechazan los paquetes entrantes o las conexiones debido al nivel de protección establecido, el rechazo se controla como si ninguna aplicación estuviera escuchando en ese socket.</span><span class="sxs-lookup"><span data-stu-id="4c838-173">When incoming packets or connections are refused due to the set protection level, rejection is handled as if no application was listening on that socket.</span></span>

> [!Note]
>
> <span data-ttu-id="4c838-174">La \_ opción de socket de nivel de protección IPv6 \_ no impone necesariamente restricciones de acceso en sockets IPv6 o restringe el recorrido NAT mediante algún método distinto de Teredo de Windows o incluso usando otra implementación de Teredo por otro proveedor.</span><span class="sxs-lookup"><span data-stu-id="4c838-174">The IPV6\_PROTECTION\_LEVEL socket option does not necessarily place access restrictions on IPv6 sockets or restrict NAT traversal using some method other than Windows Teredo or even using another implementation of Teredo by another vendor.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4c838-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c838-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c838-176">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="4c838-176">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="4c838-177">Recibir tráfico solicitado a través de Teredo</span><span class="sxs-lookup"><span data-stu-id="4c838-177">Receiving Solicited Traffic Over Teredo</span></span>](../teredo/receiving-solicited-traffic-over-teredo.md)
</dt> <dt>

[<span data-ttu-id="4c838-178">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="4c838-178">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 
