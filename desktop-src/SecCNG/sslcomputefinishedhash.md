---
description: Calcula el hash enviado en el mensaje finalizado del Protocolo de enlace del Protocolo de Capa de sockets seguros (SSL).
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: Función SslComputeFinishedHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeFinishedHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 365f3c849b0a499d2bd875c8d234bbda1911eb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001647"
---
# <a name="sslcomputefinishedhash-function"></a><span data-ttu-id="8e63e-103">SslComputeFinishedHash función)</span><span class="sxs-lookup"><span data-stu-id="8e63e-103">SslComputeFinishedHash function</span></span>

<span data-ttu-id="8e63e-104">La función **SslComputeFinishedHash** calcula el [*hash*](/windows/desktop/SecGloss/h-gly) enviado en el mensaje finalizado del Protocolo de enlace del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="8e63e-104">The **SslComputeFinishedHash** function computes the [*hash*](/windows/desktop/SecGloss/h-gly) sent in the finished message of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) handshake.</span></span> <span data-ttu-id="8e63e-105">Para obtener más información sobre la secuencia del Protocolo de enlace SSL, vea [Descripción del Protocolo de enlace de capa de sockets seguros (SSL)](https://support.microsoft.com/kb/257591).</span><span class="sxs-lookup"><span data-stu-id="8e63e-105">For more information about the SSL handshake sequence, see [Description of the Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e63e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e63e-106">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeFinishedHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8e63e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e63e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e63e-108">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e63e-108">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e63e-109">Identificador de la instancia del proveedor del protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="8e63e-109">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="8e63e-110">*hMasterKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e63e-110">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e63e-111">Identificador del objeto de [*clave maestra*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="8e63e-111">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="8e63e-112">*hHandshakeHash* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e63e-112">*hHandshakeHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e63e-113">Identificador del hash de los mensajes de protocolo de enlace.</span><span class="sxs-lookup"><span data-stu-id="8e63e-113">The handle of the hash of the handshake messages.</span></span>

</dd> <dt>

<span data-ttu-id="8e63e-114">*pbOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8e63e-114">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e63e-115">Un puntero a un búfer que recibe el hash para el mensaje de finalización.</span><span class="sxs-lookup"><span data-stu-id="8e63e-115">A pointer to a buffer that receives the hash for the finish message.</span></span>

</dd> <dt>

<span data-ttu-id="8e63e-116">*cbOutput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e63e-116">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e63e-117">La longitud, en bytes, del búfer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="8e63e-117">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8e63e-118">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e63e-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e63e-119">Una de las constantes siguientes.</span><span class="sxs-lookup"><span data-stu-id="8e63e-119">One of the following constants.</span></span>



| <span data-ttu-id="8e63e-120">Value</span><span class="sxs-lookup"><span data-stu-id="8e63e-120">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="8e63e-121">Significado</span><span class="sxs-lookup"><span data-stu-id="8e63e-121">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <span data-ttu-id="8e63e-122"><dt>**NCRYPT \_ \_ \_ Marca de cliente SSL**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="8e63e-122"><dt>**NCRYPT\_SSL\_CLIENT\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="8e63e-123">Especifica que se trata de una llamada de cliente.</span><span class="sxs-lookup"><span data-stu-id="8e63e-123">Specifies that this is a client call.</span></span><br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <span data-ttu-id="8e63e-124"><dt>**NCRYPT \_ \_ \_ Marca de servidor SSL**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="8e63e-124"><dt>**NCRYPT\_SSL\_SERVER\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="8e63e-125">Especifica que se trata de una llamada de servidor.</span><span class="sxs-lookup"><span data-stu-id="8e63e-125">Specifies that this is a server call.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e63e-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e63e-126">Return value</span></span>

<span data-ttu-id="8e63e-127">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="8e63e-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="8e63e-128">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8e63e-128">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="8e63e-129">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e63e-129">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="8e63e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e63e-130">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="8e63e-131"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>2148073510 (0x80090026)</dt></span><span class="sxs-lookup"><span data-stu-id="8e63e-131"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>2148073510 (0x80090026)</dt></span></span> </dl> | <span data-ttu-id="8e63e-132">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="8e63e-132">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8e63e-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e63e-133">Remarks</span></span>

<span data-ttu-id="8e63e-134">La función **SslComputeFinishedHash** es una de las tres funciones que se usan para generar un hash que se usará durante el protocolo de enlace SSL.</span><span class="sxs-lookup"><span data-stu-id="8e63e-134">The **SslComputeFinishedHash** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="8e63e-135">Se llama a la función [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) para obtener un identificador hash.</span><span class="sxs-lookup"><span data-stu-id="8e63e-135">The [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="8e63e-136">A la función [**SslHashHandshake**](sslhashhandshake.md) se le llama cualquier número de veces con el identificador hash para agregar datos al hash.</span><span class="sxs-lookup"><span data-stu-id="8e63e-136">The [**SslHashHandshake**](sslhashhandshake.md) function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="8e63e-137">Se llama a la función **SslComputeFinishedHash** con el identificador hash para obtener el Resumen de los datos con hash.</span><span class="sxs-lookup"><span data-stu-id="8e63e-137">The **SslComputeFinishedHash** function is called with the hash handle to obtain the digest of the hashed data.</span></span>

<span data-ttu-id="8e63e-138">El valor hash se calcula mediante el hash del secreto principal con un hash de todos los mensajes de protocolo de enlace anteriores enviados o recibidos.</span><span class="sxs-lookup"><span data-stu-id="8e63e-138">The hash value is computed by hashing the master secret with a hash of all previous handshake messages sent or received.</span></span>

<span data-ttu-id="8e63e-139">El valor de *cbOutput* determina la longitud de los datos hash.</span><span class="sxs-lookup"><span data-stu-id="8e63e-139">The value of *cbOutput* determines the length of the hash data.</span></span> <span data-ttu-id="8e63e-140">Cuando se usa el protocolo de seguridad de la [*capa de transporte*](/windows/desktop/SecGloss/t-gly) (TLS) 1,0, siempre debe ser 12 (bytes).</span><span class="sxs-lookup"><span data-stu-id="8e63e-140">When the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.0 protocol is used, this should always be 12 (bytes).</span></span> <span data-ttu-id="8e63e-141">Para obtener más información, consulte [la versión 1,0 del protocolo TLS](https://www.ietf.org/rfc/rfc2246.txt).</span><span class="sxs-lookup"><span data-stu-id="8e63e-141">For more information, see [The TLS Protocol Version 1.0](https://www.ietf.org/rfc/rfc2246.txt).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e63e-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e63e-142">Requirements</span></span>



| <span data-ttu-id="8e63e-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e63e-143">Requirement</span></span> | <span data-ttu-id="8e63e-144">Value</span><span class="sxs-lookup"><span data-stu-id="8e63e-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e63e-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e63e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="8e63e-146">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8e63e-146">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8e63e-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e63e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="8e63e-148">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e63e-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8e63e-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e63e-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e63e-150"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e63e-150"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="8e63e-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8e63e-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e63e-152"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e63e-152"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

