---
description: Representa un puntero de informe de prácticas de certificación (CPS) o el calificador de aviso de usuario.
ms.assetid: 857af3d6-aa7b-429a-a056-72573232f72c
title: Objeto de calificador
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1740e064cac53f93d9c81603477a1230c7fd7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649861"
---
# <a name="qualifier-object"></a><span data-ttu-id="dee04-103">Objeto de calificador</span><span class="sxs-lookup"><span data-stu-id="dee04-103">Qualifier object</span></span>

<span data-ttu-id="dee04-104">\[El objeto de **calificador** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="dee04-104">\[The **Qualifier** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dee04-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="dee04-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="dee04-106">El objeto **calificador** representa un puntero de declaración de prácticas de certificación (CPS) o un calificador de aviso de usuario.</span><span class="sxs-lookup"><span data-stu-id="dee04-106">The **Qualifier** object represents a Certification Practice Statement (CPS) pointer or user notice qualifier.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="dee04-107">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="dee04-107">When to use</span></span>

<span data-ttu-id="dee04-108">El objeto **calificador** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="dee04-108">The **Qualifier** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="dee04-109">Recupere el identificador de objeto del calificador.</span><span class="sxs-lookup"><span data-stu-id="dee04-109">Retrieve the object identifier of the qualifier.</span></span>
-   <span data-ttu-id="dee04-110">Recupere el identificador uniforme de recursos (URI) que señala a una CPS publicada por la [*entidad de certificación*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="dee04-110">Retrieve the Uniform Resource Identifier (URI) that points to a CPS published by the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>
-   <span data-ttu-id="dee04-111">Recupere el nombre de la organización asociada con el calificador.</span><span class="sxs-lookup"><span data-stu-id="dee04-111">Retrieve the name of the organization associated with the qualifier.</span></span>
-   <span data-ttu-id="dee04-112">Recupere el nombre y el contenido de un aviso de usuario.</span><span class="sxs-lookup"><span data-stu-id="dee04-112">Retrieve the name and content of a user notice.</span></span>

## <a name="members"></a><span data-ttu-id="dee04-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="dee04-113">Members</span></span>

<span data-ttu-id="dee04-114">El objeto **calificador** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dee04-114">The **Qualifier** object has these types of members:</span></span>

-   [<span data-ttu-id="dee04-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dee04-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dee04-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dee04-116">Properties</span></span>

<span data-ttu-id="dee04-117">El objeto **calificador** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dee04-117">The **Qualifier** object has these properties.</span></span>



| <span data-ttu-id="dee04-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dee04-118">Property</span></span>                                                          | <span data-ttu-id="dee04-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="dee04-119">Access type</span></span>          | <span data-ttu-id="dee04-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="dee04-120">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dee04-121">**CPSPointer**</span><span class="sxs-lookup"><span data-stu-id="dee04-121">**CPSPointer**</span></span>](qualifier-cpspointer.md)<br/>             | <span data-ttu-id="dee04-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dee04-122">Read-only</span></span><br/> | <span data-ttu-id="dee04-123">Recupera una cadena que contiene el URI que apunta a una CPS publicada por la CA.</span><span class="sxs-lookup"><span data-stu-id="dee04-123">Retrieves a string that contains the URI that points to a CPS published by the CA.</span></span><br/>                                       |
| [<span data-ttu-id="dee04-124">**ExplicitText**</span><span class="sxs-lookup"><span data-stu-id="dee04-124">**ExplicitText**</span></span>](qualifier-explicittext.md)<br/>         | <span data-ttu-id="dee04-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dee04-125">Read-only</span></span><br/> | <span data-ttu-id="dee04-126">Recupera una cadena que incluye el contenido del aviso de usuario.</span><span class="sxs-lookup"><span data-stu-id="dee04-126">Retrieves a string that contains the content of the user notice.</span></span> <span data-ttu-id="dee04-127">Esta propiedad puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="dee04-127">This property may be empty.</span></span><br/>                             |
| [<span data-ttu-id="dee04-128">**NoticeNumbers**</span><span class="sxs-lookup"><span data-stu-id="dee04-128">**NoticeNumbers**</span></span>](qualifier-noticenumbers.md)<br/>       | <span data-ttu-id="dee04-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dee04-129">Read-only</span></span><br/> | <span data-ttu-id="dee04-130">Recupera un objeto **NoticeNumbers** que contiene la colección de números de aviso de usuario.</span><span class="sxs-lookup"><span data-stu-id="dee04-130">Retrieves a **NoticeNumbers** object that contains the collection of user notice numbers.</span></span> <span data-ttu-id="dee04-131">Esta propiedad puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="dee04-131">This property may be empty.</span></span><br/>    |
| [<span data-ttu-id="dee04-132">**OID**</span><span class="sxs-lookup"><span data-stu-id="dee04-132">**OID**</span></span>](qualifier-oid.md)<br/>                           | <span data-ttu-id="dee04-133">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dee04-133">Read-only</span></span><br/> | <span data-ttu-id="dee04-134">Recupera un objeto [**OID**](oid.md) que identifica el calificador.</span><span class="sxs-lookup"><span data-stu-id="dee04-134">Retrieves an [**OID**](oid.md) object that identifies the qualifier.</span></span> <span data-ttu-id="dee04-135">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="dee04-135">This is the default property.</span></span><br/>                      |
| [<span data-ttu-id="dee04-136">**OrganizationName**</span><span class="sxs-lookup"><span data-stu-id="dee04-136">**OrganizationName**</span></span>](qualifier-organizationname.md)<br/> | <span data-ttu-id="dee04-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dee04-137">Read-only</span></span><br/> | <span data-ttu-id="dee04-138">Recupera una cadena que contiene el nombre de la organización asociada al calificador.</span><span class="sxs-lookup"><span data-stu-id="dee04-138">Retrieves a string that contains the name of the organization associated with the qualifier.</span></span> <span data-ttu-id="dee04-139">Esta propiedad puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="dee04-139">This property may be empty.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dee04-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dee04-140">Remarks</span></span>

<span data-ttu-id="dee04-141">No se puede crear el objeto de **calificador** .</span><span class="sxs-lookup"><span data-stu-id="dee04-141">The **Qualifier** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee04-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dee04-142">Requirements</span></span>



| <span data-ttu-id="dee04-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="dee04-143">Requirement</span></span> | <span data-ttu-id="dee04-144">Value</span><span class="sxs-lookup"><span data-stu-id="dee04-144">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dee04-145">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="dee04-145">Redistributable</span></span><br/> | <span data-ttu-id="dee04-146">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="dee04-146">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="dee04-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dee04-147">DLL</span></span><br/>             | <dl> <span data-ttu-id="dee04-148"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dee04-148"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
