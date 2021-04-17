---
description: Importa un certificado de un archivo.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: 'ICertificate2:: Load (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Load
- ICertificate2.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9193297ad7eacc1994e4bf3729a87054573b1574
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670371"
---
# <a name="icertificate2load-method"></a><span data-ttu-id="665c4-103">ICertificate2:: Load (método)</span><span class="sxs-lookup"><span data-stu-id="665c4-103">ICertificate2::Load method</span></span>

<span data-ttu-id="665c4-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="665c4-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="665c4-105">En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="665c4-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="665c4-106">El método **Load** importa un certificado de un archivo.</span><span class="sxs-lookup"><span data-stu-id="665c4-106">The **Load** method imports a certificate from a file.</span></span> <span data-ttu-id="665c4-107">Este método se presentó en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="665c4-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="665c4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="665c4-108">Syntax</span></span>


```VB
Certificate.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ], _
  [ ByVal KeyLocation ] _
)
```



## <a name="parameters"></a><span data-ttu-id="665c4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="665c4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="665c4-110">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="665c4-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="665c4-111">Una cadena que contiene la ruta de acceso a un archivo. cer o. pfx que contiene los datos del certificado.</span><span class="sxs-lookup"><span data-stu-id="665c4-111">A string that contains the path to a .cer or .pfx file that contains the certificate data.</span></span>

</dd> <dt>

<span data-ttu-id="665c4-112">*Contraseña* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="665c4-112">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="665c4-113">Cadena que contiene la contraseña de [*texto no cifrado*](../secgloss/p-gly.md) para el archivo de [*clave privada*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="665c4-113">A string that contains the [*plaintext*](../secgloss/p-gly.md) password to the [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="665c4-114">La contraseña puede contener hasta 32 caracteres Unicode, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="665c4-114">The password can contain up to 32 Unicode characters, including a terminating null character.</span></span> <span data-ttu-id="665c4-115">Para obtener información acerca de cómo proteger la contraseña, consulte [Administrar contraseñas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="665c4-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="665c4-116">*KeyStorageFlag* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="665c4-116">*KeyStorageFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="665c4-117">Un valor de la enumeración de marcas de almacenamiento de claves de CAPICOM que define las marcas de almacenamiento de claves. [**\_ \_ \_**](capicom-key-storage-flag.md)</span><span class="sxs-lookup"><span data-stu-id="665c4-117">A value of the [**CAPICOM\_KEY\_STORAGE\_FLAG**](capicom-key-storage-flag.md) enumeration that defines key storage flags.</span></span> <span data-ttu-id="665c4-118">El valor predeterminado es CAPICOM \_ key \_ Storage \_ default.</span><span class="sxs-lookup"><span data-stu-id="665c4-118">The default is CAPICOM\_KEY\_STORAGE\_DEFAULT.</span></span> <span data-ttu-id="665c4-119">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="665c4-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="665c4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="665c4-120">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="665c4-121">Significado</span><span class="sxs-lookup"><span data-stu-id="665c4-121">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <span data-ttu-id="665c4-122"><dt>**CAPICOM \_ , \_ valor predeterminado de almacenamiento de claves \_**</dt></span><span class="sxs-lookup"><span data-stu-id="665c4-122"><dt>**CAPICOM\_KEY\_STORAGE\_DEFAULT**</dt></span></span> </dl>                       | <span data-ttu-id="665c4-123">Almacenamiento de claves predeterminado.</span><span class="sxs-lookup"><span data-stu-id="665c4-123">Default key storage.</span></span><br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <span data-ttu-id="665c4-124"><dt>**el \_ almacenamiento de claves de CAPICOM \_ \_ exportable**</dt></span><span class="sxs-lookup"><span data-stu-id="665c4-124"><dt>**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</dt></span></span> </dl>              | <span data-ttu-id="665c4-125">La clave es exportable.</span><span class="sxs-lookup"><span data-stu-id="665c4-125">The key is exportable.</span></span><br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <span data-ttu-id="665c4-126"><dt>**CAPICOM \_ \_ protección del \_ usuario de almacenamiento de claves \_**</dt></span><span class="sxs-lookup"><span data-stu-id="665c4-126"><dt>**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</dt></span></span> </dl> | <span data-ttu-id="665c4-127">La clave está protegida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="665c4-127">The key is user protected.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="665c4-128">*KeyLocation* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="665c4-128">*KeyLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="665c4-129">Un valor de la enumeración de la [**\_ \_ Ubicación de la clave CAPICOM**](capicom-key-location.md) que define los tipos de ubicación de clave.</span><span class="sxs-lookup"><span data-stu-id="665c4-129">A value of the [**CAPICOM\_KEY\_LOCATION**](capicom-key-location.md) enumeration that defines key location types.</span></span> <span data-ttu-id="665c4-130">El valor predeterminado es la \_ clave de usuario actual de CAPICOM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="665c4-130">The default value is CAPICOM\_CURRENT\_USER\_KEY.</span></span> <span data-ttu-id="665c4-131">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="665c4-131">The following table shows the possible values.</span></span>



| <span data-ttu-id="665c4-132">Valor</span><span class="sxs-lookup"><span data-stu-id="665c4-132">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="665c4-133">Significado</span><span class="sxs-lookup"><span data-stu-id="665c4-133">Meaning</span></span>                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <span data-ttu-id="665c4-134"><dt>**\_tecla de \_ usuario \_ actual de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="665c4-134"><dt>**CAPICOM\_CURRENT\_USER\_KEY**</dt></span></span> </dl>    | <span data-ttu-id="665c4-135">La clave es una clave de usuario.</span><span class="sxs-lookup"><span data-stu-id="665c4-135">The key is a user key.</span></span><br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <span data-ttu-id="665c4-136"><dt>**\_clave de \_ máquina \_ local de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="665c4-136"><dt>**CAPICOM\_LOCAL\_MACHINE\_KEY**</dt></span></span> </dl> | <span data-ttu-id="665c4-137">La clave es una clave del equipo.</span><span class="sxs-lookup"><span data-stu-id="665c4-137">The key is a machine key.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="665c4-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="665c4-138">Return value</span></span>

<span data-ttu-id="665c4-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="665c4-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="665c4-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="665c4-140">Remarks</span></span>

<span data-ttu-id="665c4-141">Este método produce CAPICOM \_ E \_ no \_ se permite cuando se genera un script desde una aplicación basada en Web.</span><span class="sxs-lookup"><span data-stu-id="665c4-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="665c4-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="665c4-142">Requirements</span></span>



| <span data-ttu-id="665c4-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="665c4-143">Requirement</span></span> | <span data-ttu-id="665c4-144">Value</span><span class="sxs-lookup"><span data-stu-id="665c4-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="665c4-145">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="665c4-145">End of client support</span></span><br/> | <span data-ttu-id="665c4-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="665c4-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="665c4-147">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="665c4-147">End of server support</span></span><br/> | <span data-ttu-id="665c4-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="665c4-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="665c4-149">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="665c4-149">Redistributable</span></span><br/>       | <span data-ttu-id="665c4-150">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="665c4-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="665c4-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="665c4-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="665c4-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="665c4-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
