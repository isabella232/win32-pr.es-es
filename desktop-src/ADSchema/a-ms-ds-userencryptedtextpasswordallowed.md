---
title: atributo MS-DS-usuario-cifrado-texto-contraseña permitido
description: Indica si Active Directory almacenará la contraseña en el formato de cifrado reversible.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- 'MS-DS-User-Encrypted-Text-Password: esquema de AD de atributos permitidos'
- Esquema de AD del atributo MS-DS-UserEncryptedTextPasswordAllowed
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d99ae61566ceec94336fd58951214dfc3255d2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493570"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a><span data-ttu-id="38bbe-105">atributo MS-DS-usuario-cifrado-texto-contraseña permitido</span><span class="sxs-lookup"><span data-stu-id="38bbe-105">ms-DS-User-Encrypted-Text-Password-Allowed attribute</span></span>

<span data-ttu-id="38bbe-106">Indica si Active Directory almacenará la contraseña en el formato de cifrado reversible.</span><span class="sxs-lookup"><span data-stu-id="38bbe-106">Indicates whether Active Directory will store the password in the reversible encryption format.</span></span> <span data-ttu-id="38bbe-107">True si la contraseña se almacena en el formato de cifrado reversible; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="38bbe-107">True if the password is stored in the reversible encryption format; otherwise, False.</span></span>

> [!Note]  
> <span data-ttu-id="38bbe-108">[Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) no utiliza este atributo y solo se incluye para la integridad o la paridad con UserAccountControl.</span><span class="sxs-lookup"><span data-stu-id="38bbe-108">This attribute is not used by [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) and is only included for completeness/parity with userAccountControl.</span></span> <span data-ttu-id="38bbe-109">AD LDS no almacena contraseñas con cifrado reversible, independientemente del valor de este atributo en un objeto determinado o en la Directiva de seguridad del equipo que pertenece al cifrado reversible en el propio equipo.</span><span class="sxs-lookup"><span data-stu-id="38bbe-109">AD LDS does not store passwords with reversible encryption, regardless of this attribute's value on any given object or the computer security policy pertaining to reversible encryption on the computer itself.</span></span>

 



| <span data-ttu-id="38bbe-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="38bbe-110">Entry</span></span> | <span data-ttu-id="38bbe-111">Value</span><span class="sxs-lookup"><span data-stu-id="38bbe-111">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="38bbe-112">CN</span><span class="sxs-lookup"><span data-stu-id="38bbe-112">CN</span></span>                | <span data-ttu-id="38bbe-113">MS-DS-usuario-cifrado-texto-contraseña-permitido</span><span class="sxs-lookup"><span data-stu-id="38bbe-113">ms-DS-User-Encrypted-Text-Password-Allowed</span></span> |
| <span data-ttu-id="38bbe-114">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="38bbe-114">Ldap-Display-Name</span></span> | <span data-ttu-id="38bbe-115">MS-DS-UserEncryptedTextPasswordAllowed</span><span class="sxs-lookup"><span data-stu-id="38bbe-115">ms-DS-UserEncryptedTextPasswordAllowed</span></span>     |
| <span data-ttu-id="38bbe-116">Tamaño</span><span class="sxs-lookup"><span data-stu-id="38bbe-116">Size</span></span>              | \-                                         |
| <span data-ttu-id="38bbe-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="38bbe-117">Update Privilege</span></span>  | \-                                         |
| <span data-ttu-id="38bbe-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="38bbe-118">Update Frequency</span></span>  | \-                                         |
| <span data-ttu-id="38bbe-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="38bbe-119">Attribute-Id</span></span>      | <span data-ttu-id="38bbe-120">1.2.840.113556.1.4.1856</span><span class="sxs-lookup"><span data-stu-id="38bbe-120">1.2.840.113556.1.4.1856</span></span>                    |
| <span data-ttu-id="38bbe-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="38bbe-121">System-Id-Guid</span></span>    | <span data-ttu-id="38bbe-122">5a87c7f2-93c5-454c-a8c5-8cb09613292e</span><span class="sxs-lookup"><span data-stu-id="38bbe-122">5a87c7f2-93c5-454c-a8c5-8cb09613292e</span></span>       |
| <span data-ttu-id="38bbe-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38bbe-123">Syntax</span></span>            | [<span data-ttu-id="38bbe-124">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="38bbe-124">**Boolean**</span></span>](s-boolean.md)               |



## <a name="implementations"></a><span data-ttu-id="38bbe-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="38bbe-125">Implementations</span></span>

-   [<span data-ttu-id="38bbe-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="38bbe-126">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="38bbe-127">ADAM</span><span class="sxs-lookup"><span data-stu-id="38bbe-127">ADAM</span></span>



| <span data-ttu-id="38bbe-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="38bbe-128">Entry</span></span> | <span data-ttu-id="38bbe-129">Value</span><span class="sxs-lookup"><span data-stu-id="38bbe-129">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="38bbe-130">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38bbe-130">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="38bbe-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38bbe-131">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="38bbe-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="38bbe-132">System-Only</span></span>            | <span data-ttu-id="38bbe-133">False</span><span class="sxs-lookup"><span data-stu-id="38bbe-133">False</span></span>                                                             |
| <span data-ttu-id="38bbe-134">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38bbe-134">Is-Single-Valued</span></span>       | <span data-ttu-id="38bbe-135">True</span><span class="sxs-lookup"><span data-stu-id="38bbe-135">True</span></span>                                                              |
| <span data-ttu-id="38bbe-136">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38bbe-136">Is Indexed</span></span>             | <span data-ttu-id="38bbe-137">False</span><span class="sxs-lookup"><span data-stu-id="38bbe-137">False</span></span>                                                             |
| <span data-ttu-id="38bbe-138">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38bbe-138">In Global Catalog</span></span>      | <span data-ttu-id="38bbe-139">False</span><span class="sxs-lookup"><span data-stu-id="38bbe-139">False</span></span>                                                             |
| <span data-ttu-id="38bbe-140">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38bbe-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="38bbe-141">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38bbe-141">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="38bbe-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38bbe-142">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="38bbe-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38bbe-143">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="38bbe-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38bbe-144">Search-Flags</span></span>           | <span data-ttu-id="38bbe-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38bbe-145">0x00000000</span></span>                                                        |
| <span data-ttu-id="38bbe-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38bbe-146">System-Flags</span></span>           | <span data-ttu-id="38bbe-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38bbe-147">0x00000010</span></span>                                                        |
| <span data-ttu-id="38bbe-148">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38bbe-148">Classes used in</span></span>        | [<span data-ttu-id="38bbe-149">**Objeto MS-DS-Bindable**</span><span class="sxs-lookup"><span data-stu-id="38bbe-149">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="38bbe-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38bbe-150">Remarks</span></span>

<span data-ttu-id="38bbe-151">En ADAM, este atributo reemplaza la marca de la [**\_ contraseña de \_ texto cifrado de ad fi \_ \_ \_ permitida**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) del atributo [**UserAccountControl**](a-useraccountcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="38bbe-151">In ADAM, this attribute replaces the [**ADS\_UF\_ENCRYPTED\_TEXT\_PASSWORD\_ALLOWED**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) flag of the [**userAccountControl**](a-useraccountcontrol.md) attribute.</span></span>

 

