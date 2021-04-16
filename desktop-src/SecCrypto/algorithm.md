---
description: Especifica el algoritmo utilizado para la firma, la envoltura y las operaciones de cifrado.
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: Objeto Algorithm (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f564efe9df3122951969a45443d58ace60e9db30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670393"
---
# <a name="algorithm-object"></a><span data-ttu-id="fcc2c-103">Algorithm (objeto)</span><span class="sxs-lookup"><span data-stu-id="fcc2c-103">Algorithm object</span></span>

<span data-ttu-id="fcc2c-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fcc2c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="fcc2c-105">En su lugar, use la [**clase AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="fcc2c-105">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="fcc2c-106">El objeto **algorithm** especifica el algoritmo utilizado para la firma, la envoltura y las operaciones de cifrado.</span><span class="sxs-lookup"><span data-stu-id="fcc2c-106">The **Algorithm** object specifies the algorithm used for signing, enveloping, and encrypting operations.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="fcc2c-107">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="fcc2c-107">When to use</span></span>

<span data-ttu-id="fcc2c-108">El objeto de **algoritmo** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="fcc2c-108">The **Algorithm** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="fcc2c-109">Establezca o recupere el algoritmo que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="fcc2c-109">Set or retrieve the algorithm to be used.</span></span>
-   <span data-ttu-id="fcc2c-110">Establezca o recupere la longitud de la clave.</span><span class="sxs-lookup"><span data-stu-id="fcc2c-110">Set or retrieve the key length.</span></span>

> [!Note]  
> <span data-ttu-id="fcc2c-111">CAPICOM intenta usar el proveedor de servicios criptográficos (CSP) predeterminado del sistema.</span><span class="sxs-lookup"><span data-stu-id="fcc2c-111">CAPICOM attempts to use the system default cryptographic service provider (CSP).</span></span> <span data-ttu-id="fcc2c-112">Si ese CSP no puede proporcionar la longitud de clave o el algoritmo solicitado, CAPICOM busca un CSP proporcionado por Microsoft que pueda controlar el algoritmo y la longitud de clave solicitados, en este orden de disponibilidad: proveedor de servicios criptográficos mejorados de Microsoft, proveedor de servicios criptográficos seguros de Microsoft, proveedor de servicios criptográficos básicos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fcc2c-112">If that CSP cannot provide the requested algorithm or key length, CAPICOM searches for an available Microsoft-provided CSP that can handle the requested algorithm and key length, in this order of availability: Microsoft Enhanced Cryptographic Provider, Microsoft Strong Cryptographic Provider, Microsoft Base Cryptographic Provider.</span></span>

 

## <a name="members"></a><span data-ttu-id="fcc2c-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="fcc2c-113">Members</span></span>

<span data-ttu-id="fcc2c-114">El objeto **algorithm** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fcc2c-114">The **Algorithm** object has these types of members:</span></span>

-   [<span data-ttu-id="fcc2c-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fcc2c-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fcc2c-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fcc2c-116">Properties</span></span>

<span data-ttu-id="fcc2c-117">El objeto de **algoritmo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fcc2c-117">The **Algorithm** object has these properties.</span></span>



| <span data-ttu-id="fcc2c-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fcc2c-118">Property</span></span>                                            | <span data-ttu-id="fcc2c-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="fcc2c-119">Access type</span></span>           | <span data-ttu-id="fcc2c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="fcc2c-120">Description</span></span>                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fcc2c-121">**KeyLength**</span><span class="sxs-lookup"><span data-stu-id="fcc2c-121">**KeyLength**</span></span>](algorithm-keylength.md)<br/> | <span data-ttu-id="fcc2c-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fcc2c-122">Read/write</span></span><br/> | <span data-ttu-id="fcc2c-123">Establece o recupera la longitud de la clave.</span><span class="sxs-lookup"><span data-stu-id="fcc2c-123">Sets or retrieves the length of the key.</span></span><br/>                                                                               |
| [<span data-ttu-id="fcc2c-124">**Name**</span><span class="sxs-lookup"><span data-stu-id="fcc2c-124">**Name**</span></span>](algorithm-name.md)<br/>           | <span data-ttu-id="fcc2c-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fcc2c-125">Read/write</span></span><br/> | <span data-ttu-id="fcc2c-126">Establece o recupera el algoritmo utilizado para la firma, la envoltura y el cifrado de las operaciones.</span><span class="sxs-lookup"><span data-stu-id="fcc2c-126">Sets or retrieves the algorithm used for signing, enveloping, and encrypting operations.</span></span> <span data-ttu-id="fcc2c-127">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fcc2c-127">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fcc2c-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcc2c-128">Remarks</span></span>

<span data-ttu-id="fcc2c-129">No se puede crear el objeto de **algoritmo** .</span><span class="sxs-lookup"><span data-stu-id="fcc2c-129">The **Algorithm** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcc2c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcc2c-130">Requirements</span></span>



| <span data-ttu-id="fcc2c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcc2c-131">Requirement</span></span> | <span data-ttu-id="fcc2c-132">Value</span><span class="sxs-lookup"><span data-stu-id="fcc2c-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc2c-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fcc2c-133">End of client support</span></span><br/> | <span data-ttu-id="fcc2c-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fcc2c-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fcc2c-135">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="fcc2c-135">End of server support</span></span><br/> | <span data-ttu-id="fcc2c-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fcc2c-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fcc2c-137">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="fcc2c-137">Redistributable</span></span><br/>       | <span data-ttu-id="fcc2c-138">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="fcc2c-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fcc2c-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcc2c-139">Header</span></span><br/>                | <dl> <span data-ttu-id="fcc2c-140"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcc2c-140"><dt>Capicom.h</dt></span></span> </dl>   |
| <span data-ttu-id="fcc2c-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fcc2c-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fcc2c-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcc2c-142"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcc2c-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcc2c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc2c-144">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="fcc2c-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
