---
description: Guarda los objetos de certificado en la colección.
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Certificates. Save (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36ab04b394bddcd829d9f15e7562b72125388d33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671695"
---
# <a name="certificatessave-method"></a><span data-ttu-id="3b044-103">Certificates. Save (método)</span><span class="sxs-lookup"><span data-stu-id="3b044-103">Certificates.Save method</span></span>

<span data-ttu-id="3b044-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3b044-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3b044-105">En su lugar, use la [**clase X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="3b044-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3b044-106">El método **Save** guarda los objetos de [**certificado**](certificate.md) en la colección.</span><span class="sxs-lookup"><span data-stu-id="3b044-106">The **Save** method saves the [**Certificate**](certificate.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b044-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b044-107">Syntax</span></span>


```VB
Certificates.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal ExportFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="3b044-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b044-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b044-109">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b044-109">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b044-110">Cadena que contiene el nombre del archivo de salida donde se guardarán los certificados.</span><span class="sxs-lookup"><span data-stu-id="3b044-110">A string that contains the name of the output file where the certificates will be saved.</span></span>

</dd> <dt>

<span data-ttu-id="3b044-111">*Contraseña* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3b044-111">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3b044-112">Cadena que contiene la contraseña de [*texto no cifrado*](../secgloss/p-gly.md) para un archivo de [*clave privada*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="3b044-112">A string that contains the [*plaintext*](../secgloss/p-gly.md) password for a [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="3b044-113">El valor predeterminado es la cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="3b044-113">The default value is the empty string ("").</span></span> <span data-ttu-id="3b044-114">Se pueden usar hasta 32 caracteres Unicode, incluido un carácter nulo de terminación, para la contraseña.</span><span class="sxs-lookup"><span data-stu-id="3b044-114">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="3b044-115">Para obtener información acerca de cómo proteger la contraseña, consulte [Administrar contraseñas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="3b044-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b044-116">*Guardar como* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3b044-116">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3b044-117">Un valor de la enumeración de los [**\_ certificados CAPICOM \_ Save \_ as \_ Type**](capicom-certificates-save-as-type.md) que especifica el formato del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="3b044-117">A value of the [**CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE**](capicom-certificates-save-as-type.md) enumeration that specifies the format of the output file.</span></span> <span data-ttu-id="3b044-118">El valor predeterminado es CAPICOM \_ Certificates \_ Save \_ as \_ pfx.</span><span class="sxs-lookup"><span data-stu-id="3b044-118">The default is CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX.</span></span> <span data-ttu-id="3b044-119">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="3b044-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="3b044-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3b044-120">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="3b044-121">Significado</span><span class="sxs-lookup"><span data-stu-id="3b044-121">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <span data-ttu-id="3b044-122"><dt>**los \_ certificados \_ de CAPICOM se guardan \_ como \_ pfx**</dt></span><span class="sxs-lookup"><span data-stu-id="3b044-122"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX**</dt></span></span> </dl>                      | <span data-ttu-id="3b044-123">Los certificados se guardan como un archivo PFX.</span><span class="sxs-lookup"><span data-stu-id="3b044-123">The certificates are saved as a PFX.</span></span><br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <span data-ttu-id="3b044-124"><dt>**Los \_ certificados \_ de CAPICOM se guardan \_ como \_ pkcs7**</dt></span><span class="sxs-lookup"><span data-stu-id="3b044-124"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PKCS7**</dt></span></span> </dl>                | <span data-ttu-id="3b044-125">Los certificados se guardan como PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="3b044-125">The certificates are saved as a PKCS \#7.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <span data-ttu-id="3b044-126"><dt>**los \_ certificados \_ de CAPICOM se guardan \_ como \_ serializados**</dt></span><span class="sxs-lookup"><span data-stu-id="3b044-126"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_SERIALIZED**</dt></span></span> </dl> | <span data-ttu-id="3b044-127">Los certificados se guardan como serializados.</span><span class="sxs-lookup"><span data-stu-id="3b044-127">The certificates are saved as serialized.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3b044-128">*ExportFlag* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3b044-128">*ExportFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3b044-129">Un valor de la enumeración de la [**\_ \_ marca de exportación de CAPICOM**](capicom-export-flag.md) que especifica si se omiten los errores de exportación de claves privadas.</span><span class="sxs-lookup"><span data-stu-id="3b044-129">A value of the [**CAPICOM\_EXPORT\_FLAG**](capicom-export-flag.md) enumeration that specifies whether any private key export errors are ignored.</span></span> <span data-ttu-id="3b044-130">El valor predeterminado es CAPICOM \_ Export \_ default.</span><span class="sxs-lookup"><span data-stu-id="3b044-130">The default is CAPICOM\_EXPORT\_DEFAULT.</span></span> <span data-ttu-id="3b044-131">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="3b044-131">The following table shows the possible values.</span></span>



| <span data-ttu-id="3b044-132">Valor</span><span class="sxs-lookup"><span data-stu-id="3b044-132">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="3b044-133">Significado</span><span class="sxs-lookup"><span data-stu-id="3b044-133">Meaning</span></span>                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <span data-ttu-id="3b044-134"><dt>**\_ \_ configuración predeterminada de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="3b044-134"><dt>**CAPICOM\_EXPORT\_DEFAULT**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="3b044-135">No se omiten los errores de exportación de clave privada.</span><span class="sxs-lookup"><span data-stu-id="3b044-135">Private key export errors are not ignored.</span></span><br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <span data-ttu-id="3b044-136"><dt>**ERROR de exportación de CAPICOM \_ \_ omitir \_ \_ clave privada \_ no \_ exportable \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3b044-136"><dt>**CAPICOM\_EXPORT\_IGNORE\_PRIVATE\_KEY\_NOT\_EXPORTABLE\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="3b044-137">Se omiten los errores de exportación de clave privada.</span><span class="sxs-lookup"><span data-stu-id="3b044-137">Private key export errors are ignored.</span></span><br/>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b044-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b044-138">Return value</span></span>

<span data-ttu-id="3b044-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3b044-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b044-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b044-140">Remarks</span></span>

<span data-ttu-id="3b044-141">Este método produce CAPICOM \_ E \_ no \_ se permite cuando se genera un script desde una aplicación basada en Web.</span><span class="sxs-lookup"><span data-stu-id="3b044-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

<span data-ttu-id="3b044-142">Los objetos de [**certificado**](certificate.md) se pueden recuperar mediante el método [**Store. Load**](store-load.md) .</span><span class="sxs-lookup"><span data-stu-id="3b044-142">The [**Certificate**](certificate.md) objects can be retrieved by using the [**Store.Load**](store-load.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b044-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b044-143">Requirements</span></span>



| <span data-ttu-id="3b044-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b044-144">Requirement</span></span> | <span data-ttu-id="3b044-145">Value</span><span class="sxs-lookup"><span data-stu-id="3b044-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b044-146">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3b044-146">End of client support</span></span><br/> | <span data-ttu-id="3b044-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b044-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3b044-148">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3b044-148">End of server support</span></span><br/> | <span data-ttu-id="3b044-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b044-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3b044-150">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3b044-150">Redistributable</span></span><br/>       | <span data-ttu-id="3b044-151">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="3b044-151">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3b044-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b044-152">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3b044-153"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b044-153"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b044-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b044-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b044-155">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="3b044-155">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
