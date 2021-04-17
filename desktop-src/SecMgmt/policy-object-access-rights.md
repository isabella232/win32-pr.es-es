---
description: Enumera y describe los tipos de acceso del objeto de directiva.
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: Derechos de acceso a objetos de Directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5c762955a4c53015241086b2249c5edbc4f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666398"
---
# <a name="policy-object-access-rights"></a><span data-ttu-id="5ef82-103">Derechos de acceso a objetos de Directiva</span><span class="sxs-lookup"><span data-stu-id="5ef82-103">Policy Object Access Rights</span></span>

<span data-ttu-id="5ef82-104">El objeto de [**Directiva**](policy-object.md) tiene los siguientes tipos de acceso específicos del objeto:</span><span class="sxs-lookup"><span data-stu-id="5ef82-104">The [**Policy**](policy-object.md) object has the following object-specific access types:</span></span>



| <span data-ttu-id="5ef82-105">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="5ef82-105">Access type</span></span>                         | <span data-ttu-id="5ef82-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ef82-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef82-107">\_ \_ información local de la vista de directiva \_</span><span class="sxs-lookup"><span data-stu-id="5ef82-107">POLICY\_VIEW\_LOCAL\_INFORMATION</span></span>    | <span data-ttu-id="5ef82-108">Este tipo de acceso es necesario para leer la información de la Directiva de seguridad diversa del sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="5ef82-108">This access type is needed to read the target system's miscellaneous security policy information.</span></span> <span data-ttu-id="5ef82-109">Esto incluye la cuota predeterminada, la auditoría, el estado del servidor y la información de rol, y la información de confianza.</span><span class="sxs-lookup"><span data-stu-id="5ef82-109">This includes the default quota, auditing, server state and role information, and trust information.</span></span> <span data-ttu-id="5ef82-110">Este tipo de acceso también es necesario para enumerar los dominios, las cuentas y los [*privilegios*](/windows/desktop/SecGloss/p-gly)de confianza.</span><span class="sxs-lookup"><span data-stu-id="5ef82-110">This access type is also needed to enumerate trusted domains, accounts, and [*privileges*](/windows/desktop/SecGloss/p-gly).</span></span> |
| <span data-ttu-id="5ef82-111">DIRECTIVA \_ obtener \_ \_ información privada</span><span class="sxs-lookup"><span data-stu-id="5ef82-111">POLICY\_GET\_PRIVATE\_INFORMATION</span></span>   | <span data-ttu-id="5ef82-112">Este tipo de acceso es necesario para ver información confidencial, como los nombres de las cuentas establecidas para las relaciones de dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="5ef82-112">This access type is needed to view sensitive information, such as the names of accounts established for trusted domain relationships.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="5ef82-113">\_Administrador de confianza de directiva \_</span><span class="sxs-lookup"><span data-stu-id="5ef82-113">POLICY\_TRUST\_ADMIN</span></span>                | <span data-ttu-id="5ef82-114">Este tipo de acceso es necesario para cambiar la información del dominio de la cuenta o del dominio principal.</span><span class="sxs-lookup"><span data-stu-id="5ef82-114">This access type is needed to change the account domain or primary domain information.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="5ef82-115">\_límites de \_ cuota predeterminados de directiva establecida \_ \_</span><span class="sxs-lookup"><span data-stu-id="5ef82-115">POLICY\_SET\_DEFAULT\_QUOTA\_LIMITS</span></span> | <span data-ttu-id="5ef82-116">Establezca las cuotas del sistema predeterminadas que se aplican a las cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="5ef82-116">Set the default system quotas that are applied to user accounts.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="5ef82-117">\_secreto de creación de directiva \_</span><span class="sxs-lookup"><span data-stu-id="5ef82-117">POLICY\_CREATE\_SECRET</span></span>              | <span data-ttu-id="5ef82-118">Este tipo de acceso es necesario para crear un nuevo objeto de datos privado.</span><span class="sxs-lookup"><span data-stu-id="5ef82-118">This access type is needed to create a new Private Data object.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="5ef82-119">creación de una cuenta de directiva \_ \_</span><span class="sxs-lookup"><span data-stu-id="5ef82-119">POLICY\_CREATE\_ACCOUNT</span></span>             | <span data-ttu-id="5ef82-120">Este tipo de acceso es necesario para crear un nuevo objeto de [**cuenta**](account-object.md) .</span><span class="sxs-lookup"><span data-stu-id="5ef82-120">This access type is needed to create a new [**Account**](account-object.md) object.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="5ef82-121">\_requisitos de \_ Auditoría de conjunto de directivas \_</span><span class="sxs-lookup"><span data-stu-id="5ef82-121">POLICY\_SET\_AUDIT\_REQUIREMENTS</span></span>    | <span data-ttu-id="5ef82-122">Este tipo de acceso es necesario para actualizar los requisitos de auditoría del sistema.</span><span class="sxs-lookup"><span data-stu-id="5ef82-122">This access type is needed to update the auditing requirements of the system.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="5ef82-123">\_Administrador de \_ registro de auditoría de directiva \_</span><span class="sxs-lookup"><span data-stu-id="5ef82-123">POLICY\_AUDIT\_LOG\_ADMIN</span></span>           | <span data-ttu-id="5ef82-124">Este tipo de acceso es necesario para cambiar las características de la traza de auditoría, como su tamaño máximo o el período de retención de los registros de auditoría, o para borrar el registro.</span><span class="sxs-lookup"><span data-stu-id="5ef82-124">This access type is needed to change the characteristics of the audit trail such as its maximum size or the retention period for audit records, or to clear the log.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="5ef82-125">\_información de \_ Auditoría de vista de directiva \_</span><span class="sxs-lookup"><span data-stu-id="5ef82-125">POLICY\_VIEW\_AUDIT\_INFORMATION</span></span>    | <span data-ttu-id="5ef82-126">Este tipo de acceso es necesario para ver la información de los requisitos de auditoría o la pista de auditoría.</span><span class="sxs-lookup"><span data-stu-id="5ef82-126">This access type is needed to view audit trail or audit requirements information.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5ef82-127">\_Administrador del servidor de directivas \_</span><span class="sxs-lookup"><span data-stu-id="5ef82-127">POLICY\_SERVER\_ADMIN</span></span>               | <span data-ttu-id="5ef82-128">Este tipo de acceso es necesario para modificar el estado del servidor o la información del rol (maestro o réplica).</span><span class="sxs-lookup"><span data-stu-id="5ef82-128">This access type is needed to modify the server state or role (master/replica) information.</span></span> <span data-ttu-id="5ef82-129">También es necesario cambiar la información del origen de la réplica y del nombre de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="5ef82-129">It is also needed to change the replica source and account name information.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="5ef82-130">\_nombres de búsqueda de directivas \_</span><span class="sxs-lookup"><span data-stu-id="5ef82-130">POLICY\_LOOKUP\_NAMES</span></span>               | <span data-ttu-id="5ef82-131">Este tipo de acceso es necesario para traducir entre nombres y SID.</span><span class="sxs-lookup"><span data-stu-id="5ef82-131">This access type is needed to translate between names and SIDs.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="5ef82-132">\_privilegio de creación de directiva \_</span><span class="sxs-lookup"><span data-stu-id="5ef82-132">POLICY\_CREATE\_PRIVILEGE</span></span>           | <span data-ttu-id="5ef82-133">Todavía no se admite.</span><span class="sxs-lookup"><span data-stu-id="5ef82-133">Not yet supported.</span></span>                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a><span data-ttu-id="5ef82-134">Máscaras de acceso genéricas</span><span class="sxs-lookup"><span data-stu-id="5ef82-134">Generic Access Masks</span></span>

<span data-ttu-id="5ef82-135">El objeto de [**Directiva**](policy-object.md) publica las siguientes asignaciones de tipos de acceso genéricos en tipos de acceso específicos:</span><span class="sxs-lookup"><span data-stu-id="5ef82-135">The [**Policy**](policy-object.md) object publishes the following mappings from generic access types to specific access types:</span></span>

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                                        POLICY_SERVER_ADMIN

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_LOOKUP_NAMES
```

## <a name="standard-access-types"></a><span data-ttu-id="5ef82-136">Tipos de acceso estándar</span><span class="sxs-lookup"><span data-stu-id="5ef82-136">Standard Access Types</span></span>

<span data-ttu-id="5ef82-137">Este objeto no admite el tipo de acceso estándar SINCRONIZAr (opcional).</span><span class="sxs-lookup"><span data-stu-id="5ef82-137">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="5ef82-138">Se admiten todos los tipos de acceso necesarios.</span><span class="sxs-lookup"><span data-stu-id="5ef82-138">All required access types are supported.</span></span> <span data-ttu-id="5ef82-139">La máscara de todos los tipos de acceso admitidos para este tipo de objeto es:</span><span class="sxs-lookup"><span data-stu-id="5ef82-139">The mask of all supported access types for this object type is:</span></span>

``` syntax
    POLICY_ALL_ACCESS STANDARD_RIGHTS_REQUIRED |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                    POLICY_SERVER_ADMIN
                    POLICY_LOOKUP_NAMES
```

 

 
