---
description: Importa los certificados de un archivo en el almacén.
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Store. Load (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 32261a6fd8c5cf4382832d8286d63ce5d44fb542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671837"
---
# <a name="storeload-method"></a><span data-ttu-id="13801-103">Store. Load (método)</span><span class="sxs-lookup"><span data-stu-id="13801-103">Store.Load method</span></span>

<span data-ttu-id="13801-104">\[El método **Load** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="13801-104">\[The **Load** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="13801-105">En su lugar, use la [**clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="13801-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="13801-106">El método **Load** importa los certificados de un archivo en el almacén.</span><span class="sxs-lookup"><span data-stu-id="13801-106">The **Load** method imports certificates from a file into the store.</span></span>

## <a name="syntax"></a><span data-ttu-id="13801-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13801-107">Syntax</span></span>


```VB
Store.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="13801-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13801-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13801-109">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13801-109">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13801-110">La cadena que contiene la ruta de acceso a un archivo. cer,. SST,. SPC,. p7s o. pfx, o cualquier archivo firmado con Authenticode.</span><span class="sxs-lookup"><span data-stu-id="13801-110">The string that contains the path to a .cer, .sst, .spc, .p7s, or .pfx file, or any Authenticode signed file.</span></span>

</dd> <dt>

<span data-ttu-id="13801-111">*Contraseña* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="13801-111">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="13801-112">Cadena que contiene la contraseña de texto no cifrado del archivo.</span><span class="sxs-lookup"><span data-stu-id="13801-112">The string that contains the plaintext password to the file.</span></span> <span data-ttu-id="13801-113">Se pueden usar hasta 32 caracteres Unicode, incluido un carácter nulo de terminación, para la contraseña.</span><span class="sxs-lookup"><span data-stu-id="13801-113">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="13801-114">Para obtener información acerca de cómo proteger la contraseña, consulte [Administrar contraseñas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="13801-114">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="13801-115">*KeyStorageFlag* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="13801-115">*KeyStorageFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="13801-116">Un valor de la enumeración de marcas de almacenamiento de claves de CAPICOM que define las marcas de almacenamiento de claves. [**\_ \_ \_**](capicom-key-storage-flag.md)</span><span class="sxs-lookup"><span data-stu-id="13801-116">A value of the [**CAPICOM\_KEY\_STORAGE\_FLAG**](capicom-key-storage-flag.md) enumeration that defines key storage flags.</span></span> <span data-ttu-id="13801-117">El valor predeterminado es CAPICOM \_ key \_ Storage \_ default.</span><span class="sxs-lookup"><span data-stu-id="13801-117">The default is CAPICOM\_KEY\_STORAGE\_DEFAULT.</span></span> <span data-ttu-id="13801-118">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="13801-118">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="13801-119">Valor</span><span class="sxs-lookup"><span data-stu-id="13801-119">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="13801-120">Significado</span><span class="sxs-lookup"><span data-stu-id="13801-120">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <span data-ttu-id="13801-121"><dt>**CAPICOM \_ , \_ valor predeterminado de almacenamiento de claves \_**</dt></span><span class="sxs-lookup"><span data-stu-id="13801-121"><dt>**CAPICOM\_KEY\_STORAGE\_DEFAULT**</dt></span></span> </dl>                       | <span data-ttu-id="13801-122">Almacenamiento de claves predeterminado.</span><span class="sxs-lookup"><span data-stu-id="13801-122">Default key storage.</span></span><br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <span data-ttu-id="13801-123"><dt>**el \_ almacenamiento de claves de CAPICOM \_ \_ exportable**</dt></span><span class="sxs-lookup"><span data-stu-id="13801-123"><dt>**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</dt></span></span> </dl>              | <span data-ttu-id="13801-124">La clave es exportable.</span><span class="sxs-lookup"><span data-stu-id="13801-124">The key is exportable.</span></span><br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <span data-ttu-id="13801-125"><dt>**CAPICOM \_ \_ protección del \_ usuario de almacenamiento de claves \_**</dt></span><span class="sxs-lookup"><span data-stu-id="13801-125"><dt>**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</dt></span></span> </dl> | <span data-ttu-id="13801-126">La clave está protegida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="13801-126">The key is user protected.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13801-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13801-127">Return value</span></span>

<span data-ttu-id="13801-128">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="13801-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13801-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13801-129">Remarks</span></span>

<span data-ttu-id="13801-130">Si se llama al método **Load** en un almacén de memoria, los contenedores de claves creados se eliminarán cuando se elimine el almacén de memoria.</span><span class="sxs-lookup"><span data-stu-id="13801-130">If the **Load** method is called on a memory store, any key containers that are created will be deleted when the memory store is deleted.</span></span> <span data-ttu-id="13801-131">Por ejemplo, si se carga un archivo. pfx en un almacén de memoria y posteriormente se agrega a un almacén del sistema (por ejemplo, el almacén My) del almacén de memoria, el certificado del almacén My no contendrá una clave.</span><span class="sxs-lookup"><span data-stu-id="13801-131">For example, if a .pfx file is loaded into a memory store and later added to a system store (such as the My store) from the memory store, the certificate in the My store will not contain a key.</span></span> <span data-ttu-id="13801-132">En este caso, el archivo. pfx debe cargarse directamente en mi almacén.</span><span class="sxs-lookup"><span data-stu-id="13801-132">In this case, the .pfx file should be loaded directly into the My store.</span></span>

<span data-ttu-id="13801-133">Este método produce CAPICOM \_ E \_ no \_ se permite cuando se genera un script desde una aplicación basada en Web.</span><span class="sxs-lookup"><span data-stu-id="13801-133">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

<span data-ttu-id="13801-134">Si la contraseña no puede descifrar el archivo de clave privada, se debe consultar el [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="13801-134">If the password fails to decrypt the private key file, then the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) should be queried.</span></span> <span data-ttu-id="13801-135">Si el CSP predeterminado es el proveedor de servicios criptográficos de base de Microsoft y se produce un error en la operación de descifrado, se debe volver a intentar la operación de descifrado con el proveedor de servicios criptográficos seguros de Microsoft o con el proveedor de cifrado mejorado de Microsoft, lo que esté disponible</span><span class="sxs-lookup"><span data-stu-id="13801-135">If the default CSP is the Microsoft Base Cryptographic Provider and the decrypt operation fails, then the decrypt operation should be tried again with the Microsoft Strong Cryptographic Provider or Microsoft Enhanced Cryptographic Provider, whichever is available.</span></span>

<span data-ttu-id="13801-136">Si el certificado que se carga en el almacén es el mismo que el que ya existe, el método **Load** eliminará el certificado existente del almacén y, a continuación, agregará el nuevo certificado.</span><span class="sxs-lookup"><span data-stu-id="13801-136">If the certificate being loaded into the store is the same as one that is already there, the **Load** method will delete the existing certificate from the store and then add the new certificate.</span></span> <span data-ttu-id="13801-137">El nuevo certificado heredará las propiedades del certificado existente.</span><span class="sxs-lookup"><span data-stu-id="13801-137">The new certificate will inherit properties from the existing certificate.</span></span> <span data-ttu-id="13801-138">El contenedor de claves privadas existente se reemplaza por el nuevo contenedor de claves privadas.</span><span class="sxs-lookup"><span data-stu-id="13801-138">The existing private key container is replaced by the new private key container.</span></span>

## <a name="requirements"></a><span data-ttu-id="13801-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13801-139">Requirements</span></span>



| <span data-ttu-id="13801-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="13801-140">Requirement</span></span> | <span data-ttu-id="13801-141">Value</span><span class="sxs-lookup"><span data-stu-id="13801-141">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13801-142">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="13801-142">Redistributable</span></span><br/> | <span data-ttu-id="13801-143">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="13801-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="13801-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13801-144">DLL</span></span><br/>             | <dl> <span data-ttu-id="13801-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13801-145"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13801-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="13801-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13801-147">**Store**</span><span class="sxs-lookup"><span data-stu-id="13801-147">**Store**</span></span>](store.md)
</dt> </dl>

 

 
