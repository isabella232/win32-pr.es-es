---
description: La ocultación es una extensión a la suplantación que permite un mejor control sobre cómo COM suplanta a un cliente a través de un proxy. Al igual que muchas formas de seguridad de WMI, se establece la ocultación a través de las interfaces CoSetProxyBlanket y CoInitializeSecurity.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Implementar Cloaking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac73d7aacf32a2168dc3651b82ae1ce3a977cf5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277931"
---
# <a name="implementing-cloaking"></a><span data-ttu-id="4e213-104">Implementar Cloaking</span><span class="sxs-lookup"><span data-stu-id="4e213-104">Implementing Cloaking</span></span>

<span data-ttu-id="4e213-105">La ocultación es una extensión a la suplantación que permite un mejor control sobre cómo COM suplanta a un cliente a través de un proxy.</span><span class="sxs-lookup"><span data-stu-id="4e213-105">Cloaking is an extension to impersonation that allows for better control over how COM impersonates a client over a proxy.</span></span> <span data-ttu-id="4e213-106">Al igual que muchas formas de seguridad de WMI, se establece la ocultación a través de las interfaces [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="4e213-106">Like many forms of WMI security, you set cloaking through the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) interfaces.</span></span>

<span data-ttu-id="4e213-107">COM proporciona las siguientes formas de Cloaking:</span><span class="sxs-lookup"><span data-stu-id="4e213-107">COM provides the following forms of cloaking:</span></span>

-   <span data-ttu-id="4e213-108">estática</span><span class="sxs-lookup"><span data-stu-id="4e213-108">Static</span></span>

    <span data-ttu-id="4e213-109">COM establece la identidad del token por el subproceso o el token de proceso en la primera llamada al proxy.</span><span class="sxs-lookup"><span data-stu-id="4e213-109">COM establishes the token identity by the thread or process token on the first call to the proxy.</span></span> <span data-ttu-id="4e213-110">Si utiliza el Cloaking estático con [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), establezca la identidad del proxy para la vida del proxy.</span><span class="sxs-lookup"><span data-stu-id="4e213-110">If you use static cloaking with [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), you set the identity of the proxy for the life of the proxy.</span></span>

-   <span data-ttu-id="4e213-111">Dinámica</span><span class="sxs-lookup"><span data-stu-id="4e213-111">Dynamic</span></span>

    <span data-ttu-id="4e213-112">COM restablece la identidad del token del subproceso o token del proceso en cada llamada al proxy.</span><span class="sxs-lookup"><span data-stu-id="4e213-112">COM reestablishes the token identity from the thread or process token on each call to the proxy.</span></span> <span data-ttu-id="4e213-113">Dado que COM comprueba la identidad en cada llamada, el Cloaking dinámico permite un mayor control sobre la identidad del cliente.</span><span class="sxs-lookup"><span data-stu-id="4e213-113">Because COM checks the identity on each call, dynamic cloaking allows for finer control over the client identity.</span></span> <span data-ttu-id="4e213-114">Sin embargo, el Cloaking dinámico es menos eficaz que el Cloaking estático.</span><span class="sxs-lookup"><span data-stu-id="4e213-114">However, dynamic cloaking is less efficient than static cloaking.</span></span>

<span data-ttu-id="4e213-115">Cuando se establece la ocultación junto con el nivel de delegación de la suplantación, un servidor puede propagar la identidad de un cliente entre servidores, incluso si los servidores son remotos.</span><span class="sxs-lookup"><span data-stu-id="4e213-115">When you set cloaking in conjunction with the delegation level of impersonation, a server can propagate the identity of a client across servers, even if the servers are remote.</span></span> <span data-ttu-id="4e213-116">Si no habilita la ocultación, COM realiza cualquier llamada desde un servidor local a un servidor remoto en el contexto del proceso de servidor real.</span><span class="sxs-lookup"><span data-stu-id="4e213-116">If you do not enable cloaking, COM makes any call from a local server to a remote server under the context of the actual server process.</span></span>

<span data-ttu-id="4e213-117">La ocultación permite a WMI suplantar a un cliente para obtener acceso a recursos de red locales y remotos en varios límites de equipos.</span><span class="sxs-lookup"><span data-stu-id="4e213-117">Cloaking lets WMI impersonate a client to access both local and remote network resources across multiple computer boundaries.</span></span> <span data-ttu-id="4e213-118">WMI puede pasar la identidad del cliente a servidores locales y remotos, como otras instancias remotas de WMI.</span><span class="sxs-lookup"><span data-stu-id="4e213-118">WMI can pass the identity of the client to local and remote servers, such as other remote instances of WMI.</span></span> <span data-ttu-id="4e213-119">Estos servidores remotos pueden realizar operaciones en el contexto de cliente inicial.</span><span class="sxs-lookup"><span data-stu-id="4e213-119">Those remote servers can then perform operations under the initial client context.</span></span>

<span data-ttu-id="4e213-120">En el procedimiento siguiente se describe cómo usar juntos la ocultación y la delegación.</span><span class="sxs-lookup"><span data-stu-id="4e213-120">The following procedure describes how to use cloaking and delegation together.</span></span>

<span data-ttu-id="4e213-121">**Para usar la ocultación y la delegación juntas**</span><span class="sxs-lookup"><span data-stu-id="4e213-121">**To use cloaking and delegation together**</span></span>

1.  <span data-ttu-id="4e213-122">Establezca el servicio de autenticación en Kerberos.</span><span class="sxs-lookup"><span data-stu-id="4e213-122">Set the authentication service to Kerberos.</span></span>

    <span data-ttu-id="4e213-123">Kerberos es el único servicio de autenticación que admite el Cloaking y la delegación remotos.</span><span class="sxs-lookup"><span data-stu-id="4e213-123">Kerberos is the only authentication service that supports remote cloaking and delegation.</span></span> <span data-ttu-id="4e213-124">Esto significa que la ocultación y la delegación solo se pueden usar en servidores remotos.</span><span class="sxs-lookup"><span data-stu-id="4e213-124">This means that cloaking and delegation can only be used on remote servers.</span></span>

2.  <span data-ttu-id="4e213-125">Marque la cuenta de inicio de sesión del servidor como "de confianza para delegación" en el Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="4e213-125">Mark the server login account as "Trusted for Delegation" in the Active Directory services.</span></span>
3.  <span data-ttu-id="4e213-126">Marque la cuenta de inicio de sesión de cliente como "la cuenta es importante y no se puede delegar" en Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="4e213-126">Mark the client login account as "Account is sensitive and cannot be delegated" in Active Directory services.</span></span>

<span data-ttu-id="4e213-127">Por ejemplo, una llamada al proveedor de vistas, que puede devolver objetos de varias instancias de WMI en varios equipos, puede beneficiarse de la delegación y la ocultación.</span><span class="sxs-lookup"><span data-stu-id="4e213-127">For example, a call to the View Provider, which may return objects from multiple instances of WMI on multiple computers, can benefit from delegation and cloaking.</span></span>

 

 
