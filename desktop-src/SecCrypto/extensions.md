---
description: Representa una colección de objetos de extensión.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Extensions (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3af518d6f1918c82d5819b04a086195c06b79740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671021"
---
# <a name="extensions-object"></a><span data-ttu-id="d49c8-103">Extensions (objeto)</span><span class="sxs-lookup"><span data-stu-id="d49c8-103">Extensions object</span></span>

<span data-ttu-id="d49c8-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d49c8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d49c8-105">En su lugar, use la [**clase X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d49c8-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d49c8-106">El objeto **extensions** representa una colección de objetos de [**extensión**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="d49c8-106">The **Extensions** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="d49c8-107">Cada objeto de [**extensión**](extension.md) representa una única extensión de certificado.</span><span class="sxs-lookup"><span data-stu-id="d49c8-107">Each [**Extension**](extension.md) object represents a single certificate extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d49c8-108">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="d49c8-108">When to use</span></span>

<span data-ttu-id="d49c8-109">El objeto de **extensiones** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="d49c8-109">The **Extensions** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="d49c8-110">Recupere el número de extensiones de certificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="d49c8-110">Retrieve the number of certificate extensions in the collection.</span></span>
-   <span data-ttu-id="d49c8-111">Recupera un objeto de [**extensión**](extension.md) específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="d49c8-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="d49c8-112">Recorrer en iteración la colección.</span><span class="sxs-lookup"><span data-stu-id="d49c8-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="d49c8-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="d49c8-113">Members</span></span>

<span data-ttu-id="d49c8-114">El objeto **extensions** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d49c8-114">The **Extensions** object has these types of members:</span></span>

-   [<span data-ttu-id="d49c8-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d49c8-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d49c8-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d49c8-116">Properties</span></span>

<span data-ttu-id="d49c8-117">El objeto **extensions** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d49c8-117">The **Extensions** object has these properties.</span></span>



| <span data-ttu-id="d49c8-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d49c8-118">Property</span></span>                                           | <span data-ttu-id="d49c8-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="d49c8-119">Access type</span></span>          | <span data-ttu-id="d49c8-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d49c8-120">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d49c8-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="d49c8-121">**\_NewEnum**</span></span>](extensions-newenum.md)<br/> | <span data-ttu-id="d49c8-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49c8-122">Read-only</span></span><br/> | <span data-ttu-id="d49c8-123">Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="d49c8-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="d49c8-124">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="d49c8-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="d49c8-125">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="d49c8-125">**Count**</span></span>](extensions-count.md)<br/>       | <span data-ttu-id="d49c8-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49c8-126">Read-only</span></span><br/> | <span data-ttu-id="d49c8-127">Recupera el número de objetos de [**extensión**](extension.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="d49c8-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="d49c8-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d49c8-128">**Item**</span></span>](extensions-item.md)<br/>         | <span data-ttu-id="d49c8-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49c8-129">Read-only</span></span><br/> | <span data-ttu-id="d49c8-130">Recupera el objeto de [**extensión**](extension.md) que representa la extensión de certificado indizada de la colección.</span><span class="sxs-lookup"><span data-stu-id="d49c8-130">Retrieves the [**Extension**](extension.md) object that represents the indexed certificate extension of the collection.</span></span> <span data-ttu-id="d49c8-131">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d49c8-131">This is the default property.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="d49c8-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d49c8-132">Remarks</span></span>

<span data-ttu-id="d49c8-133">El método [**Certificate. Extensions**](certificate-extensions.md) devuelve el objeto **extensions** .</span><span class="sxs-lookup"><span data-stu-id="d49c8-133">The **Extensions** object is returned by the [**Certificate.Extensions**](certificate-extensions.md) method.</span></span>

<span data-ttu-id="d49c8-134">No se puede crear el objeto **extensions** .</span><span class="sxs-lookup"><span data-stu-id="d49c8-134">The **Extensions** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="d49c8-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d49c8-135">Requirements</span></span>



| <span data-ttu-id="d49c8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d49c8-136">Requirement</span></span> | <span data-ttu-id="d49c8-137">Value</span><span class="sxs-lookup"><span data-stu-id="d49c8-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d49c8-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d49c8-138">End of client support</span></span><br/> | <span data-ttu-id="d49c8-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d49c8-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d49c8-140">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d49c8-140">End of server support</span></span><br/> | <span data-ttu-id="d49c8-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d49c8-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d49c8-142">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d49c8-142">Redistributable</span></span><br/>       | <span data-ttu-id="d49c8-143">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="d49c8-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d49c8-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d49c8-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d49c8-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d49c8-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
