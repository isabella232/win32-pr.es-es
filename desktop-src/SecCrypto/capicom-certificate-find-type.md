---
description: El \_ \_ \_ tipo de enumeración buscar certificado de CAPICOM define el tipo de criterio de búsqueda usado para buscar certificados específicos. Este tipo de enumeración se presentó en CAPICOM 2,0.
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: Enumeración CAPICOM_CERTIFICATE_FIND_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_FIND_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: c5c867b230ba2045d97619d7f55e257bd7803b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670505"
---
# <a name="capicom_certificate_find_type-enumeration"></a><span data-ttu-id="076f8-104">\_ \_ Enumeración de tipo de búsqueda de certificado de CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="076f8-104">CAPICOM\_CERTIFICATE\_FIND\_TYPE enumeration</span></span>

<span data-ttu-id="076f8-105">El tipo de enumeración **\_ \_ Buscar \_ certificado de CAPICOM** define el tipo de criterio de búsqueda usado para buscar certificados específicos.</span><span class="sxs-lookup"><span data-stu-id="076f8-105">The **CAPICOM\_CERTIFICATE\_FIND\_TYPE** enumeration type defines the type of search criteria used to find specific certificates.</span></span> <span data-ttu-id="076f8-106">Este tipo de enumeración se presentó en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="076f8-106">This enumeration type was introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="076f8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="076f8-107">Members</span></span>



| <span data-ttu-id="076f8-108">Miembro</span><span class="sxs-lookup"><span data-stu-id="076f8-108">Member</span></span>                                                | <span data-ttu-id="076f8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="076f8-109">Description</span></span>                                                                                                                                 | <span data-ttu-id="076f8-110">Value</span><span class="sxs-lookup"><span data-stu-id="076f8-110">Value</span></span> |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="076f8-111">**Certificado de CAPICOM, \_ \_ Buscar \_ \_ hash SHA1**</span><span class="sxs-lookup"><span data-stu-id="076f8-111">**CAPICOM\_CERTIFICATE\_FIND\_SHA1\_HASH**</span></span>            | <span data-ttu-id="076f8-112">Devuelve certificados que coinciden con un hash SHA1 especificado.</span><span class="sxs-lookup"><span data-stu-id="076f8-112">Returns certificates matching a specified SHA1 hash.</span></span><br/>                                                                             | <span data-ttu-id="076f8-113">0</span><span class="sxs-lookup"><span data-stu-id="076f8-113">0</span></span>     |
| <span data-ttu-id="076f8-114">**\_el certificado de CAPICOM \_ encuentra \_ \_ el nombre del firmante**</span><span class="sxs-lookup"><span data-stu-id="076f8-114">**CAPICOM\_CERTIFICATE\_FIND\_SUBJECT\_NAME**</span></span>         | <span data-ttu-id="076f8-115">Devuelve certificados cuyo nombre de sujeto coincide exactamente o parcialmente con un nombre de sujeto especificado.</span><span class="sxs-lookup"><span data-stu-id="076f8-115">Returns certificates whose subject name exactly or partially matches a specified subject name.</span></span><br/>                                   | <span data-ttu-id="076f8-116">1</span><span class="sxs-lookup"><span data-stu-id="076f8-116">1</span></span>     |
| <span data-ttu-id="076f8-117">**\_nombre del \_ emisor de búsqueda de certificado de \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="076f8-117">**CAPICOM\_CERTIFICATE\_FIND\_ISSUER\_NAME**</span></span>          | <span data-ttu-id="076f8-118">Devuelve certificados cuyo nombre de emisor coincide exactamente o parcialmente con un nombre de emisor especificado.</span><span class="sxs-lookup"><span data-stu-id="076f8-118">Returns certificates whose issuer name exactly or partially matches a specified issuer name.</span></span><br/>                                     | <span data-ttu-id="076f8-119">2</span><span class="sxs-lookup"><span data-stu-id="076f8-119">2</span></span>     |
| <span data-ttu-id="076f8-120">**nombre de la raíz del certificado de CAPICOM \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="076f8-120">**CAPICOM\_CERTIFICATE\_FIND\_ROOT\_NAME**</span></span>            | <span data-ttu-id="076f8-121">Devuelve certificados cuyo nombre de sujeto raíz coincide exactamente o parcialmente con un nombre de sujeto raíz especificado.</span><span class="sxs-lookup"><span data-stu-id="076f8-121">Returns certificates whose root subject name exactly or partially matches a specified root subject name.</span></span><br/>                         | <span data-ttu-id="076f8-122">3</span><span class="sxs-lookup"><span data-stu-id="076f8-122">3</span></span>     |
| <span data-ttu-id="076f8-123">**\_nombre de \_ plantilla de búsqueda de certificado de CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="076f8-123">**CAPICOM\_CERTIFICATE\_FIND\_TEMPLATE\_NAME**</span></span>        | <span data-ttu-id="076f8-124">Devuelve certificados cuyo nombre de plantilla coincide con un nombre de plantilla especificado.</span><span class="sxs-lookup"><span data-stu-id="076f8-124">Returns certificates whose template name matches a specified template name.</span></span><br/>                                                      | <span data-ttu-id="076f8-125">4</span><span class="sxs-lookup"><span data-stu-id="076f8-125">4</span></span>     |
| <span data-ttu-id="076f8-126">**\_extensión de \_ búsqueda de certificado de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="076f8-126">**CAPICOM\_CERTIFICATE\_FIND\_EXTENSION**</span></span>             | <span data-ttu-id="076f8-127">Devuelve los certificados que tienen una extensión que coincide con una extensión especificada.</span><span class="sxs-lookup"><span data-stu-id="076f8-127">Returns certificates that have an extension that matches a specified extension.</span></span><br/>                                                  | <span data-ttu-id="076f8-128">5</span><span class="sxs-lookup"><span data-stu-id="076f8-128">5</span></span>     |
| <span data-ttu-id="076f8-129">**\_ \_ \_ propiedad extendida de búsqueda de certificado de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="076f8-129">**CAPICOM\_CERTIFICATE\_FIND\_EXTENDED\_PROPERTY**</span></span>    | <span data-ttu-id="076f8-130">Devuelve los certificados que tienen una propiedad extendida cuyo identificador de propiedad coincide con un identificador de propiedad especificado.</span><span class="sxs-lookup"><span data-stu-id="076f8-130">Returns certificates that have an extended property whose property identifier matches a specified property identifier.</span></span><br/>           | <span data-ttu-id="076f8-131">6</span><span class="sxs-lookup"><span data-stu-id="076f8-131">6</span></span>     |
| <span data-ttu-id="076f8-132">**\_Directiva de \_ aplicación de búsqueda de certificado de CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="076f8-132">**CAPICOM\_CERTIFICATE\_FIND\_APPLICATION\_POLICY**</span></span>   | <span data-ttu-id="076f8-133">Devuelve los certificados del almacén que tienen una extensión de uso mejorado de clave o una propiedad combinada con un identificador de uso.</span><span class="sxs-lookup"><span data-stu-id="076f8-133">Returns certificates in the store that have either an enhanced key usage extension or property combined with a usage identifier.</span></span><br/> | <span data-ttu-id="076f8-134">7</span><span class="sxs-lookup"><span data-stu-id="076f8-134">7</span></span>     |
| <span data-ttu-id="076f8-135">**\_Directiva de \_ certificado de búsqueda \_ \_ de certificado de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="076f8-135">**CAPICOM\_CERTIFICATE\_FIND\_CERTIFICATE\_POLICY**</span></span>   | <span data-ttu-id="076f8-136">Devuelve certificados que contienen un OID de directiva especificado.</span><span class="sxs-lookup"><span data-stu-id="076f8-136">Returns certificates containing a specified policy OID.</span></span><br/>                                                                          | <span data-ttu-id="076f8-137">8</span><span class="sxs-lookup"><span data-stu-id="076f8-137">8</span></span>     |
| <span data-ttu-id="076f8-138">**tiempo de búsqueda de certificado de CAPICOM \_ \_ \_ \_ válido**</span><span class="sxs-lookup"><span data-stu-id="076f8-138">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_VALID**</span></span>           | <span data-ttu-id="076f8-139">Devuelve certificados cuya hora es válida.</span><span class="sxs-lookup"><span data-stu-id="076f8-139">Returns certificates whose time is valid.</span></span><br/>                                                                                        | <span data-ttu-id="076f8-140">9</span><span class="sxs-lookup"><span data-stu-id="076f8-140">9</span></span>     |
| <span data-ttu-id="076f8-141">**tiempo de búsqueda de certificado de CAPICOM \_ \_ \_ \_ no \_ \_ válido todavía**</span><span class="sxs-lookup"><span data-stu-id="076f8-141">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_NOT\_YET\_VALID**</span></span> | <span data-ttu-id="076f8-142">Devuelve certificados cuya hora todavía no es válida.</span><span class="sxs-lookup"><span data-stu-id="076f8-142">Returns certificates whose time is not yet valid.</span></span><br/>                                                                                | <span data-ttu-id="076f8-143">10</span><span class="sxs-lookup"><span data-stu-id="076f8-143">10</span></span>    |
| <span data-ttu-id="076f8-144">**tiempo de búsqueda de certificado de CAPICOM \_ \_ \_ \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="076f8-144">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_EXPIRED**</span></span>         | <span data-ttu-id="076f8-145">Devuelve los certificados cuya hora ha expirado.</span><span class="sxs-lookup"><span data-stu-id="076f8-145">Returns certificates whose time has expired.</span></span><br/>                                                                                     | <span data-ttu-id="076f8-146">11</span><span class="sxs-lookup"><span data-stu-id="076f8-146">11</span></span>    |
| <span data-ttu-id="076f8-147">**uso de la clave de certificado de CAPICOM \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="076f8-147">**CAPICOM\_CERTIFICATE\_FIND\_KEY\_USAGE**</span></span>            | <span data-ttu-id="076f8-148">Devuelve certificados que contienen una clave que se puede usar de la manera especificada.</span><span class="sxs-lookup"><span data-stu-id="076f8-148">Returns certificates containing a key that can be used in the specified manner.</span></span><br/>                                                  | <span data-ttu-id="076f8-149">12</span><span class="sxs-lookup"><span data-stu-id="076f8-149">12</span></span>    |



## <a name="remarks"></a><span data-ttu-id="076f8-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="076f8-150">Remarks</span></span>

<span data-ttu-id="076f8-151">El método Certificates [**. Find**](certificates-find.md) usa el tipo de enumeración **\_ \_ Buscar \_ certificado de CAPICOM** .</span><span class="sxs-lookup"><span data-stu-id="076f8-151">The **CAPICOM\_CERTIFICATE\_FIND\_TYPE** enumeration type is used by the [**Certificates.Find**](certificates-find.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="076f8-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="076f8-152">Requirements</span></span>



| <span data-ttu-id="076f8-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="076f8-153">Requirement</span></span> | <span data-ttu-id="076f8-154">Value</span><span class="sxs-lookup"><span data-stu-id="076f8-154">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="076f8-155">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="076f8-155">Redistributable</span></span><br/> | <span data-ttu-id="076f8-156">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="076f8-156">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="076f8-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="076f8-157">Header</span></span><br/>          | <dl> <span data-ttu-id="076f8-158"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="076f8-158"><dt>Capicom.h</dt></span></span> </dl> |



 

 




