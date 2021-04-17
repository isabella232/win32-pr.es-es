---
description: Representa una colección de objetos de firmante.
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: Objeto signers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 75eba0ecb2592bf7efc27ecdd63288179e306651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670525"
---
# <a name="signers-object"></a><span data-ttu-id="0290a-103">Objeto signers</span><span class="sxs-lookup"><span data-stu-id="0290a-103">Signers object</span></span>

<span data-ttu-id="0290a-104">\[El objeto **signers** está disponible para su uso en los sistemas operativos especificados en la sección requirements.</span><span class="sxs-lookup"><span data-stu-id="0290a-104">\[The **Signers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0290a-105">En su lugar, use una colección de objetos CmsSigner.</span><span class="sxs-lookup"><span data-stu-id="0290a-105">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="0290a-106">Para obtener más información, vea la [**clase CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="0290a-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="0290a-107">El objeto de **firma** representa una colección de objetos de [**firmante**](signer.md) .</span><span class="sxs-lookup"><span data-stu-id="0290a-107">The **Signers** object represents a collection of [**Signer**](signer.md) objects.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="0290a-108">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="0290a-108">When to use</span></span>

<span data-ttu-id="0290a-109">El objeto **signers** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="0290a-109">The **Signers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="0290a-110">Recupere el número de certificados de la colección.</span><span class="sxs-lookup"><span data-stu-id="0290a-110">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="0290a-111">Recupera un objeto de **firma** específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="0290a-111">Retrieve a specific **Signers** object from the collection.</span></span>
-   <span data-ttu-id="0290a-112">Recorrer en iteración la colección.</span><span class="sxs-lookup"><span data-stu-id="0290a-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="0290a-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="0290a-113">Members</span></span>

<span data-ttu-id="0290a-114">El objeto **signers** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0290a-114">The **Signers** object has these types of members:</span></span>

-   [<span data-ttu-id="0290a-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0290a-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0290a-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0290a-116">Properties</span></span>

<span data-ttu-id="0290a-117">El objeto **signers** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0290a-117">The **Signers** object has these properties.</span></span>



| <span data-ttu-id="0290a-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0290a-118">Property</span></span>                                        | <span data-ttu-id="0290a-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="0290a-119">Access type</span></span>          | <span data-ttu-id="0290a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="0290a-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0290a-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="0290a-121">**\_NewEnum**</span></span>](signers-newenum.md)<br/> | <span data-ttu-id="0290a-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0290a-122">Read-only</span></span><br/> | <span data-ttu-id="0290a-123">Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="0290a-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="0290a-124">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="0290a-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="0290a-125">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="0290a-125">**Count**</span></span>](signers-count.md)<br/>       | <span data-ttu-id="0290a-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0290a-126">Read-only</span></span><br/> | <span data-ttu-id="0290a-127">Número de objetos de [**firmante**](signer.md) en la colección.</span><span class="sxs-lookup"><span data-stu-id="0290a-127">Number of [**Signer**](signer.md) objects in the collection.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="0290a-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0290a-128">**Item**</span></span>](signers-item.md)<br/>         | <span data-ttu-id="0290a-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0290a-129">Read-only</span></span><br/> | <span data-ttu-id="0290a-130">Recupera el objeto de [**firmante**](signer.md) que representa el firmante indizado.</span><span class="sxs-lookup"><span data-stu-id="0290a-130">Retrieves the [**Signer**](signer.md) object that represents the indexed signer.</span></span> <span data-ttu-id="0290a-131">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0290a-131">This is the default property.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="0290a-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0290a-132">Remarks</span></span>

<span data-ttu-id="0290a-133">No se puede crear el objeto **signers** .</span><span class="sxs-lookup"><span data-stu-id="0290a-133">The **Signers** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="0290a-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0290a-134">Requirements</span></span>



| <span data-ttu-id="0290a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0290a-135">Requirement</span></span> | <span data-ttu-id="0290a-136">Value</span><span class="sxs-lookup"><span data-stu-id="0290a-136">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0290a-137">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0290a-137">Redistributable</span></span><br/> | <span data-ttu-id="0290a-138">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="0290a-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0290a-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0290a-139">DLL</span></span><br/>             | <dl> <span data-ttu-id="0290a-140"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0290a-140"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0290a-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="0290a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0290a-142">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="0290a-142">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
