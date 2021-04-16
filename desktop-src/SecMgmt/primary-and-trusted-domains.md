---
description: En los siguientes términos se describen los dominios que existen en los sistemas remotos.
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: Dominios principales y de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d69a8bf5f5a8363f8de726c6183fd4de820665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540982"
---
# <a name="primary-and-trusted-domains"></a><span data-ttu-id="f8d4a-103">Dominios principales y de confianza</span><span class="sxs-lookup"><span data-stu-id="f8d4a-103">Primary and Trusted Domains</span></span>

<span data-ttu-id="f8d4a-104">En los siguientes términos se describen los dominios que existen en los sistemas remotos.</span><span class="sxs-lookup"><span data-stu-id="f8d4a-104">The following terms describe domains that exist on remote systems.</span></span>

-   [<span data-ttu-id="f8d4a-105">Dominio principal</span><span class="sxs-lookup"><span data-stu-id="f8d4a-105">Primary Domain</span></span>](#primary-domain)
-   [<span data-ttu-id="f8d4a-106">Dominio de confianza</span><span class="sxs-lookup"><span data-stu-id="f8d4a-106">Trusted Domain</span></span>](#primary-and-trusted-domains)

## <a name="primary-domain"></a><span data-ttu-id="f8d4a-107">Dominio principal</span><span class="sxs-lookup"><span data-stu-id="f8d4a-107">Primary Domain</span></span>

<span data-ttu-id="f8d4a-108">Un dominio principal es el dominio responsable del establecimiento de relaciones de confianza adicionales y la realización de la autenticación (o para pasar una solicitud de autenticación a un dominio de confianza adecuado).</span><span class="sxs-lookup"><span data-stu-id="f8d4a-108">A primary domain is the domain that is responsible for establishing further trust relationships and performing authentication (or for passing an authentication request on to an appropriate trusted domain).</span></span> <span data-ttu-id="f8d4a-109">Los controladores de dominio del controlador de dominio principal o pasan las solicitudes de autenticación que se originan en la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f8d4a-109">The domain controllers in the primary domain handle or pass along authentication requests that originate at the workstation.</span></span>

<span data-ttu-id="f8d4a-110">Cuando se produce el inicio de sesión, LSA comprueba la información de autenticación de los dominios integrados y de cuenta.</span><span class="sxs-lookup"><span data-stu-id="f8d4a-110">When logon occurs, the LSA checks the built-in and account domains for authentication information.</span></span> <span data-ttu-id="f8d4a-111">Si la cuenta en la que se inicia sesión no se encuentra en ninguno de estos dominios, la solicitud de inicio de sesión se entrega en el dominio principal del sistema.</span><span class="sxs-lookup"><span data-stu-id="f8d4a-111">If the account being logged on to is not in either of these domains, the logon request is handed off to the system's primary domain.</span></span>

## <a name="trusted-domain"></a><span data-ttu-id="f8d4a-112">Dominio de confianza</span><span class="sxs-lookup"><span data-stu-id="f8d4a-112">Trusted Domain</span></span>

<span data-ttu-id="f8d4a-113">Un dominio de confianza es un dominio en el que confía el sistema local para autenticar a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="f8d4a-113">A trusted domain is a domain that the local system trusts to authenticate users.</span></span> <span data-ttu-id="f8d4a-114">En otras palabras, si un dominio de confianza autentica a un usuario o una aplicación, esta autenticación la aceptan todos los dominios que confían en el dominio de autenticación.</span><span class="sxs-lookup"><span data-stu-id="f8d4a-114">In other words, if a user or application is authenticated by a trusted domain, this authentication is accepted by all domains that trust the authenticating domain.</span></span>

<span data-ttu-id="f8d4a-115">Cada dominio subordinado tiene automáticamente una relación de confianza bidireccional con el dominio principal.</span><span class="sxs-lookup"><span data-stu-id="f8d4a-115">Each subordinate domain automatically has a two-way trust relationship with the main domain.</span></span> <span data-ttu-id="f8d4a-116">De forma predeterminada, esta confianza es transitiva, lo que significa que si un sistema confía en el dominio A, también confía en todos los dominios en los que confía el dominio A.</span><span class="sxs-lookup"><span data-stu-id="f8d4a-116">By default, this trust is transitive, meaning that if a system trusts Domain A, it also trusts all domains that Domain A trusts.</span></span> <span data-ttu-id="f8d4a-117">Las confianzas unidireccionales también se admiten en sistemas operativos anteriores a Windows 2000, que no admiten confianzas transitivas bidireccionales.</span><span class="sxs-lookup"><span data-stu-id="f8d4a-117">One-way trusts are also supported for operating systems earlier than Windows 2000, which do not support transitive, two-way trusts.</span></span>

<span data-ttu-id="f8d4a-118">La [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) tiene un tipo de objeto, [**TrustedDomain**](the-trusteddomain-object-type.md), que se usa para almacenar información sobre las relaciones de confianza, incluido el nombre y el [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) del dominio de confianza, la cuenta del dominio que se utilizará para las solicitudes de autenticación, las solicitudes de traducción de nombres y SID y los nombres de los controladores de dominio del dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="f8d4a-118">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) has an object type, [**TrustedDomain**](the-trusteddomain-object-type.md), that is used to store information about trust relationships, including the name and [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the trusted domain, the account in the domain to use for authentication requests, name and SID translation requests, and the names of domain controllers in the trusted domain.</span></span>

<span data-ttu-id="f8d4a-119">En los controladores de dominio, el LSA crea una instancia de un objeto [**TrustedDomain**](the-trusteddomain-object-type.md) para cada dominio de confianza del sistema local.</span><span class="sxs-lookup"><span data-stu-id="f8d4a-119">On domain controllers, the LSA creates an instance of a [**TrustedDomain**](the-trusteddomain-object-type.md) object for each domain trusted by the local system.</span></span>

<span data-ttu-id="f8d4a-120">Por ejemplo, si una estación de trabajo de Windows XP confía en un controlador de dominio de Windows 2000 que, a su vez, confía en otros cuatro sistemas, la estación de trabajo, conectada mediante confianza transitiva, tendrá cinco objetos [**TrustedDomain**](the-trusteddomain-object-type.md) en su sistema local.</span><span class="sxs-lookup"><span data-stu-id="f8d4a-120">For example, if a Windows XP workstation trusts a Windows 2000 domain controller that in turn trusts four other systems, the workstation, connected using transitive trust, will have five [**TrustedDomain**](the-trusteddomain-object-type.md) objects on its local system.</span></span>

 

 
