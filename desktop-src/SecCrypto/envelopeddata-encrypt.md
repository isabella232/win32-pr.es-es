---
description: Genera una clave de sesión y cifra los datos y sobres.
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: EnvelopedData. Encrypt (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ecdb665a8e70ff329f25398eb855ff3e82c96cfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649709"
---
# <a name="envelopeddataencrypt-method"></a><span data-ttu-id="bcaf2-103">EnvelopedData. Encrypt (método)</span><span class="sxs-lookup"><span data-stu-id="bcaf2-103">EnvelopedData.Encrypt method</span></span>

<span data-ttu-id="bcaf2-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="bcaf2-105">En su lugar, use la [**clase EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="bcaf2-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="bcaf2-106">El método **Encrypt** genera una clave de sesión, utiliza esa clave para cifrar el contenido, incluye el contenido cifrado de cada destinatario mediante el cifrado de la clave de sesión con la clave pública de cada destinatario y, a continuación, devuelve el [*BLOB*](../secgloss/b-gly.md) que contiene el contenido cifrado y las claves de sesión cifrada como una cadena codificada.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-106">The **Encrypt** method generates a session key, uses that key to encrypt the contents, envelops the encrypted content for each recipient by encrypting the session key with each recipient's public key, and then returns the [*BLOB*](../secgloss/b-gly.md) that contains the encrypted contents and the encrypted session keys as an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcaf2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bcaf2-107">Syntax</span></span>


```VB
EnvelopedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="bcaf2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcaf2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcaf2-109">*EncodingType* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bcaf2-109">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bcaf2-110">Un valor de la enumeración de [**\_ \_ tipo de codificación CAPICOM**](capicom-encoding-type.md) que indica el tipo de codificación utilizado para codificar los datos con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-110">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the encoding type used to encode the enveloped data.</span></span> <span data-ttu-id="bcaf2-111">El valor de codificación predeterminado es CAPICOM \_ codificado en \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-111">The default encoding value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="bcaf2-112">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="bcaf2-113">Valor</span><span class="sxs-lookup"><span data-stu-id="bcaf2-113">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="bcaf2-114">Significado</span><span class="sxs-lookup"><span data-stu-id="bcaf2-114">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="bcaf2-115"><dt>**CAPICOM \_ codificar \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="bcaf2-115"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="bcaf2-116">Este tipo de codificación solo se utiliza cuando los datos de entrada tienen un tipo de codificación desconocido.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-116">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="bcaf2-117">Si este valor se usa para especificar el tipo de codificación de la salida, \_ se usará CAPICOM encode \_ Base64 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-117">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="bcaf2-118">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-118">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="bcaf2-119"><dt>**CAPICOM, codificación \_ \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="bcaf2-119"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="bcaf2-120">Los datos se guardan como una cadena codificada en Base64.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-120">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="bcaf2-121"><dt>**\_código binario de codificación de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bcaf2-121"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="bcaf2-122">Los datos se guardan como una secuencia binaria pura.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-122">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcaf2-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bcaf2-123">Return value</span></span>

<span data-ttu-id="bcaf2-124">Este método devuelve un BLOB que contiene los datos con doble cifrado en una cadena codificada.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-124">This method returns a BLOB that contains the enveloped data in an encoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcaf2-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bcaf2-125">Remarks</span></span>

<span data-ttu-id="bcaf2-126">El BLOB devuelto contiene el contenido cifrado y una clave de sesión cifrada para cada destinatario previsto.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-126">The returned BLOB contains the encrypted content and an encrypted session key for each intended recipient.</span></span> <span data-ttu-id="bcaf2-127">Estas claves de sesión se cifran mediante la clave pública de cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-127">These session keys are encrypted using the public key of each recipient.</span></span> <span data-ttu-id="bcaf2-128">Las claves de sesión cifradas solo se pueden descifrar con la clave privada de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-128">The encrypted session keys can be decrypted only with a recipient's private key.</span></span>

<span data-ttu-id="bcaf2-129">Si la propiedad [**Recipients**](envelopeddata-recipients.md) no contiene ninguna información, este método busca en el almacén de certificados AddressBook del usuario actual los destinatarios potenciales.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-129">If the [**Recipients**](envelopeddata-recipients.md) property does not contain any information, this method searches the current user's AddressBook certificate store for potential recipients.</span></span> <span data-ttu-id="bcaf2-130">Si se encuentra más de un posible destinatario, se solicita al usuario que seleccione un destinatario en un cuadro de diálogo de selección.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-130">If more than one potential recipient is found, the user is prompted to select a recipient from a selection dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcaf2-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcaf2-131">Requirements</span></span>



| <span data-ttu-id="bcaf2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcaf2-132">Requirement</span></span> | <span data-ttu-id="bcaf2-133">Value</span><span class="sxs-lookup"><span data-stu-id="bcaf2-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcaf2-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bcaf2-134">End of client support</span></span><br/> | <span data-ttu-id="bcaf2-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcaf2-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bcaf2-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="bcaf2-136">End of server support</span></span><br/> | <span data-ttu-id="bcaf2-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcaf2-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bcaf2-138">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="bcaf2-138">Redistributable</span></span><br/>       | <span data-ttu-id="bcaf2-139">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="bcaf2-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bcaf2-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bcaf2-140">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bcaf2-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcaf2-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcaf2-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcaf2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcaf2-143">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="bcaf2-143">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="bcaf2-144">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="bcaf2-144">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
