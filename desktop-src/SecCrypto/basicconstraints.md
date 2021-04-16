---
description: Representa la extensión de restricciones básicas de un certificado.
ms.assetid: c21794f6-7654-4140-8114-0edb398d6de8
title: Objeto BasicConstraints
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85e912542b09b02297f5119392115857259f70f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671411"
---
# <a name="basicconstraints-object"></a><span data-ttu-id="5aff8-103">Objeto BasicConstraints</span><span class="sxs-lookup"><span data-stu-id="5aff8-103">BasicConstraints object</span></span>

<span data-ttu-id="5aff8-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5aff8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="5aff8-105">En su lugar, use la [**clase X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="5aff8-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="5aff8-106">El objeto **BasicConstraints** representa la extensión de restricciones básicas de un certificado.</span><span class="sxs-lookup"><span data-stu-id="5aff8-106">The **BasicConstraints** object represents the basic constraints extension of a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="5aff8-107">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="5aff8-107">When to use</span></span>

<span data-ttu-id="5aff8-108">El objeto **BasicConstraints** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="5aff8-108">The **BasicConstraints** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="5aff8-109">Determine si la extensión de restricciones básicas está presente.</span><span class="sxs-lookup"><span data-stu-id="5aff8-109">Determine whether the basic constraints extension is present.</span></span>
-   <span data-ttu-id="5aff8-110">Determine si la extensión de restricciones básicas está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="5aff8-110">Determine whether the basic constraints extension is marked critical.</span></span>
-   <span data-ttu-id="5aff8-111">Determine si el certificado está restringido a las entidades de certificación.</span><span class="sxs-lookup"><span data-stu-id="5aff8-111">Determine whether the certificate is constrained to certificate authorities.</span></span>
-   <span data-ttu-id="5aff8-112">Determine si la restricción de longitud de ruta de acceso está presente y recupere el valor de la restricción de longitud de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="5aff8-112">Determine whether the path length constraint is present and retrieve the path length constraint value.</span></span>

## <a name="members"></a><span data-ttu-id="5aff8-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="5aff8-113">Members</span></span>

<span data-ttu-id="5aff8-114">El objeto **BasicConstraints** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5aff8-114">The **BasicConstraints** object has these types of members:</span></span>

-   [<span data-ttu-id="5aff8-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5aff8-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5aff8-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5aff8-116">Properties</span></span>

<span data-ttu-id="5aff8-117">El objeto **BasicConstraints** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5aff8-117">The **BasicConstraints** object has these properties.</span></span>



| <span data-ttu-id="5aff8-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5aff8-118">Property</span></span>                                                                                     | <span data-ttu-id="5aff8-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="5aff8-119">Access type</span></span>          | <span data-ttu-id="5aff8-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aff8-120">Description</span></span>                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5aff8-121">**IsCertificateAuthority**</span><span class="sxs-lookup"><span data-stu-id="5aff8-121">**IsCertificateAuthority**</span></span>](basicconstraints-iscertificateauthority.md)<br/>         | <span data-ttu-id="5aff8-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5aff8-122">Read-only</span></span><br/> | <span data-ttu-id="5aff8-123">Recupera un valor booleano que indica si el certificado es para una [*entidad de certificación*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="5aff8-123">Retrieves a Boolean value that indicates whether the certificate is for a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span><br/> |
| [<span data-ttu-id="5aff8-124">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="5aff8-124">**IsCritical**</span></span>](basicconstraints-iscritical.md)<br/>                                 | <span data-ttu-id="5aff8-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5aff8-125">Read-only</span></span><br/> | <span data-ttu-id="5aff8-126">Recupera un valor booleano que indica si la extensión de restricción básica está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="5aff8-126">Retrieves a Boolean value that indicates whether the basic constraint extension is marked critical.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="5aff8-127">**IsPathLenConstraintPresent**</span><span class="sxs-lookup"><span data-stu-id="5aff8-127">**IsPathLenConstraintPresent**</span></span>](basicconstraints-ispathlenconstraintpresent.md)<br/> | <span data-ttu-id="5aff8-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5aff8-128">Read-only</span></span><br/> | <span data-ttu-id="5aff8-129">Recupera un valor booleano que indica si la restricción de longitud de ruta de acceso del certificado está presente.</span><span class="sxs-lookup"><span data-stu-id="5aff8-129">Retrieves a Boolean value that indicates whether the certificate's path length constraint is present.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="5aff8-130">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="5aff8-130">**IsPresent**</span></span>](basicconstraints-ispresent.md)<br/>                                   | <span data-ttu-id="5aff8-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5aff8-131">Read-only</span></span><br/> | <span data-ttu-id="5aff8-132">Recupera un valor booleano que indica si la extensión de restricciones básicas está presente.</span><span class="sxs-lookup"><span data-stu-id="5aff8-132">Retrieves a Boolean value that indicates whether the basic constraints extension is present.</span></span> <span data-ttu-id="5aff8-133">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5aff8-133">This is the default property.</span></span><br/>                                                                              |
| [<span data-ttu-id="5aff8-134">**PathLenConstraint**</span><span class="sxs-lookup"><span data-stu-id="5aff8-134">**PathLenConstraint**</span></span>](basicconstraints-pathlenconstraint.md)<br/>                   | <span data-ttu-id="5aff8-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5aff8-135">Read-only</span></span><br/> | <span data-ttu-id="5aff8-136">Recupera el valor de la restricción de longitud de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="5aff8-136">Retrieves the value of the path length constraint.</span></span><br/>                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="5aff8-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aff8-137">Remarks</span></span>

<span data-ttu-id="5aff8-138">No se puede crear el objeto **BasicConstraints** .</span><span class="sxs-lookup"><span data-stu-id="5aff8-138">The **BasicConstraints** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aff8-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aff8-139">Requirements</span></span>



| <span data-ttu-id="5aff8-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aff8-140">Requirement</span></span> | <span data-ttu-id="5aff8-141">Value</span><span class="sxs-lookup"><span data-stu-id="5aff8-141">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5aff8-142">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5aff8-142">End of client support</span></span><br/> | <span data-ttu-id="5aff8-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5aff8-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5aff8-144">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5aff8-144">End of server support</span></span><br/> | <span data-ttu-id="5aff8-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5aff8-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5aff8-146">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="5aff8-146">Redistributable</span></span><br/>       | <span data-ttu-id="5aff8-147">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="5aff8-147">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5aff8-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5aff8-148">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5aff8-149"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aff8-149"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aff8-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aff8-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aff8-151">Objetos de criptografía</span><span class="sxs-lookup"><span data-stu-id="5aff8-151">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
