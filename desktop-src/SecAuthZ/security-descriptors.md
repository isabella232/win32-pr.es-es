---
description: Un descriptor de seguridad contiene la información de seguridad asociada a un objeto protegible.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Descriptor de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f864505f135b46d3e16a4e369c019444918fb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908169"
---
# <a name="security-descriptors"></a><span data-ttu-id="ad0de-103">Descriptor de seguridad</span><span class="sxs-lookup"><span data-stu-id="ad0de-103">Security Descriptors</span></span>

<span data-ttu-id="ad0de-104">Un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) contiene la información de seguridad asociada a un [objeto protegible](securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ad0de-104">A [*security descriptor*](/windows/desktop/SecGloss/s-gly) contains the security information associated with a [securable object](securable-objects.md).</span></span> <span data-ttu-id="ad0de-105">Un descriptor de seguridad está formado por una estructura de [**\_ descriptores de seguridad**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) y su información de seguridad asociada.</span><span class="sxs-lookup"><span data-stu-id="ad0de-105">A security descriptor consists of a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) structure and its associated security information.</span></span> <span data-ttu-id="ad0de-106">Un descriptor de seguridad puede incluir la siguiente información de seguridad:</span><span class="sxs-lookup"><span data-stu-id="ad0de-106">A security descriptor can include the following security information:</span></span>

-   <span data-ttu-id="ad0de-107">[Identificadores de seguridad](security-identifiers.md) (SID) para el propietario y el grupo primario de un objeto.</span><span class="sxs-lookup"><span data-stu-id="ad0de-107">[Security identifiers](security-identifiers.md) (SIDs) for the owner and primary group of an object.</span></span>
-   <span data-ttu-id="ad0de-108">[DACL](access-control-lists.md) que especifica los derechos de acceso permitidos o denegados a usuarios o grupos determinados.</span><span class="sxs-lookup"><span data-stu-id="ad0de-108">A [DACL](access-control-lists.md) that specifies the access rights allowed or denied to particular users or groups.</span></span>
-   <span data-ttu-id="ad0de-109">[SACL](access-control-lists.md) que especifica los tipos de intentos de acceso que generan registros de auditoría para el objeto.</span><span class="sxs-lookup"><span data-stu-id="ad0de-109">A [SACL](access-control-lists.md) that specifies the types of access attempts that generate audit records for the object.</span></span>
-   <span data-ttu-id="ad0de-110">Conjunto de bits de control que califican el significado de un descriptor de seguridad o sus miembros individuales.</span><span class="sxs-lookup"><span data-stu-id="ad0de-110">A set of control bits that qualify the meaning of a security descriptor or its individual members.</span></span>

<span data-ttu-id="ad0de-111">Las aplicaciones no deben manipular directamente el contenido de un descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ad0de-111">Applications must not directly manipulate the contents of a security descriptor.</span></span> <span data-ttu-id="ad0de-112">La API de Windows proporciona funciones para establecer y recuperar la información de seguridad en el descriptor de seguridad de un objeto.</span><span class="sxs-lookup"><span data-stu-id="ad0de-112">The Windows API provides functions for setting and retrieving the security information in an object's security descriptor.</span></span> <span data-ttu-id="ad0de-113">Además, hay funciones para crear e inicializar un descriptor de seguridad para un nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="ad0de-113">In addition, there are functions for creating and initializing a security descriptor for a new object.</span></span>

<span data-ttu-id="ad0de-114">Las aplicaciones que trabajan con descriptores de seguridad en Active Directory objetos pueden utilizar las funciones de seguridad de Windows o las interfaces de seguridad proporcionadas por las interfaces de servicio Active Directory (ADSI).</span><span class="sxs-lookup"><span data-stu-id="ad0de-114">Applications working with security descriptors on Active Directory objects can use the Windows security functions or the security interfaces provided by the Active Directory Service Interfaces (ADSI).</span></span> <span data-ttu-id="ad0de-115">Para obtener más información acerca de las interfaces de seguridad ADSI, vea [Cómo funciona Access Control en Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="ad0de-115">For more information about ADSI security interfaces, see [How Access Control Works in Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).</span></span>

 

 
