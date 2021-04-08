---
title: Configuración de IPsec
description: La plataforma de filtrado de Windows (WFP) es la plataforma subyacente para Firewall de Windows con seguridad avanzada.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af8e3d0a23713c0505082555fe260bc562dfa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995197"
---
# <a name="ipsec-configuration"></a><span data-ttu-id="39257-103">Configuración de IPsec</span><span class="sxs-lookup"><span data-stu-id="39257-103">IPsec Configuration</span></span>

<span data-ttu-id="39257-104">La plataforma de filtrado de Windows (WFP) es la plataforma subyacente para Firewall de Windows con seguridad avanzada.</span><span class="sxs-lookup"><span data-stu-id="39257-104">Windows Filtering Platform (WFP) is the underlying platform for Windows Firewall with Advanced Security.</span></span> <span data-ttu-id="39257-105">WFP se usa para configurar reglas de filtrado de red, que incluyen reglas que rigen la protección del tráfico de red con IPsec.</span><span class="sxs-lookup"><span data-stu-id="39257-105">WFP is used to configure network filtering rules, which include rules that govern securing network traffic with IPsec.</span></span> <span data-ttu-id="39257-106">Los desarrolladores de aplicaciones pueden configurar IPsec directamente mediante la API de WFP, con el fin de aprovechar un modelo de filtrado de tráfico de red más granular que el modelo expuesto a través del complemento Microsoft Management Console (MMC) para Firewall de Windows con seguridad avanzada.</span><span class="sxs-lookup"><span data-stu-id="39257-106">Application developers may configure IPsec directly using the WFP API, in order to take advantage of a more granular network traffic filtering model than the model exposed through the Microsoft Management Console (MMC) snap-in for Windows Firewall with Advanced Security.</span></span>

## <a name="what-is-ipsec"></a><span data-ttu-id="39257-107">Qué es IPsec</span><span class="sxs-lookup"><span data-stu-id="39257-107">What is IPsec</span></span>

<span data-ttu-id="39257-108">El protocolo de seguridad de Internet (IPsec) es un conjunto de protocolos de seguridad que se usan para transferir paquetes IP de forma confidencial a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="39257-108">Internet Protocol Security (IPsec) is a set of security protocols used to transfer IP packets confidentially across the Internet.</span></span> <span data-ttu-id="39257-109">IPsec es obligatorio para todas las implementaciones de IPv6 y opcional para IPv4.</span><span class="sxs-lookup"><span data-stu-id="39257-109">IPsec is mandatory for all IPv6 implementations and optional for IPv4.</span></span>

<span data-ttu-id="39257-110">El tráfico IP protegido tiene dos encabezados IPsec opcionales, que identifican los tipos de protección criptográfica aplicadas al paquete IP e incluyen información para descodificar el paquete protegido.</span><span class="sxs-lookup"><span data-stu-id="39257-110">Secured IP traffic has two optional IPsec headers, which identify the types of cryptographic protection applied to the IP packet and include information for decoding the protected packet.</span></span>

<span data-ttu-id="39257-111">El encabezado de carga de seguridad encapsuladora (ESP) se usa para la privacidad y la protección frente a modificaciones malintencionadas mediante la autenticación y el cifrado opcional.</span><span class="sxs-lookup"><span data-stu-id="39257-111">The Encapsulating Security Payload (ESP) header is used for privacy and protection against malicious modification by performing authentication and optional encryption.</span></span> <span data-ttu-id="39257-112">Se puede usar para el tráfico que atraviesa los enrutadores de traducción de direcciones de red (NAT).</span><span class="sxs-lookup"><span data-stu-id="39257-112">It can be used for traffic that traverses Network Address Translation (NAT) routers.</span></span>

<span data-ttu-id="39257-113">El encabezado de autenticación (AH) solo se usa para la protección contra modificaciones malintencionadas mediante la autenticación de.</span><span class="sxs-lookup"><span data-stu-id="39257-113">The Authentication Header (AH) is used only for protection against malicious modification by performing authentication.</span></span> <span data-ttu-id="39257-114">No se puede usar para el tráfico que atraviesa los enrutadores NAT.</span><span class="sxs-lookup"><span data-stu-id="39257-114">It cannot be used for traffic that traverses NAT routers.</span></span>

<span data-ttu-id="39257-115">Para obtener más información acerca de IPsec, vea también:</span><span class="sxs-lookup"><span data-stu-id="39257-115">For more information on IPsec, see also:</span></span>

<dl>

<span data-ttu-id="39257-116">[Referencia técnica de IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="39257-116">[IPsec Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))</span></span>  
</dl>

## <a name="what-is-ike"></a><span data-ttu-id="39257-117">Qué es IKE</span><span class="sxs-lookup"><span data-stu-id="39257-117">What is IKE</span></span>

<span data-ttu-id="39257-118">Intercambio de claves por red (IKE) es un protocolo de intercambio de claves que forma parte del conjunto de protocolos IPsec.</span><span class="sxs-lookup"><span data-stu-id="39257-118">Internet Key Exchange (IKE) is a key exchange protocol that is part of the IPsec protocol set.</span></span> <span data-ttu-id="39257-119">IKE se usa al configurar una conexión segura y realiza el intercambio seguro de claves secretas y otros parámetros relacionados con la protección sin la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="39257-119">IKE is used while setting up a secure connection and accomplishes the safe exchange of secret keys and other protection-related parameters without the intervention of the user.</span></span>

<span data-ttu-id="39257-120">Para obtener más información sobre IKE, vea también:</span><span class="sxs-lookup"><span data-stu-id="39257-120">For more information on IKE, see also:</span></span>

<dl>

<span data-ttu-id="39257-121">[Intercambio de claves por red](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="39257-121">[Internet Key Exchange](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))</span></span>  
</dl>

## <a name="what-is-authip"></a><span data-ttu-id="39257-122">Qué es AuthIP</span><span class="sxs-lookup"><span data-stu-id="39257-122">What is AuthIP</span></span>

<span data-ttu-id="39257-123">Protocolo de Internet autenticado (AuthIP) es un nuevo protocolo de intercambio de claves que expande IKE como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="39257-123">Authenticated Internet Protocol (AuthIP) is a new key exchange protocol that expands IKE as follows.</span></span>

<dl> <span data-ttu-id="39257-124">Aunque IKE solo es compatible con las credenciales de autenticación de equipo, AuthIP también admite:</span><span class="sxs-lookup"><span data-stu-id="39257-124">While IKE only supports computer authentication credentials, AuthIP also supports:</span></span>

-   <span data-ttu-id="39257-125">Credenciales de usuario: NTLM, Kerberos, certificados.</span><span class="sxs-lookup"><span data-stu-id="39257-125">User credentials: NTLM, Kerberos, certificates.</span></span>
-   <span data-ttu-id="39257-126">Certificados de mantenimiento de protección de acceso a redes (NAP).</span><span class="sxs-lookup"><span data-stu-id="39257-126">Network Access Protection (NAP) health certificates.</span></span>
-   <span data-ttu-id="39257-127">Credencial anónima, que se usa para la autenticación opcional.</span><span class="sxs-lookup"><span data-stu-id="39257-127">Anonymous credential, used for optional authentication.</span></span>
-   <span data-ttu-id="39257-128">Combinación de credenciales; por ejemplo, una combinación de credenciales de Kerberos de equipo y de usuario.</span><span class="sxs-lookup"><span data-stu-id="39257-128">Combination of credentials; for example, a combination of machine and user Kerberos credentials.</span></span>

  
<span data-ttu-id="39257-129">AuthIP tiene un mecanismo de reintento de autenticación que comprueba todos los métodos de autenticación configurados antes de que se produzca un error en la conexión.</span><span class="sxs-lookup"><span data-stu-id="39257-129">AuthIP has an authentication-retry mechanism that verifies all configured authentication methods before failing the connection.</span></span>  
<span data-ttu-id="39257-130">AuthIP se puede usar con sockets seguros para implementar el tráfico protegido por IPsec basado en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39257-130">AuthIP can be used with secure sockets to implement application-based IPsec secured traffic.</span></span> <span data-ttu-id="39257-131">Proporciona:</span><span class="sxs-lookup"><span data-stu-id="39257-131">It provides:</span></span>

-   <span data-ttu-id="39257-132">Cifrado y autenticación por Socket.</span><span class="sxs-lookup"><span data-stu-id="39257-132">Per-socket authentication and encryption.</span></span> <span data-ttu-id="39257-133">Vea [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="39257-133">See [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) for more information.</span></span>
-   <span data-ttu-id="39257-134">Suplantación del cliente.</span><span class="sxs-lookup"><span data-stu-id="39257-134">Client impersonation.</span></span> <span data-ttu-id="39257-135">(IPsec suplanta el contexto de seguridad en el que se crea el socket).</span><span class="sxs-lookup"><span data-stu-id="39257-135">(IPsec impersonates the security context under which the socket is created.)</span></span>
-   <span data-ttu-id="39257-136">Validación del nombre del mismo nivel entrante y saliente.</span><span class="sxs-lookup"><span data-stu-id="39257-136">Inbound and outbound peer name validation.</span></span> <span data-ttu-id="39257-137">Vea [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="39257-137">See [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) for more information.</span></span>

  
</dl>

<span data-ttu-id="39257-138">Para obtener más información sobre AuthIP, vea también:</span><span class="sxs-lookup"><span data-stu-id="39257-138">For more information on AuthIP, see also:</span></span>

<dl>

[<span data-ttu-id="39257-139">AuthIP en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39257-139">AuthIP in Windows Vista</span></span>](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a><span data-ttu-id="39257-140">Qué es una directiva de IPsec</span><span class="sxs-lookup"><span data-stu-id="39257-140">What is an IPsec Policy</span></span>

<span data-ttu-id="39257-141">Una directiva IPsec es un conjunto de reglas que determinan el tipo de tráfico IP que debe protegerse mediante IPsec y cómo proteger ese tráfico.</span><span class="sxs-lookup"><span data-stu-id="39257-141">An IPsec policy is a set of rules that determine which type of IP traffic needs to be secured using IPsec and how to secure that traffic.</span></span> <span data-ttu-id="39257-142">Solo una directiva IPsec está activa en un equipo al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="39257-142">Only one IPsec policy is active on a computer at one time.</span></span>

<span data-ttu-id="39257-143">Para obtener más información acerca de la implementación de directivas IPsec, abra el complemento de MMC Directiva de seguridad local (SECPOL. msc), presione F1 para mostrar la ayuda y, a continuación, seleccione crear y usar directivas IPsec en la tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="39257-143">To learn more about implementing IPsec policies, open the Local Security Policy MMC snap-in (secpol.msc), press F1 to display the Help, and then select Creating and Using IPsec Policies from the table of contents.</span></span>

<span data-ttu-id="39257-144">Para obtener más información sobre las directivas IPsec, vea también:</span><span class="sxs-lookup"><span data-stu-id="39257-144">For more information on IPsec policies, see also:</span></span>

<dl>

<span data-ttu-id="39257-145">[Información general sobre los conceptos de la directiva IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="39257-145">[Overview of IPsec Policy Concepts](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span></span>  
<span data-ttu-id="39257-146">[Descripción de una directiva IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="39257-146">[Description of an IPsec Policy](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))</span></span>  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a><span data-ttu-id="39257-147">Cómo usar WFP para configurar directivas IPsec</span><span class="sxs-lookup"><span data-stu-id="39257-147">How to Use WFP to Configure IPsec Policies</span></span>

<span data-ttu-id="39257-148">La implementación de Microsoft de IPsec usa la plataforma de filtrado de Windows para configurar las directivas de IPsec.</span><span class="sxs-lookup"><span data-stu-id="39257-148">The Microsoft implementation of IPsec uses Windows Filtering Platform to setup IPsec policies.</span></span> <span data-ttu-id="39257-149">Las directivas IPsec se implementan agregando filtros en varias capas de WFP como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="39257-149">IPsec policies are implemented by adding filters at various WFP layers as follows.</span></span>

-   <span data-ttu-id="39257-150">En las capas de la \_ capa FWPM \_ IKEEXT \_ V {4 \| 6}, agregue filtros que especifiquen las directivas de negociación usadas por los módulos de claves (IKE/AuthIP) durante los intercambios del modo principal (mm).</span><span class="sxs-lookup"><span data-stu-id="39257-150">At the FWPM\_LAYER\_IKEEXT\_V{4\|6} layers add filters that specify the negotiation policies used by the keying modules (IKE/AuthIP) during Main Mode (MM) exchanges.</span></span> <span data-ttu-id="39257-151">Los métodos de autenticación y los algoritmos criptográficos se especifican en estas capas.</span><span class="sxs-lookup"><span data-stu-id="39257-151">Authentication methods and cryptographic algorithms are specified at these layers.</span></span>
-   <span data-ttu-id="39257-152">En la capa de FWPM, las \_ \_ capas de IPSec \_ V {4 \| 6} agregan filtros que especifican las directivas de negociación utilizadas por los módulos de creación de claves durante el modo rápido (QM) y los intercambios de modo extendido (EM).</span><span class="sxs-lookup"><span data-stu-id="39257-152">At the FWPM\_LAYER\_IPSEC\_V{4\|6} layers add filters that specify the negotiation policies used by the keying modules during Quick Mode (QM) and Extended Mode (EM) exchanges.</span></span> <span data-ttu-id="39257-153">Los encabezados IPsec (AH/ESP) y los algoritmos criptográficos se especifican en estas capas.</span><span class="sxs-lookup"><span data-stu-id="39257-153">IPsec headers (AH/ESP) and cryptographic algorithms are specified at these layers.</span></span>

    <span data-ttu-id="39257-154">Una directiva de negociación se especifica como un contexto de proveedor de directivas asociado al filtro.</span><span class="sxs-lookup"><span data-stu-id="39257-154">A negotiation policy is specified as a policy provider context associated with the filter.</span></span> <span data-ttu-id="39257-155">El módulo de creación de claves enumera los contextos del proveedor de directivas en función de las características del tráfico y obtiene la Directiva que se va a utilizar para la negociación de seguridad.</span><span class="sxs-lookup"><span data-stu-id="39257-155">The keying module enumerates the policy provider contexts based on the traffic characteristics and obtains the policy to use for the security negotiation.</span></span>

    > [!Note]  
    > <span data-ttu-id="39257-156">La API de WFP se puede usar para especificar directamente las asociaciones de seguridad (SAs) y, por lo tanto, para omitir la Directiva de negociación del módulo de creación de claves.</span><span class="sxs-lookup"><span data-stu-id="39257-156">The WFP API can be used to specify the Security Associations (SAs) directly and therefore to ignore the keying module negotiation policy.</span></span>

     

-   <span data-ttu-id="39257-157">En el nivel de FWPM de \_ \_ transporte de entrada \_ \_ v {4 \| 6} y el transporte de nivel FWPM de \_ salida de capa \_ \_ \_ v {4 \| 6} capas, agregue filtros que invoquen llamadas y determine qué flujo de tráfico debe protegerse.</span><span class="sxs-lookup"><span data-stu-id="39257-157">At the FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} and FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} layers add filters that invoke callouts and determine which traffic flow should be secured.</span></span>
-   <span data-ttu-id="39257-158">En la capa de FWPM, la recepción de la \_ solicitud de aceptación de autenticación de \_ Ale \_ \_ \_ \_ V {4 \| 6} capas agrega filtros que implementan el filtrado de identidades y la Directiva por aplicación.</span><span class="sxs-lookup"><span data-stu-id="39257-158">At the FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} layers add filters that implement identity filtering and per-application policy.</span></span>

<span data-ttu-id="39257-159">En el diagrama siguiente se muestra la interacción de los distintos componentes de WFP, con respecto a la operación de IPsec.</span><span class="sxs-lookup"><span data-stu-id="39257-159">The following diagram illustrates the interaction of the various WFP components, with respect to IPsec operation.</span></span>![configuración de IPsec con la plataforma de filtrado de Windows](images/ipsec-configuration.jpg)

<span data-ttu-id="39257-161">Una vez que se configura IPsec, se integra con WFP y extiende las capacidades de filtrado de WFP proporcionando la información que se va a usar como condiciones de filtrado en los niveles de autorización de cumplimiento del nivel de aplicación (ALE).</span><span class="sxs-lookup"><span data-stu-id="39257-161">Once IPsec is configured, it integrates with WFP and extends the WFP filtering capabilities by providing information to be used as filtering conditions at the Application Layer Enforcement (ALE) authorization layers.</span></span> <span data-ttu-id="39257-162">Por ejemplo, IPsec proporciona el usuario remoto y la identidad de la máquina remota, que WFP expone en los niveles de autorización de conexión y aceptación de ALE.</span><span class="sxs-lookup"><span data-stu-id="39257-162">For example, IPsec provides the remote user and remote machine identity, which WFP exposes at the ALE connect and accept authorization layers.</span></span> <span data-ttu-id="39257-163">Esta información se puede usar para la autorización de identidad remota específica mediante una implementación de Firewall basada en WFP.</span><span class="sxs-lookup"><span data-stu-id="39257-163">This information can be used for fine-grained remote identity authorization by a WFP-based firewall implementation.</span></span>

<span data-ttu-id="39257-164">A continuación se muestra una directiva de aislamiento de ejemplo que se puede implementar mediante IPsec:</span><span class="sxs-lookup"><span data-stu-id="39257-164">Below is a sample isolation policy that may be implemented using IPsec:</span></span>

-   <span data-ttu-id="39257-165">FWPM de nivel de la capa de la versión de reversión \_ \_ \_ V {4 \| 6}: autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="39257-165">FWPM\_LAYER\_IKEEXT\_V{4\|6} layers – Kerberos authentication.</span></span>
-   <span data-ttu-id="39257-166">\_Nivel \_ de FWPM IPSec \_ V {4 \| 6} capas: Ah/SHA-1.</span><span class="sxs-lookup"><span data-stu-id="39257-166">FWPM\_LAYER\_IPSEC\_V{4\|6} layers – AH/SHA-1.</span></span>
-   <span data-ttu-id="39257-167">\_Transporte de \_ entrada de capa FWPM \_ \_ v {4 \| 6} y \_ \_ transporte de salida de capa FWPM \_ \_ v {4 \| 6} capas: detección de negociación para todo el tráfico de red.</span><span class="sxs-lookup"><span data-stu-id="39257-167">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} and FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} layers - negotiation discovery for all network traffic.</span></span>
-   <span data-ttu-id="39257-168">\_La recepción de la auth de Ale de la capa FWPM \_ \_ \_ \_ acepta \_ V {4 \| 6} niveles: IPSec necesario para todo el tráfico de red.</span><span class="sxs-lookup"><span data-stu-id="39257-168">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} layers - IPsec required for all network traffic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39257-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="39257-169">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="39257-170">**Capas de WFP**</span><span class="sxs-lookup"><span data-stu-id="39257-170">**WFP Layers**</span></span>
</dt> <dt>

[<span data-ttu-id="39257-171">**Filtrado de identificadores de capas**</span><span class="sxs-lookup"><span data-stu-id="39257-171">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="39257-172">Niveles ALE</span><span class="sxs-lookup"><span data-stu-id="39257-172">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

<span data-ttu-id="39257-173">**Escenarios de directivas IPsec implementados mediante la API de WFP:**</span><span class="sxs-lookup"><span data-stu-id="39257-173">**IPsec Policy Scenarios Implemented using WFP API:**</span></span>
</dt> <dt>

[<span data-ttu-id="39257-174">modo de transporte</span><span class="sxs-lookup"><span data-stu-id="39257-174">Transport Mode</span></span>](regular-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="39257-175">Modo de transporte de detección de negociación</span><span class="sxs-lookup"><span data-stu-id="39257-175">Negotiation Discovery Transport Mode</span></span>](negotiation-discovery-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="39257-176">Modo de transporte de detección de negociación en modo de límite</span><span class="sxs-lookup"><span data-stu-id="39257-176">Negotiation Discovery Transport Mode in Boundary Mode</span></span>](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[<span data-ttu-id="39257-177">Modo de túnel</span><span class="sxs-lookup"><span data-stu-id="39257-177">Tunnel Mode</span></span>](tunnel-mode.md)
</dt> <dt>

[<span data-ttu-id="39257-178">Cifrado garantizado</span><span class="sxs-lookup"><span data-stu-id="39257-178">Guaranteed Encryption</span></span>](guaranteed-encryption.md)
</dt> <dt>

[<span data-ttu-id="39257-179">Autorización de identidad remota</span><span class="sxs-lookup"><span data-stu-id="39257-179">Remote Identity Authorization</span></span>](remote-identity-authorization.md)
</dt> <dt>

[<span data-ttu-id="39257-180">SAs de IPsec manual</span><span class="sxs-lookup"><span data-stu-id="39257-180">Manual IPsec SAs</span></span>](manual-ipsec-sas.md)
</dt> <dt>

[<span data-ttu-id="39257-181">Exenciones de IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="39257-181">IKE/AuthIP Exemptions</span></span>](ike-exemptions.md)
</dt> <dt>

<span data-ttu-id="39257-182">**Soluciones IPsec:**</span><span class="sxs-lookup"><span data-stu-id="39257-182">**IPsec Solutions:**</span></span>
</dt> <dt>

<span data-ttu-id="39257-183">[Aislamiento de servidor y dominio](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="39257-183">[Server and Domain Isolation](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span></span>
</dt> </dl>

 

 