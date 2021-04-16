---
description: Guarda el certificado en un archivo.
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: 'ICertificate2:: Save (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Save
- ICertificate2.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3427feb86c705f5558d083bc39673fdf77553f58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690275"
---
# <a name="icertificate2save-method"></a><span data-ttu-id="303fd-103">ICertificate2:: Save (método)</span><span class="sxs-lookup"><span data-stu-id="303fd-103">ICertificate2::Save method</span></span>

<span data-ttu-id="303fd-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="303fd-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="303fd-105">En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="303fd-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="303fd-106">El método **Save** guarda el certificado en un archivo.</span><span class="sxs-lookup"><span data-stu-id="303fd-106">The **Save** method saves the certificate to a file.</span></span> <span data-ttu-id="303fd-107">Este método se presentó en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="303fd-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="303fd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="303fd-108">Syntax</span></span>


```VB
Certificate.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal IncludeOption ] _
)
```



## <a name="parameters"></a><span data-ttu-id="303fd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="303fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="303fd-110">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="303fd-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="303fd-111">Cadena que contiene el nombre del archivo de salida en el que se guardará el certificado.</span><span class="sxs-lookup"><span data-stu-id="303fd-111">A string that contains the name of the output file where the certificate will be saved.</span></span>

</dd> <dt>

<span data-ttu-id="303fd-112">*Contraseña* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="303fd-112">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="303fd-113">Cadena que contiene la contraseña de [*texto no cifrado*](../secgloss/p-gly.md) para un archivo de [*clave privada*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="303fd-113">A string that contains the [*plaintext*](../secgloss/p-gly.md) password for a [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="303fd-114">La contraseña puede contener hasta 32 caracteres Unicode, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="303fd-114">The password can contain up to 32 Unicode characters, including a terminating null character.</span></span> <span data-ttu-id="303fd-115">Para obtener información acerca de cómo proteger la contraseña, consulte [Administrar contraseñas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="303fd-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="303fd-116">*Guardar como* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="303fd-116">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="303fd-117">Un valor de la enumeración de [**\_ \_ \_ \_ tipo guardar como del certificado de CAPICOM**](capicom-certificate-save-as-type.md) que especifica el formato del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="303fd-117">A value of the [**CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE**](capicom-certificate-save-as-type.md) enumeration that specifies the format of the output file.</span></span> <span data-ttu-id="303fd-118">El valor predeterminado es **CAPICOM \_ Certificate \_ Save \_ as \_ cer**.</span><span class="sxs-lookup"><span data-stu-id="303fd-118">The default is **CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**.</span></span> <span data-ttu-id="303fd-119">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="303fd-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="303fd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="303fd-120">Value</span></span>                                                                                                                                                                                                                  | <span data-ttu-id="303fd-121">Significado</span><span class="sxs-lookup"><span data-stu-id="303fd-121">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <span data-ttu-id="303fd-122"><dt>**\_certificado \_ de CAPICOM guardar \_ como \_ cer**</dt></span><span class="sxs-lookup"><span data-stu-id="303fd-122"><dt>**CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**</dt></span></span> </dl> | <span data-ttu-id="303fd-123">El archivo de salida se formateará como un archivo. cer sin ninguna clave privada guardada.</span><span class="sxs-lookup"><span data-stu-id="303fd-123">The output file will be formatted as a .cer file with no private keys saved.</span></span><br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <span data-ttu-id="303fd-124"><dt>**el \_ certificado \_ de CAPICOM se guarda \_ como \_ pfx**</dt></span><span class="sxs-lookup"><span data-stu-id="303fd-124"><dt>**CAPICOM\_CERTIFICATE\_SAVE\_AS\_PFX**</dt></span></span> </dl> | <span data-ttu-id="303fd-125">El archivo de salida se formateará como un archivo. pfx (PKCS \# 12) y las claves privadas asociadas que se puedan exportar también se guardarán.</span><span class="sxs-lookup"><span data-stu-id="303fd-125">The output file will be formatted as a .pfx (PKCS \#12) file and any associated private keys that are exportable will also be saved.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="303fd-126">*IncludeOption* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="303fd-126">*IncludeOption* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="303fd-127">Un valor de la enumeración de la [**\_ \_ \_ opción incluir certificado de CAPICOM**](capicom-certificate-include-option.md) que especifica cuántos certificados de la cadena se guardan en el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="303fd-127">A value of the [**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**](capicom-certificate-include-option.md) enumeration that specifies how many certificates in the chain are saved to the output file.</span></span> <span data-ttu-id="303fd-128">El valor predeterminado es el certificado de CAPICOM \_ \_ incluir \_ solo la \_ entidad final \_ .</span><span class="sxs-lookup"><span data-stu-id="303fd-128">The default is CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY.</span></span> <span data-ttu-id="303fd-129">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="303fd-129">The following table shows the possible values.</span></span>



| <span data-ttu-id="303fd-130">Valor</span><span class="sxs-lookup"><span data-stu-id="303fd-130">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="303fd-131">Significado</span><span class="sxs-lookup"><span data-stu-id="303fd-131">Meaning</span></span>                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <span data-ttu-id="303fd-132"><dt>**el \_ certificado de CAPICOM \_ incluye una \_ cadena excepto la \_ \_ raíz**</dt></span><span class="sxs-lookup"><span data-stu-id="303fd-132"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</dt></span></span> </dl> | <span data-ttu-id="303fd-133">Guarda todos los certificados de la cadena con la excepción de la entidad raíz.</span><span class="sxs-lookup"><span data-stu-id="303fd-133">Saves all certificates in the chain with the exception of the root entity</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <span data-ttu-id="303fd-134"><dt>**el \_ certificado de CAPICOM \_ incluye una \_ \_ cadena entera**</dt></span><span class="sxs-lookup"><span data-stu-id="303fd-134"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</dt></span></span> </dl>                    | <span data-ttu-id="303fd-135">Guarda la cadena de certificados completa</span><span class="sxs-lookup"><span data-stu-id="303fd-135">Saves the complete certificate chain</span></span><br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <span data-ttu-id="303fd-136"><dt>**el \_ certificado de CAPICOM \_ incluye \_ \_ solo la entidad final \_**</dt></span><span class="sxs-lookup"><span data-stu-id="303fd-136"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</dt></span></span> </dl>       | <span data-ttu-id="303fd-137">Guarda solo el certificado de entidad final</span><span class="sxs-lookup"><span data-stu-id="303fd-137">Saves only the end entity certificate</span></span><br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="303fd-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="303fd-138">Return value</span></span>

<span data-ttu-id="303fd-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="303fd-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="303fd-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="303fd-140">Remarks</span></span>

<span data-ttu-id="303fd-141">Este método produce CAPICOM \_ E \_ no \_ se permite cuando se genera un script desde una aplicación basada en Web.</span><span class="sxs-lookup"><span data-stu-id="303fd-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="303fd-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="303fd-142">Requirements</span></span>



| <span data-ttu-id="303fd-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="303fd-143">Requirement</span></span> | <span data-ttu-id="303fd-144">Value</span><span class="sxs-lookup"><span data-stu-id="303fd-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="303fd-145">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="303fd-145">End of client support</span></span><br/> | <span data-ttu-id="303fd-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="303fd-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="303fd-147">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="303fd-147">End of server support</span></span><br/> | <span data-ttu-id="303fd-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="303fd-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="303fd-149">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="303fd-149">Redistributable</span></span><br/>       | <span data-ttu-id="303fd-150">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="303fd-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="303fd-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="303fd-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="303fd-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="303fd-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
