---
description: Todas las operaciones normales de RSA/Schannel y Diffie-Hellman/Schannel usan el \_ par de claves pública y privada de KEYEXCHANGE.
ms.assetid: e12afdbb-7ba8-444e-a43f-e262b481a353
title: Uso del par de claves pública y privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dba78c487c433875ed23ce3f2f3c87a86b07c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688037"
---
# <a name="publicprivate-key-pair-usage"></a><span data-ttu-id="19595-103">Uso del par de claves pública y privada</span><span class="sxs-lookup"><span data-stu-id="19595-103">Public/Private Key Pair Usage</span></span>

<span data-ttu-id="19595-104">Todas las operaciones normales de [*RSA*](../secgloss/r-gly.md)/Schannel y [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel usan \_ el [*par de claves pública y privada*](../secgloss/p-gly.md)de KEYEXCHANGE.</span><span class="sxs-lookup"><span data-stu-id="19595-104">All normal [*RSA*](../secgloss/r-gly.md)/Schannel and [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel operations use the AT\_KEYEXCHANGE [*public/private key pair*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="19595-105">Para proporcionar [*autenticación*](../secgloss/a-gly.md)de servidor, el servidor de las operaciones Schannel debe tener acceso a su certificado [*X. 509*](../secgloss/x-gly.md) que contiene su clave pública y tener acceso a la [*clave privada*](../secgloss/p-gly.md)correspondiente.</span><span class="sxs-lookup"><span data-stu-id="19595-105">To provide server [*authentication*](../secgloss/a-gly.md), the server-side of Schannel operations must have access to its [*X.509*](../secgloss/x-gly.md) certificate containing its public key and access to the matching [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="19595-106">El lado cliente de [*Schannel*](../secgloss/s-gly.md) necesita su certificado con su clave pública y acceso a su clave privada si se implementa la autenticación del cliente.</span><span class="sxs-lookup"><span data-stu-id="19595-106">The client-side of [*Schannel*](../secgloss/s-gly.md) needs its certificate with its public key and access to its private key if client authentication is implemented.</span></span>

<span data-ttu-id="19595-107">Dado que los motores de protocolo Schannel nunca usan el \_ par de claves pública y privada de la firma, ese par de claves no es compatible con un nuevo CSP que solo admite RSA/Schannel o Diffie-Hellman/Schannel.</span><span class="sxs-lookup"><span data-stu-id="19595-107">Since Schannel protocol engines never use the AT\_SIGNATURE public/private key pair, that key pair need not be supported by a new CSP supporting only RSA/Schannel or Diffie-Hellman/Schannel.</span></span>

<span data-ttu-id="19595-108">Si un motor de protocolo usa un conjunto de cifrado de exportación SSL 3,0 con un \_ par de claves at KEYEXCHANGE superior a 512 bits, el servidor debe utilizar un par de claves RSA adicional.</span><span class="sxs-lookup"><span data-stu-id="19595-108">If a protocol engine uses an SSL 3.0 export cipher suite with an AT\_KEYEXCHANGE key pair larger than 512 bits, the server must use an additional RSA key pair.</span></span> <span data-ttu-id="19595-109">Este par de claves adicional siempre es exactamente 512 bits y puede ser efímero.</span><span class="sxs-lookup"><span data-stu-id="19595-109">This additional key pair is always exactly 512 bits and it can be ephemeral.</span></span> <span data-ttu-id="19595-110">El par se almacena como un \_ elemento en KEYEXCHANGE en un contenedor de claves propiedad del motor de protocolo.</span><span class="sxs-lookup"><span data-stu-id="19595-110">The pair is stored as an AT\_KEYEXCHANGE element in a key container owned by the protocol engine.</span></span> <span data-ttu-id="19595-111">Un identificador de este contenedor de claves se adquiere normalmente en el inicio del motor de protocolo.</span><span class="sxs-lookup"><span data-stu-id="19595-111">A handle to this key container is typically acquired at protocol engine startup.</span></span>

<span data-ttu-id="19595-112">Diffie-Hellman solo admite [*CALG \_ DH \_ EPHEM*](../secgloss/c-gly.md) y usa claves públicas RSA o DSS normales.</span><span class="sxs-lookup"><span data-stu-id="19595-112">Diffie-Hellman supports only [*CALG\_DH\_EPHEM*](../secgloss/c-gly.md) and uses normal RSA or DSS public keys.</span></span>

 

 
