---
description: Crea una firma digital en el contenido que se va a firmar. Una firma digital consta de un hash del contenido que se va a firmar y que se cifra mediante la clave privada del firmante.
ms.assetid: ee98a36c-f9a9-4247-ae48-7b1a10b92be4
title: SignedData. Sign (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9f885bb110b51264bc6108ca8c0f881cc48f7710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690059"
---
# <a name="signeddatasign-method"></a><span data-ttu-id="93943-104">SignedData. Sign (método)</span><span class="sxs-lookup"><span data-stu-id="93943-104">SignedData.Sign method</span></span>

<span data-ttu-id="93943-105">\[El método **Sign** está disponible para su uso en los sistemas operativos especificados en la sección requirements.</span><span class="sxs-lookup"><span data-stu-id="93943-105">\[The **Sign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="93943-106">En su lugar, use la [**clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="93943-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="93943-107">El método **Sign** crea una [*firma digital*](../secgloss/d-gly.md) en el contenido que se va a firmar.</span><span class="sxs-lookup"><span data-stu-id="93943-107">The **Sign** method creates a [*digital signature*](../secgloss/d-gly.md) on the content to be signed.</span></span> <span data-ttu-id="93943-108">Una firma digital consta de un [*hash*](../secgloss/h-gly.md) del contenido que se va a firmar y que se cifra mediante la clave privada del firmante.</span><span class="sxs-lookup"><span data-stu-id="93943-108">A digital signature consists of a [*hash*](../secgloss/h-gly.md) of the content to be signed that is encrypted by using the private key of the signer.</span></span> <span data-ttu-id="93943-109">Este método solo se puede usar después de que se haya inicializado la propiedad [**SignedData. Content**](signeddata-content.md) .</span><span class="sxs-lookup"><span data-stu-id="93943-109">This method can only be used after the [**SignedData.Content**](signeddata-content.md) property has been initialized.</span></span> <span data-ttu-id="93943-110">Si se llama al método **Sign** en un objeto que ya tiene una firma, se reemplaza la firma anterior.</span><span class="sxs-lookup"><span data-stu-id="93943-110">If the **Sign** method is called on an object that already has a signature, the old signature is replaced.</span></span> <span data-ttu-id="93943-111">La firma se crea mediante el algoritmo de firma de SHA1.</span><span class="sxs-lookup"><span data-stu-id="93943-111">The signature is created by using the SHA1 signing algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="93943-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93943-112">Syntax</span></span>


```VB
SignedData.Sign( _
  [ ByVal Signer ], _
  [ ByVal bDetached ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="93943-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93943-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93943-114">*Firmante* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="93943-114">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93943-115">Referencia al objeto [**firmante**](signer.md) del firmante de los datos.</span><span class="sxs-lookup"><span data-stu-id="93943-115">A reference to the [**Signer**](signer.md) object of the signer of the data.</span></span> <span data-ttu-id="93943-116">El objeto de **firmante** debe tener acceso a la [*clave privada*](../secgloss/p-gly.md) del [*certificado*](../secgloss/c-gly.md) usado para firmar.</span><span class="sxs-lookup"><span data-stu-id="93943-116">The **Signer** object must have access to the [*private key*](../secgloss/p-gly.md) of the [*certificate*](../secgloss/c-gly.md) used to sign.</span></span> <span data-ttu-id="93943-117">Este parámetro puede ser **null**; para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="93943-117">This parameter can be **NULL**; for more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="93943-118">*bDetached* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="93943-118">*bDetached* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93943-119">Si es **true**, se desasocian los datos que se van a firmar; es decir, el contenido que está firmado no se incluye como parte del objeto firmado.</span><span class="sxs-lookup"><span data-stu-id="93943-119">If **True**, the data to be signed is detached; that is, the content that is signed is not included as part of the signed object.</span></span> <span data-ttu-id="93943-120">Para comprobar la firma en el contenido separado, una aplicación debe tener una copia del contenido original.</span><span class="sxs-lookup"><span data-stu-id="93943-120">To verify the signature on detached content, an application must have a copy of the original content.</span></span> <span data-ttu-id="93943-121">El contenido separado se usa a menudo para reducir el tamaño de un objeto firmado que se va a enviar a través de la web, si el destinatario del mensaje firmado tiene una copia original de los datos firmados.</span><span class="sxs-lookup"><span data-stu-id="93943-121">Detached content is often used to decrease the size of a signed object to be sent across the web, if the recipient of the signed message has an original copy of the signed data.</span></span> <span data-ttu-id="93943-122">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="93943-122">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="93943-123">*EncodingType* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="93943-123">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93943-124">Un valor de la enumeración de [ \_ \_ tipo de codificación CAPICOM](capicom-encoding-type.md) que indica cómo se van a codificar los datos firmados.</span><span class="sxs-lookup"><span data-stu-id="93943-124">A value of the [CAPICOM\_ENCODING\_TYPE](capicom-encoding-type.md) enumeration that indicates how the signed data is to be encoded.</span></span> <span data-ttu-id="93943-125">El valor predeterminado es CAPICOM \_ encode \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="93943-125">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="93943-126">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="93943-126">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="93943-127">Valor</span><span class="sxs-lookup"><span data-stu-id="93943-127">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="93943-128">Significado</span><span class="sxs-lookup"><span data-stu-id="93943-128">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="93943-129"><dt>**CAPICOM \_ codificar \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="93943-129"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="93943-130">Este tipo de codificación solo se utiliza cuando los datos de entrada tienen un tipo de codificación desconocido.</span><span class="sxs-lookup"><span data-stu-id="93943-130">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="93943-131">Si este valor se usa para especificar el tipo de codificación de la salida, \_ se usará CAPICOM encode \_ Base64 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="93943-131">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="93943-132">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="93943-132">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="93943-133"><dt>**CAPICOM, codificación \_ \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="93943-133"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="93943-134">Los datos se guardan como una cadena codificada en Base64.</span><span class="sxs-lookup"><span data-stu-id="93943-134">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="93943-135"><dt>**\_código binario de codificación de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="93943-135"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="93943-136">Los datos se guardan como una secuencia binaria pura.</span><span class="sxs-lookup"><span data-stu-id="93943-136">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93943-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93943-137">Return value</span></span>

<span data-ttu-id="93943-138">Este método devuelve una cadena que contiene los datos firmados y codificados.</span><span class="sxs-lookup"><span data-stu-id="93943-138">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="93943-139">Si se produce un error en este método, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="93943-139">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="93943-140">El objeto **Err** contendrá información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="93943-140">The **Err** object will contain additional information about the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="93943-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93943-141">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93943-142">Cuando se llama a este método desde un script Web, el script debe usar la clave privada para crear una firma digital.</span><span class="sxs-lookup"><span data-stu-id="93943-142">When this method is called from a web script, the script needs to use your private key to create a digital signature.</span></span> <span data-ttu-id="93943-143">Permitir a los sitios web que no son de confianza usar su clave privada es un riesgo para la seguridad.</span><span class="sxs-lookup"><span data-stu-id="93943-143">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="93943-144">Un cuadro de diálogo que pregunta si el sitio web puede usar su clave privada aparece cuando se llama por primera vez a este método.</span><span class="sxs-lookup"><span data-stu-id="93943-144">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="93943-145">Si permite que el script use su clave privada para crear una firma digital y selecciona "no volver a mostrar este cuadro de diálogo", el cuadro de diálogo ya no aparecerá en ningún script del dominio que use la clave privada para crear una firma digital.</span><span class="sxs-lookup"><span data-stu-id="93943-145">If you allow the script to use your private key to create a digital signature and select "Do not show this dialog box again," the dialog box will no longer appear for any script within that domain that uses your private key to create a digital signature.</span></span> <span data-ttu-id="93943-146">Sin embargo, los scripts que se encuentran fuera de ese dominio y que intentan usar la clave privada para crear una firma digital seguirán provocando que aparezca este cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="93943-146">However, scripts outside that domain that attempt to use your private key to create a digital signature will still cause this dialog box to appear.</span></span> <span data-ttu-id="93943-147">Si no permite que el script use su clave privada y selecciona "no volver a mostrar este cuadro de diálogo", se rechazará automáticamente la capacidad de usar la clave privada para crear firmas digitales en los scripts de ese dominio.</span><span class="sxs-lookup"><span data-stu-id="93943-147">If you do not allow the script to use your private key and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to use your private key to create digital signatures.</span></span>

 

<span data-ttu-id="93943-148">Dado que la creación de una [*firma digital*](../secgloss/d-gly.md) requiere el uso de una [*clave privada*](../secgloss/p-gly.md), las aplicaciones basadas en Web que intenten usar este método requerirán mensajes de interfaz de usuario que permitan al usuario aprobar el uso de la clave privada por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="93943-148">Because creating a [*digital signature*](../secgloss/d-gly.md) requires the use of a [*private key*](../secgloss/p-gly.md), web-based applications that attempt to use this method will require user interface prompts that allow the user to approve the use of the private key, for security reasons.</span></span>

<span data-ttu-id="93943-149">Los resultados siguientes se aplican al valor del parámetro *Signer* :</span><span class="sxs-lookup"><span data-stu-id="93943-149">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="93943-150">Si el parámetro del *firmante* no es **null**, este método utiliza la clave privada a la que apunta el certificado asociado para cifrar la firma.</span><span class="sxs-lookup"><span data-stu-id="93943-150">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the signature.</span></span> <span data-ttu-id="93943-151">Si no está disponible la clave privada a la que apunta el certificado, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="93943-151">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="93943-152">Si el parámetro de *firmante* es **null** y hay exactamente un certificado en el usuario actual \_ mi almacén que tiene acceso a una clave privada, ese certificado se usa para crear la firma.</span><span class="sxs-lookup"><span data-stu-id="93943-152">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key, that certificate is used to create the signature.</span></span>
-   <span data-ttu-id="93943-153">Si el parámetro de *firmante* es **null**, el valor de la propiedad [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) es true y hay más de un certificado en el \_ usuario actual My Store con una clave privada disponible, aparece un cuadro de diálogo que permite al usuario seleccionar qué certificado se usa.</span><span class="sxs-lookup"><span data-stu-id="93943-153">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="93943-154">Si el parámetro de *firmante* es **null** y la propiedad [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) es false, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="93943-154">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="93943-155">Si el parámetro de *firmante* es **null** y no hay ningún certificado en el \_ usuario actual My Store con una clave privada disponible, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="93943-155">If the *Signer* parameter is **NULL** and there is no certificate in the CURRENT\_USER MY store with an available private key, the method fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="93943-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93943-156">Requirements</span></span>



| <span data-ttu-id="93943-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="93943-157">Requirement</span></span> | <span data-ttu-id="93943-158">Value</span><span class="sxs-lookup"><span data-stu-id="93943-158">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93943-159">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="93943-159">Redistributable</span></span><br/> | <span data-ttu-id="93943-160">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="93943-160">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="93943-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93943-161">DLL</span></span><br/>             | <dl> <span data-ttu-id="93943-162"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93943-162"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93943-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="93943-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93943-164">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="93943-164">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="93943-165">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="93943-165">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
