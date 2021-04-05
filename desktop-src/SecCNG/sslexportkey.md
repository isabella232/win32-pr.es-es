---
description: Devuelve una clave de sesión de protocolo Capa de sockets seguros (SSL) o una clave efímera pública en un BLOB serializado.
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: Función SslExportKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c5fcbcfa1a8b6c1aa9922b98a7699bdf2bf4b0fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001642"
---
# <a name="sslexportkey-function"></a><span data-ttu-id="f6434-103">SslExportKey función)</span><span class="sxs-lookup"><span data-stu-id="f6434-103">SslExportKey function</span></span>

<span data-ttu-id="f6434-104">La función **SslExportKey** devuelve una [*clave de sesión*](/windows/desktop/SecGloss/s-gly) de [*Protocolo capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL) o una clave efímera pública en un [*BLOB*](/windows/desktop/SecGloss/b-gly)serializado.</span><span class="sxs-lookup"><span data-stu-id="f6434-104">The **SslExportKey** function returns an [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) [*session key*](/windows/desktop/SecGloss/s-gly) or public ephemeral key into a serialized [*BLOB*](/windows/desktop/SecGloss/b-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="f6434-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6434-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslExportKey(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hKey,
  _In_      LPCWSTR            pszBlobType,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f6434-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6434-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6434-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6434-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6434-108">Identificador de la instancia del proveedor del protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="f6434-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="f6434-109">*hKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6434-109">*hKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6434-110">Identificador de la clave que se va a exportar.</span><span class="sxs-lookup"><span data-stu-id="f6434-110">The handle of the key to export.</span></span>

<span data-ttu-id="f6434-111">Si no especifica una clave, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="f6434-111">When you are not specifying a key, set this parameter to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="f6434-112">Un identificador *hKey* se obtiene mediante una llamada a la función [**SslOpenPrivateKey**](sslopenprivatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="f6434-112">A *hKey* handle is obtained by calling the [**SslOpenPrivateKey**](sslopenprivatekey.md) function.</span></span> <span data-ttu-id="f6434-113">No se admiten los identificadores obtenidos de la función [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) .</span><span class="sxs-lookup"><span data-stu-id="f6434-113">Handles obtained from the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function are not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="f6434-114">*pszBlobType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6434-114">*pszBlobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6434-115">Una cadena Unicode terminada en null que contiene un identificador que especifica el tipo de BLOB que se va a exportar.</span><span class="sxs-lookup"><span data-stu-id="f6434-115">A null-terminated Unicode string that contains an identifier that specifies the type of BLOB to export.</span></span> <span data-ttu-id="f6434-116">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f6434-116">This can be one of the following values.</span></span>



| <span data-ttu-id="f6434-117">Value</span><span class="sxs-lookup"><span data-stu-id="f6434-117">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="f6434-118">Significado</span><span class="sxs-lookup"><span data-stu-id="f6434-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <span data-ttu-id="f6434-119"><dt>**\_ \_ BLOB público de BCRYPT DH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6434-119"><dt>**BCRYPT\_DH\_PUBLIC\_BLOB**</dt></span></span> </dl>    | <span data-ttu-id="f6434-120">Exportar una [*clave pública*](/windows/desktop/SecGloss/p-gly)de Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="f6434-120">Export a Diffie-Hellman [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="f6434-121">El búfer *pbOutput* recibe una estructura de BLOB de [**clave de BCRYPT \_ \_ \_ DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) seguida inmediatamente de los datos de clave.</span><span class="sxs-lookup"><span data-stu-id="f6434-121">The *pbOutput* buffer receives a [**BCRYPT\_DH\_KEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <span data-ttu-id="f6434-122"><dt>**\_BLOB ECCPUBLIC de BCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6434-122"><dt>**BCRYPT\_ECCPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="f6434-123">Exportar una clave pública de [*criptografía de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC).</span><span class="sxs-lookup"><span data-stu-id="f6434-123">Export an [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC) public key.</span></span> <span data-ttu-id="f6434-124">El búfer *pbOutput* recibe una estructura de [**\_ \_ blobs ECCKEY de BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) seguida inmediatamente de los datos clave.</span><span class="sxs-lookup"><span data-stu-id="f6434-124">The *pbOutput* buffer receives a [**BCRYPT\_ECCKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) structure immediately followed by the key data.</span></span><br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <span data-ttu-id="f6434-125"><dt>**\_BLOB de \_ clave \_ opaca de BCRYPT**</dt></span><span class="sxs-lookup"><span data-stu-id="f6434-125"><dt>**BCRYPT\_OPAQUE\_KEY\_BLOB**</dt></span></span> </dl> | <span data-ttu-id="f6434-126">Exportar una clave simétrica en un formato específico de un único proveedor de [*servicios criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP).</span><span class="sxs-lookup"><span data-stu-id="f6434-126">Export a symmetric key in a format that is specific to a single [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span> <span data-ttu-id="f6434-127">Los blobs opacos no se pueden transferir y se deben importar mediante el mismo *proveedor de servicios criptográficos* (CSP) que generó el BLOB.</span><span class="sxs-lookup"><span data-stu-id="f6434-127">Opaque BLOBs are not transferable and must be imported by using the same *cryptographic service provider* (CSP) that generated the BLOB.</span></span><br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <span data-ttu-id="f6434-128"><dt>**\_BLOB RSAPUBLIC de BCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6434-128"><dt>**BCRYPT\_RSAPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="f6434-129">Exportar una clave pública RSA.</span><span class="sxs-lookup"><span data-stu-id="f6434-129">Export an RSA public key.</span></span> <span data-ttu-id="f6434-130">El búfer *pbOutput* recibe una estructura de [**\_ \_ blobs RSAKEY de BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) seguida inmediatamente de los datos clave.</span><span class="sxs-lookup"><span data-stu-id="f6434-130">The *pbOutput* buffer receives a [**BCRYPT\_RSAKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="f6434-131">*pbOutput* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f6434-131">*pbOutput* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f6434-132">La dirección de un búfer que recibe el [*BLOB de clave*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="f6434-132">The address of a buffer that receives the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="f6434-133">El parámetro *cbOutput* contiene el tamaño de este búfer.</span><span class="sxs-lookup"><span data-stu-id="f6434-133">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="f6434-134">Si este parámetro es **null**, esta función colocará el tamaño necesario, en bytes, en el **valor DWORD** al que apunta el parámetro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="f6434-134">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f6434-135">*cbOutput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6434-135">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6434-136">Tamaño, en bytes, del búfer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="f6434-136">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f6434-137">*pcbResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f6434-137">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6434-138">Dirección de una variable **DWORD** que recibe el número de bytes copiados en el búfer de *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="f6434-138">The address of a **DWORD** variable that receives the number of bytes copied to the *pbOutput* buffer.</span></span> <span data-ttu-id="f6434-139">Si el parámetro *pbOutput* se establece en **null** cuando se llama a la función, el tamaño necesario para el búfer *pbOutput* , en bytes, se devuelve en el **valor DWORD** al que apunta este parámetro.</span><span class="sxs-lookup"><span data-stu-id="f6434-139">If the *pbOutput* parameter is set to **NULL** when the function is called, the required size for the *pbOutput* buffer, in bytes, is returned in the **DWORD** pointed to by this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f6434-140">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6434-140">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6434-141">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f6434-141">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6434-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6434-142">Return value</span></span>

<span data-ttu-id="f6434-143">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="f6434-143">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="f6434-144">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="f6434-144">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="f6434-145">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="f6434-145">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="f6434-146">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6434-146">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="f6434-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6434-147">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="f6434-148"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="f6434-148"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="f6434-149">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="f6434-149">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f6434-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6434-150">Remarks</span></span>

<span data-ttu-id="f6434-151">La función **SslExportKey** facilita el transporte de claves de sesión de un proceso a otro, así como la exportación de la parte pública de una clave efímera.</span><span class="sxs-lookup"><span data-stu-id="f6434-151">The **SslExportKey** function facilitates transporting session keys from one process to another as well as exporting the public portion an ephemeral key.</span></span>

<span data-ttu-id="f6434-152">Al exportar las claves de sesión, el tipo de BLOB es opaco, lo que significa que el formato del BLOB es irrelevante siempre que las funciones **SslExportKey** y [**SslImportKey**](sslimportkey.md) puedan interpretarlo.</span><span class="sxs-lookup"><span data-stu-id="f6434-152">When exporting session keys, the BLOB type is opaque, meaning that the format of the BLOB is irrelevant as long as both the **SslExportKey** and [**SslImportKey**](sslimportkey.md) functions can interpret it.</span></span>

<span data-ttu-id="f6434-153">Al exportar la parte pública de una clave efímera, el tipo de BLOB debe ser el tipo adecuado, como el blob **\_ público ncrypt DH \_ \_** o el **\_ \_ BLOB ECCPUBLIC ncrypt**.</span><span class="sxs-lookup"><span data-stu-id="f6434-153">When exporting the public portion of an ephemeral key the BLOB type must be the appropriate type, such as **NCRYPT\_DH\_PUBLIC\_BLOB** or **NCRYPT\_ECCPUBLIC\_BLOB**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6434-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6434-154">Requirements</span></span>



| <span data-ttu-id="f6434-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6434-155">Requirement</span></span> | <span data-ttu-id="f6434-156">Value</span><span class="sxs-lookup"><span data-stu-id="f6434-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6434-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6434-157">Minimum supported client</span></span><br/> | <span data-ttu-id="f6434-158">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f6434-158">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f6434-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6434-159">Minimum supported server</span></span><br/> | <span data-ttu-id="f6434-160">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6434-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f6434-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6434-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6434-162"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6434-162"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="f6434-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6434-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6434-164"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6434-164"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

