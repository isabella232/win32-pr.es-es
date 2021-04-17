---
description: Proporciona propiedades y métodos para cifrar y descifrar datos mediante una clave de sesión derivada de un secreto.
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: EncryptedData (objeto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 123e0973343e4990dd2d49cfb321d739085358f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670439"
---
# <a name="encrypteddata-object"></a><span data-ttu-id="600f4-103">EncryptedData (objeto)</span><span class="sxs-lookup"><span data-stu-id="600f4-103">EncryptedData object</span></span>

<span data-ttu-id="600f4-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="600f4-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="600f4-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones de la API de Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) y [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para cifrar y descifrar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="600f4-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="600f4-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="600f4-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="600f4-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="600f4-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="600f4-108">El objeto **EncryptedData** proporciona propiedades y métodos para cifrar y descifrar los datos mediante una [*clave de sesión*](../secgloss/s-gly.md) derivada de un secreto.</span><span class="sxs-lookup"><span data-stu-id="600f4-108">The **EncryptedData** object provides properties and methods to encrypt and decrypt data using a [*session key*](../secgloss/s-gly.md) derived from a secret.</span></span>

> [!Note]  
> <span data-ttu-id="600f4-109">CAPICOM no admite el tipo de \# contenido de PKCS 7 EncryptedData, pero usa una estructura ASN no estándar para **EncryptedData**.</span><span class="sxs-lookup"><span data-stu-id="600f4-109">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for **EncryptedData**.</span></span> <span data-ttu-id="600f4-110">Por lo tanto, solo CAPICOM puede descifrar un objeto **EncryptedData** de CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="600f4-110">Therefore, only CAPICOM can decrypt a CAPICOM **EncryptedData** object.</span></span>

 

## <a name="members"></a><span data-ttu-id="600f4-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="600f4-111">Members</span></span>

<span data-ttu-id="600f4-112">El objeto **EncryptedData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="600f4-112">The **EncryptedData** object has these types of members:</span></span>

-   [<span data-ttu-id="600f4-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="600f4-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="600f4-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="600f4-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="600f4-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="600f4-115">Methods</span></span>

<span data-ttu-id="600f4-116">El objeto **EncryptedData** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="600f4-116">The **EncryptedData** object has these methods.</span></span>



| <span data-ttu-id="600f4-117">Método</span><span class="sxs-lookup"><span data-stu-id="600f4-117">Method</span></span>                                       | <span data-ttu-id="600f4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="600f4-118">Description</span></span>                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="600f4-119">**Descifrado**</span><span class="sxs-lookup"><span data-stu-id="600f4-119">**Decrypt**</span></span>](encrypteddata-decrypt.md)     | <span data-ttu-id="600f4-120">Descifra el contenido cifrado mediante el secreto.</span><span class="sxs-lookup"><span data-stu-id="600f4-120">Decrypts encrypted content using the secret.</span></span><br/>                                 |
| [<span data-ttu-id="600f4-121">**Cifrado**</span><span class="sxs-lookup"><span data-stu-id="600f4-121">**Encrypt**</span></span>](encrypteddata-encrypt.md)     | <span data-ttu-id="600f4-122">Cifra el contenido con el algoritmo de cifrado y secreto actual.</span><span class="sxs-lookup"><span data-stu-id="600f4-122">Encrypts the content using the current secret and encryption algorithm.</span></span><br/>      |
| [<span data-ttu-id="600f4-123">**SetSecret**</span><span class="sxs-lookup"><span data-stu-id="600f4-123">**SetSecret**</span></span>](encrypteddata-setsecret.md) | <span data-ttu-id="600f4-124">Establece el secreto del que se deriva la clave de sesión de cifrado/descifrado.</span><span class="sxs-lookup"><span data-stu-id="600f4-124">Sets the secret from which the encryption/decryption session key is derived.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="600f4-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="600f4-125">Properties</span></span>

<span data-ttu-id="600f4-126">El objeto **EncryptedData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="600f4-126">The **EncryptedData** object has these properties.</span></span>



| <span data-ttu-id="600f4-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="600f4-127">Property</span></span>                                                | <span data-ttu-id="600f4-128">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="600f4-128">Access type</span></span>           | <span data-ttu-id="600f4-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="600f4-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="600f4-130">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="600f4-130">**Algorithm**</span></span>](encrypteddata-algorithm.md)<br/> | <span data-ttu-id="600f4-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="600f4-131">Read-only</span></span><br/>  | <span data-ttu-id="600f4-132">Algoritmo usado para el cifrado y el descifrado.</span><span class="sxs-lookup"><span data-stu-id="600f4-132">Algorithm used for encryption/decryption.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="600f4-133">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="600f4-133">**Content**</span></span>](encrypteddata-content.md)<br/>     | <span data-ttu-id="600f4-134">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="600f4-134">Read/write</span></span><br/> | <span data-ttu-id="600f4-135">Contenido que se va a cifrar o descifrar.</span><span class="sxs-lookup"><span data-stu-id="600f4-135">The content to be encrypted or decrypted.</span></span> <span data-ttu-id="600f4-136">La configuración de esta propiedad debe realizarse antes de llamar al método de [**cifrado**](encrypteddata-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="600f4-136">Setting this property must be done before the [**Encrypt**](encrypteddata-encrypt.md) method is called.</span></span> <br/> <span data-ttu-id="600f4-137">Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el [*Estado*](../secgloss/s-gly.md) completo del objeto y se pierde cualquier contenido cifrado en el objeto.</span><span class="sxs-lookup"><span data-stu-id="600f4-137">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span><br/> <span data-ttu-id="600f4-138">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="600f4-138">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="600f4-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="600f4-139">Remarks</span></span>

<span data-ttu-id="600f4-140">Se puede crear el objeto **EncryptedData** y es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="600f4-140">The **EncryptedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="600f4-141">El ProgID del objeto **EncryptedData** es CAPICOM. EncryptedData. 1.</span><span class="sxs-lookup"><span data-stu-id="600f4-141">The ProgID for the **EncryptedData** object is CAPICOM.EncryptedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="600f4-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="600f4-142">Requirements</span></span>



| <span data-ttu-id="600f4-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="600f4-143">Requirement</span></span> | <span data-ttu-id="600f4-144">Value</span><span class="sxs-lookup"><span data-stu-id="600f4-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="600f4-145">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="600f4-145">End of client support</span></span><br/> | <span data-ttu-id="600f4-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="600f4-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="600f4-147">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="600f4-147">End of server support</span></span><br/> | <span data-ttu-id="600f4-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="600f4-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="600f4-149">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="600f4-149">Redistributable</span></span><br/>       | <span data-ttu-id="600f4-150">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="600f4-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="600f4-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="600f4-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="600f4-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="600f4-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="600f4-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="600f4-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="600f4-154">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="600f4-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
