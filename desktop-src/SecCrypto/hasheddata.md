---
description: Proporciona funcionalidad para aplicar un algoritmo hash a una cadena.
ms.assetid: 893639c2-57b9-48f6-bf60-a21c3368ffeb
title: Objeto HashedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b6e54d7d2ca52ceafe500615af4063dfc7310b0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670573"
---
# <a name="hasheddata-object"></a><span data-ttu-id="2345e-103">Objeto HashedData</span><span class="sxs-lookup"><span data-stu-id="2345e-103">HashedData object</span></span>

<span data-ttu-id="2345e-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2345e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2345e-105">En su lugar, use la [**clase HashAlgorithm**](/previous-versions/windows/) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="2345e-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="2345e-106">El objeto **HashedData** proporciona funcionalidad para aplicar un algoritmo hash a una cadena.</span><span class="sxs-lookup"><span data-stu-id="2345e-106">The **HashedData** object provides functionality for hashing a string.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="2345e-107">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="2345e-107">When to use</span></span>

<span data-ttu-id="2345e-108">El objeto **HashedData** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="2345e-108">The **HashedData** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="2345e-109">Especifique la cadena de contenido que contiene los datos a los que se va a aplicar un algoritmo hash.</span><span class="sxs-lookup"><span data-stu-id="2345e-109">Specify the content string that contains the data to be hashed.</span></span>
-   <span data-ttu-id="2345e-110">Aplique un algoritmo hash especificado a la cadena de contenido.</span><span class="sxs-lookup"><span data-stu-id="2345e-110">Apply a specified hash algorithm to the content string.</span></span>

## <a name="members"></a><span data-ttu-id="2345e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2345e-111">Members</span></span>

<span data-ttu-id="2345e-112">El objeto **HashedData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2345e-112">The **HashedData** object has these types of members:</span></span>

-   [<span data-ttu-id="2345e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2345e-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="2345e-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2345e-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2345e-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="2345e-115">Methods</span></span>

<span data-ttu-id="2345e-116">El objeto **HashedData** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2345e-116">The **HashedData** object has these methods.</span></span>



| <span data-ttu-id="2345e-117">Método</span><span class="sxs-lookup"><span data-stu-id="2345e-117">Method</span></span>                          | <span data-ttu-id="2345e-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="2345e-118">Description</span></span>                                        |
|:--------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="2345e-119">**LM**</span><span class="sxs-lookup"><span data-stu-id="2345e-119">**Hash**</span></span>](hasheddata-hash.md) | <span data-ttu-id="2345e-120">Crea un hash de la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="2345e-120">Creates a hash of the specified string.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2345e-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2345e-121">Properties</span></span>

<span data-ttu-id="2345e-122">El objeto **HashedData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2345e-122">The **HashedData** object has these properties.</span></span>



| <span data-ttu-id="2345e-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2345e-123">Property</span></span>                                             | <span data-ttu-id="2345e-124">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="2345e-124">Access type</span></span>           | <span data-ttu-id="2345e-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="2345e-125">Description</span></span>                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2345e-126">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="2345e-126">**Algorithm**</span></span>](hasheddata-algorithm.md)<br/> | <span data-ttu-id="2345e-127">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2345e-127">Read/write</span></span><br/> | <span data-ttu-id="2345e-128">Establece o recupera el tipo de algoritmo hash que se usa.</span><span class="sxs-lookup"><span data-stu-id="2345e-128">Sets or retrieves the type of hashing algorithm used.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="2345e-129">**Value**</span><span class="sxs-lookup"><span data-stu-id="2345e-129">**Value**</span></span>](hasheddata-value.md)<br/>         | <span data-ttu-id="2345e-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="2345e-130">Read-only</span></span><br/>  | <span data-ttu-id="2345e-131">Recupera los datos a los que se ha aplicado un algoritmo hash después de llamar correctamente al método [**hash**](hasheddata-hash.md) .</span><span class="sxs-lookup"><span data-stu-id="2345e-131">Retrieves the hashed data after successful calls to the [**Hash**](hasheddata-hash.md) method.</span></span> <span data-ttu-id="2345e-132">El hash se devuelve en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="2345e-132">The hash is returned in hexadecimal format.</span></span> <span data-ttu-id="2345e-133">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2345e-133">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2345e-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2345e-134">Remarks</span></span>

<span data-ttu-id="2345e-135">Para crear el hash de una gran cantidad de datos, llame al método [**hash**](hasheddata-hash.md) para cada fragmento de datos.</span><span class="sxs-lookup"><span data-stu-id="2345e-135">To create the hash of a large amount of data, call the [**Hash**](hasheddata-hash.md) method for each piece of data.</span></span> <span data-ttu-id="2345e-136">El hash de cada fragmento de datos se concatena a la propiedad [**Value**](hasheddata-value.md) hasta que se lee la propiedad.</span><span class="sxs-lookup"><span data-stu-id="2345e-136">The hash of each piece of data is concatenated to the [**Value**](hasheddata-value.md) property until the property is read.</span></span> <span data-ttu-id="2345e-137">El contenido de la propiedad **Value** se restablece cuando se lee la propiedad.</span><span class="sxs-lookup"><span data-stu-id="2345e-137">The contents of the **Value** property are reset when the property is read.</span></span>

<span data-ttu-id="2345e-138">Se puede crear el objeto **HashedData** y es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="2345e-138">The **HashedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="2345e-139">El identificador de programa (ProgID) del objeto **HashedData** es "CAPICOM. HashedData. 1 ".</span><span class="sxs-lookup"><span data-stu-id="2345e-139">The ProgID for the **HashedData** object is "CAPICOM.HashedData.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="2345e-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2345e-140">Requirements</span></span>



| <span data-ttu-id="2345e-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="2345e-141">Requirement</span></span> | <span data-ttu-id="2345e-142">Value</span><span class="sxs-lookup"><span data-stu-id="2345e-142">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2345e-143">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2345e-143">End of client support</span></span><br/> | <span data-ttu-id="2345e-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2345e-144">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2345e-145">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="2345e-145">End of server support</span></span><br/> | <span data-ttu-id="2345e-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2345e-146">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2345e-147">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="2345e-147">Redistributable</span></span><br/>       | <span data-ttu-id="2345e-148">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="2345e-148">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2345e-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2345e-149">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2345e-150"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2345e-150"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
