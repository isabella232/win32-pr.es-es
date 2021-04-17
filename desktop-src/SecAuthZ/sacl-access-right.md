---
description: El \_ derecho de acceso de seguridad del sistema de acceso \_ controla la capacidad de obtener o establecer la SACL en un descriptor de seguridad de objetos. El sistema concede este derecho de acceso si el \_ \_ privilegio de nombre de seguridad se habilita en el token de acceso del subproceso que lo solicita.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Derecho de acceso SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2366f30748a93294d4f30122102d656fb2590d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666661"
---
# <a name="sacl-access-right"></a><span data-ttu-id="16ae5-104">Derecho de acceso SACL</span><span class="sxs-lookup"><span data-stu-id="16ae5-104">SACL Access Right</span></span>

<span data-ttu-id="16ae5-105">El \_ derecho de acceso de seguridad del sistema de acceso \_ controla la capacidad de obtener o establecer la SACL en el [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)de un objeto.</span><span class="sxs-lookup"><span data-stu-id="16ae5-105">The ACCESS\_SYSTEM\_SECURITY access right controls the ability to get or set the SACL in an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="16ae5-106">El sistema concede este derecho de acceso solo si el \_ \_ privilegio de nombre de seguridad se habilita en el [*token de acceso*](/windows/desktop/SecGloss/a-gly) del subproceso que lo solicita.</span><span class="sxs-lookup"><span data-stu-id="16ae5-106">The system grants this access right only if the SE\_SECURITY\_NAME privilege is enabled in the [*access token*](/windows/desktop/SecGloss/a-gly) of the requesting thread.</span></span>

<span data-ttu-id="16ae5-107">**Para tener acceso a la SACL de un objeto**</span><span class="sxs-lookup"><span data-stu-id="16ae5-107">**To access an object's SACL**</span></span>

1.  <span data-ttu-id="16ae5-108">Llame a la función [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para habilitar el \_ privilegio de nombre de seguridad de se \_ .</span><span class="sxs-lookup"><span data-stu-id="16ae5-108">Call the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable the SE\_SECURITY\_NAME privilege.</span></span>
2.  <span data-ttu-id="16ae5-109">Solicite el \_ derecho de acceso de seguridad del sistema de acceso \_ cuando abra un identificador para el objeto.</span><span class="sxs-lookup"><span data-stu-id="16ae5-109">Request the ACCESS\_SYSTEM\_SECURITY access right when you open a handle to the object.</span></span>
3.  <span data-ttu-id="16ae5-110">Obtiene o establece la SACL del objeto mediante una función como [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) o [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).</span><span class="sxs-lookup"><span data-stu-id="16ae5-110">Get or set the object's SACL by using a function such as [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) or [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).</span></span>
4.  <span data-ttu-id="16ae5-111">Llame a [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para deshabilitar el privilegio de nombre de seguridad de se \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="16ae5-111">Call [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) to disable the SE\_SECURITY\_NAME privilege.</span></span>

<span data-ttu-id="16ae5-112">Para acceder a una SACL mediante las funciones [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) o [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , habilite el \_ privilegio de nombre de seguridad de se \_ .</span><span class="sxs-lookup"><span data-stu-id="16ae5-112">To access a SACL using the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) or [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) functions, enable the SE\_SECURITY\_NAME privilege.</span></span> <span data-ttu-id="16ae5-113">La función solicita internamente el derecho de acceso.</span><span class="sxs-lookup"><span data-stu-id="16ae5-113">The function internally requests the access right.</span></span>

<span data-ttu-id="16ae5-114">El \_ \_ derecho de acceso de seguridad del sistema de acceso no es válido en una DACL porque las DACL no controlan el acceso a una SACL.</span><span class="sxs-lookup"><span data-stu-id="16ae5-114">The ACCESS\_SYSTEM\_SECURITY access right is not valid in a DACL because DACLs do not control access to a SACL.</span></span> <span data-ttu-id="16ae5-115">Sin embargo, puede usar el \_ \_ derecho de acceso de seguridad del sistema de acceso en una SACL para auditar los intentos de usar el derecho de acceso.</span><span class="sxs-lookup"><span data-stu-id="16ae5-115">However, you can use the ACCESS\_SYSTEM\_SECURITY access right in a SACL to audit attempts to use the access right.</span></span>

 

 
