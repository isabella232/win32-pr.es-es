---
title: Acerca de EAP
description: Protocolo de autenticación extensible (EAP), un estándar compatible con muchos componentes de red de Microsoft.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Protocolo de autenticación extensible, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631299c9e57a233794dde8bf205d98b8c91b76c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421530"
---
# <a name="about-eap"></a><span data-ttu-id="8fed2-104">Acerca de EAP</span><span class="sxs-lookup"><span data-stu-id="8fed2-104">About EAP</span></span>

<span data-ttu-id="8fed2-105">En este tema se describe el protocolo de autenticación extensible (EAP), un estándar que admiten muchos componentes de red de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8fed2-105">This topic describes Extensible Authentication Protocol (EAP), a standard supported by many Microsoft networking components.</span></span>

## <a name="eap-components"></a><span data-ttu-id="8fed2-106">Componentes de EAP</span><span class="sxs-lookup"><span data-stu-id="8fed2-106">EAP Components</span></span>

<span data-ttu-id="8fed2-107">EAP es fundamental para proteger la seguridad de LAN inalámbricas (802.1 X), LAN cableadas y redes privadas virtuales (VPN) y de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="8fed2-107">EAP is crucial for protecting the security of wireless (802.1X) LANs, wired LANs, and dial-up and Virtual Private Networks (VPNs).</span></span>

<span data-ttu-id="8fed2-108">Los componentes siguientes admiten el protocolo EAP.</span><span class="sxs-lookup"><span data-stu-id="8fed2-108">The following components support the EAP protocol.</span></span>

-   <span data-ttu-id="8fed2-109">Los clientes y servidores de acceso remoto de Microsoft para acceso telefónico y VPN (PPTP y L2TP/IPSec) implementan EAP como una extensión de PPP.</span><span class="sxs-lookup"><span data-stu-id="8fed2-109">Microsoft Remote Access Clients and Servers for both dial-up and VPN (PPTP and L2TP/IPSec) implement EAP as an extension to PPP.</span></span> <span data-ttu-id="8fed2-110">Para obtener más información, consulte [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span><span class="sxs-lookup"><span data-stu-id="8fed2-110">For more information, see [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span></span>
-   <span data-ttu-id="8fed2-111">Los clientes de LAN inalámbrica y cableada compatibles con IEEE 802.1 X de Microsoft implementan EAP tal y como se define en el borrador estándar IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="8fed2-111">Microsoft IEEE 802.1X compatible wireless and wired LAN clients implement EAP as defined in the IEEE 802.1X draft standard.</span></span>
-   <span data-ttu-id="8fed2-112">El servidor RADIUS de Microsoft, denominado servicio de autenticación de Internet (IAS), implementa EAP tal y como se define en [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).</span><span class="sxs-lookup"><span data-stu-id="8fed2-112">Microsoft RADIUS server, called Internet Authentication Service (IAS) implement EAP as defined in [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).</span></span>

<span data-ttu-id="8fed2-113">Todos los componentes anteriores admiten esta arquitectura extensible a través del kit de desarrollo de software (SDK) de Microsoft Windows, lo que permite integrar módulos de autenticación de terceros.</span><span class="sxs-lookup"><span data-stu-id="8fed2-113">All of the above components support this extensible architecture through the Microsoft Windows Software Development Kit (SDK), making it possible to integrate third-party authentication modules.</span></span> <span data-ttu-id="8fed2-114">Este mecanismo extensible se puede usar para admitir los protocolos de autenticación de tarjetas de token, Kerberos, clave pública y S/Key.</span><span class="sxs-lookup"><span data-stu-id="8fed2-114">This extensible mechanism can be used to support token cards, Kerberos, Public Key, and S/Key authentication protocols.</span></span>

## <a name="protected-extensible-authentication-protocol"></a><span data-ttu-id="8fed2-115">Protocolo de autenticación extensible protegido</span><span class="sxs-lookup"><span data-stu-id="8fed2-115">Protected Extensible Authentication Protocol</span></span>

<span data-ttu-id="8fed2-116">Además de EAP, la implementación inalámbrica (802.1 X) y el servidor RADIUS también admiten un estándar emergente denominado EAP protegido (PEAP).</span><span class="sxs-lookup"><span data-stu-id="8fed2-116">In addition to EAP, the wireless (802.1X) implementation and RADIUS server also support an emerging standard called Protected EAP (PEAP).</span></span>

<span data-ttu-id="8fed2-117">PEAP proporciona varios servicios clave a otros protocolos de autenticación EAP, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="8fed2-117">PEAP provides several key services to other EAP authentication protocols, as follows.</span></span>

-   <span data-ttu-id="8fed2-118">PEAP cifra los paquetes EAP de otros protocolos de autenticación EAP mediante seguridad de la capa de transporte (TLS), una tecnología basada en capa de sockets seguros (SSL).</span><span class="sxs-lookup"><span data-stu-id="8fed2-118">PEAP encrypts EAP packets of other EAP authentication protocols using Transport Layer Security (TLS), a Secure Socket Layer (SSL) based technology.</span></span> <span data-ttu-id="8fed2-119">Para obtener más información, consulte [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).</span><span class="sxs-lookup"><span data-stu-id="8fed2-119">For more information, see [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).</span></span>
-   <span data-ttu-id="8fed2-120">PEAP autentica el lado servidor mediante un certificado de servidor, con el servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="8fed2-120">PEAP authenticates the server-side using a Server Certificate, with RADIUS server.</span></span>
-   <span data-ttu-id="8fed2-121">PEAP ofrece una funcionalidad de reautenticación rápida que admite la itinerancia eficaz entre dispositivos inalámbricos.</span><span class="sxs-lookup"><span data-stu-id="8fed2-121">PEAP offers fast re-authentication capability that supports efficient roaming between wireless devices.</span></span>
-   <span data-ttu-id="8fed2-122">PEAP administra la fragmentación y el reensamblado de los paquetes EAP.</span><span class="sxs-lookup"><span data-stu-id="8fed2-122">PEAP manages the fragmentation and re-assembly of EAP packets.</span></span>
-   <span data-ttu-id="8fed2-123">PEAP genera claves utilizadas para cifrar el tráfico inalámbrico.</span><span class="sxs-lookup"><span data-stu-id="8fed2-123">PEAP generates keys used for encrypting wireless traffic.</span></span>

<span data-ttu-id="8fed2-124">PEAP facilita la escritura de un protocolo EAP, ya que el programador ya no tiene que resolver estos problemas.</span><span class="sxs-lookup"><span data-stu-id="8fed2-124">PEAP makes it much easier to write an EAP protocol because the programmer no longer has to address these issues.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fed2-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8fed2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fed2-126">Acerca de EAP y EAPHost</span><span class="sxs-lookup"><span data-stu-id="8fed2-126">About EAP and EAPHost</span></span>](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 




