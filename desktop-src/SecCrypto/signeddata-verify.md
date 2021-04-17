---
description: Determina si las firmas de los datos firmados en el objeto SignedData son válidas.
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: SignedData. verify (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3cb48943a826296c13df80130171442fc29435f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670503"
---
# <a name="signeddataverify-method"></a><span data-ttu-id="63d8c-103">SignedData. verify (método)</span><span class="sxs-lookup"><span data-stu-id="63d8c-103">SignedData.Verify method</span></span>

<span data-ttu-id="63d8c-104">\[El método **Verify** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="63d8c-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="63d8c-105">En su lugar, use la [**clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="63d8c-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="63d8c-106">El método **Verify** determina si las [*firmas*](../secgloss/d-gly.md) de los datos firmados en el objeto [**SignedData**](signeddata.md) son válidas.</span><span class="sxs-lookup"><span data-stu-id="63d8c-106">The **Verify** method determines whether the [*signatures*](../secgloss/d-gly.md) on signed data in the [**SignedData**](signeddata.md) object are valid.</span></span> <span data-ttu-id="63d8c-107">Para comprobar una firma, el [*hash*](../secgloss/h-gly.md) cifrado del contenido se descifra mediante la clave pública del firmante del certificado del firmante.</span><span class="sxs-lookup"><span data-stu-id="63d8c-107">To verify a signature, the encrypted [*hash*](../secgloss/h-gly.md) of the contents is decrypted by using the signer's public key from the signer's certificate.</span></span> <span data-ttu-id="63d8c-108">El hash descifrado se compara con un nuevo hash del contenido de los datos.</span><span class="sxs-lookup"><span data-stu-id="63d8c-108">The decrypted hash is compared to a new hash of the data content.</span></span> <span data-ttu-id="63d8c-109">Una firma es válida si los valores hash coinciden.</span><span class="sxs-lookup"><span data-stu-id="63d8c-109">A signature is valid if the hashes match.</span></span> <span data-ttu-id="63d8c-110">Además, este método también crea una cadena de certificados para determinar la validez del certificado que proporciona la [*clave pública*](../secgloss/p-gly.md) utilizada para descifrar el hash.</span><span class="sxs-lookup"><span data-stu-id="63d8c-110">In addition, this method also builds a certificate chain to determine the validity of the certificate that provides the [*public key*](../secgloss/p-gly.md) used to decrypt the hash.</span></span>

## <a name="syntax"></a><span data-ttu-id="63d8c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63d8c-111">Syntax</span></span>


```VB
SignedData.Verify( _
  ByVal SignedMessage, _
  [ ByVal bDetached ], _
  [ ByVal VerifyFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="63d8c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63d8c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63d8c-113">*SignedMessage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63d8c-113">*SignedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63d8c-114">Cadena que contiene el mensaje firmado que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="63d8c-114">A string that contains the signed message to be verified.</span></span>

</dd> <dt>

<span data-ttu-id="63d8c-115">*bDetached* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="63d8c-115">*bDetached* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63d8c-116">Si es **true**, se desasocian los datos que se van a firmar; es decir, el contenido que está firmado no se incluye como parte del objeto firmado.</span><span class="sxs-lookup"><span data-stu-id="63d8c-116">If **True**, the data to be signed is detached; that is, the content that is signed is not included as part of the signed object.</span></span> <span data-ttu-id="63d8c-117">Para comprobar la firma en el contenido separado, una aplicación debe tener una copia del contenido original.</span><span class="sxs-lookup"><span data-stu-id="63d8c-117">To verify the signature on detached content, an application must have a copy of the original content.</span></span> <span data-ttu-id="63d8c-118">El contenido separado se usa a menudo para reducir el tamaño de un objeto firmado que se va a enviar a través de la web, si el destinatario del mensaje firmado tiene una copia original de los datos firmados.</span><span class="sxs-lookup"><span data-stu-id="63d8c-118">Detached content is often used to decrease the size of a signed object to be sent across the web, if the recipient of the signed message has an original copy of the signed data.</span></span> <span data-ttu-id="63d8c-119">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="63d8c-119">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="63d8c-120">*VerifyFlag* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="63d8c-120">*VerifyFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63d8c-121">Un valor de la enumeración de la marca de comprobación de [ \_ \_ datos \_ \_ firmados de CAPICOM](capicom-signed-data-verify-flag.md) que indica la Directiva de comprobación.</span><span class="sxs-lookup"><span data-stu-id="63d8c-121">A value of the [CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG](capicom-signed-data-verify-flag.md) enumeration that indicates the verification policy.</span></span> <span data-ttu-id="63d8c-122">El valor predeterminado es CAPICOM \_ Verify \_ Signature \_ and \_ Certificate.</span><span class="sxs-lookup"><span data-stu-id="63d8c-122">The default value is CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE.</span></span> <span data-ttu-id="63d8c-123">Con este valor, se comprueba la validez del certificado y la validez de la firma.</span><span class="sxs-lookup"><span data-stu-id="63d8c-123">Using this value, both the validity of the certificate and the validity of the signature are checked.</span></span> <span data-ttu-id="63d8c-124">Este parámetro se puede establecer para comprobar la firma y no el certificado.</span><span class="sxs-lookup"><span data-stu-id="63d8c-124">This parameter may be set to verify the signature and not the certificate.</span></span> <span data-ttu-id="63d8c-125">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="63d8c-125">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="63d8c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="63d8c-126">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="63d8c-127">Significado</span><span class="sxs-lookup"><span data-stu-id="63d8c-127">Meaning</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <span data-ttu-id="63d8c-128"><dt>**CAPICOM \_ comprobar \_ solo la firma \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63d8c-128"><dt>**CAPICOM\_VERIFY\_SIGNATURE\_ONLY**</dt></span></span> </dl>                                   | <span data-ttu-id="63d8c-129">Solo se comprueba la firma.</span><span class="sxs-lookup"><span data-stu-id="63d8c-129">Only the signature is checked.</span></span><br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <span data-ttu-id="63d8c-130"><dt>**CAPICOM \_ comprobar la \_ firma \_ y el \_ certificado**</dt></span><span class="sxs-lookup"><span data-stu-id="63d8c-130"><dt>**CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE**</dt></span></span> </dl> | <span data-ttu-id="63d8c-131">Se comprueban tanto la firma como la validez del certificado utilizado para crear la firma.</span><span class="sxs-lookup"><span data-stu-id="63d8c-131">Both the signature and the validity of the certificate used to create the signature are checked.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63d8c-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63d8c-132">Return value</span></span>

<span data-ttu-id="63d8c-133">Este método devuelve una cadena que contiene los datos firmados y codificados.</span><span class="sxs-lookup"><span data-stu-id="63d8c-133">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="63d8c-134">Si se produce un error en este método, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="63d8c-134">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="63d8c-135">El objeto **Err** contendrá información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="63d8c-135">The **Err** object will contain additional information about the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="63d8c-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63d8c-136">Requirements</span></span>



| <span data-ttu-id="63d8c-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="63d8c-137">Requirement</span></span> | <span data-ttu-id="63d8c-138">Value</span><span class="sxs-lookup"><span data-stu-id="63d8c-138">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63d8c-139">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="63d8c-139">Redistributable</span></span><br/> | <span data-ttu-id="63d8c-140">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="63d8c-140">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="63d8c-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63d8c-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="63d8c-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63d8c-142"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63d8c-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="63d8c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63d8c-144">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="63d8c-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="63d8c-145">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="63d8c-145">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
