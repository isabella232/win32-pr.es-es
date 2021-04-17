---
description: TLS es un estándar estrechamente relacionado con SSL 3,0 y a veces se conoce como &\# 0034; SSL 3,1&\# 0034;.
ms.assetid: 92b1b486-7e10-48a2-b1d2-56d4e472dbe4
title: TLS frente a SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac1a2e783b6f3355127a3148f1575f73119f6604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668246"
---
# <a name="tls-vs-ssl"></a><span data-ttu-id="4ae4b-103">TLS frente a SSL</span><span class="sxs-lookup"><span data-stu-id="4ae4b-103">TLS vs. SSL</span></span>

<span data-ttu-id="4ae4b-104">TLS es un estándar estrechamente relacionado con SSL 3,0 y a veces se denomina "SSL 3,1".</span><span class="sxs-lookup"><span data-stu-id="4ae4b-104">TLS is a standard closely related to SSL 3.0, and is sometimes referred to as "SSL 3.1".</span></span> <span data-ttu-id="4ae4b-105">TLS reemplaza a SSL 2,0 y debe usarse en el nuevo desarrollo.</span><span class="sxs-lookup"><span data-stu-id="4ae4b-105">TLS supersedes SSL 2.0 and should be used in new development.</span></span> <span data-ttu-id="4ae4b-106">A partir de Windows 10, versión 1607 y Windows Server 2016, se ha quitado SSL 2,0 y ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="4ae4b-106">Beginning with Windows 10, version 1607 and Windows Server 2016, SSL 2.0 has been removed and is no longer supported.</span></span>

<span data-ttu-id="4ae4b-107">Las aplicaciones que requieren un alto nivel de interoperabilidad deben admitir SSL 3,0 y TLS.</span><span class="sxs-lookup"><span data-stu-id="4ae4b-107">Applications that require a high level of interoperability should support SSL 3.0 and TLS.</span></span> <span data-ttu-id="4ae4b-108">Debido a las similitudes entre estos dos protocolos, los detalles de SSL no se incluyen en esta documentación, excepto cuando difieren de TLS.</span><span class="sxs-lookup"><span data-stu-id="4ae4b-108">Because of the similarities between these two protocols, SSL details are not included in this documentation, except where they differ from TLS.</span></span> <span data-ttu-id="4ae4b-109">A continuación se indican los [documentos RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):</span><span class="sxs-lookup"><span data-stu-id="4ae4b-109">The following is from [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):</span></span>

<span data-ttu-id="4ae4b-110">"Las diferencias entre este protocolo y SSL 3,0 no son espectaculares, pero son lo suficientemente importantes como para que TLS 1,0 y SSL 3,0 no interoperen (aunque TLS 1,0 incorpora un mecanismo por el que una implementación de TLS puede hacer una copia de seguridad en SSL 3,0)".</span><span class="sxs-lookup"><span data-stu-id="4ae4b-110">"The differences between this protocol and SSL 3.0 are not dramatic, but they are significant enough that TLS 1.0 and SSL 3.0 do not interoperate (although TLS 1.0 does incorporate a mechanism by which a TLS implementation can back down to SSL 3.0)."</span></span>

 

 



