---
description: Enumera los conjuntos de cifrado admitidos por un proveedor de protocolo de protocolo Capa de sockets seguros (SSL).
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: Función SslEnumCipherSuites (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumCipherSuites
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8991842f38f3d3dc3d721cd30ebfb857ad20308a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360607"
---
# <a name="sslenumciphersuites-function"></a><span data-ttu-id="92e90-103">SslEnumCipherSuites función)</span><span class="sxs-lookup"><span data-stu-id="92e90-103">SslEnumCipherSuites function</span></span>

<span data-ttu-id="92e90-104">La función **SslEnumCipherSuites** enumera los conjuntos de cifrado admitidos por un proveedor de protocolo de [*Protocolo capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="92e90-104">The **SslEnumCipherSuites** function enumerates the cipher suites supported by a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="92e90-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92e90-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEnumCipherSuites(
  _In_     NCRYPT_PROV_HANDLE      hSslProvider,
  _In_opt_ NCRYPT_KEY_HANDLE       hPrivateKey,
  _Out_    NCRYPT_SSL_CIPHER_SUITE **ppCipherSuite,
  _Inout_  PVOID                   *ppEnumState,
  _In_     DWORD                   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="92e90-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92e90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92e90-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92e90-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92e90-108">Identificador de la instancia del proveedor del protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="92e90-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="92e90-109">*hPrivateKey* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="92e90-109">*hPrivateKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="92e90-110">Identificador de una [*clave privada*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="92e90-110">The handle of a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="92e90-111">Cuando se especifica una clave privada, **SslEnumCipherSuites** enumera los conjuntos de cifrado que son compatibles con la clave privada.</span><span class="sxs-lookup"><span data-stu-id="92e90-111">When a private key is specified, **SslEnumCipherSuites** enumerates the cipher suites that are compatible with the private key.</span></span> <span data-ttu-id="92e90-112">Por ejemplo, si la clave privada es una clave DSS, solo \_ se devuelven los conjuntos de cifrado de DSS DHE.</span><span class="sxs-lookup"><span data-stu-id="92e90-112">For example, if the private key is a DSS key, then only the DSS\_DHE cipher suites are returned.</span></span> <span data-ttu-id="92e90-113">Si la clave privada es una clave RSA, pero no admite operaciones de descifrado sin procesar, no se devuelven los conjuntos de cifrado de SSL2.</span><span class="sxs-lookup"><span data-stu-id="92e90-113">If the private key is an RSA key, but it does not support raw decryption operations, then the SSL2 cipher suites are not returned.</span></span>

<span data-ttu-id="92e90-114">Establezca este parámetro en **null** cuando no especifique una clave privada.</span><span class="sxs-lookup"><span data-stu-id="92e90-114">Set this parameter to **NULL** when you are not specifying a private key.</span></span>

> [!Note]  
> <span data-ttu-id="92e90-115">Un identificador *hPrivateKey* se obtiene mediante una llamada a la función [**SslOpenPrivateKey**](sslopenprivatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="92e90-115">A *hPrivateKey* handle is obtained by calling the [**SslOpenPrivateKey**](sslopenprivatekey.md) function.</span></span> <span data-ttu-id="92e90-116">No se admiten los identificadores obtenidos de la función [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) .</span><span class="sxs-lookup"><span data-stu-id="92e90-116">Handles obtained from the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function are not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="92e90-117">*ppCipherSuite* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="92e90-117">*ppCipherSuite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92e90-118">Puntero a una estructura [**de \_ \_ \_ conjunto de cifrado SSL de NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) para recibir la dirección del siguiente conjunto de cifrado de la lista.</span><span class="sxs-lookup"><span data-stu-id="92e90-118">A pointer to a [**NCRYPT\_SSL\_CIPHER\_SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) structure to receive the address of the next cipher suite in the list.</span></span>

</dd> <dt>

<span data-ttu-id="92e90-119">*ppEnumState* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="92e90-119">*ppEnumState* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="92e90-120">Puntero a un búfer que indica la posición actual en la lista de conjuntos de cifrado.</span><span class="sxs-lookup"><span data-stu-id="92e90-120">A pointer to a buffer that indicates the current position in the list of cipher suites.</span></span>

<span data-ttu-id="92e90-121">Establezca el puntero en **null** en la primera llamada a **SslEnumCipherSuites**.</span><span class="sxs-lookup"><span data-stu-id="92e90-121">Set the pointer to **NULL** on the first call to **SslEnumCipherSuites**.</span></span> <span data-ttu-id="92e90-122">En cada llamada subsiguiente, pase el valor sin modificar de nuevo a **SslEnumCipherSuites**.</span><span class="sxs-lookup"><span data-stu-id="92e90-122">On each subsequent call, pass the unmodified value back to **SslEnumCipherSuites**.</span></span>

<span data-ttu-id="92e90-123">Cuando no hay más conjuntos de cifrado disponibles, debe liberar *ppEnumState* llamando a la función [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="92e90-123">When there are no more cipher suites available, you should free *ppEnumState* by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="92e90-124">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92e90-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92e90-125">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="92e90-125">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92e90-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92e90-126">Return value</span></span>

<span data-ttu-id="92e90-127">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="92e90-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="92e90-128">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="92e90-128">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="92e90-129">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="92e90-129">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="92e90-130">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92e90-130">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="92e90-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="92e90-131">Description</span></span>                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="92e90-132"><dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="92e90-132"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>      | <span data-ttu-id="92e90-133">No hay suficiente memoria disponible para asignar los búferes necesarios.</span><span class="sxs-lookup"><span data-stu-id="92e90-133">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="92e90-134"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="92e90-134"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="92e90-135">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="92e90-135">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="92e90-136"><dt>**NTE \_ NO hay \_ más \_ elementos**</dt> <dt>0x8009002AL</dt></span><span class="sxs-lookup"><span data-stu-id="92e90-136"><dt>**NTE\_NO\_MORE\_ITEMS**</dt> <dt>0x8009002AL</dt></span></span> </dl> | <span data-ttu-id="92e90-137">No se admite ningún conjunto de cifrado adicional.</span><span class="sxs-lookup"><span data-stu-id="92e90-137">No additional cipher suites are supported.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="92e90-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92e90-138">Remarks</span></span>

<span data-ttu-id="92e90-139">Para enumerar todos los conjuntos de cifrado admitidos por el proveedor SSL, llame a la función **SslEnumCipherSuites** en un bucle hasta que NTE no se devuelvan **\_ \_ más \_ elementos** .</span><span class="sxs-lookup"><span data-stu-id="92e90-139">To enumerate all cipher suites supported by the SSL provider, call the **SslEnumCipherSuites** function in a loop until **NTE\_NO\_MORE\_ITEMS** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="92e90-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92e90-140">Requirements</span></span>



| <span data-ttu-id="92e90-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="92e90-141">Requirement</span></span> | <span data-ttu-id="92e90-142">Value</span><span class="sxs-lookup"><span data-stu-id="92e90-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="92e90-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92e90-143">Minimum supported client</span></span><br/> | <span data-ttu-id="92e90-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="92e90-144">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="92e90-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92e90-145">Minimum supported server</span></span><br/> | <span data-ttu-id="92e90-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="92e90-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="92e90-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92e90-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="92e90-148"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="92e90-148"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="92e90-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92e90-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="92e90-150"><dt>Ncrypt. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92e90-150"><dt>Ncrypt.lib</dt></span></span> </dl>    |
| <span data-ttu-id="92e90-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="92e90-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92e90-152"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92e90-152"><dt>Ncrypt.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="92e90-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="92e90-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92e90-154">**\_conjunto de \_ cifrado SSL de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="92e90-154">**NCRYPT\_SSL\_CIPHER\_SUITE**</span></span>](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

