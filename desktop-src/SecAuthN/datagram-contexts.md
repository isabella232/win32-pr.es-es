---
description: La semántica de los contextos de datagramas o sin conexión difiere ligeramente de la de los contextos orientados a la conexión.
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: Contextos de datagramas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d233a0ba397e67a13b1c25588cf81b6f12c31d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154773"
---
# <a name="datagram-contexts"></a><span data-ttu-id="34c99-103">Contextos de datagramas</span><span class="sxs-lookup"><span data-stu-id="34c99-103">Datagram Contexts</span></span>

<span data-ttu-id="34c99-104">La semántica de los contextos de [*datagramas*](/windows/desktop/SecGloss/d-gly)o sin conexión difiere ligeramente de la de los contextos orientados a la conexión.</span><span class="sxs-lookup"><span data-stu-id="34c99-104">The semantics for [*datagram*](/windows/desktop/SecGloss/d-gly), or connectionless, contexts differ slightly from those for connection-oriented contexts.</span></span> <span data-ttu-id="34c99-105">En el [*contexto*](/windows/desktop/SecGloss/c-gly)sin conexión de un datagrama, un servidor no puede determinar si el cliente se ha cerrado o ha finalizado la conexión.</span><span class="sxs-lookup"><span data-stu-id="34c99-105">In a datagram's connectionless [*context*](/windows/desktop/SecGloss/c-gly), a server cannot determine when the client has shut down or otherwise terminated the connection.</span></span> <span data-ttu-id="34c99-106">En otras palabras, no se pasa ningún aviso de finalización de la aplicación de transporte al servidor como sucedería en un contexto orientado a la conexión.</span><span class="sxs-lookup"><span data-stu-id="34c99-106">In other words, no termination notice is passed from the transport application to the server as would occur in a connection-oriented context.</span></span>

<span data-ttu-id="34c99-107">Para utilizar un contexto de datagrama, un cliente establece la \_ \_ marca de datagrama req de ISC en su llamada a la función [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .</span><span class="sxs-lookup"><span data-stu-id="34c99-107">To use a datagram context, a client sets the ISC\_REQ\_DATAGRAM flag in its call to the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34c99-108">El paquete de [Microsoft Kerberos](microsoft-kerberos.md) no admite contextos de datagramas en modo de usuario a usuario.</span><span class="sxs-lookup"><span data-stu-id="34c99-108">The [Microsoft Kerberos](microsoft-kerberos.md) package does not support datagram contexts in user-to-user mode.</span></span>

 

<span data-ttu-id="34c99-109">Para admitir mejor algunos modelos, especialmente RPC de estilo DCE, se aplican las reglas siguientes cuando el cliente usa un contexto de datagrama:</span><span class="sxs-lookup"><span data-stu-id="34c99-109">To better support some models, particularly DCE-style RPC, the following rules apply when the client uses a datagram context:</span></span>

-   <span data-ttu-id="34c99-110">El [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly) no genera un [*BLOB*](/windows/desktop/SecGloss/b-gly) de autenticación (objeto binario grande) en la primera llamada a [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="34c99-110">The [*security package*](/windows/desktop/SecGloss/s-gly) does not produce an authentication [*BLOB*](/windows/desktop/SecGloss/b-gly) (binary large object) on the first call to [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span> <span data-ttu-id="34c99-111">Sin embargo, el cliente puede utilizar el contexto de seguridad devuelto en una llamada a la función [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para generar una firma para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="34c99-111">However, the client can use the returned security context in a call to the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to generate a signature for a message.</span></span>
-   <span data-ttu-id="34c99-112">El paquete de seguridad debe permitir que el contexto se vuelva a establecer varias veces para permitir que el servidor Quite la conexión sin previo aviso.</span><span class="sxs-lookup"><span data-stu-id="34c99-112">The security package must allow for the context to be re-established multiple times to allow the server to drop the connection without notice.</span></span> <span data-ttu-id="34c99-113">Esto implica que cualquier clave utilizada en las funciones [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) y [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) se puede restablecer a un [*Estado*](/windows/desktop/SecGloss/s-gly)coherente.</span><span class="sxs-lookup"><span data-stu-id="34c99-113">This implies that any keys used in the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions can be reset to a consistent [*state*](/windows/desktop/SecGloss/s-gly).</span></span>
-   <span data-ttu-id="34c99-114">El paquete de seguridad permite al llamador especificar la información de la secuencia y proporciona esa información de secuencia en el lado del receptor.</span><span class="sxs-lookup"><span data-stu-id="34c99-114">The security package allows the caller to specify sequence information, and provides that sequence information at the receiver side.</span></span> <span data-ttu-id="34c99-115">Esto se suma a cualquier información de secuencia mantenida por el paquete.</span><span class="sxs-lookup"><span data-stu-id="34c99-115">This is in addition to any sequence information maintained by the package.</span></span>

<span data-ttu-id="34c99-116">Un paquete de seguridad establece la \_ marca de datagrama de marca SECPKG \_ para indicar que admite la semántica de datagramas.</span><span class="sxs-lookup"><span data-stu-id="34c99-116">A security package sets the SECPKG\_FLAG\_DATAGRAM flag to indicate that it supports datagram semantics.</span></span>

 

 
