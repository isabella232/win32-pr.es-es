---
description: El objeto EnvelopedData proporciona propiedades y métodos para envolver los datos para la privacidad mediante cifrado.
ms.assetid: 7c5f3e3d-6a70-455d-8921-20495eec4b3e
title: Objeto EnvelopedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5309061c6ab315a089a1e1d8b9488556cae9f31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649708"
---
# <a name="envelopeddata-object"></a><span data-ttu-id="a88b7-103">Objeto EnvelopedData</span><span class="sxs-lookup"><span data-stu-id="a88b7-103">EnvelopedData object</span></span>

<span data-ttu-id="a88b7-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a88b7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a88b7-105">En su lugar, use la [**clase EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="a88b7-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="a88b7-106">El objeto **EnvelopedData** proporciona propiedades y métodos para envolver los datos para la privacidad mediante cifrado.</span><span class="sxs-lookup"><span data-stu-id="a88b7-106">The **EnvelopedData** object provides properties and methods to envelop data for privacy by encryption.</span></span> <span data-ttu-id="a88b7-107">Para envolver los datos, se genera una clave criptográfica de sesión.</span><span class="sxs-lookup"><span data-stu-id="a88b7-107">To envelop data, a session cryptographic key is generated.</span></span> <span data-ttu-id="a88b7-108">A continuación, esa [*clave de sesión*](../secgloss/s-gly.md) se cifra para cada destinatario previsto mediante la [*clave pública*](../secgloss/p-gly.md) de ese destinatario previsto del certificado del destinatario.</span><span class="sxs-lookup"><span data-stu-id="a88b7-108">That [*session key*](../secgloss/s-gly.md) is then encrypted for each intended recipient using the [*public key*](../secgloss/p-gly.md) of that intended recipient from the recipient's certificate.</span></span> <span data-ttu-id="a88b7-109">Los datos cifrados y el conjunto de claves de sesión cifradas se pueden enviar a todos los destinatarios deseados.</span><span class="sxs-lookup"><span data-stu-id="a88b7-109">The encrypted data and the set of encrypted session keys can be sent to all intended recipients.</span></span> <span data-ttu-id="a88b7-110">El mensaje generado está en \# formato PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="a88b7-110">The message generated is in PKCS \#7 format.</span></span>

## <a name="members"></a><span data-ttu-id="a88b7-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a88b7-111">Members</span></span>

<span data-ttu-id="a88b7-112">El objeto **EnvelopedData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a88b7-112">The **EnvelopedData** object has these types of members:</span></span>

-   [<span data-ttu-id="a88b7-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a88b7-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="a88b7-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a88b7-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a88b7-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="a88b7-115">Methods</span></span>

<span data-ttu-id="a88b7-116">El objeto **EnvelopedData** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a88b7-116">The **EnvelopedData** object has these methods.</span></span>



| <span data-ttu-id="a88b7-117">Método</span><span class="sxs-lookup"><span data-stu-id="a88b7-117">Method</span></span>                                   | <span data-ttu-id="a88b7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a88b7-118">Description</span></span>                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a88b7-119">**Descifrado**</span><span class="sxs-lookup"><span data-stu-id="a88b7-119">**Decrypt**</span></span>](envelopeddata-decrypt.md) | <span data-ttu-id="a88b7-120">Descifra el contenido con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="a88b7-120">Decrypts enveloped content.</span></span><br/>                                                                      |
| [<span data-ttu-id="a88b7-121">**Cifrado**</span><span class="sxs-lookup"><span data-stu-id="a88b7-121">**Encrypt**</span></span>](envelopeddata-encrypt.md) | <span data-ttu-id="a88b7-122">Cifra el contenido, cifra una clave de sesión para cada destinatario y devuelve el BLOB cifrado.</span><span class="sxs-lookup"><span data-stu-id="a88b7-122">Encrypts the content, encrypts a session key for each recipient, and returns the encrypted BLOB.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a88b7-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a88b7-123">Properties</span></span>

<span data-ttu-id="a88b7-124">El objeto **EnvelopedData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a88b7-124">The **EnvelopedData** object has these properties.</span></span>



| <span data-ttu-id="a88b7-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a88b7-125">Property</span></span>                                                  | <span data-ttu-id="a88b7-126">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="a88b7-126">Access type</span></span>           | <span data-ttu-id="a88b7-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="a88b7-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a88b7-128">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="a88b7-128">**Algorithm**</span></span>](envelopeddata-algorithm.md)<br/>   | <span data-ttu-id="a88b7-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a88b7-129">Read/write</span></span><br/> | <span data-ttu-id="a88b7-130">Algoritmo de cifrado y [*longitud de clave*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a88b7-130">Encryption algorithm and [*key length*](../secgloss/k-gly.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="a88b7-131">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="a88b7-131">**Content**</span></span>](envelopeddata-content.md)<br/>       | <span data-ttu-id="a88b7-132">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a88b7-132">Read/write</span></span><br/> | <span data-ttu-id="a88b7-133">El contenido de texto sin formato de un mensaje que se va a acercar.</span><span class="sxs-lookup"><span data-stu-id="a88b7-133">The plaintext content of a message to be enveloped.</span></span> <span data-ttu-id="a88b7-134">La configuración de esta propiedad debe realizarse antes de llamar al método de [**cifrado**](envelopeddata-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="a88b7-134">Setting this property must be done before the [**Encrypt**](envelopeddata-encrypt.md) method is called.</span></span><br/> <span data-ttu-id="a88b7-135">Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el [*Estado*](../secgloss/s-gly.md) completo del objeto y se pierde cualquier contenido cifrado en el objeto.</span><span class="sxs-lookup"><span data-stu-id="a88b7-135">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span><br/> <span data-ttu-id="a88b7-136">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a88b7-136">This is the default property.</span></span><br/> |
| [<span data-ttu-id="a88b7-137">**Recipients**</span><span class="sxs-lookup"><span data-stu-id="a88b7-137">**Recipients**</span></span>](envelopeddata-recipients.md)<br/> | <span data-ttu-id="a88b7-138">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a88b7-138">Read-only</span></span><br/>  | <span data-ttu-id="a88b7-139">Colección de objetos de [**certificado**](certificate.md) para recibir el mensaje con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="a88b7-139">Collection of [**Certificate**](certificate.md) objects to receive the enveloped message.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="a88b7-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a88b7-140">Remarks</span></span>

<span data-ttu-id="a88b7-141">Se puede crear el objeto **EnvelopedData** y es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="a88b7-141">The **EnvelopedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="a88b7-142">El ProgID del objeto **EnvelopedData** es CAPICOM. EnvelopedData. 1.</span><span class="sxs-lookup"><span data-stu-id="a88b7-142">The ProgID for the **EnvelopedData** object is CAPICOM.EnvelopedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="a88b7-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a88b7-143">Requirements</span></span>



| <span data-ttu-id="a88b7-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="a88b7-144">Requirement</span></span> | <span data-ttu-id="a88b7-145">Value</span><span class="sxs-lookup"><span data-stu-id="a88b7-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a88b7-146">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a88b7-146">End of client support</span></span><br/> | <span data-ttu-id="a88b7-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a88b7-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a88b7-148">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a88b7-148">End of server support</span></span><br/> | <span data-ttu-id="a88b7-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a88b7-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a88b7-150">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a88b7-150">Redistributable</span></span><br/>       | <span data-ttu-id="a88b7-151">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="a88b7-151">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a88b7-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a88b7-152">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a88b7-153"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a88b7-153"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a88b7-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="a88b7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a88b7-155">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="a88b7-155">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
