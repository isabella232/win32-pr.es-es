---
description: Representa un bloque de datos codificados ASN. 1.
ms.assetid: af7acc5f-da0a-4235-8496-05db94664ea5
title: Objeto EncodedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d05fce31ad4ef08bf9f573c0158a683bdbeba739
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671713"
---
# <a name="encodeddata-object"></a><span data-ttu-id="3f98e-103">Objeto EncodedData</span><span class="sxs-lookup"><span data-stu-id="3f98e-103">EncodedData object</span></span>

<span data-ttu-id="3f98e-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3f98e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3f98e-105">En su lugar, use la [**clase AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="3f98e-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="3f98e-106">El objeto **EncodedData** representa un bloque de datos codificados ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="3f98e-106">The **EncodedData** object represents a block of ASN.1 encoded data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="3f98e-107">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="3f98e-107">When to use</span></span>

<span data-ttu-id="3f98e-108">Varias propiedades de objeto de CAPICOM devuelven el objeto **EncodedData** .</span><span class="sxs-lookup"><span data-stu-id="3f98e-108">The **EncodedData** object is returned by several CAPICOM object properties.</span></span> <span data-ttu-id="3f98e-109">Cuando se devuelve, este objeto se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="3f98e-109">When returned, this object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="3f98e-110">Obtener una representación de cadena de los datos codificados.</span><span class="sxs-lookup"><span data-stu-id="3f98e-110">Obtain a string representation of the encoded data.</span></span>
-   <span data-ttu-id="3f98e-111">Obtiene el objeto descodificador, si existe, que está asociado a los datos codificados.</span><span class="sxs-lookup"><span data-stu-id="3f98e-111">Obtain the decoder object, if it exists, that is associated with the encoded data.</span></span>
-   <span data-ttu-id="3f98e-112">Determine el tipo de datos codificados.</span><span class="sxs-lookup"><span data-stu-id="3f98e-112">Determine the type of encoded data.</span></span>

## <a name="members"></a><span data-ttu-id="3f98e-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="3f98e-113">Members</span></span>

<span data-ttu-id="3f98e-114">El objeto **EncodedData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3f98e-114">The **EncodedData** object has these types of members:</span></span>

-   [<span data-ttu-id="3f98e-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="3f98e-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="3f98e-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3f98e-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3f98e-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="3f98e-117">Methods</span></span>

<span data-ttu-id="3f98e-118">El objeto **EncodedData** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3f98e-118">The **EncodedData** object has these methods.</span></span>



| <span data-ttu-id="3f98e-119">Método</span><span class="sxs-lookup"><span data-stu-id="3f98e-119">Method</span></span>                                 | <span data-ttu-id="3f98e-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f98e-120">Description</span></span>                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="3f98e-121">**Descodificador**</span><span class="sxs-lookup"><span data-stu-id="3f98e-121">**Decoder**</span></span>](encodeddata-decoder.md) | <span data-ttu-id="3f98e-122">Obtiene un objeto descodificador, si existe uno.</span><span class="sxs-lookup"><span data-stu-id="3f98e-122">Obtains a decoder object, if one exists.</span></span><br/>             |
| [<span data-ttu-id="3f98e-123">**Aplique**</span><span class="sxs-lookup"><span data-stu-id="3f98e-123">**Format**</span></span>](encodeddata-format.md)   | <span data-ttu-id="3f98e-124">Devuelve una representación de cadena de los datos codificados.</span><span class="sxs-lookup"><span data-stu-id="3f98e-124">Returns a string representation of the encoded data.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3f98e-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3f98e-125">Properties</span></span>

<span data-ttu-id="3f98e-126">El objeto **EncodedData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3f98e-126">The **EncodedData** object has these properties.</span></span>



| <span data-ttu-id="3f98e-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3f98e-127">Property</span></span>                                      | <span data-ttu-id="3f98e-128">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="3f98e-128">Access type</span></span>          | <span data-ttu-id="3f98e-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f98e-129">Description</span></span>                                                          |
|:----------------------------------------------|:---------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="3f98e-130">**Value**</span><span class="sxs-lookup"><span data-stu-id="3f98e-130">**Value**</span></span>](encodeddata-value.md)<br/> | <span data-ttu-id="3f98e-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3f98e-131">Read-only</span></span><br/> | <span data-ttu-id="3f98e-132">Recupera los datos codificados.</span><span class="sxs-lookup"><span data-stu-id="3f98e-132">Retrieves the encoded data.</span></span> <span data-ttu-id="3f98e-133">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3f98e-133">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3f98e-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f98e-134">Remarks</span></span>

<span data-ttu-id="3f98e-135">El único tipo admitido de datos codificados es [**CertificatePolicies**](certificatepolicies.md).</span><span class="sxs-lookup"><span data-stu-id="3f98e-135">The only supported type of encoded data is [**CertificatePolicies**](certificatepolicies.md).</span></span>

<span data-ttu-id="3f98e-136">No se puede crear el objeto **EncodedData** .</span><span class="sxs-lookup"><span data-stu-id="3f98e-136">The **EncodedData** object cannot be created.</span></span>

<span data-ttu-id="3f98e-137">Las siguientes propiedades de objeto CAPICOM devuelven un objeto **EncodedData** :</span><span class="sxs-lookup"><span data-stu-id="3f98e-137">The following CAPICOM object properties return an **EncodedData** object:</span></span>

-   <span data-ttu-id="3f98e-138">**PublicKey. EncodedKey**</span><span class="sxs-lookup"><span data-stu-id="3f98e-138">**PublicKey.EncodedKey**</span></span>
-   <span data-ttu-id="3f98e-139">**PublicKey. EncodedParameters**</span><span class="sxs-lookup"><span data-stu-id="3f98e-139">**PublicKey.EncodedParameters**</span></span>
-   <span data-ttu-id="3f98e-140">**Extensión. EncodedData**</span><span class="sxs-lookup"><span data-stu-id="3f98e-140">**Extension.EncodedData**</span></span>
-   <span data-ttu-id="3f98e-141">**Policy. EncodedData**</span><span class="sxs-lookup"><span data-stu-id="3f98e-141">**Policy.EncodedData**</span></span>

## <a name="requirements"></a><span data-ttu-id="3f98e-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f98e-142">Requirements</span></span>



| <span data-ttu-id="3f98e-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f98e-143">Requirement</span></span> | <span data-ttu-id="3f98e-144">Value</span><span class="sxs-lookup"><span data-stu-id="3f98e-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f98e-145">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3f98e-145">End of client support</span></span><br/> | <span data-ttu-id="3f98e-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f98e-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3f98e-147">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3f98e-147">End of server support</span></span><br/> | <span data-ttu-id="3f98e-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f98e-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3f98e-149">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3f98e-149">Redistributable</span></span><br/>       | <span data-ttu-id="3f98e-150">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="3f98e-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3f98e-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f98e-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3f98e-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f98e-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
