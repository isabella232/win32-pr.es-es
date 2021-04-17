---
description: Deriva una clave de sesión del secreto y cifra el valor de la propiedad de contenido usando esa clave. Devuelve el contenido cifrado como una cadena codificada.
ms.assetid: aa6f6e6a-208b-4e9c-b530-08673ab9d794
title: EncryptedData. Encrypt (método) (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 04d7bf8a337c1bcfa0a024b84304fe50c035f9dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670441"
---
# <a name="encrypteddataencrypt-method"></a><span data-ttu-id="5cb9f-104">EncryptedData. Encrypt (método)</span><span class="sxs-lookup"><span data-stu-id="5cb9f-104">EncryptedData.Encrypt method</span></span>

<span data-ttu-id="5cb9f-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5cb9f-106">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones de la API de Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) y [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para cifrar y descifrar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="5cb9f-107">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="5cb9f-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="5cb9f-108">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="5cb9f-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="5cb9f-109">El método **Encrypt** deriva una clave de sesión del secreto y cifra el valor de la propiedad de [**contenido**](encrypteddata-content.md) usando esa clave.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-109">The **Encrypt** method derives a session key from the secret and encrypts the [**Content**](encrypteddata-content.md) property value using that key.</span></span> <span data-ttu-id="5cb9f-110">Devuelve el contenido cifrado como una cadena codificada.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-110">It returns the encrypted content as an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cb9f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5cb9f-111">Syntax</span></span>


```VB
EncryptedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5cb9f-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5cb9f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cb9f-113">*EncodingType* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5cb9f-113">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5cb9f-114">Un valor de la enumeración de [**\_ \_ tipo de codificación CAPICOM**](capicom-encoding-type.md) que indica el tipo de codificación utilizado para codificar los datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-114">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the encoding type used to encode the encrypted data.</span></span> <span data-ttu-id="5cb9f-115">El valor predeterminado es CAPICOM \_ encode \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-115">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="5cb9f-116">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="5cb9f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5cb9f-117">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="5cb9f-118">Significado</span><span class="sxs-lookup"><span data-stu-id="5cb9f-118">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="5cb9f-119"><dt>**CAPICOM \_ codificar \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="5cb9f-119"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="5cb9f-120">Este tipo de codificación solo se utiliza cuando los datos de entrada tienen un tipo de codificación desconocido.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-120">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="5cb9f-121">Si este valor se usa para especificar el tipo de codificación de la salida, \_ se usará CAPICOM encode \_ Base64 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-121">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="5cb9f-122">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-122">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="5cb9f-123"><dt>**CAPICOM, codificación \_ \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="5cb9f-123"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="5cb9f-124">Los datos se guardan como una cadena codificada en Base64.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-124">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="5cb9f-125"><dt>**\_código binario de codificación de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5cb9f-125"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="5cb9f-126">Los datos se guardan como una secuencia binaria pura.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-126">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cb9f-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5cb9f-127">Return value</span></span>

<span data-ttu-id="5cb9f-128">Cadena que contiene los datos cifrados codificados.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-128">A string that contains the encrypted, encoded data.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cb9f-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5cb9f-129">Remarks</span></span>

<span data-ttu-id="5cb9f-130">Antes de llamar al método **Encrypt** , establezca la propiedad [**Content**](encrypteddata-content.md) y llame al método [**SetSecret**](encrypteddata-setsecret.md) .</span><span class="sxs-lookup"><span data-stu-id="5cb9f-130">Before calling the **Encrypt** method, set the [**Content**](encrypteddata-content.md) property and call the [**SetSecret**](encrypteddata-setsecret.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cb9f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cb9f-131">Requirements</span></span>



| <span data-ttu-id="5cb9f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cb9f-132">Requirement</span></span> | <span data-ttu-id="5cb9f-133">Value</span><span class="sxs-lookup"><span data-stu-id="5cb9f-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5cb9f-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5cb9f-134">End of client support</span></span><br/> | <span data-ttu-id="5cb9f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5cb9f-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5cb9f-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5cb9f-136">End of server support</span></span><br/> | <span data-ttu-id="5cb9f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cb9f-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5cb9f-138">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="5cb9f-138">Redistributable</span></span><br/>       | <span data-ttu-id="5cb9f-139">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="5cb9f-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5cb9f-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cb9f-140">Header</span></span><br/>                | <dl> <span data-ttu-id="5cb9f-141"><dt>InfoCard. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cb9f-141"><dt>Infocard.h</dt></span></span> </dl>  |
| <span data-ttu-id="5cb9f-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5cb9f-142">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5cb9f-143"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cb9f-143"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cb9f-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="5cb9f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cb9f-145">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="5cb9f-145">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="5cb9f-146">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="5cb9f-146">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
