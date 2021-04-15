---
description: Descifra una cadena de datos cifrada y codificada.
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: EncryptedData. Decrypt (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aa702a5cefc46f6d0cbe5d7e0fba17ff03596b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649539"
---
# <a name="encrypteddatadecrypt-method"></a><span data-ttu-id="b82d9-103">EncryptedData. Decrypt (método)</span><span class="sxs-lookup"><span data-stu-id="b82d9-103">EncryptedData.Decrypt method</span></span>

<span data-ttu-id="b82d9-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b82d9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b82d9-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones de la API de Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) y [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para cifrar y descifrar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="b82d9-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="b82d9-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="b82d9-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="b82d9-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="b82d9-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="b82d9-108">El método **descifrado** descifra una cadena de datos cifrada y codificada.</span><span class="sxs-lookup"><span data-stu-id="b82d9-108">The **Decrypt** method decrypts an encrypted and encoded data string.</span></span> <span data-ttu-id="b82d9-109">Los datos de texto no cifrado resultantes se convierten en la propiedad de [**contenido**](encrypteddata-content.md) del objeto [**EncryptedData**](encrypteddata.md) .</span><span class="sxs-lookup"><span data-stu-id="b82d9-109">The resulting plaintext data becomes the [**Content**](encrypteddata-content.md) property of the [**EncryptedData**](encrypteddata.md) object.</span></span> <span data-ttu-id="b82d9-110">Se produce un error en el descifrado del contenido a menos que el secreto, establecido por el método [**SetSecret**](encrypteddata-setsecret.md) , sea exactamente el mismo que el secreto que se usa para derivar la clave utilizada para cifrar el contenido.</span><span class="sxs-lookup"><span data-stu-id="b82d9-110">Decryption of the content fails unless the secret, set by the [**SetSecret**](encrypteddata-setsecret.md) method, is exactly the same as the secret used to derive the key used to encrypt the content.</span></span>

## <a name="syntax"></a><span data-ttu-id="b82d9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b82d9-111">Syntax</span></span>


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="b82d9-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b82d9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b82d9-113">*EncryptedMessage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b82d9-113">*EncryptedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b82d9-114">Cadena que contiene los datos cifrados codificados que se van a descifrar.</span><span class="sxs-lookup"><span data-stu-id="b82d9-114">String that contains the encoded, encrypted data to be decrypted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b82d9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b82d9-115">Return value</span></span>

<span data-ttu-id="b82d9-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b82d9-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b82d9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b82d9-117">Remarks</span></span>

<span data-ttu-id="b82d9-118">La clave de sesión derivada del secreto actual se usa para el descifrado.</span><span class="sxs-lookup"><span data-stu-id="b82d9-118">The session key derived from the current secret is used for the decryption.</span></span> <span data-ttu-id="b82d9-119">Este método no producirá el texto no cifrado correcto a menos que el secreto actual coincida exactamente con el secreto utilizado para cifrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b82d9-119">This method will not produce the correct plaintext unless the current secret exactly matches the secret used to encrypt the message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b82d9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b82d9-120">Requirements</span></span>



| <span data-ttu-id="b82d9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b82d9-121">Requirement</span></span> | <span data-ttu-id="b82d9-122">Value</span><span class="sxs-lookup"><span data-stu-id="b82d9-122">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b82d9-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b82d9-123">End of client support</span></span><br/> | <span data-ttu-id="b82d9-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b82d9-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b82d9-125">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b82d9-125">End of server support</span></span><br/> | <span data-ttu-id="b82d9-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b82d9-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b82d9-127">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b82d9-127">Redistributable</span></span><br/>       | <span data-ttu-id="b82d9-128">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="b82d9-128">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b82d9-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b82d9-129">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b82d9-130"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b82d9-130"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b82d9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b82d9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b82d9-132">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="b82d9-132">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="b82d9-133">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="b82d9-133">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
