---
description: Enumera las enumeraciones usadas por las funciones de administración de directivas de LSA.
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: Enumeraciones de administración de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bec2cdd731e2a3befe75e543f692d93bc5d9ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276999"
---
# <a name="security-management-enumerations"></a><span data-ttu-id="ca130-103">Enumeraciones de administración de seguridad</span><span class="sxs-lookup"><span data-stu-id="ca130-103">Security Management Enumerations</span></span>

<span data-ttu-id="ca130-104">Las enumeraciones de administración de seguridad son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="ca130-104">The security management enumerations include the following:</span></span>

-   [<span data-ttu-id="ca130-105">Enumeraciones de directivas de LSA</span><span class="sxs-lookup"><span data-stu-id="ca130-105">LSA Policy Enumerations</span></span>](#lsa-policy-enumerations)
-   [<span data-ttu-id="ca130-106">Enumeraciones más seguras</span><span class="sxs-lookup"><span data-stu-id="ca130-106">Safer Enumerations</span></span>](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a><span data-ttu-id="ca130-107">Enumeraciones de directivas de LSA</span><span class="sxs-lookup"><span data-stu-id="ca130-107">LSA Policy Enumerations</span></span>

<span data-ttu-id="ca130-108">Las funciones de administración de directivas de LSA usan los siguientes tipos de enumeración.</span><span class="sxs-lookup"><span data-stu-id="ca130-108">The following enumeration types are used by the LSA policy management functions.</span></span>



| <span data-ttu-id="ca130-109">Enumeración</span><span class="sxs-lookup"><span data-stu-id="ca130-109">Enumeration</span></span>                                                                               | <span data-ttu-id="ca130-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca130-110">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca130-111">**\_tipo de \_ evento de auditoría de directiva \_**</span><span class="sxs-lookup"><span data-stu-id="ca130-111">**POLICY\_AUDIT\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | <span data-ttu-id="ca130-112">Define los tipos de eventos que el sistema puede auditar.</span><span class="sxs-lookup"><span data-stu-id="ca130-112">Defines the types of events the system can audit.</span></span>                                                                                     |
| [<span data-ttu-id="ca130-113">**\_clase de información de directiva \_**</span><span class="sxs-lookup"><span data-stu-id="ca130-113">**POLICY\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | <span data-ttu-id="ca130-114">Define los tipos de información que se pueden establecer o consultar para un objeto de [**Directiva**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="ca130-114">Defines the types of information that can be set or queried for a [**Policy**](policy-object.md) object.</span></span>                             |
| [<span data-ttu-id="ca130-115">**DIRECTIVA \_ LSA \_ ( \_ rol de servidor)**</span><span class="sxs-lookup"><span data-stu-id="ca130-115">**POLICY\_LSA\_SERVER\_ROLE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | <span data-ttu-id="ca130-116">Indicar el rol de un servidor LSA.</span><span class="sxs-lookup"><span data-stu-id="ca130-116">Indicate the role of an LSA server.</span></span>                                                                                                   |
| [<span data-ttu-id="ca130-117">**\_clase de \_ información de notificación de directiva \_**</span><span class="sxs-lookup"><span data-stu-id="ca130-117">**POLICY\_NOTIFICATION\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | <span data-ttu-id="ca130-118">Define los tipos de información de directivas e información de dominio de directivas para los que la aplicación puede solicitar notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="ca130-118">Defines the types of policy information and policy domain information for which your application can request notification of changes.</span></span> |
| [<span data-ttu-id="ca130-119">**\_Estado de \_ habilitación del servidor de directivas \_**</span><span class="sxs-lookup"><span data-stu-id="ca130-119">**POLICY\_SERVER\_ENABLE\_STATE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | <span data-ttu-id="ca130-120">Representa el estado del servidor LSA, es decir, si está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="ca130-120">Represents the state of the LSA server, that is, whether it is enabled or disabled.</span></span>                                                   |
| [<span data-ttu-id="ca130-121">**\_clase de información de confianza \_**</span><span class="sxs-lookup"><span data-stu-id="ca130-121">**TRUSTED\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | <span data-ttu-id="ca130-122">Define los tipos de información que se pueden establecer o consultar para un dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="ca130-122">Defines the types of information that can be set or queried for a trusted domain.</span></span>                                                     |



 

## <a name="safer-enumerations"></a><span data-ttu-id="ca130-123">Enumeraciones más seguras</span><span class="sxs-lookup"><span data-stu-id="ca130-123">Safer Enumerations</span></span>

<span data-ttu-id="ca130-124">[Safe](safer.md) usa los siguientes tipos enumerados.</span><span class="sxs-lookup"><span data-stu-id="ca130-124">[Safer](safer.md) uses the following enumerated types.</span></span>



| <span data-ttu-id="ca130-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="ca130-125">Name</span></span>                                                               | <span data-ttu-id="ca130-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca130-126">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca130-127">**\_tipos de identificación más seguros \_**</span><span class="sxs-lookup"><span data-stu-id="ca130-127">**SAFER\_IDENTIFICATION\_TYPES**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | <span data-ttu-id="ca130-128">Tipo de enumeración que define los tipos posibles de estructuras de reglas de identificación que se pueden identificar mediante la estructura de [**\_ \_ encabezado de identificación más segura**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) .</span><span class="sxs-lookup"><span data-stu-id="ca130-128">Enumeration type that defines the possible types of identification rule structures that can be identified by the [**SAFER\_IDENTIFICATION\_HEADER**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) structure.</span></span> |
| [<span data-ttu-id="ca130-129">**\_clase de \_ información de objeto más segura \_**</span><span class="sxs-lookup"><span data-stu-id="ca130-129">**SAFER\_OBJECT\_INFO\_CLASS**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | <span data-ttu-id="ca130-130">Tipo de enumeración que define el tipo de información solicitada sobre un objeto más seguro.</span><span class="sxs-lookup"><span data-stu-id="ca130-130">Enumeration type that defines the type of information requested about a Safer object.</span></span>                                                                                                            |
| [<span data-ttu-id="ca130-131">**\_clase de \_ información de directiva más segura \_**</span><span class="sxs-lookup"><span data-stu-id="ca130-131">**SAFER\_POLICY\_INFO\_CLASS**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | <span data-ttu-id="ca130-132">Tipo de enumeración que define las maneras en las que se puede consultar una directiva.</span><span class="sxs-lookup"><span data-stu-id="ca130-132">Enumeration type that defines the ways in which a policy may be queried.</span></span>                                                                                                                         |



 

 

 



