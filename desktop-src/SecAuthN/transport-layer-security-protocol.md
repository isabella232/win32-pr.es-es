---
description: Schannel admite las versiones 1,0, 1,1 y 1,2 del protocolo seguridad de la capa de transporte (TLS).
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: Protocolo de seguridad de la capa de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf35fbfb59fee80617e6eccab66d7cec538e61ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668125"
---
# <a name="transport-layer-security-protocol"></a><span data-ttu-id="fb9c0-103">Protocolo de seguridad de la capa de transporte</span><span class="sxs-lookup"><span data-stu-id="fb9c0-103">Transport Layer Security Protocol</span></span>

<span data-ttu-id="fb9c0-104">Schannel admite las versiones 1,0, 1,1 y 1,2 del [*Protocolo seguridad de la capa de transporte (TLS)*](../secgloss/t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fb9c0-104">Schannel supports versions 1.0, 1.1, and 1.2 of the [*Transport Layer Security (TLS) protocol*](../secgloss/t-gly.md).</span></span> <span data-ttu-id="fb9c0-105">Este protocolo es un estándar del sector diseñado para proteger la privacidad de la información que se comunica a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="fb9c0-105">This protocol is an industry standard designed to protect the privacy of information communicated over the Internet.</span></span> <span data-ttu-id="fb9c0-106">TLS supone que un transporte orientado a la conexión, normalmente TCP, está en uso.</span><span class="sxs-lookup"><span data-stu-id="fb9c0-106">TLS assumes that a connection-oriented transport, typically TCP, is in use.</span></span> <span data-ttu-id="fb9c0-107">El protocolo TLS permite a las aplicaciones cliente/servidor detectar los riesgos de seguridad siguientes:</span><span class="sxs-lookup"><span data-stu-id="fb9c0-107">The TLS protocol allows client/server applications to detect the following security risks:</span></span>

-   <span data-ttu-id="fb9c0-108">Manipulación de mensajes</span><span class="sxs-lookup"><span data-stu-id="fb9c0-108">Message tampering</span></span>
-   <span data-ttu-id="fb9c0-109">Interceptación de mensajes</span><span class="sxs-lookup"><span data-stu-id="fb9c0-109">Message interception</span></span>
-   <span data-ttu-id="fb9c0-110">Falsificación de mensajes</span><span class="sxs-lookup"><span data-stu-id="fb9c0-110">Message forgery</span></span>

<span data-ttu-id="fb9c0-111">La especificación completa del protocolo TLS está disponible en el sitio web de IETF: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) .</span><span class="sxs-lookup"><span data-stu-id="fb9c0-111">The full specification of the TLS Protocol is available from the IETF website: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt).</span></span>

## <a name="organization-of-tls"></a><span data-ttu-id="fb9c0-112">Organización de TLS</span><span class="sxs-lookup"><span data-stu-id="fb9c0-112">Organization of TLS</span></span>

<span data-ttu-id="fb9c0-113">Los siguientes pasos están relacionados con el uso de TLS para la comunicación entre cliente y servidor:</span><span class="sxs-lookup"><span data-stu-id="fb9c0-113">The following steps are involved in using TLS for client/server communication:</span></span>

 <span data-ttu-id="fb9c0-114">**Para utilizar TLS para la comunicación entre cliente y servidor**</span><span class="sxs-lookup"><span data-stu-id="fb9c0-114">**To use TLS for client/server communication**</span></span>

1.  <span data-ttu-id="fb9c0-115">Negociación del conjunto de protocolos y el protocolo de enlace</span><span class="sxs-lookup"><span data-stu-id="fb9c0-115">Handshake and cipher suite negotiation</span></span>
2.  <span data-ttu-id="fb9c0-116">Autenticación de entidades</span><span class="sxs-lookup"><span data-stu-id="fb9c0-116">Authentication of parties</span></span>
3.  <span data-ttu-id="fb9c0-117">Intercambio de información relacionada con claves</span><span class="sxs-lookup"><span data-stu-id="fb9c0-117">Key-related information exchange</span></span>
4.  <span data-ttu-id="fb9c0-118">Intercambio de datos de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="fb9c0-118">Application data exchange</span></span>

<span data-ttu-id="fb9c0-119">Los pasos que componen TLS están divididos en dos protocolos que, juntos, proporcionan seguridad de conexión:</span><span class="sxs-lookup"><span data-stu-id="fb9c0-119">The steps that make up TLS are divided into two protocols that, together, provide connection security:</span></span>

-   <span data-ttu-id="fb9c0-120">[Protocolo de enlace TLS](tls-handshake-protocol.md): (pasos 1 a 3)</span><span class="sxs-lookup"><span data-stu-id="fb9c0-120">[TLS Handshake Protocol](tls-handshake-protocol.md)— (steps 1 – 3)</span></span>
-   <span data-ttu-id="fb9c0-121">[Protocolo de registro de TLS](tls-record-protocol.md): (paso 4)</span><span class="sxs-lookup"><span data-stu-id="fb9c0-121">[TLS Record Protocol](tls-record-protocol.md)— (step 4)</span></span>

## <a name="sspi-with-tls-implementations"></a><span data-ttu-id="fb9c0-122">SSPI con implementaciones de TLS</span><span class="sxs-lookup"><span data-stu-id="fb9c0-122">SSPI with TLS implementations</span></span>

<span data-ttu-id="fb9c0-123">Dado que TLS no tiene una especificación GSSAPI, es posible que los implementadores de TLS no estén familiarizados con las funciones SSPI.</span><span class="sxs-lookup"><span data-stu-id="fb9c0-123">Because TLS does not have a GSSAPI specification, TLS implementers may not be familiar with the SSPI functions.</span></span> <span data-ttu-id="fb9c0-124">Las aplicaciones llaman a las funciones SSPI para enumerar los paquetes disponibles, crear y trabajar con identificadores de credenciales, crear contextos de seguridad y garantizar la privacidad de la integridad del mensaje.</span><span class="sxs-lookup"><span data-stu-id="fb9c0-124">Applications call the SSPI functions to enumerate available packages, create and work with handles to credentials, create security contexts and ensure message integrity privacy.</span></span>

<span data-ttu-id="fb9c0-125">Para admitir las funciones SSPI usadas por las aplicaciones de modo de usuario, las funciones enumeradas en [funciones implementadas por SSP/APS de modo de usuario](/windows/desktop/SecAuthN/authentication-functions) deben ser compatibles con las implementaciones de TLS como schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="fb9c0-125">To support the SSPI functions used by user mode applications, the functions listed in [Functions Implemented by User-mode SSP/APs](/windows/desktop/SecAuthN/authentication-functions) need to be supported by TLS implementations such as schannel.dll.</span></span>

<span data-ttu-id="fb9c0-126">Para obtener más información sobre las funciones SSPI y las funciones SSP, consulte [funciones de autenticación](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="fb9c0-126">For details about the SSPI functions and SSP functions, see [Authentication Functions](authentication-functions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb9c0-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb9c0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb9c0-128">Conjuntos de cifrado TLS</span><span class="sxs-lookup"><span data-stu-id="fb9c0-128">TLS Cipher Suites</span></span>](tls-cipher-suites.md)
</dt> <dt>

[<span data-ttu-id="fb9c0-129">TLS frente a SSL</span><span class="sxs-lookup"><span data-stu-id="fb9c0-129">TLS vs. SSL</span></span>](tls-versus-ssl.md)
</dt> </dl>

 

 
