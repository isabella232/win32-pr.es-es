---
title: Credential Guard y aplicaciones de terceros
description: Credential Guard no permite que SSP de terceros soliciten hashes de contraseña de LSA.
ms.assetid: DA518005-C603-41CF-BBB9-2B46414653A5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a036ba5db5b86ab7c186b25e4d858b1badc60bd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487731"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a><span data-ttu-id="85ea2-103">Proveedores de compatibilidad con seguridad de terceros con Credential Guard</span><span class="sxs-lookup"><span data-stu-id="85ea2-103">Third party Security Support Providers with Credential Guard</span></span>

<span data-ttu-id="85ea2-104">Credential Guard no permite que SSP de terceros soliciten hashes de contraseña de LSA.</span><span class="sxs-lookup"><span data-stu-id="85ea2-104">Credential Guard does not allow 3rd party SSPs to ask for password hashes from LSA.</span></span> <span data-ttu-id="85ea2-105">Sin embargo, los SSP y puntos de acceso personalizados siguen recibiendo la notificación de la contraseña cuando un usuario inicia sesión o cambia su contraseña.</span><span class="sxs-lookup"><span data-stu-id="85ea2-105">However, SSPs and APs still get notified of the password when a user logs on and/or changes their password.</span></span> <span data-ttu-id="85ea2-106">No se admite el uso de API no documentadas dentro de los SSP y puntos de acceso personalizados.</span><span class="sxs-lookup"><span data-stu-id="85ea2-106">Any use of undocumented APIs within custom SSPs and APs are not supported.</span></span>

<span data-ttu-id="85ea2-107">Cuando la amplitud y profundidad de las protecciones que ofrece Credential Guard aumentan, las versiones posteriores de Windows 10 que ejecuten Credential Guard podrían influir en los escenarios que estaban funcionando en el pasado.</span><span class="sxs-lookup"><span data-stu-id="85ea2-107">As the depth and breadth of protections provided by Credential Guard are increased, subsequent releases of Windows 10 with Credential Guard running may impact scenarios that were working in the past.</span></span> <span data-ttu-id="85ea2-108">Por ejemplo, Credential Guard puede bloquear el uso de un tipo determinado de credencial o un componente determinado para evitar que el malware aproveche las vulnerabilidades.</span><span class="sxs-lookup"><span data-stu-id="85ea2-108">For example, Credential Guard may block the use of a particular type of credential or a particular component to prevent malware from taking advantage of vulnerabilities.</span></span> <span data-ttu-id="85ea2-109">Por lo tanto, te recomendamos que los escenarios necesarios para las operaciones de una organización se prueben antes de actualizar un dispositivo que con Credential Guard en ejecución.</span><span class="sxs-lookup"><span data-stu-id="85ea2-109">Therefore, we recommend that scenarios required for operations in an organization are tested before upgrading a device that has Credential Guard running.</span></span>

<span data-ttu-id="85ea2-110">Consulte [este artículo](/windows/security/identity-protection/credential-guard/credential-guard) para obtener la descripción completa y las mitigaciones recomendadas.</span><span class="sxs-lookup"><span data-stu-id="85ea2-110">Please refer to [this article](/windows/security/identity-protection/credential-guard/credential-guard) for the full description and recommended mitigations.</span></span>

 

 