---
description: Colección de objetos PolicyInformation.
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: Objeto CertificatePolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8ec217276b5d038f85f33887b771b0afa0c6e40a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690392"
---
# <a name="certificatepolicies-object"></a><span data-ttu-id="17b45-103">Objeto CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="17b45-103">CertificatePolicies object</span></span>

<span data-ttu-id="17b45-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="17b45-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="17b45-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para que las directivas de certificado recuperen las directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="17b45-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="17b45-106">El objeto **CertificatePolicies** representa una colección de objetos [**PolicyInformation**](policyinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="17b45-106">The **CertificatePolicies** object represents a collection of [**PolicyInformation**](policyinformation.md) objects.</span></span> <span data-ttu-id="17b45-107">Cada objeto [**PolicyInformation**](policyinformation.md) representa una única directiva de certificado.</span><span class="sxs-lookup"><span data-stu-id="17b45-107">Each [**PolicyInformation**](policyinformation.md) object represents a single certificate policy.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="17b45-108">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="17b45-108">When to use</span></span>

<span data-ttu-id="17b45-109">El objeto **CertificatePolicies** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="17b45-109">The **CertificatePolicies** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="17b45-110">Recupere el número de directivas de certificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="17b45-110">Retrieve the number of certificate policies in the collection.</span></span>
-   <span data-ttu-id="17b45-111">Recupera un objeto [**PolicyInformation**](policyinformation.md) específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="17b45-111">Retrieve a specific [**PolicyInformation**](policyinformation.md) object from the collection.</span></span>
-   <span data-ttu-id="17b45-112">Recorrer en iteración la colección.</span><span class="sxs-lookup"><span data-stu-id="17b45-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="17b45-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="17b45-113">Members</span></span>

<span data-ttu-id="17b45-114">El objeto **CertificatePolicies** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="17b45-114">The **CertificatePolicies** object has these types of members:</span></span>

-   [<span data-ttu-id="17b45-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17b45-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17b45-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17b45-116">Properties</span></span>

<span data-ttu-id="17b45-117">El objeto **CertificatePolicies** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="17b45-117">The **CertificatePolicies** object has these properties.</span></span>



| <span data-ttu-id="17b45-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="17b45-118">Property</span></span>                                                    | <span data-ttu-id="17b45-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="17b45-119">Access type</span></span>          | <span data-ttu-id="17b45-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="17b45-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17b45-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="17b45-121">**\_NewEnum**</span></span>](certificatepolicies-newenum.md)<br/> | <span data-ttu-id="17b45-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="17b45-122">Read-only</span></span><br/> | <span data-ttu-id="17b45-123">Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="17b45-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="17b45-124">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="17b45-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="17b45-125">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="17b45-125">**Count**</span></span>](certificatepolicies-count.md)<br/>       | <span data-ttu-id="17b45-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="17b45-126">Read-only</span></span><br/> | <span data-ttu-id="17b45-127">Recupera el número de objetos [**PolicyInformation**](policyinformation.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="17b45-127">Retrieves the number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="17b45-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="17b45-128">**Item**</span></span>](certificatepolicies-item.md)<br/>         | <span data-ttu-id="17b45-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="17b45-129">Read-only</span></span><br/> | <span data-ttu-id="17b45-130">Recupera un objeto [**PolicyInformation**](policyinformation.md) que representa la Directiva de certificado indizada de la colección.</span><span class="sxs-lookup"><span data-stu-id="17b45-130">Retrieves a [**PolicyInformation**](policyinformation.md) object that represents the indexed certificate policy of the collection.</span></span> <span data-ttu-id="17b45-131">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="17b45-131">This is the default property.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="17b45-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17b45-132">Remarks</span></span>

<span data-ttu-id="17b45-133">No se puede crear el objeto **CertificatePolicies** .</span><span class="sxs-lookup"><span data-stu-id="17b45-133">The **CertificatePolicies** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b45-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17b45-134">Requirements</span></span>



| <span data-ttu-id="17b45-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="17b45-135">Requirement</span></span> | <span data-ttu-id="17b45-136">Value</span><span class="sxs-lookup"><span data-stu-id="17b45-136">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17b45-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="17b45-137">End of client support</span></span><br/> | <span data-ttu-id="17b45-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17b45-138">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="17b45-139">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="17b45-139">End of server support</span></span><br/> | <span data-ttu-id="17b45-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17b45-140">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="17b45-141">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="17b45-141">Redistributable</span></span><br/>       | <span data-ttu-id="17b45-142">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="17b45-142">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="17b45-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="17b45-143">DLL</span></span><br/>                   | <dl> <span data-ttu-id="17b45-144"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17b45-144"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
