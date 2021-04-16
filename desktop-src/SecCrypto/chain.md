---
description: Representa una cadena de confianza de certificado.
ms.assetid: 45ed686f-4a7f-4df9-8366-98b825c3c657
title: Chain (objeto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fa3432767ccfdb60a2e3bc0a50ddbbcf565e0aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690246"
---
# <a name="chain-object"></a><span data-ttu-id="b2742-103">Chain (objeto)</span><span class="sxs-lookup"><span data-stu-id="b2742-103">Chain object</span></span>

<span data-ttu-id="b2742-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b2742-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b2742-105">En su lugar, use la [**clase X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b2742-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b2742-106">El objeto de **cadena** representa una cadena de confianza de certificado.</span><span class="sxs-lookup"><span data-stu-id="b2742-106">The **Chain** object represents a certificate trust chain.</span></span>

<span data-ttu-id="b2742-107">Este objeto proporciona propiedades y métodos para crear una cadena de confianza de certificados para comprobar la validez de los certificados.</span><span class="sxs-lookup"><span data-stu-id="b2742-107">This object provides properties and methods to build a certificate trust chain to check the validity of certificates.</span></span> <span data-ttu-id="b2742-108">La cadena se genera mediante el valor de la propiedad [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) y la configuración de directiva de un objeto [**CertificateStatus**](certificatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="b2742-108">The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property value and the policy settings of a [**CertificateStatus**](certificatestatus.md) object.</span></span>

<span data-ttu-id="b2742-109">El objeto **Chain** expone las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="b2742-109">The **Chain** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="b2742-110">**IChain2**: introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b2742-110">**IChain2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="b2742-111">**IChain**: introducido en CAPICOM 1,0.</span><span class="sxs-lookup"><span data-stu-id="b2742-111">**IChain**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b2742-112">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="b2742-112">When to use</span></span>

<span data-ttu-id="b2742-113">El objeto de **cadena** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="b2742-113">The **Chain** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="b2742-114">Cree una cadena de confianza de certificados.</span><span class="sxs-lookup"><span data-stu-id="b2742-114">Build a certificate trust chain.</span></span>
-   <span data-ttu-id="b2742-115">Obtenga los OID de todas las directivas de aplicación y certificado válidas para la cadena.</span><span class="sxs-lookup"><span data-stu-id="b2742-115">Obtain the OIDs of all the certificate and application policies valid for the chain.</span></span>
-   <span data-ttu-id="b2742-116">Compruebe el estado de los certificados de la cadena.</span><span class="sxs-lookup"><span data-stu-id="b2742-116">Verify the status of the certificates in the chain.</span></span>
-   <span data-ttu-id="b2742-117">Obtener información de error extendida.</span><span class="sxs-lookup"><span data-stu-id="b2742-117">Obtain extended error information.</span></span>
-   <span data-ttu-id="b2742-118">Recupere la colección de certificados de la cadena.</span><span class="sxs-lookup"><span data-stu-id="b2742-118">Retrieve the collection of certificates in the chain.</span></span>

## <a name="members"></a><span data-ttu-id="b2742-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="b2742-119">Members</span></span>

<span data-ttu-id="b2742-120">El objeto de **cadena** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b2742-120">The **Chain** object has these types of members:</span></span>

-   [<span data-ttu-id="b2742-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="b2742-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="b2742-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b2742-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b2742-123">Métodos</span><span class="sxs-lookup"><span data-stu-id="b2742-123">Methods</span></span>

<span data-ttu-id="b2742-124">El objeto de **cadena** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b2742-124">The **Chain** object has these methods.</span></span>



| <span data-ttu-id="b2742-125">Método</span><span class="sxs-lookup"><span data-stu-id="b2742-125">Method</span></span>                                                   | <span data-ttu-id="b2742-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2742-126">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2742-127">**ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="b2742-127">**ApplicationPolicies**</span></span>](chain-applicationpolicies.md) | <span data-ttu-id="b2742-128">Devuelve una colección de [**OID**](oids.md) que representa los OID de directiva de aplicación válidos para la cadena.</span><span class="sxs-lookup"><span data-stu-id="b2742-128">Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs valid for the chain.</span></span><br/> <span data-ttu-id="b2742-129">(Se hereda de **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="b2742-129">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                          |
| [<span data-ttu-id="b2742-130">**Build**</span><span class="sxs-lookup"><span data-stu-id="b2742-130">**Build**</span></span>](chain-build.md)                             | <span data-ttu-id="b2742-131">Crea una cadena de comprobación de certificados desde un certificado final al [*certificado raíz*](../secgloss/r-gly.md)de confianza, y devuelve un valor booleano que indica la validez global de la cadena.</span><span class="sxs-lookup"><span data-stu-id="b2742-131">Builds a certificate verification chain from an end certificate to the trusted [*root certificate*](../secgloss/r-gly.md), returning a Boolean value that indicates the overall validity of the chain.</span></span><br/> <span data-ttu-id="b2742-132">(Se hereda de **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="b2742-132">(Inherited from **ChainIChain2IChain**)</span></span> |
| [<span data-ttu-id="b2742-133">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="b2742-133">**CertificatePolicies**</span></span>](chain-certificatepolicies.md) | <span data-ttu-id="b2742-134">Devuelve una colección de [**OID**](oids.md) que representa los OID de directiva de certificado válidos para la cadena.</span><span class="sxs-lookup"><span data-stu-id="b2742-134">Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.</span></span><br/> <span data-ttu-id="b2742-135">(Se hereda de **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="b2742-135">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                          |
| [<span data-ttu-id="b2742-136">**ExtendedErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b2742-136">**ExtendedErrorInfo**</span></span>](chain-extendederrorinfo.md)     | <span data-ttu-id="b2742-137">Devuelve una cadena que contiene información de error adicional sobre la entrada indizada.</span><span class="sxs-lookup"><span data-stu-id="b2742-137">Returns a string that contains additional error information about the indexed entry.</span></span><br/> <span data-ttu-id="b2742-138">(Se hereda de **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="b2742-138">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="b2742-139">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b2742-139">Properties</span></span>

<span data-ttu-id="b2742-140">El objeto de **cadena** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b2742-140">The **Chain** object has these properties.</span></span>



| <span data-ttu-id="b2742-141">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b2742-141">Property</span></span>                                              | <span data-ttu-id="b2742-142">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="b2742-142">Access type</span></span>          | <span data-ttu-id="b2742-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2742-143">Description</span></span>                                                                                                                                                                                 |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2742-144">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="b2742-144">**Certificates**</span></span>](chain-certificates.md)<br/> | <span data-ttu-id="b2742-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="b2742-145">Read-only</span></span><br/> | <span data-ttu-id="b2742-146">Recupera una colección de [**certificados**](certificates.md) que representa los certificados de la cadena.</span><span class="sxs-lookup"><span data-stu-id="b2742-146">Retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain.</span></span> <span data-ttu-id="b2742-147">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b2742-147">This is the default property.</span></span><br/> <span data-ttu-id="b2742-148">(Se hereda de **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="b2742-148">(Inherited from **ChainIChain2IChain**)</span></span> |
| [<span data-ttu-id="b2742-149">**Status**</span><span class="sxs-lookup"><span data-stu-id="b2742-149">**Status**</span></span>](chain-status.md)<br/>             | <span data-ttu-id="b2742-150">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="b2742-150">Read-only</span></span><br/> | <span data-ttu-id="b2742-151">Recupera el estado de validez de la cadena o de un certificado específico de la cadena.</span><span class="sxs-lookup"><span data-stu-id="b2742-151">Retrieves the validity status of the chain or a specific certificate in the chain.</span></span><br/> <span data-ttu-id="b2742-152">(Se hereda de **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="b2742-152">(Inherited from **ChainIChain2IChain**)</span></span>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="b2742-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2742-153">Remarks</span></span>

<span data-ttu-id="b2742-154">Se puede crear el objeto de **cadena** y es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="b2742-154">The **Chain** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="b2742-155">El ProgID del objeto de **cadena** es "CAPICOM. Chain. 2 ".</span><span class="sxs-lookup"><span data-stu-id="b2742-155">The ProgID for the **Chain** object is "CAPICOM.Chain.2".</span></span>

<span data-ttu-id="b2742-156">**CAPICOM 1. *x*:** el ProgID del objeto de **cadena** es CAPICOM. Cadena. 1.</span><span class="sxs-lookup"><span data-stu-id="b2742-156">**CAPICOM 1.*x*:** The ProgID for the **Chain** object is CAPICOM.Chain.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2742-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2742-157">Requirements</span></span>



| <span data-ttu-id="b2742-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2742-158">Requirement</span></span> | <span data-ttu-id="b2742-159">Value</span><span class="sxs-lookup"><span data-stu-id="b2742-159">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2742-160">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b2742-160">End of client support</span></span><br/> | <span data-ttu-id="b2742-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2742-161">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b2742-162">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b2742-162">End of server support</span></span><br/> | <span data-ttu-id="b2742-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2742-163">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b2742-164">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b2742-164">Redistributable</span></span><br/>       | <span data-ttu-id="b2742-165">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="b2742-165">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b2742-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2742-166">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b2742-167"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2742-167"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2742-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2742-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2742-169">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="b2742-169">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
