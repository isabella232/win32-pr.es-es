---
description: Representa una colección de calificadores.
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: Qualifiers (objeto) (iAds. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e873019d6fbfb21de8be430d7960f697b39eeca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690264"
---
# <a name="qualifiers-object"></a><span data-ttu-id="5ee5c-103">Calificadors (objeto)</span><span class="sxs-lookup"><span data-stu-id="5ee5c-103">Qualifiers object</span></span>

<span data-ttu-id="5ee5c-104">\[El objeto **calificadores** está disponible para su uso en los sistemas operativos especificados en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="5ee5c-104">\[The **Qualifiers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5ee5c-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="5ee5c-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="5ee5c-106">El objeto **Qualifiers** representa una colección de calificadores.</span><span class="sxs-lookup"><span data-stu-id="5ee5c-106">The **Qualifiers** object represents a collection of qualifiers.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="5ee5c-107">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="5ee5c-107">When to use</span></span>

<span data-ttu-id="5ee5c-108">El objeto **calificadores** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="5ee5c-108">The **Qualifiers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="5ee5c-109">Recupera una propiedad extendida específica de la colección.</span><span class="sxs-lookup"><span data-stu-id="5ee5c-109">Retrieve a specific extended property from the collection.</span></span>
-   <span data-ttu-id="5ee5c-110">Recupere el número de propiedades extendidas de la colección.</span><span class="sxs-lookup"><span data-stu-id="5ee5c-110">Retrieve the number of extended properties in the collection.</span></span>
-   <span data-ttu-id="5ee5c-111">Recorrer en iteración la colección.</span><span class="sxs-lookup"><span data-stu-id="5ee5c-111">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="5ee5c-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="5ee5c-112">Members</span></span>

<span data-ttu-id="5ee5c-113">El objeto **Qualifiers** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5ee5c-113">The **Qualifiers** object has these types of members:</span></span>

-   [<span data-ttu-id="5ee5c-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5ee5c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ee5c-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5ee5c-115">Properties</span></span>

<span data-ttu-id="5ee5c-116">El objeto **Qualifiers** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5ee5c-116">The **Qualifiers** object has these properties.</span></span>



| <span data-ttu-id="5ee5c-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5ee5c-117">Property</span></span>                                           | <span data-ttu-id="5ee5c-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="5ee5c-118">Access type</span></span>          | <span data-ttu-id="5ee5c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ee5c-119">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ee5c-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="5ee5c-120">**\_NewEnum**</span></span>](qualifiers-newenum.md)<br/> | <span data-ttu-id="5ee5c-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5ee5c-121">Read-only</span></span><br/> | <span data-ttu-id="5ee5c-122">Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="5ee5c-122">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="5ee5c-123">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="5ee5c-123">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="5ee5c-124">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="5ee5c-124">**Count**</span></span>](qualifiers-count.md)<br/>       | <span data-ttu-id="5ee5c-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5ee5c-125">Read-only</span></span><br/> | <span data-ttu-id="5ee5c-126">Recupera el número de calificadores de la colección.</span><span class="sxs-lookup"><span data-stu-id="5ee5c-126">Retrieves the number of qualifiers in the collection.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="5ee5c-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5ee5c-127">**Item**</span></span>](qualifiers-item.md)<br/>         | <span data-ttu-id="5ee5c-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5ee5c-128">Read-only</span></span><br/> | <span data-ttu-id="5ee5c-129">Recupera un objeto [**calificador**](qualifier.md) que representa el calificador indizado de la colección.</span><span class="sxs-lookup"><span data-stu-id="5ee5c-129">Retrieves a [**Qualifier**](qualifier.md) object that represents the indexed qualifier of the collection.</span></span> <span data-ttu-id="5ee5c-130">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5ee5c-130">This is the default property.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="5ee5c-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ee5c-131">Remarks</span></span>

<span data-ttu-id="5ee5c-132">No se puede crear el objeto **calificadores** .</span><span class="sxs-lookup"><span data-stu-id="5ee5c-132">The **Qualifiers** object cannot be created.</span></span>

<span data-ttu-id="5ee5c-133">La propiedad de objeto [**PolicyInformation. Qualifiers**](policyinformation-qualifiers.md) CAPICOM devuelve un objeto de **calificadores** .</span><span class="sxs-lookup"><span data-stu-id="5ee5c-133">The [**PolicyInformation.Qualifiers**](policyinformation-qualifiers.md) CAPICOM object property returns a **Qualifiers** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ee5c-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ee5c-134">Requirements</span></span>



| <span data-ttu-id="5ee5c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ee5c-135">Requirement</span></span> | <span data-ttu-id="5ee5c-136">Value</span><span class="sxs-lookup"><span data-stu-id="5ee5c-136">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee5c-137">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="5ee5c-137">Redistributable</span></span><br/> | <span data-ttu-id="5ee5c-138">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="5ee5c-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5ee5c-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ee5c-139">Header</span></span><br/>          | <dl> <span data-ttu-id="5ee5c-140"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ee5c-140"><dt>Iads.h</dt></span></span> </dl>      |
| <span data-ttu-id="5ee5c-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ee5c-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="5ee5c-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ee5c-142"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
