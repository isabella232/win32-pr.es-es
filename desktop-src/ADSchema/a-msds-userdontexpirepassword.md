---
title: atributo de contraseña MS-DS-usuario-no-expiren
description: Indica si la contraseña de la cuenta a la que hacen referencia este atributo expirará.
ms.assetid: bafbcb4a-ee45-4f88-8fb2-93840efd1289
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de contraseña MS-DS-usuario-no-expiren
- Esquema de AD de atributo msDS-UserDontExpirePassword
topic_type:
- apiref
api_name:
- ms-DS-User-Dont-Expire-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d5c0fa709f549a523d628433ee2b3aa626278e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151648"
---
# <a name="ms-ds-user-dont-expire-password-attribute"></a><span data-ttu-id="e7065-105">atributo de contraseña MS-DS-usuario-no-expiren</span><span class="sxs-lookup"><span data-stu-id="e7065-105">ms-DS-User-Dont-Expire-Password attribute</span></span>

<span data-ttu-id="e7065-106">Indica si la contraseña de la cuenta a la que hacen referencia este atributo expirará.</span><span class="sxs-lookup"><span data-stu-id="e7065-106">Indicates whether the password for the account this attribute references will expire.</span></span> <span data-ttu-id="e7065-107">True si la contraseña no va a expirar; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="e7065-107">True if the password will not expire; otherwise, False.</span></span>



| <span data-ttu-id="e7065-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="e7065-108">Entry</span></span> | <span data-ttu-id="e7065-109">Value</span><span class="sxs-lookup"><span data-stu-id="e7065-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e7065-110">CN</span><span class="sxs-lookup"><span data-stu-id="e7065-110">CN</span></span>                | <span data-ttu-id="e7065-111">MS-DS-usuario-no-expire-contraseña</span><span class="sxs-lookup"><span data-stu-id="e7065-111">ms-DS-User-Dont-Expire-Password</span></span>      |
| <span data-ttu-id="e7065-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e7065-112">Ldap-Display-Name</span></span> | <span data-ttu-id="e7065-113">msDS-UserDontExpirePassword</span><span class="sxs-lookup"><span data-stu-id="e7065-113">msDS-UserDontExpirePassword</span></span>          |
| <span data-ttu-id="e7065-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e7065-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="e7065-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e7065-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e7065-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e7065-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e7065-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e7065-117">Attribute-Id</span></span>      | <span data-ttu-id="e7065-118">1.2.840.113556.1.4.1855</span><span class="sxs-lookup"><span data-stu-id="e7065-118">1.2.840.113556.1.4.1855</span></span>              |
| <span data-ttu-id="e7065-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e7065-119">System-Id-Guid</span></span>    | <span data-ttu-id="e7065-120">8788193a-2925-43d9-a221-bb7fff397675</span><span class="sxs-lookup"><span data-stu-id="e7065-120">8788193a-2925-43d9-a221-bb7fff397675</span></span> |
| <span data-ttu-id="e7065-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7065-121">Syntax</span></span>            | [<span data-ttu-id="e7065-122">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="e7065-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="e7065-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e7065-123">Implementations</span></span>

-   [<span data-ttu-id="e7065-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e7065-124">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="e7065-125">ADAM</span><span class="sxs-lookup"><span data-stu-id="e7065-125">ADAM</span></span>



| <span data-ttu-id="e7065-126">Entrada</span><span class="sxs-lookup"><span data-stu-id="e7065-126">Entry</span></span> | <span data-ttu-id="e7065-127">Value</span><span class="sxs-lookup"><span data-stu-id="e7065-127">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e7065-128">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e7065-128">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e7065-129">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7065-129">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e7065-130">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7065-130">System-Only</span></span>            | <span data-ttu-id="e7065-131">False</span><span class="sxs-lookup"><span data-stu-id="e7065-131">False</span></span>                                                             |
| <span data-ttu-id="e7065-132">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e7065-132">Is-Single-Valued</span></span>       | <span data-ttu-id="e7065-133">True</span><span class="sxs-lookup"><span data-stu-id="e7065-133">True</span></span>                                                              |
| <span data-ttu-id="e7065-134">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e7065-134">Is Indexed</span></span>             | <span data-ttu-id="e7065-135">False</span><span class="sxs-lookup"><span data-stu-id="e7065-135">False</span></span>                                                             |
| <span data-ttu-id="e7065-136">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e7065-136">In Global Catalog</span></span>      | <span data-ttu-id="e7065-137">False</span><span class="sxs-lookup"><span data-stu-id="e7065-137">False</span></span>                                                             |
| <span data-ttu-id="e7065-138">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e7065-138">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7065-139">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7065-139">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e7065-140">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7065-140">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="e7065-141">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7065-141">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="e7065-142">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7065-142">Search-Flags</span></span>           | <span data-ttu-id="e7065-143">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7065-143">0x00000000</span></span>                                                        |
| <span data-ttu-id="e7065-144">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7065-144">System-Flags</span></span>           | <span data-ttu-id="e7065-145">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7065-145">0x00000010</span></span>                                                        |
| <span data-ttu-id="e7065-146">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e7065-146">Classes used in</span></span>        | [<span data-ttu-id="e7065-147">**Objeto MS-DS-Bindable**</span><span class="sxs-lookup"><span data-stu-id="e7065-147">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e7065-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7065-148">Remarks</span></span>

<span data-ttu-id="e7065-149">En ADAM, este atributo reemplaza la marca de la [**\_ \_ \_ \_ passwd ad fi no expire**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) en el atributo [**UserAccountControl**](a-useraccountcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="e7065-149">In ADAM, this attribute replaces the [**ADS\_UF\_DONT\_EXPIRE\_PASSWD**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) flag of the [**userAccountControl**](a-useraccountcontrol.md) attribute.</span></span>

 

