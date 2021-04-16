---
description: Crea una firma digital en el contenido con firma anterior.
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: SignedData. Cosign (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.CoSign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1ab2a24a20fd65fad9622b775bedc59cfa28301a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671643"
---
# <a name="signeddatacosign-method"></a><span data-ttu-id="043dc-103">SignedData. Cosign (método)</span><span class="sxs-lookup"><span data-stu-id="043dc-103">SignedData.CoSign method</span></span>

<span data-ttu-id="043dc-104">\[El método de **cofirma** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="043dc-104">\[The **CoSign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="043dc-105">En su lugar, use la [**clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="043dc-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="043dc-106">El método de **cofirma** crea una [*firma digital*](../secgloss/d-gly.md) en el contenido con firma anterior.</span><span class="sxs-lookup"><span data-stu-id="043dc-106">The **CoSign** method creates a [*digital signature*](../secgloss/d-gly.md) on previously signed content.</span></span>

## <a name="syntax"></a><span data-ttu-id="043dc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="043dc-107">Syntax</span></span>


```VB
SignedData.CoSign( _
  [ ByVal Signer ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="043dc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="043dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="043dc-109">*Firmante* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="043dc-109">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="043dc-110">Referencia al objeto [**firmante**](signer.md) del firmante de los datos.</span><span class="sxs-lookup"><span data-stu-id="043dc-110">A reference to the [**Signer**](signer.md) object of the signer of the data.</span></span> <span data-ttu-id="043dc-111">El objeto de **firmante** debe tener acceso a la clave privada del certificado usado para firmar.</span><span class="sxs-lookup"><span data-stu-id="043dc-111">The **Signer** object must have access to the private key of the certificate used to sign.</span></span> <span data-ttu-id="043dc-112">Este parámetro puede ser **null**; para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="043dc-112">This parameter can be **NULL**; for more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="043dc-113">*EncodingType* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="043dc-113">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="043dc-114">Un valor de la enumeración de [**\_ \_ tipo de codificación CAPICOM**](capicom-encoding-type.md) que indica cómo se van a codificar los datos firmados.</span><span class="sxs-lookup"><span data-stu-id="043dc-114">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates how the signed data is to be encoded.</span></span> <span data-ttu-id="043dc-115">El valor predeterminado es CAPICOM \_ encode \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="043dc-115">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="043dc-116">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="043dc-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="043dc-117">Valor</span><span class="sxs-lookup"><span data-stu-id="043dc-117">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="043dc-118">Significado</span><span class="sxs-lookup"><span data-stu-id="043dc-118">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="043dc-119"><dt>**CAPICOM \_ codificar \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="043dc-119"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="043dc-120">Este tipo de codificación solo se utiliza cuando los datos de entrada tienen un tipo de codificación desconocido.</span><span class="sxs-lookup"><span data-stu-id="043dc-120">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="043dc-121">Si este valor se usa para especificar el tipo de codificación de la salida, \_ se usará CAPICOM encode \_ Base64 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="043dc-121">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="043dc-122">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="043dc-122">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="043dc-123"><dt>**CAPICOM, codificación \_ \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="043dc-123"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="043dc-124">Los datos se guardan como una cadena codificada en Base64.</span><span class="sxs-lookup"><span data-stu-id="043dc-124">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="043dc-125"><dt>**\_código binario de codificación de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="043dc-125"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="043dc-126">Los datos se guardan como una secuencia binaria pura.</span><span class="sxs-lookup"><span data-stu-id="043dc-126">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="043dc-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="043dc-127">Return value</span></span>

<span data-ttu-id="043dc-128">Este método devuelve una cadena que contiene los datos firmados y codificados.</span><span class="sxs-lookup"><span data-stu-id="043dc-128">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="043dc-129">Si se produce un error en este método, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="043dc-129">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="043dc-130">El objeto **Err** contendrá información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="043dc-130">The **Err** object will contain additional information about the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="043dc-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="043dc-131">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="043dc-132">Cuando se llama a este método desde un script Web, el script debe usar la [*clave privada*](../secgloss/p-gly.md) para crear una firma digital.</span><span class="sxs-lookup"><span data-stu-id="043dc-132">When this method is called from a web script, the script needs to use your [*private key*](../secgloss/p-gly.md) to create a digital signature.</span></span> <span data-ttu-id="043dc-133">Permitir a los sitios web que no son de confianza usar su clave privada es un riesgo para la seguridad.</span><span class="sxs-lookup"><span data-stu-id="043dc-133">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="043dc-134">Un cuadro de diálogo que pregunta si el sitio web puede usar su clave privada aparece cuando se llama por primera vez a este método.</span><span class="sxs-lookup"><span data-stu-id="043dc-134">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="043dc-135">Si permite que el script use su clave privada para crear una firma digital y selecciona "no volver a mostrar este cuadro de diálogo", el cuadro de diálogo ya no aparecerá en ningún script del dominio que use la clave privada para crear una firma digital.</span><span class="sxs-lookup"><span data-stu-id="043dc-135">If you allow the script to use your private key to create a digital signature and select "Do not show this dialog box again," the dialog box will no longer appear for any script within that domain that uses your private key to create a digital signature.</span></span> <span data-ttu-id="043dc-136">Sin embargo, los scripts que se encuentran fuera de ese dominio y que intentan usar la clave privada para crear una firma digital seguirán provocando que aparezca este cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="043dc-136">However, scripts outside that domain that attempt to use your private key to create a digital signature will still cause this dialog box to appear.</span></span> <span data-ttu-id="043dc-137">Si no permite que el script use su clave privada y selecciona "no volver a mostrar este cuadro de diálogo", se rechazará automáticamente la capacidad de usar la clave privada para crear firmas digitales en los scripts de ese dominio.</span><span class="sxs-lookup"><span data-stu-id="043dc-137">If you do not allow the script to use your private key and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to use your private key to create digital signatures.</span></span>

 

<span data-ttu-id="043dc-138">No se garantiza que los cofirmantes estén en ningún orden determinado.</span><span class="sxs-lookup"><span data-stu-id="043dc-138">Cosigners are not guaranteed to be in any particular order.</span></span>

<span data-ttu-id="043dc-139">Los resultados siguientes se aplican al valor del parámetro *Signer* :</span><span class="sxs-lookup"><span data-stu-id="043dc-139">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="043dc-140">Si el parámetro del *firmante* no es **null**, este método utiliza la clave privada a la que apunta el certificado asociado para cifrar la cofirma.</span><span class="sxs-lookup"><span data-stu-id="043dc-140">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the cosignature.</span></span> <span data-ttu-id="043dc-141">Si no está disponible la clave privada a la que apunta el certificado, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="043dc-141">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="043dc-142">Si el parámetro de *firmante* es **null** y hay exactamente un certificado en el usuario actual \_ mi almacén que tiene acceso a una clave privada, ese certificado se usa para crear la firma.</span><span class="sxs-lookup"><span data-stu-id="043dc-142">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key, that certificate is used to create the cosignature.</span></span>
-   <span data-ttu-id="043dc-143">Si el parámetro de *firmante* es **null**, el valor de la propiedad [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) es true y hay más de un certificado en el \_ usuario actual My Store con una clave privada disponible, aparece un cuadro de diálogo que permite al usuario seleccionar qué certificado se usa.</span><span class="sxs-lookup"><span data-stu-id="043dc-143">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="043dc-144">Si el parámetro de *firmante* es **null** y la propiedad [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) es false, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="043dc-144">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="043dc-145">Si el parámetro de *firmante* es **null** y no hay ningún certificado en el \_ usuario actual My Store con una clave privada disponible, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="043dc-145">If the *Signer* parameter is **NULL** and there is no certificate in the CURRENT\_USER MY store with an available private key, the method fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="043dc-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="043dc-146">Requirements</span></span>



| <span data-ttu-id="043dc-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="043dc-147">Requirement</span></span> | <span data-ttu-id="043dc-148">Value</span><span class="sxs-lookup"><span data-stu-id="043dc-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="043dc-149">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="043dc-149">Redistributable</span></span><br/> | <span data-ttu-id="043dc-150">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="043dc-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="043dc-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="043dc-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="043dc-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="043dc-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="043dc-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="043dc-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="043dc-154">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="043dc-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="043dc-155">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="043dc-155">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
