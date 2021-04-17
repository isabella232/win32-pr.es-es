---
description: Contiene información sobre cómo construir una cadena de confianza de certificados.
ms.assetid: 120cd79e-7c9b-45f3-8596-091b674e73d8
title: Objeto CertificateStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e9a6cb31a00f4d2943e68670930e6cbc4436b6b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670681"
---
# <a name="certificatestatus-object"></a><span data-ttu-id="613e8-103">Objeto CertificateStatus</span><span class="sxs-lookup"><span data-stu-id="613e8-103">CertificateStatus object</span></span>

<span data-ttu-id="613e8-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="613e8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="613e8-105">En su lugar, use la [**estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="613e8-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="613e8-106">El objeto **CertificateStatus** contiene información sobre cómo construir una cadena de confianza de certificados.</span><span class="sxs-lookup"><span data-stu-id="613e8-106">The **CertificateStatus** object contains information about how to construct a certificate trust chain.</span></span>

## <a name="members"></a><span data-ttu-id="613e8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="613e8-107">Members</span></span>

<span data-ttu-id="613e8-108">El objeto **CertificateStatus** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="613e8-108">The **CertificateStatus** object has these types of members:</span></span>

-   [<span data-ttu-id="613e8-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="613e8-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="613e8-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="613e8-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="613e8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="613e8-111">Methods</span></span>

<span data-ttu-id="613e8-112">El objeto **CertificateStatus** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="613e8-112">The **CertificateStatus** object has these methods.</span></span>



| <span data-ttu-id="613e8-113">Método</span><span class="sxs-lookup"><span data-stu-id="613e8-113">Method</span></span>                                                               | <span data-ttu-id="613e8-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="613e8-114">Description</span></span>                                                                                                                                  |
|:---------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="613e8-115">**ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="613e8-115">**ApplicationPolicies**</span></span>](certificatestatus-applicationpolicies.md) | <span data-ttu-id="613e8-116">Devuelve una colección de [**OID**](oids.md) que representa los OID de directiva de aplicación.</span><span class="sxs-lookup"><span data-stu-id="613e8-116">Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs.</span></span><br/>                                           |
| [<span data-ttu-id="613e8-117">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="613e8-117">**CertificatePolicies**</span></span>](certificatestatus-certificatepolicies.md) | <span data-ttu-id="613e8-118">Devuelve una colección de [**OID**](oids.md) que representa los OID de directiva de certificado utilizados durante la compilación de la cadena.</span><span class="sxs-lookup"><span data-stu-id="613e8-118">Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs used during chain building.</span></span><br/>                |
| [<span data-ttu-id="613e8-119">**EKU**</span><span class="sxs-lookup"><span data-stu-id="613e8-119">**EKU**</span></span>](certificatestatus-eku.md)                                 | <span data-ttu-id="613e8-120">Devuelve el objeto [**EKU**](eku.md) que se usa para establecer los elementos EKU que se van a comprobar en el establecimiento del estado de validez de un certificado.</span><span class="sxs-lookup"><span data-stu-id="613e8-120">Returns the [**EKU**](eku.md) object used to set the EKU elements to be checked in establishing a certificate's validity status.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="613e8-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="613e8-121">Properties</span></span>

<span data-ttu-id="613e8-122">El objeto **CertificateStatus** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="613e8-122">The **CertificateStatus** object has these properties.</span></span>



| <span data-ttu-id="613e8-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="613e8-123">Property</span></span>                                                                        | <span data-ttu-id="613e8-124">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="613e8-124">Access type</span></span>           | <span data-ttu-id="613e8-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="613e8-125">Description</span></span>                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="613e8-126">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="613e8-126">**Certificates**</span></span>](certificatestatus-certificates.md)<br/>               | <span data-ttu-id="613e8-127">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613e8-127">Read/write</span></span><br/> | <span data-ttu-id="613e8-128">Establece o recupera la colección de certificados que se puede utilizar para generar la cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="613e8-128">Sets or retrieves the collection of certificates that can be used to build the certificate chain.</span></span><br/> <span data-ttu-id="613e8-129">**CAPICOM 2.0.0.3 y versiones anteriores:** No se admite la propiedad [**Certificates**](certificatestatus-certificates.md) .</span><span class="sxs-lookup"><span data-stu-id="613e8-129">**CAPICOM 2.0.0.3 and earlier:** The [**Certificates**](certificatestatus-certificates.md) property is not supported.</span></span><br/>                    |
| [<span data-ttu-id="613e8-130">**CheckFlag**</span><span class="sxs-lookup"><span data-stu-id="613e8-130">**CheckFlag**</span></span>](certificatestatus-checkflag.md)<br/>                     | <span data-ttu-id="613e8-131">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613e8-131">Read/write</span></span><br/> | <span data-ttu-id="613e8-132">Marca de comprobación de validez.</span><span class="sxs-lookup"><span data-stu-id="613e8-132">Validity check flag.</span></span> <span data-ttu-id="613e8-133">Los valores se pueden combinar con un operador lógico **or** .</span><span class="sxs-lookup"><span data-stu-id="613e8-133">Values can be joined by using a logical **OR** operator.</span></span> <span data-ttu-id="613e8-134">La marca de verificación predeterminada es [**CAPICOM \_ check \_ online \_ All**](capicom-check-flag.md).</span><span class="sxs-lookup"><span data-stu-id="613e8-134">The default check flag is [**CAPICOM\_CHECK\_ONLINE\_ALL**](capicom-check-flag.md).</span></span><br/>                                                                                     |
| [<span data-ttu-id="613e8-135">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="613e8-135">**Result**</span></span>](certificatestatus-result.md)<br/>                           | <span data-ttu-id="613e8-136">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="613e8-136">Read-only</span></span><br/>  | <span data-ttu-id="613e8-137">Indica si el certificado es válido.</span><span class="sxs-lookup"><span data-stu-id="613e8-137">Indicates whether the certificate is valid.</span></span> <span data-ttu-id="613e8-138">La validez del certificado se comprueba con la configuración actual de la propiedad [**CheckFlag**](certificatestatus-checkflag.md) y la configuración de directiva del certificado.</span><span class="sxs-lookup"><span data-stu-id="613e8-138">The certificate's validity is checked using the current setting of the [**CheckFlag**](certificatestatus-checkflag.md) property and the policy settings of the certificate.</span></span> <span data-ttu-id="613e8-139">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="613e8-139">This is the default property.</span></span><br/> |
| [<span data-ttu-id="613e8-140">**UrlRetrievalTimeout**</span><span class="sxs-lookup"><span data-stu-id="613e8-140">**UrlRetrievalTimeout**</span></span>](certificatestatus-urlretrievaltimeout.md)<br/> | <span data-ttu-id="613e8-141">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613e8-141">Read/write</span></span><br/> | <span data-ttu-id="613e8-142">Establece o recupera el período de tiempo antes de que se determine una dirección URL como inaccesible.</span><span class="sxs-lookup"><span data-stu-id="613e8-142">Sets or retrieves the length of time before a URL is determined to be unreachable.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="613e8-143">**VerificationTime**</span><span class="sxs-lookup"><span data-stu-id="613e8-143">**VerificationTime**</span></span>](certificatestatus-verificationtime.md)<br/>       | <span data-ttu-id="613e8-144">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613e8-144">Read/write</span></span><br/> | <span data-ttu-id="613e8-145">Establece o recupera la hora a la que se ha comprobado el certificado.</span><span class="sxs-lookup"><span data-stu-id="613e8-145">Sets or retrieves the time that the certificate was verified.</span></span><br/>                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="613e8-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="613e8-146">Remarks</span></span>

<span data-ttu-id="613e8-147">No se puede crear el objeto **CertificateStatus** .</span><span class="sxs-lookup"><span data-stu-id="613e8-147">The **CertificateStatus** object cannot be created.</span></span>

<span data-ttu-id="613e8-148">El método [**Certificate. IsValid**](certificate-isvalid.md) devuelve el objeto **CertificateStatus** .</span><span class="sxs-lookup"><span data-stu-id="613e8-148">The **CertificateStatus** object is returned by the [**Certificate.IsValid**](certificate-isvalid.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="613e8-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="613e8-149">Requirements</span></span>



| <span data-ttu-id="613e8-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="613e8-150">Requirement</span></span> | <span data-ttu-id="613e8-151">Value</span><span class="sxs-lookup"><span data-stu-id="613e8-151">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="613e8-152">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="613e8-152">End of client support</span></span><br/> | <span data-ttu-id="613e8-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="613e8-153">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="613e8-154">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="613e8-154">End of server support</span></span><br/> | <span data-ttu-id="613e8-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="613e8-155">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="613e8-156">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="613e8-156">Redistributable</span></span><br/>       | <span data-ttu-id="613e8-157">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="613e8-157">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="613e8-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="613e8-158">DLL</span></span><br/>                   | <dl> <span data-ttu-id="613e8-159"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="613e8-159"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="613e8-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="613e8-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="613e8-161">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="613e8-161">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="613e8-162">**IAM**</span><span class="sxs-lookup"><span data-stu-id="613e8-162">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
