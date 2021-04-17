---
description: Importa una clave en el proveedor de protocolo del Protocolo de Capa de sockets seguros (SSL).
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: Función SslImportKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8bf1b03fd5d51974db3676dcdbccc2a2b0fa4323
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666956"
---
# <a name="sslimportkey-function"></a><span data-ttu-id="3ac49-103">SslImportKey función)</span><span class="sxs-lookup"><span data-stu-id="3ac49-103">SslImportKey function</span></span>

<span data-ttu-id="3ac49-104">La función **SslImportKey** importa una clave en el proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="3ac49-104">The **SslImportKey** function imports a key into the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ac49-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ac49-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslImportKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phKey,
  _In_  LPCWSTR            pszBlobType,
  _In_  PBYTE              pbKeyBlob,
  _In_  DWORD              cbKeyBlob,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3ac49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ac49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ac49-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3ac49-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac49-108">Identificador de la instancia del proveedor del protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="3ac49-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="3ac49-109">*phKey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3ac49-109">*phKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac49-110">Puntero al identificador de la [*clave criptográfica*](/windows/desktop/SecGloss/c-gly) para recibir la clave importada.</span><span class="sxs-lookup"><span data-stu-id="3ac49-110">A pointer to the handle of the [*cryptographic key*](/windows/desktop/SecGloss/c-gly) to receive the imported key.</span></span>

</dd> <dt>

<span data-ttu-id="3ac49-111">*pszBlobType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3ac49-111">*pszBlobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac49-112">Una cadena Unicode terminada en null que contiene un identificador que especifica el tipo de [*BLOB*](/windows/desktop/SecGloss/b-gly) que se encuentra en el búfer de *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="3ac49-112">A null-terminated Unicode string that contains an identifier that specifies the type of [*BLOB*](/windows/desktop/SecGloss/b-gly) that is contained in the *pbInput* buffer.</span></span> <span data-ttu-id="3ac49-113">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3ac49-113">This can be one of the following values.</span></span>



| <span data-ttu-id="3ac49-114">Value</span><span class="sxs-lookup"><span data-stu-id="3ac49-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="3ac49-115">Significado</span><span class="sxs-lookup"><span data-stu-id="3ac49-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <span data-ttu-id="3ac49-116"><dt>**\_ \_ BLOB público de BCRYPT DH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac49-116"><dt>**BCRYPT\_DH\_PUBLIC\_BLOB**</dt></span></span> </dl>    | <span data-ttu-id="3ac49-117">Exportar una [*clave pública*](/windows/desktop/SecGloss/p-gly)de Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="3ac49-117">Export a Diffie-Hellman [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="3ac49-118">El búfer *pbOutput* recibe una estructura de BLOB de [**clave de BCRYPT \_ \_ \_ DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) seguida inmediatamente de los datos de clave.</span><span class="sxs-lookup"><span data-stu-id="3ac49-118">The *pbOutput* buffer receives a [**BCRYPT\_DH\_KEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <span data-ttu-id="3ac49-119"><dt>**\_BLOB ECCPUBLIC de BCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac49-119"><dt>**BCRYPT\_ECCPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="3ac49-120">Exportar una [*clave pública*](/windows/desktop/SecGloss/p-gly)de [*criptografía de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC).</span><span class="sxs-lookup"><span data-stu-id="3ac49-120">Export an [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC) [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="3ac49-121">El búfer *pbOutput* recibe una estructura de [**\_ \_ blobs ECCKEY de BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) seguida inmediatamente de los datos clave.</span><span class="sxs-lookup"><span data-stu-id="3ac49-121">The *pbOutput* buffer receives a [**BCRYPT\_ECCKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) structure immediately followed by the key data.</span></span><br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <span data-ttu-id="3ac49-122"><dt>**\_BLOB de \_ clave \_ opaca de BCRYPT**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac49-122"><dt>**BCRYPT\_OPAQUE\_KEY\_BLOB**</dt></span></span> </dl> | <span data-ttu-id="3ac49-123">Exportar una [*clave simétrica*](/windows/desktop/SecGloss/s-gly) en un formato específico de un único proveedor de [*servicios criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP).</span><span class="sxs-lookup"><span data-stu-id="3ac49-123">Export a [*symmetric key*](/windows/desktop/SecGloss/s-gly) in a format that is specific to a single [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span> <span data-ttu-id="3ac49-124">Los blobs opacos no se pueden transferir y se deben importar mediante el mismo CSP que generó el BLOB.</span><span class="sxs-lookup"><span data-stu-id="3ac49-124">Opaque BLOBs are not transferable and must be imported by using the same CSP that generated the BLOB.</span></span><br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <span data-ttu-id="3ac49-125"><dt>**\_BLOB RSAPUBLIC de BCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac49-125"><dt>**BCRYPT\_RSAPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="3ac49-126">Exportar una clave pública [*RSA*](/windows/desktop/SecGloss/r-gly) .</span><span class="sxs-lookup"><span data-stu-id="3ac49-126">Export an [*RSA*](/windows/desktop/SecGloss/r-gly) public key.</span></span> <span data-ttu-id="3ac49-127">El búfer *pbOutput* recibe una estructura de [**\_ \_ blobs RSAKEY de BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) seguida inmediatamente de los datos clave.</span><span class="sxs-lookup"><span data-stu-id="3ac49-127">The *pbOutput* buffer receives a [**BCRYPT\_RSAKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="3ac49-128">*pbKeyBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3ac49-128">*pbKeyBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac49-129">Puntero al búfer que contiene el BLOB de [*clave*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="3ac49-129">A pointer to the buffer that contains the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span>

</dd> <dt>

<span data-ttu-id="3ac49-130">*cbKeyBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3ac49-130">*cbKeyBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac49-131">Tamaño, en bytes, del búfer *pbKeyBlob* .</span><span class="sxs-lookup"><span data-stu-id="3ac49-131">The size, in bytes, of the *pbKeyBlob* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3ac49-132">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3ac49-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac49-133">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="3ac49-133">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ac49-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ac49-134">Return value</span></span>

<span data-ttu-id="3ac49-135">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="3ac49-135">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="3ac49-136">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="3ac49-136">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="3ac49-137">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="3ac49-137">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="3ac49-138">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ac49-138">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="3ac49-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ac49-139">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3ac49-140"><dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="3ac49-140"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="3ac49-141">No hay suficiente memoria disponible para asignar los búferes necesarios.</span><span class="sxs-lookup"><span data-stu-id="3ac49-141">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="3ac49-142"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="3ac49-142"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="3ac49-143">El identificador de *hSslProvider* no es válido.</span><span class="sxs-lookup"><span data-stu-id="3ac49-143">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="3ac49-144"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="3ac49-144"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="3ac49-145">El parámetro *phKey* es **null**.</span><span class="sxs-lookup"><span data-stu-id="3ac49-145">The *phKey* parameter is **NULL**.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="3ac49-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ac49-146">Remarks</span></span>

<span data-ttu-id="3ac49-147">Puede usar la función **SslImportKey** para importar claves de sesión como parte del proceso de transferencia de claves de sesión de un proceso a otro.</span><span class="sxs-lookup"><span data-stu-id="3ac49-147">You can use the **SslImportKey** function to import session keys as a part of the process of transferring session keys from one process to another.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ac49-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ac49-148">Requirements</span></span>



| <span data-ttu-id="3ac49-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ac49-149">Requirement</span></span> | <span data-ttu-id="3ac49-150">Value</span><span class="sxs-lookup"><span data-stu-id="3ac49-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac49-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ac49-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3ac49-152">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3ac49-152">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3ac49-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ac49-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3ac49-154">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ac49-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3ac49-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ac49-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ac49-156"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ac49-156"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="3ac49-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ac49-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ac49-158"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ac49-158"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

