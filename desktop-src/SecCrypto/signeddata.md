---
description: Proporciona propiedades y métodos para establecer el contenido que se va a firmar con una firma digital, para firmar o cofirmar datos digitalmente, y para comprobar la firma digital de los datos firmados. El mensaje firmado está en \# formato PKCS 7.
ms.assetid: 500437e8-a637-4e89-9ac9-aa3ea20d437f
title: Objeto SignedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d0424826f7dc5d041b877ced1cd7f50490d7801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690057"
---
# <a name="signeddata-object"></a><span data-ttu-id="58c73-104">Objeto SignedData</span><span class="sxs-lookup"><span data-stu-id="58c73-104">SignedData object</span></span>

<span data-ttu-id="58c73-105">\[El objeto **SignedData** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="58c73-105">\[The **SignedData** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="58c73-106">En su lugar, use la [**clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="58c73-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="58c73-107">El objeto **SignedData** proporciona propiedades y métodos para establecer el contenido que se va a firmar con una [*firma digital*](../secgloss/d-gly.md), firmar o cofirmar datos digitalmente y comprobar la firma digital de los datos firmados.</span><span class="sxs-lookup"><span data-stu-id="58c73-107">The **SignedData** object provides properties and methods to establish the content to be signed with a [*digital signature*](../secgloss/d-gly.md), to sign or cosign data digitally, and to verify the digital signature of signed data.</span></span> <span data-ttu-id="58c73-108">El mensaje firmado está en \# formato PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="58c73-108">The signed message is in PKCS \#7 format.</span></span>

<span data-ttu-id="58c73-109">Una firma de datos, si se comprueba, demuestra la asociación entre un firmante y los datos, y muestra que los datos no se cambiaron de ningún modo una vez creada la firma.</span><span class="sxs-lookup"><span data-stu-id="58c73-109">A data signature, if verified, proves the association between a signer and data and shows that the data was not changed in any way after the signature was created.</span></span>

## <a name="members"></a><span data-ttu-id="58c73-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="58c73-110">Members</span></span>

<span data-ttu-id="58c73-111">El objeto **SignedData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="58c73-111">The **SignedData** object has these types of members:</span></span>

-   [<span data-ttu-id="58c73-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="58c73-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="58c73-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="58c73-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="58c73-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="58c73-114">Methods</span></span>

<span data-ttu-id="58c73-115">El objeto **SignedData** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="58c73-115">The **SignedData** object has these methods.</span></span>



| <span data-ttu-id="58c73-116">Método</span><span class="sxs-lookup"><span data-stu-id="58c73-116">Method</span></span>                              | <span data-ttu-id="58c73-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="58c73-117">Description</span></span>                                                         |
|:------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="58c73-118">**Firmar**</span><span class="sxs-lookup"><span data-stu-id="58c73-118">**CoSign**</span></span>](signeddata-cosign.md) | <span data-ttu-id="58c73-119">Firma un mensaje ya firmado.</span><span class="sxs-lookup"><span data-stu-id="58c73-119">Cosigns an already signed message.</span></span><br/>                       |
| [<span data-ttu-id="58c73-120">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="58c73-120">**Sign**</span></span>](signeddata-sign.md)     | <span data-ttu-id="58c73-121">Crea una firma digital en el contenido que se va a firmar.</span><span class="sxs-lookup"><span data-stu-id="58c73-121">Creates a digital signature on the content to be signed.</span></span><br/> |
| [<span data-ttu-id="58c73-122">**Ver**</span><span class="sxs-lookup"><span data-stu-id="58c73-122">**Verify**</span></span>](signeddata-verify.md) | <span data-ttu-id="58c73-123">Determina la validez de una firma o signaturas.</span><span class="sxs-lookup"><span data-stu-id="58c73-123">Determines the validity of a signature or signatures.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="58c73-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="58c73-124">Properties</span></span>

<span data-ttu-id="58c73-125">El objeto **SignedData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="58c73-125">The **SignedData** object has these properties.</span></span>



| <span data-ttu-id="58c73-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="58c73-126">Property</span></span>                                                   | <span data-ttu-id="58c73-127">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="58c73-127">Access type</span></span>           | <span data-ttu-id="58c73-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="58c73-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58c73-129">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="58c73-129">**Certificates**</span></span>](signeddata-certificates.md)<br/> | <span data-ttu-id="58c73-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="58c73-130">Read-only</span></span><br/>  | <span data-ttu-id="58c73-131">Recupera la colección de [**certificados**](certificates.md) de los datos firmados.</span><span class="sxs-lookup"><span data-stu-id="58c73-131">Retrieves the [**Certificates**](certificates.md) collection of the signed data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="58c73-132">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="58c73-132">**Content**</span></span>](signeddata-content.md)<br/>           | <span data-ttu-id="58c73-133">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="58c73-133">Read/write</span></span><br/> | <span data-ttu-id="58c73-134">Datos que se van a firmar.</span><span class="sxs-lookup"><span data-stu-id="58c73-134">Data to be signed.</span></span> <span data-ttu-id="58c73-135">Esta propiedad se debe inicializar antes de que se llame al método [**Sign**](signeddata-sign.md) .</span><span class="sxs-lookup"><span data-stu-id="58c73-135">This property must be initialized before the [**Sign**](signeddata-sign.md) method is called.</span></span><br/> <span data-ttu-id="58c73-136">Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el [*Estado*](../secgloss/s-gly.md) completo del objeto y se pierde cualquier firma asociada al objeto antes de que se cambiara la propiedad.</span><span class="sxs-lookup"><span data-stu-id="58c73-136">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any signature that was associated with the object before the property was changed is lost.</span></span><br/> <span data-ttu-id="58c73-137">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="58c73-137">This is the default property.</span></span><br/> |
| [<span data-ttu-id="58c73-138">**Firmantes**</span><span class="sxs-lookup"><span data-stu-id="58c73-138">**Signers**</span></span>](signeddata-signers.md)<br/>           | <span data-ttu-id="58c73-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="58c73-139">Read-only</span></span><br/>  | <span data-ttu-id="58c73-140">Recupera la colección de [**firmantes**](signers.md) que representa los creadores de firmas de los datos.</span><span class="sxs-lookup"><span data-stu-id="58c73-140">Retrieves the [**Signers**](signers.md) collection that represents the signature creators of the data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="58c73-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58c73-141">Remarks</span></span>

<span data-ttu-id="58c73-142">Se puede crear el objeto **SignedData** y es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="58c73-142">The **SignedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="58c73-143">El ProgID del objeto **SignedData** es CAPICOM. SignedData. 1.</span><span class="sxs-lookup"><span data-stu-id="58c73-143">The ProgID for the **SignedData** object is CAPICOM.SignedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="58c73-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58c73-144">Requirements</span></span>



| <span data-ttu-id="58c73-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="58c73-145">Requirement</span></span> | <span data-ttu-id="58c73-146">Value</span><span class="sxs-lookup"><span data-stu-id="58c73-146">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58c73-147">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="58c73-147">Redistributable</span></span><br/> | <span data-ttu-id="58c73-148">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="58c73-148">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="58c73-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="58c73-149">DLL</span></span><br/>             | <dl> <span data-ttu-id="58c73-150"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58c73-150"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58c73-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="58c73-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58c73-152">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="58c73-152">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
