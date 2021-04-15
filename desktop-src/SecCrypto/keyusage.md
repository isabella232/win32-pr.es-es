---
description: Proporciona acceso de solo lectura a las propiedades de uso de claves de un certificado.
ms.assetid: 8b8e9076-1a4f-4383-ac4b-1322d52949f0
title: Objeto KeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d2324b4e1e06650f2eed7b63337f2bd48520498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689910"
---
# <a name="keyusage-object"></a><span data-ttu-id="92d5c-103">Objeto KeyUsage</span><span class="sxs-lookup"><span data-stu-id="92d5c-103">KeyUsage object</span></span>

<span data-ttu-id="92d5c-104">\[El objeto **KeyUsage** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="92d5c-104">\[The **KeyUsage** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="92d5c-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="92d5c-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="92d5c-106">El objeto **KeyUsage** proporciona acceso de solo lectura a las propiedades de uso de claves de un certificado.</span><span class="sxs-lookup"><span data-stu-id="92d5c-106">The **KeyUsage** object provides read-only access to key usage properties of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="92d5c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="92d5c-107">Members</span></span>

<span data-ttu-id="92d5c-108">El objeto **KeyUsage** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="92d5c-108">The **KeyUsage** object has these types of members:</span></span>

-   [<span data-ttu-id="92d5c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="92d5c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92d5c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="92d5c-110">Properties</span></span>

<span data-ttu-id="92d5c-111">El objeto **KeyUsage** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="92d5c-111">The **KeyUsage** object has these properties.</span></span>



| <span data-ttu-id="92d5c-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="92d5c-112">Property</span></span>                                                                           | <span data-ttu-id="92d5c-113">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="92d5c-113">Access type</span></span>          | <span data-ttu-id="92d5c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d5c-114">Description</span></span>                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92d5c-115">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="92d5c-115">**IsCritical**</span></span>](keyusage-iscritical.md)<br/>                               | <span data-ttu-id="92d5c-116">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="92d5c-116">Read-only</span></span><br/> | <span data-ttu-id="92d5c-117">Recupera un valor booleano que indica si la extensión **KeyUsage** está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="92d5c-117">Retrieves a Boolean value that indicates whether the **KeyUsage** extension is marked critical.</span></span><br/>                                  |
| [<span data-ttu-id="92d5c-118">**IsCRLSignEnabled**</span><span class="sxs-lookup"><span data-stu-id="92d5c-118">**IsCRLSignEnabled**</span></span>](keyusage-iscrlsignenabled.md)<br/>                   | <span data-ttu-id="92d5c-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="92d5c-119">Read-only</span></span><br/> | <span data-ttu-id="92d5c-120">Recupera un valor booleano que indica si se ha establecido el bit bit crlsign.</span><span class="sxs-lookup"><span data-stu-id="92d5c-120">Retrieves a Boolean value that indicates whether the CRLSign bit is set.</span></span><br/>                                                         |
| [<span data-ttu-id="92d5c-121">**IsDataEnciphermentEnabled**</span><span class="sxs-lookup"><span data-stu-id="92d5c-121">**IsDataEnciphermentEnabled**</span></span>](keyusage-isdataenciphermentenabled.md)<br/> | <span data-ttu-id="92d5c-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="92d5c-122">Read-only</span></span><br/> | <span data-ttu-id="92d5c-123">Recupera un valor booleano que indica si se ha establecido el bit dataEncipherment.</span><span class="sxs-lookup"><span data-stu-id="92d5c-123">Retrieves a Boolean value that indicates whether the dataEncipherment bit is set.</span></span><br/>                                                |
| [<span data-ttu-id="92d5c-124">**IsDecipherOnlyEnabled**</span><span class="sxs-lookup"><span data-stu-id="92d5c-124">**IsDecipherOnlyEnabled**</span></span>](keyusage-isdecipheronlyenabled.md)<br/>         | <span data-ttu-id="92d5c-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="92d5c-125">Read-only</span></span><br/> | <span data-ttu-id="92d5c-126">Recupera un valor booleano que indica si se ha establecido el bit decipherOnly.</span><span class="sxs-lookup"><span data-stu-id="92d5c-126">Retrieves a Boolean value that indicates whether the decipherOnly bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="92d5c-127">**IsDigitalSignatureEnabled**</span><span class="sxs-lookup"><span data-stu-id="92d5c-127">**IsDigitalSignatureEnabled**</span></span>](keyusage-isdigitalsignatureenabled.md)<br/> | <span data-ttu-id="92d5c-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="92d5c-128">Read-only</span></span><br/> | <span data-ttu-id="92d5c-129">Recupera un valor booleano que indica si se ha establecido el bit digitalSignature.</span><span class="sxs-lookup"><span data-stu-id="92d5c-129">Retrieves a Boolean value that indicates whether the digitalSignature bit is set.</span></span><br/>                                                |
| [<span data-ttu-id="92d5c-130">**IsEncipherOnlyEnabled**</span><span class="sxs-lookup"><span data-stu-id="92d5c-130">**IsEncipherOnlyEnabled**</span></span>](keyusage-isencipheronlyenabled.md)<br/>         | <span data-ttu-id="92d5c-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="92d5c-131">Read-only</span></span><br/> | <span data-ttu-id="92d5c-132">Recupera un valor booleano que indica si se ha establecido el bit encipherOnly.</span><span class="sxs-lookup"><span data-stu-id="92d5c-132">Retrieves a Boolean value that indicates whether the encipherOnly bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="92d5c-133">**IsKeyAgreementEnabled**</span><span class="sxs-lookup"><span data-stu-id="92d5c-133">**IsKeyAgreementEnabled**</span></span>](keyusage-iskeyagreementenabled.md)<br/>         | <span data-ttu-id="92d5c-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="92d5c-134">Read-only</span></span><br/> | <span data-ttu-id="92d5c-135">Recupera un valor booleano que indica si se ha establecido el bit keyAgreement.</span><span class="sxs-lookup"><span data-stu-id="92d5c-135">Retrieves a Boolean value that indicates whether the keyAgreement bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="92d5c-136">**IsKeyCertSignEnabled**</span><span class="sxs-lookup"><span data-stu-id="92d5c-136">**IsKeyCertSignEnabled**</span></span>](keyusage-iskeycertsignenabled.md)<br/>           | <span data-ttu-id="92d5c-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="92d5c-137">Read-only</span></span><br/> | <span data-ttu-id="92d5c-138">Recupera un valor booleano que indica si se ha establecido el bit bit keycertsign.</span><span class="sxs-lookup"><span data-stu-id="92d5c-138">Retrieves a Boolean value that indicates whether the keyCertSign bit is set.</span></span><br/>                                                     |
| [<span data-ttu-id="92d5c-139">**IsKeyEnciphermentEnabled**</span><span class="sxs-lookup"><span data-stu-id="92d5c-139">**IsKeyEnciphermentEnabled**</span></span>](keyusage-iskeyenciphermentenabled.md)<br/>   | <span data-ttu-id="92d5c-140">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="92d5c-140">Read-only</span></span><br/> | <span data-ttu-id="92d5c-141">Recupera un valor booleano que indica si se ha establecido el bit keyEncipherment.</span><span class="sxs-lookup"><span data-stu-id="92d5c-141">Retrieves a Boolean value that indicates whether the keyEncipherment bit is set.</span></span><br/>                                                 |
| [<span data-ttu-id="92d5c-142">**IsNonRepudiationEnabled**</span><span class="sxs-lookup"><span data-stu-id="92d5c-142">**IsNonRepudiationEnabled**</span></span>](keyusage-isnonrepudiationenabled.md)<br/>     | <span data-ttu-id="92d5c-143">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="92d5c-143">Read-only</span></span><br/> | <span data-ttu-id="92d5c-144">Recupera un valor booleano que indica si se ha establecido el bit nonRepudiationEnabled.</span><span class="sxs-lookup"><span data-stu-id="92d5c-144">Retrieves a Boolean value that indicates whether the nonRepudiationEnabled bit is set.</span></span><br/>                                           |
| [<span data-ttu-id="92d5c-145">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="92d5c-145">**IsPresent**</span></span>](keyusage-ispresent.md)<br/>                                 | <span data-ttu-id="92d5c-146">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="92d5c-146">Read-only</span></span><br/> | <span data-ttu-id="92d5c-147">Recupera un valor booleano que indica si la extensión **KeyUsage** está presente.</span><span class="sxs-lookup"><span data-stu-id="92d5c-147">Retrieves a Boolean value that indicates whether the **KeyUsage** extension is present.</span></span><br/> <span data-ttu-id="92d5c-148">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="92d5c-148">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="92d5c-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92d5c-149">Remarks</span></span>

<span data-ttu-id="92d5c-150">No se puede crear el objeto **KeyUsage** .</span><span class="sxs-lookup"><span data-stu-id="92d5c-150">The **KeyUsage** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="92d5c-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92d5c-151">Requirements</span></span>



| <span data-ttu-id="92d5c-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="92d5c-152">Requirement</span></span> | <span data-ttu-id="92d5c-153">Value</span><span class="sxs-lookup"><span data-stu-id="92d5c-153">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92d5c-154">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="92d5c-154">Redistributable</span></span><br/> | <span data-ttu-id="92d5c-155">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="92d5c-155">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="92d5c-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="92d5c-156">DLL</span></span><br/>             | <dl> <span data-ttu-id="92d5c-157"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92d5c-157"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92d5c-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="92d5c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92d5c-159">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="92d5c-159">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
