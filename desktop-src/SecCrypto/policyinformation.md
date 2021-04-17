---
description: Proporciona acceso a la información de la Directiva de una extensión.
ms.assetid: 03d627b3-2d44-4637-97a4-85cdcaf3e4d3
title: Objeto PolicyInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d0cc89d6f993b72763083e69bb88e848134e8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670431"
---
# <a name="policyinformation-object"></a><span data-ttu-id="0b40c-103">Objeto PolicyInformation</span><span class="sxs-lookup"><span data-stu-id="0b40c-103">PolicyInformation object</span></span>

<span data-ttu-id="0b40c-104">\[El objeto **PolicyInformation** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="0b40c-104">\[The **PolicyInformation** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0b40c-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar la información de la Directiva en la extensión de directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="0b40c-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="0b40c-106">El objeto **PolicyInformation** proporciona acceso a la información de la Directiva de una extensión.</span><span class="sxs-lookup"><span data-stu-id="0b40c-106">The **PolicyInformation** object provides access to the policy information of an extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="0b40c-107">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="0b40c-107">When to use</span></span>

<span data-ttu-id="0b40c-108">El objeto **PolicyInformation** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="0b40c-108">The **PolicyInformation** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="0b40c-109">Recupere el OID de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="0b40c-109">Retrieve the policy OID.</span></span>
-   <span data-ttu-id="0b40c-110">Recupera una colección de los calificadores de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="0b40c-110">Retrieve a collection of the policy's qualifiers.</span></span>

## <a name="members"></a><span data-ttu-id="0b40c-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b40c-111">Members</span></span>

<span data-ttu-id="0b40c-112">El objeto **PolicyInformation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0b40c-112">The **PolicyInformation** object has these types of members:</span></span>

-   [<span data-ttu-id="0b40c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b40c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b40c-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b40c-114">Properties</span></span>

<span data-ttu-id="0b40c-115">El objeto **PolicyInformation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0b40c-115">The **PolicyInformation** object has these properties.</span></span>



| <span data-ttu-id="0b40c-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0b40c-116">Property</span></span>                                                      | <span data-ttu-id="0b40c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b40c-117">Description</span></span>                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b40c-118">**OID**</span><span class="sxs-lookup"><span data-stu-id="0b40c-118">**OID**</span></span>](policyinformation-oid.md)<br/>               | <span data-ttu-id="0b40c-119">Recupera el OID de la Directiva, como un objeto [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="0b40c-119">Retrieves the policy's OID, as an [**OID**](oid.md) object.</span></span> <span data-ttu-id="0b40c-120">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0b40c-120">This is the default property.</span></span><br/>       |
| [<span data-ttu-id="0b40c-121">**Calificadores**</span><span class="sxs-lookup"><span data-stu-id="0b40c-121">**Qualifiers**</span></span>](policyinformation-qualifiers.md)<br/> | <span data-ttu-id="0b40c-122">Recupera una colección de los calificadores de la Directiva, como un objeto [**calificadores**](qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="0b40c-122">Retrieves a collection of the policy's qualifiers, as a [**Qualifiers**](qualifiers.md) object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b40c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b40c-123">Remarks</span></span>

<span data-ttu-id="0b40c-124">No se puede crear el objeto **PolicyInformation** .</span><span class="sxs-lookup"><span data-stu-id="0b40c-124">The **PolicyInformation** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b40c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b40c-125">Requirements</span></span>



| <span data-ttu-id="0b40c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b40c-126">Requirement</span></span> | <span data-ttu-id="0b40c-127">Value</span><span class="sxs-lookup"><span data-stu-id="0b40c-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b40c-128">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0b40c-128">Redistributable</span></span><br/> | <span data-ttu-id="0b40c-129">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="0b40c-129">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0b40c-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b40c-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="0b40c-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b40c-131"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
