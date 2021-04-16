---
description: El tipo de derechos de acceso del objeto de cuenta tiene los siguientes tipos de acceso.
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: Derechos de acceso a objetos de cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d69ba0939286564517c7293da136e88aa0367a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546222"
---
# <a name="account-object-access-rights"></a><span data-ttu-id="1339d-103">Derechos de acceso a objetos de cuenta</span><span class="sxs-lookup"><span data-stu-id="1339d-103">Account Object Access Rights</span></span>

<span data-ttu-id="1339d-104">El tipo de derechos de acceso del objeto de cuenta tiene los siguientes tipos de acceso.</span><span class="sxs-lookup"><span data-stu-id="1339d-104">The Account Object Access Rights type has the following access types.</span></span>



| <span data-ttu-id="1339d-105">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="1339d-105">Access type</span></span>                     | <span data-ttu-id="1339d-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="1339d-106">Description</span></span>                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1339d-107">vista de cuentas \_</span><span class="sxs-lookup"><span data-stu-id="1339d-107">ACCOUNT\_VIEW</span></span>                   | <span data-ttu-id="1339d-108">Este tipo de acceso es necesario para leer la información de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="1339d-108">This access type is required to read the account information.</span></span> <span data-ttu-id="1339d-109">Esto incluye los [*privilegios*](/windows/desktop/SecGloss/p-gly) asignados a la cuenta, las cuotas de memoria asignadas y los tipos de acceso especiales que se conceden.</span><span class="sxs-lookup"><span data-stu-id="1339d-109">This includes the [*privileges*](/windows/desktop/SecGloss/p-gly) assigned to the account, memory quotas assigned, and any special access types granted.</span></span> |
| <span data-ttu-id="1339d-110">\_privilegios de ajuste de cuenta \_</span><span class="sxs-lookup"><span data-stu-id="1339d-110">ACCOUNT\_ADJUST\_PRIVILEGES</span></span>     | <span data-ttu-id="1339d-111">Este tipo de acceso es necesario para asignar o quitar privilegios de una cuenta.</span><span class="sxs-lookup"><span data-stu-id="1339d-111">This access type is required to assign privileges to or remove privileges from an account.</span></span>                                                                                                                                                            |
| <span data-ttu-id="1339d-112">\_cuotas de ajuste de cuenta \_</span><span class="sxs-lookup"><span data-stu-id="1339d-112">ACCOUNT\_ADJUST\_QUOTAS</span></span>         | <span data-ttu-id="1339d-113">Este tipo de acceso es necesario para cambiar las cuotas del sistema asignadas a una cuenta.</span><span class="sxs-lookup"><span data-stu-id="1339d-113">This access type is required to change the system quotas assigned to an account.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="1339d-114">\_ajustar cuenta \_ \_ acceso al sistema</span><span class="sxs-lookup"><span data-stu-id="1339d-114">ACCOUNT\_ADJUST\_SYSTEM\_ACCESS</span></span> | <span data-ttu-id="1339d-115">Este tipo de acceso es necesario para actualizar las marcas de acceso del sistema de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="1339d-115">This access type is required to update the system access flags for the account.</span></span>                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a><span data-ttu-id="1339d-116">Máscaras de acceso genéricas</span><span class="sxs-lookup"><span data-stu-id="1339d-116">Generic Access Masks</span></span>

<span data-ttu-id="1339d-117">El objeto [**account**](account-object.md) publica las siguientes asignaciones de tipos de acceso genéricos en tipos de acceso específicos.</span><span class="sxs-lookup"><span data-stu-id="1339d-117">The [**Account**](account-object.md) object publishes the following mappings from generic access types to specific access types.</span></span>

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                        ACCOUNT_VIEW 
            
    GENERIC_WRITE       STANDARD_RIGHTS_WRITE |
                        ACCOUNT_ADJUST_PRIVILEGES |
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS

    GENERIC_EXECUTE        STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a><span data-ttu-id="1339d-118">Tipos de acceso estándar</span><span class="sxs-lookup"><span data-stu-id="1339d-118">Standard Access Types</span></span>

<span data-ttu-id="1339d-119">Este objeto no admite el tipo de acceso estándar SINCRONIZAr (opcional).</span><span class="sxs-lookup"><span data-stu-id="1339d-119">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="1339d-120">Se admiten todos los tipos de acceso necesarios.</span><span class="sxs-lookup"><span data-stu-id="1339d-120">All required access types are supported.</span></span> <span data-ttu-id="1339d-121">La máscara de todos los tipos de acceso admitidos para este tipo de objeto es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="1339d-121">The mask of all supported access types for this object type is as follows.</span></span>

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
