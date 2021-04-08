---
description: Microsoft Negotiate es un proveedor de soporte técnico de seguridad que actúa como un nivel de aplicación entre la interfaz del proveedor de compatibilidad para seguridad y el resto de SSP.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Microsoft Negotiate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ce57a8f8924120dcce51e50e05de90fd6774b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001087"
---
# <a name="microsoft-negotiate"></a><span data-ttu-id="63a3e-103">Microsoft Negotiate</span><span class="sxs-lookup"><span data-stu-id="63a3e-103">Microsoft Negotiate</span></span>

<span data-ttu-id="63a3e-104">Microsoft Negotiate es un [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSP) que actúa como un nivel de aplicación entre la [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) ([SSPI](sspi.md)) y el otro SSP.</span><span class="sxs-lookup"><span data-stu-id="63a3e-104">Microsoft Negotiate is a [*security support provider*](../secgloss/s-gly.md) (SSP) that acts as an application layer between [*Security Support Provider Interface*](../secgloss/s-gly.md) ([SSPI](sspi.md)) and the other SSPs.</span></span> <span data-ttu-id="63a3e-105">Cuando una aplicación llama en SSPI para iniciar sesión en una red, puede especificar un SSP para que procese la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63a3e-105">When an application calls into SSPI to log on to a network, it can specify an SSP to process the request.</span></span> <span data-ttu-id="63a3e-106">Si la aplicación especifica Negotiate, Negotiate analiza la solicitud y elige el mejor SSP para controlar la solicitud en función de la Directiva de seguridad configurada por el cliente.</span><span class="sxs-lookup"><span data-stu-id="63a3e-106">If the application specifies Negotiate, Negotiate analyzes the request and picks the best SSP to handle the request based on customer-configured security policy.</span></span>

<span data-ttu-id="63a3e-107">Actualmente, el paquete de seguridad Negotiate selecciona entre [Kerberos](microsoft-kerberos.md) y [NTLM](microsoft-ntlm.md).</span><span class="sxs-lookup"><span data-stu-id="63a3e-107">Currently, the Negotiate security package selects between [Kerberos](microsoft-kerberos.md) and [NTLM](microsoft-ntlm.md).</span></span> <span data-ttu-id="63a3e-108">Negotiate selecciona Kerberos a menos que no pueda usarse en uno de los sistemas implicados en la autenticación o la aplicación que realiza la llamada no haya proporcionado información suficiente para usar Kerberos.</span><span class="sxs-lookup"><span data-stu-id="63a3e-108">Negotiate selects Kerberos unless it cannot be used by one of the systems involved in the authentication or the calling application did not provide sufficient information to use Kerberos.</span></span>

<span data-ttu-id="63a3e-109">Para permitir que Negotiate Seleccione el proveedor de seguridad de [Kerberos](microsoft-kerberos.md) , la aplicación cliente debe proporcionar un [*nombre principal de servicio*](../secgloss/s-gly.md) (SPN), un nombre principal de usuario (UPN) o un nombre de cuenta NetBIOS como nombre de destino.</span><span class="sxs-lookup"><span data-stu-id="63a3e-109">To allow Negotiate to select the [Kerberos](microsoft-kerberos.md) security provider, the client application must provide a [*service principal name*](../secgloss/s-gly.md) (SPN), a user principal name (UPN), or a NetBIOS account name as the target name.</span></span> <span data-ttu-id="63a3e-110">De lo contrario, Negotiate siempre selecciona el proveedor de seguridad [NTLM](microsoft-ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="63a3e-110">Otherwise, Negotiate always selects the [NTLM](microsoft-ntlm.md) security provider.</span></span>

<span data-ttu-id="63a3e-111">Un servidor que usa el paquete Negotiate puede responder a las aplicaciones cliente que seleccionan específicamente el proveedor de seguridad [Kerberos](microsoft-kerberos.md) o [NTLM](microsoft-ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="63a3e-111">A server that uses the Negotiate package is able to respond to client applications that specifically select either the [Kerberos](microsoft-kerberos.md) or [NTLM](microsoft-ntlm.md) security provider.</span></span> <span data-ttu-id="63a3e-112">Sin embargo, una aplicación cliente debe saber que un servidor admite el paquete Negotiate para solicitar autenticación mediante Negotiate.</span><span class="sxs-lookup"><span data-stu-id="63a3e-112">However, a client application must know that a server supports the Negotiate package to request authentication using Negotiate.</span></span> <span data-ttu-id="63a3e-113">Un servidor que no admita Negotiate no podrá responder siempre a las solicitudes de clientes que especifiquen Negotiate como SSP.</span><span class="sxs-lookup"><span data-stu-id="63a3e-113">A server that does not support Negotiate cannot always respond to requests from clients that specify Negotiate as the SSP.</span></span>

## <a name="reasons-to-use-the-negotiate-package"></a><span data-ttu-id="63a3e-114">Razones para usar el paquete Negotiate</span><span class="sxs-lookup"><span data-stu-id="63a3e-114">Reasons to Use the Negotiate Package</span></span>

-   <span data-ttu-id="63a3e-115">Permite que el sistema use el protocolo disponible más seguro (más seguro).</span><span class="sxs-lookup"><span data-stu-id="63a3e-115">Allows the system to use the strongest (most secure) available protocol.</span></span>
-   <span data-ttu-id="63a3e-116">Garantiza la compatibilidad con versiones posteriores de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63a3e-116">Ensures forward compatibility for your application.</span></span>
-   <span data-ttu-id="63a3e-117">Garantiza que la aplicación exhibe el comportamiento que se ajusta a la Directiva de seguridad establecida por el cliente.</span><span class="sxs-lookup"><span data-stu-id="63a3e-117">Ensures that your application exhibits behavior that is in accordance with the security policy set by the customer.</span></span>

 

 
