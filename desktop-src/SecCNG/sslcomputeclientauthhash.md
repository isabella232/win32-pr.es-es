---
description: Calcula un hash que se usará durante la autenticación del certificado.
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: Función SslComputeClientAuthHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: faea1699657efd92049068e48ff361c48242e9c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276361"
---
# <a name="sslcomputeclientauthhash-function"></a><span data-ttu-id="bc945-103">SslComputeClientAuthHash función)</span><span class="sxs-lookup"><span data-stu-id="bc945-103">SslComputeClientAuthHash function</span></span>

<span data-ttu-id="bc945-104">La función **SslComputeClientAuthHash** calcula un [*hash*](/windows/desktop/SecGloss/h-gly) que se usará durante la autenticación de [*certificados*](/windows/desktop/SecGloss/c-gly) .</span><span class="sxs-lookup"><span data-stu-id="bc945-104">The **SslComputeClientAuthHash** function computes a [*hash*](/windows/desktop/SecGloss/h-gly) to use during [*certificate*](/windows/desktop/SecGloss/c-gly) authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc945-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc945-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _In_  LPCWSTR            pszAlgId,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="bc945-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc945-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc945-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc945-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc945-108">Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="bc945-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="bc945-109">*hMasterKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc945-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc945-110">Identificador del objeto de [*clave maestra*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="bc945-110">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="bc945-111">*hHandshakeHash* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc945-111">*hHandshakeHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc945-112">Identificador del hash del Protocolo de enlace calculado hasta ahora.</span><span class="sxs-lookup"><span data-stu-id="bc945-112">The handle of the hash of the handshake computed so far.</span></span>

</dd> <dt>

<span data-ttu-id="bc945-113">*pszAlgId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc945-113">*pszAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc945-114">Puntero a una cadena Unicode terminada en null que identifica el [*algoritmo criptográfico*](/windows/desktop/SecGloss/c-gly)solicitado.</span><span class="sxs-lookup"><span data-stu-id="bc945-114">A pointer to a null-terminated Unicode string that identifies the requested [*cryptographic algorithm*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="bc945-115">Puede ser uno de los [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) estándar o el identificador de otro algoritmo registrado.</span><span class="sxs-lookup"><span data-stu-id="bc945-115">This can be one of the standard [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) or the identifier for another registered algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="bc945-116">*pbOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bc945-116">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc945-117">La dirección de un búfer que recibe el [*BLOB de clave*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="bc945-117">The address of a buffer that receives the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="bc945-118">El parámetro *cbOutput* contiene el tamaño de este búfer.</span><span class="sxs-lookup"><span data-stu-id="bc945-118">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="bc945-119">Si este parámetro es **null**, esta función colocará el tamaño necesario, en bytes, en el **valor DWORD** al que apunta el parámetro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="bc945-119">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="bc945-120">*cbOutput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc945-120">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc945-121">La longitud, en bytes, del búfer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="bc945-121">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="bc945-122">*pcbResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bc945-122">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc945-123">Un puntero a un valor **DWORD** que especifica la longitud, en bytes, del hash escrito en el búfer de *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="bc945-123">A pointer to a **DWORD** value that specifies the length, in bytes, of the hash written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="bc945-124">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc945-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc945-125">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="bc945-125">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc945-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc945-126">Return value</span></span>

<span data-ttu-id="bc945-127">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="bc945-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="bc945-128">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="bc945-128">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="bc945-129">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="bc945-129">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="bc945-130">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc945-130">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="bc945-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc945-131">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="bc945-132"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="bc945-132"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="bc945-133">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="bc945-133">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bc945-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc945-134">Remarks</span></span>

<span data-ttu-id="bc945-135">La función **SslComputeClientAuthHash** calcula el hash que se envía en el mensaje de comprobación de certificado del Protocolo de enlace SSL.</span><span class="sxs-lookup"><span data-stu-id="bc945-135">The **SslComputeClientAuthHash** function computes the hash that is sent in the certificate verification message of the SSL handshake.</span></span> <span data-ttu-id="bc945-136">El valor hash se calcula creando un hash que contiene el secreto principal con un hash de todos los mensajes de protocolo de enlace anteriores enviados o recibidos.</span><span class="sxs-lookup"><span data-stu-id="bc945-136">The hash value is computed by creating a hash that contains the master secret with a hash of all previous handshake messages sent or received.</span></span> <span data-ttu-id="bc945-137">Para obtener más información sobre la secuencia del Protocolo de enlace SSL, vea [Descripción del Protocolo de enlace de capa de sockets seguros (SSL)](https://support.microsoft.com/kb/257591).</span><span class="sxs-lookup"><span data-stu-id="bc945-137">For more information about the SSL handshake sequence, see [Description of the Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span></span>

<span data-ttu-id="bc945-138">La forma en que se calcula el hash depende del protocolo y del conjunto de cifrado utilizado.</span><span class="sxs-lookup"><span data-stu-id="bc945-138">The manner in which the hash is computed depends on the protocol and cipher suite used.</span></span> <span data-ttu-id="bc945-139">Además, el hash depende del tipo de clave de autenticación de cliente utilizada. el parámetro *pszAlgId* indica el tipo de clave que se usa para la autenticación del cliente.</span><span class="sxs-lookup"><span data-stu-id="bc945-139">In addition, the hash depends on the type of client authentication key used; the *pszAlgId* parameter indicates the type of key used for client authentication.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc945-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc945-140">Requirements</span></span>



| <span data-ttu-id="bc945-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc945-141">Requirement</span></span> | <span data-ttu-id="bc945-142">Value</span><span class="sxs-lookup"><span data-stu-id="bc945-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc945-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc945-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bc945-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bc945-144">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bc945-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc945-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bc945-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc945-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bc945-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc945-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc945-148"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc945-148"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="bc945-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc945-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc945-150"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc945-150"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

