---
description: La Directiva de vales de Kerberos se define en el nivel de dominio y se implementa mediante el Centro de distribución de claves del dominio (KDC).
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Directiva Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4559353e65a25a380c0c2aa4bb7e5d56f7681af1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652727"
---
# <a name="kerberos-policy"></a><span data-ttu-id="f639e-103">Directiva Kerberos</span><span class="sxs-lookup"><span data-stu-id="f639e-103">Kerberos Policy</span></span>

<span data-ttu-id="f639e-104">La Directiva de vales de Kerberos se define en el nivel de dominio y se implementa mediante el [*centro de distribución de claves*](../secgloss/k-gly.md) del dominio (KDC).</span><span class="sxs-lookup"><span data-stu-id="f639e-104">Kerberos ticket policy is defined at the domain level and implemented by the domain's [*Key Distribution Center*](../secgloss/k-gly.md) (KDC).</span></span> <span data-ttu-id="f639e-105">La Directiva de Kerberos se almacena en el Active Directory como un subconjunto de los atributos de la Directiva de seguridad de dominio.</span><span class="sxs-lookup"><span data-stu-id="f639e-105">Kerberos policy is stored in the Active Directory as a subset of the attributes of domain security policy.</span></span> <span data-ttu-id="f639e-106">De forma predeterminada, solo los miembros del grupo administradores de dominio pueden establecer las opciones de directiva.</span><span class="sxs-lookup"><span data-stu-id="f639e-106">By default, policy options can be set only by members of the Domain Administrators group.</span></span> <span data-ttu-id="f639e-107">La Directiva de dominio incluye opciones que:</span><span class="sxs-lookup"><span data-stu-id="f639e-107">Domain policy includes options that:</span></span>

-   <span data-ttu-id="f639e-108">Admitir vales postfechados</span><span class="sxs-lookup"><span data-stu-id="f639e-108">Support postdated tickets</span></span>
-   <span data-ttu-id="f639e-109">Delegación restringida de compatibilidad (solo Windows Server 2003)</span><span class="sxs-lookup"><span data-stu-id="f639e-109">Support constrained delegation (Windows Server 2003 only)</span></span>
-   <span data-ttu-id="f639e-110">Vales de soporte técnico que se pueden reenviar</span><span class="sxs-lookup"><span data-stu-id="f639e-110">Support tickets that can be forwarded</span></span>
-   <span data-ttu-id="f639e-111">Compatibilidad con vales renovables</span><span class="sxs-lookup"><span data-stu-id="f639e-111">Support renewable tickets</span></span>
-   <span data-ttu-id="f639e-112">Establecer la antigüedad máxima del vale</span><span class="sxs-lookup"><span data-stu-id="f639e-112">Set maximum ticket age</span></span>
-   <span data-ttu-id="f639e-113">Establecer antigüedad máxima de renovación</span><span class="sxs-lookup"><span data-stu-id="f639e-113">Set maximum renewal age</span></span>
-   <span data-ttu-id="f639e-114">Establecer la antigüedad máxima del vale de proxy</span><span class="sxs-lookup"><span data-stu-id="f639e-114">Set maximum proxy ticket age</span></span>
-   <span data-ttu-id="f639e-115">Cerrar la sesión de los usuarios cuando expiren los vales</span><span class="sxs-lookup"><span data-stu-id="f639e-115">Forcibly log off users when tickets expire</span></span>

<span data-ttu-id="f639e-116">Con la [*delegación restringida*](../secgloss/c-gly.md), un equipo puede establecerse para permitir el reenvío de credenciales únicamente a una lista específica de servicios.</span><span class="sxs-lookup"><span data-stu-id="f639e-116">With [*constrained delegation*](../secgloss/c-gly.md), a computer can be set to allow forwarding of credentials only to a specific list of services.</span></span> <span data-ttu-id="f639e-117">Estos servicios deben residir en el mismo dominio que el equipo que reenvía las credenciales.</span><span class="sxs-lookup"><span data-stu-id="f639e-117">Those services must reside in the same domain as the computer forwarding the credentials.</span></span> <span data-ttu-id="f639e-118">En *delegación restringida*, los vales ya no se envían desde el cliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="f639e-118">Under *constrained delegation*, tickets are no longer sent from the client to the server.</span></span> <span data-ttu-id="f639e-119">El equipo servidor crea vales de servicio para reenviar según sea necesario a partir de la información usada para autenticar el cliente.</span><span class="sxs-lookup"><span data-stu-id="f639e-119">The server computer creates service tickets to forward as necessary from information used to authenticate the client.</span></span>

<span data-ttu-id="f639e-120">Aunque la Directiva de Kerberos para un dominio puede permitir la autenticación delegada al permitir que se reenvíen vales, ese aspecto de la Directiva no necesita aplicarse a todos los usuarios o a todos los equipos.</span><span class="sxs-lookup"><span data-stu-id="f639e-120">Although Kerberos policy for a domain may permit delegated authentication by allowing tickets to be forwarded, that aspect of policy need not apply to all users or all computers.</span></span> <span data-ttu-id="f639e-121">Un atributo de una cuenta de usuario individual se puede establecer para deshabilitar el reenvío de [*las credenciales*](../secgloss/c-gly.md) de ese usuario en cualquier servidor.</span><span class="sxs-lookup"><span data-stu-id="f639e-121">An attribute of an individual user account can be set to disable forwarding of that user's [*credentials*](../secgloss/c-gly.md) by any server.</span></span> <span data-ttu-id="f639e-122">Se puede establecer un atributo de la cuenta de un equipo individual para deshabilitar el reenvío de credenciales de cualquier usuario.</span><span class="sxs-lookup"><span data-stu-id="f639e-122">An attribute of an individual computer's account can be set to disable forwarding of credentials from any user.</span></span> <span data-ttu-id="f639e-123">En ambos casos, la delegación se puede deshabilitar mediante la creación de una directiva de grupo para aplicarla a todos los usuarios o a todos los equipos de una unidad organizativa de la Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f639e-123">In both cases, delegation can be disabled by creating a group policy to apply to all users or all computers in an organizational unit of the Active Directory.</span></span>

<span data-ttu-id="f639e-124">**Windows XP/2000:** No se admite la delegación restringida.</span><span class="sxs-lookup"><span data-stu-id="f639e-124">**Windows XP/2000:** Constrained delegation is not supported.</span></span>

 

 
