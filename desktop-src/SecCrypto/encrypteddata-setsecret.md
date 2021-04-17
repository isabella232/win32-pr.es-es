---
description: Establece el valor del secreto que se usa para derivar la clave de sesión criptográfica usada para cifrar y descifrar los datos.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: EncryptedData. SetSecret (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c8d30355b022a593ca17519e3ccfa876a5b07b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670440"
---
# <a name="encrypteddatasetsecret-method"></a><span data-ttu-id="47d53-103">EncryptedData. SetSecret (método)</span><span class="sxs-lookup"><span data-stu-id="47d53-103">EncryptedData.SetSecret method</span></span>

<span data-ttu-id="47d53-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="47d53-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="47d53-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones de la API de Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) y [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para cifrar y descifrar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="47d53-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="47d53-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="47d53-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="47d53-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="47d53-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="47d53-108">El método **SetSecret** establece el valor del secreto que se usa para derivar la [*clave de sesión*](../secgloss/s-gly.md) criptográfica usada para cifrar y descifrar los datos.</span><span class="sxs-lookup"><span data-stu-id="47d53-108">The **SetSecret** method sets the value of the secret used to derive the cryptographic [*session key*](../secgloss/s-gly.md) used to encrypt and decrypt data.</span></span>

## <a name="syntax"></a><span data-ttu-id="47d53-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47d53-109">Syntax</span></span>


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="47d53-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47d53-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47d53-111">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="47d53-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47d53-112">Cadena que contiene un secreto que se usa para crear una clave criptográfica de sesión.</span><span class="sxs-lookup"><span data-stu-id="47d53-112">A string that contains a secret used to create a session cryptographic key.</span></span>

</dd> <dt>

<span data-ttu-id="47d53-113">*SecretType* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="47d53-113">*SecretType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="47d53-114">Un valor de la enumeración de [**\_ \_ tipo de secreto de CAPICOM**](capicom-secret-type.md) que indica el tipo de secreto usado para generar la clave de sesión.</span><span class="sxs-lookup"><span data-stu-id="47d53-114">A value of the [**CAPICOM\_SECRET\_TYPE**](capicom-secret-type.md) enumeration that indicates the kind of secret used to generate the session key.</span></span> <span data-ttu-id="47d53-115">El valor predeterminado es la \_ contraseña del secreto de CAPICOM \_ .</span><span class="sxs-lookup"><span data-stu-id="47d53-115">The default value is CAPICOM\_SECRET\_PASSWORD.</span></span> <span data-ttu-id="47d53-116">Este parámetro puede ser el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="47d53-116">This parameter can be the following value.</span></span>



| <span data-ttu-id="47d53-117">Value</span><span class="sxs-lookup"><span data-stu-id="47d53-117">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="47d53-118">Significado</span><span class="sxs-lookup"><span data-stu-id="47d53-118">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <span data-ttu-id="47d53-119"><dt>**\_contraseña secreta de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="47d53-119"><dt>**CAPICOM\_SECRET\_PASSWORD**</dt></span></span> </dl> | <span data-ttu-id="47d53-120">La clave de cifrado debe derivarse de una contraseña.</span><span class="sxs-lookup"><span data-stu-id="47d53-120">The encryption key is to be derived from a password.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47d53-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47d53-121">Return value</span></span>

<span data-ttu-id="47d53-122">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="47d53-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47d53-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47d53-123">Remarks</span></span>

<span data-ttu-id="47d53-124">El secreto se usa para crear la clave de sesión para el cifrado o descifrado.</span><span class="sxs-lookup"><span data-stu-id="47d53-124">The secret is used to create the session key for encryption or decryption.</span></span> <span data-ttu-id="47d53-125">Se debe usar el mismo secreto para ambas operaciones.</span><span class="sxs-lookup"><span data-stu-id="47d53-125">The same secret must be used for both operations.</span></span> <span data-ttu-id="47d53-126">Si se pierde el secreto que se usa para cifrar los datos, los datos cifrados no se pueden descifrar.</span><span class="sxs-lookup"><span data-stu-id="47d53-126">If the secret used to encrypt data is lost, the encrypted data cannot be decrypted.</span></span>

<span data-ttu-id="47d53-127">Si es adecuado para su aplicación, considere la posibilidad de usar [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) o [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) para proteger el secreto antes y después de usarlo.</span><span class="sxs-lookup"><span data-stu-id="47d53-127">If appropriate for your application, consider using [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) or [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) to protect the secret before and after use.</span></span> <span data-ttu-id="47d53-128">Borre la memoria asociada al secreto cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="47d53-128">Clear the memory associated with the secret when done.</span></span>

## <a name="requirements"></a><span data-ttu-id="47d53-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47d53-129">Requirements</span></span>



| <span data-ttu-id="47d53-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="47d53-130">Requirement</span></span> | <span data-ttu-id="47d53-131">Value</span><span class="sxs-lookup"><span data-stu-id="47d53-131">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47d53-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="47d53-132">End of client support</span></span><br/> | <span data-ttu-id="47d53-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47d53-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="47d53-134">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="47d53-134">End of server support</span></span><br/> | <span data-ttu-id="47d53-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47d53-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="47d53-136">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="47d53-136">Redistributable</span></span><br/>       | <span data-ttu-id="47d53-137">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="47d53-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="47d53-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47d53-138">DLL</span></span><br/>                   | <dl> <span data-ttu-id="47d53-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47d53-139"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47d53-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="47d53-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d53-141">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="47d53-141">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="47d53-142">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="47d53-142">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
