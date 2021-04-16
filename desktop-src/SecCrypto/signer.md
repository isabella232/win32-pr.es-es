---
description: Establece el firmante de un objeto SignedData o SignedCode.
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: Objeto de firmante
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 974341eb996f2b5d3701757a5352ef56e2837390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671495"
---
# <a name="signer-object"></a><span data-ttu-id="876c2-103">Objeto de firmante</span><span class="sxs-lookup"><span data-stu-id="876c2-103">Signer object</span></span>

<span data-ttu-id="876c2-104">\[El objeto de **firmante** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="876c2-104">\[The **Signer** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="876c2-105">En su lugar, use la [**clase CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="876c2-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="876c2-106">El objeto de **firmante** establece el firmante de un objeto [**SignedData**](signeddata.md) o [**SignedCode**](signedcode.md) .</span><span class="sxs-lookup"><span data-stu-id="876c2-106">The **Signer** object establishes the signer of a [**SignedData**](signeddata.md) or [**SignedCode**](signedcode.md) object.</span></span> <span data-ttu-id="876c2-107">El [**certificado**](certificate.md) del objeto **firmante** debe tener una clave privada disponible que pueda usarse para firmar datos.</span><span class="sxs-lookup"><span data-stu-id="876c2-107">The [**Certificate**](certificate.md) of the **Signer** object must have an available private key that can be used to sign data.</span></span>

## <a name="members"></a><span data-ttu-id="876c2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="876c2-108">Members</span></span>

<span data-ttu-id="876c2-109">El objeto de **firmante** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="876c2-109">The **Signer** object has these types of members:</span></span>

-   [<span data-ttu-id="876c2-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="876c2-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="876c2-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="876c2-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="876c2-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="876c2-112">Methods</span></span>

<span data-ttu-id="876c2-113">El objeto de **firmante** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="876c2-113">The **Signer** object has these methods.</span></span>



| <span data-ttu-id="876c2-114">Método</span><span class="sxs-lookup"><span data-stu-id="876c2-114">Method</span></span>                      | <span data-ttu-id="876c2-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="876c2-115">Description</span></span>                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="876c2-116">**Cargar**</span><span class="sxs-lookup"><span data-stu-id="876c2-116">**Load**</span></span>](signer-load.md) | <span data-ttu-id="876c2-117">Carga un certificado de firma desde un archivo PFX especificado.</span><span class="sxs-lookup"><span data-stu-id="876c2-117">Loads a signing certificate from a specified PFX file.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="876c2-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="876c2-118">Properties</span></span>

<span data-ttu-id="876c2-119">El objeto de **firmante** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="876c2-119">The **Signer** object has these properties.</span></span>



| <span data-ttu-id="876c2-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="876c2-120">Property</span></span>                                                                     | <span data-ttu-id="876c2-121">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="876c2-121">Access type</span></span>           | <span data-ttu-id="876c2-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="876c2-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="876c2-123">**AuthenticatedAttributes**</span><span class="sxs-lookup"><span data-stu-id="876c2-123">**AuthenticatedAttributes**</span></span>](signer-authenticatedattributes.md)<br/> | <span data-ttu-id="876c2-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="876c2-124">Read-only</span></span><br/>  | <span data-ttu-id="876c2-125">Colección de atributos autenticados.</span><span class="sxs-lookup"><span data-stu-id="876c2-125">The collection of authenticated attributes.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="876c2-126">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="876c2-126">**Certificate**</span></span>](signer-certificate.md)<br/>                         | <span data-ttu-id="876c2-127">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="876c2-127">Read/write</span></span><br/> | <span data-ttu-id="876c2-128">Objeto de [**certificado**](certificate.md) que representa el certificado de un firmante de los datos.</span><span class="sxs-lookup"><span data-stu-id="876c2-128">The [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span><br/> <span data-ttu-id="876c2-129">Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el [*Estado*](../secgloss/s-gly.md) completo del objeto.</span><span class="sxs-lookup"><span data-stu-id="876c2-129">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span><br/> <span data-ttu-id="876c2-130">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="876c2-130">This is the default property.</span></span><br/> |
| [<span data-ttu-id="876c2-131">**IAM**</span><span class="sxs-lookup"><span data-stu-id="876c2-131">**Chain**</span></span>](signer-chain.md)<br/>                                     | <span data-ttu-id="876c2-132">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="876c2-132">Read-only</span></span><br/>  | <span data-ttu-id="876c2-133">Cadena del firmante.</span><span class="sxs-lookup"><span data-stu-id="876c2-133">The chain of the signer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="876c2-134">**Opciones**</span><span class="sxs-lookup"><span data-stu-id="876c2-134">**Options**</span></span>](signer-options.md)<br/>                                 | <span data-ttu-id="876c2-135">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="876c2-135">Read/write</span></span><br/> | <span data-ttu-id="876c2-136">Establece o recupera la opción de certificado del firmante.</span><span class="sxs-lookup"><span data-stu-id="876c2-136">Sets or retrieves the signer's certificate option.</span></span><br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="876c2-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="876c2-137">Remarks</span></span>

<span data-ttu-id="876c2-138">Se puede crear el objeto **firmante** y es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="876c2-138">The **Signer** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="876c2-139">El ProgID del objeto de **firmante** es CAPICOM. Firmante. 2.</span><span class="sxs-lookup"><span data-stu-id="876c2-139">The ProgID for the **Signer** object is CAPICOM.Signer.2.</span></span>

<span data-ttu-id="876c2-140">**CAPICOM 1. *x*:** el ProgID del objeto de **firmante** es CAPICOM. Firmante. 1.</span><span class="sxs-lookup"><span data-stu-id="876c2-140">**CAPICOM 1.*x*:** The ProgID for the **Signer** object is CAPICOM.Signer.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="876c2-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="876c2-141">Requirements</span></span>



| <span data-ttu-id="876c2-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="876c2-142">Requirement</span></span> | <span data-ttu-id="876c2-143">Value</span><span class="sxs-lookup"><span data-stu-id="876c2-143">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="876c2-144">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="876c2-144">Redistributable</span></span><br/> | <span data-ttu-id="876c2-145">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="876c2-145">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="876c2-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="876c2-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="876c2-147"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="876c2-147"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="876c2-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="876c2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="876c2-149">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="876c2-149">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
