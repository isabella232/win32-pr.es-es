---
description: Representa una colección de objetos EKU.
ms.assetid: 04b9f0bf-e1d4-4a2c-be5d-bae7c1090bdb
title: EKU (objeto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 56fd6eaeb5a00549cbb4ee659b99ece391e0ebed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671431"
---
# <a name="ekus-object"></a><span data-ttu-id="aa582-103">EKU (objeto)</span><span class="sxs-lookup"><span data-stu-id="aa582-103">EKUs object</span></span>

<span data-ttu-id="aa582-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aa582-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="aa582-105">En su lugar, use la [**clase X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="aa582-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="aa582-106">El objeto **EKU** representa una colección de objetos [**EKU**](eku.md) .</span><span class="sxs-lookup"><span data-stu-id="aa582-106">The **EKUs** object represents a collection of [**EKU**](eku.md) objects.</span></span> <span data-ttu-id="aa582-107">Cada objeto [**EKU**](eku.md) representa una única propiedad de uso de clave extendida (EKU) de un certificado.</span><span class="sxs-lookup"><span data-stu-id="aa582-107">Each [**EKU**](eku.md) object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="aa582-108">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="aa582-108">When to use</span></span>

<span data-ttu-id="aa582-109">La colección **EKU** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="aa582-109">The **EKUs** collection is used to perform the following tasks:</span></span>

-   <span data-ttu-id="aa582-110">Recupere el número de propiedades EKU de la colección.</span><span class="sxs-lookup"><span data-stu-id="aa582-110">Retrieve the number of EKU properties in the collection.</span></span>
-   <span data-ttu-id="aa582-111">Recupera un objeto [**EKU**](eku.md) específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="aa582-111">Retrieve a specific [**EKU**](eku.md) object from the collection.</span></span>
-   <span data-ttu-id="aa582-112">Recorrer en iteración la colección.</span><span class="sxs-lookup"><span data-stu-id="aa582-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="aa582-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa582-113">Members</span></span>

<span data-ttu-id="aa582-114">El objeto **EKU** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="aa582-114">The **EKUs** object has these types of members:</span></span>

-   [<span data-ttu-id="aa582-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa582-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa582-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa582-116">Properties</span></span>

<span data-ttu-id="aa582-117">El objeto **EKU** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="aa582-117">The **EKUs** object has these properties.</span></span>



| <span data-ttu-id="aa582-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aa582-118">Property</span></span>                                     | <span data-ttu-id="aa582-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="aa582-119">Access type</span></span>          | <span data-ttu-id="aa582-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa582-120">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa582-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="aa582-121">**\_NewEnum**</span></span>](ekus-newenum.md)<br/> | <span data-ttu-id="aa582-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa582-122">Read-only</span></span><br/> | <span data-ttu-id="aa582-123">Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="aa582-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="aa582-124">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="aa582-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="aa582-125">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="aa582-125">**Count**</span></span>](ekus-count.md)<br/>       | <span data-ttu-id="aa582-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa582-126">Read-only</span></span><br/> | <span data-ttu-id="aa582-127">Recupera el número de objetos [**EKU**](eku.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="aa582-127">Retrieves the number of [**EKU**](eku.md) objects in the collection.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="aa582-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aa582-128">**Item**</span></span>](ekus-item.md)<br/>         | <span data-ttu-id="aa582-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa582-129">Read-only</span></span><br/> | <span data-ttu-id="aa582-130">Recupera el objeto [**EKU**](eku.md) que representa la propiedad de EKU indizado.</span><span class="sxs-lookup"><span data-stu-id="aa582-130">Retrieves the [**EKU**](eku.md) object that represents the indexed EKU property.</span></span> <span data-ttu-id="aa582-131">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="aa582-131">This is the default property.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="aa582-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa582-132">Remarks</span></span>

<span data-ttu-id="aa582-133">La propiedad [**ExtendedKeyUsage. EKU**](extendedkeyusage-ekus.md) recupera esta colección.</span><span class="sxs-lookup"><span data-stu-id="aa582-133">This collection is retrieved by the [**ExtendedKeyUsage.EKUs**](extendedkeyusage-ekus.md) property.</span></span>

<span data-ttu-id="aa582-134">No se puede crear el objeto **EKU** .</span><span class="sxs-lookup"><span data-stu-id="aa582-134">The **EKUs** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa582-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa582-135">Requirements</span></span>



| <span data-ttu-id="aa582-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa582-136">Requirement</span></span> | <span data-ttu-id="aa582-137">Value</span><span class="sxs-lookup"><span data-stu-id="aa582-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa582-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="aa582-138">End of client support</span></span><br/> | <span data-ttu-id="aa582-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa582-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="aa582-140">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="aa582-140">End of server support</span></span><br/> | <span data-ttu-id="aa582-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa582-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aa582-142">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="aa582-142">Redistributable</span></span><br/>       | <span data-ttu-id="aa582-143">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="aa582-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="aa582-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa582-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="aa582-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa582-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
