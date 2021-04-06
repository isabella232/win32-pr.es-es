---
description: Devuelve una \_ \_ \_ estructura de longitud de cifrado SSL de NCRYPT que contiene las longitudes de encabezado y finalizador del Protocolo de entrada, el conjunto de cifrado y el tipo de clave.
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: Función SslLookupCipherLengths (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherLengths
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e756fb84d47ed877ffe4afcd54ce93c53a768e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001595"
---
# <a name="ssllookupcipherlengths-function"></a><span data-ttu-id="6772e-103">SslLookupCipherLengths función)</span><span class="sxs-lookup"><span data-stu-id="6772e-103">SslLookupCipherLengths function</span></span>

<span data-ttu-id="6772e-104">La función **SslLookupCipherLengths** devuelve una estructura de [**\_ \_ \_ longitudes de cifrado SSL de NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) que contiene las longitudes de encabezado y finalizador del Protocolo de entrada, el conjunto de cifrado y el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="6772e-104">The **SslLookupCipherLengths** function returns an [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) structure that contains the header and trailer lengths of the input protocol, cipher suite, and key type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6772e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6772e-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_  NCRYPT_PROV_HANDLE        hSslProvider,
  _In_  DWORD                     dwProtocol,
  _In_  DWORD                     dwCipherSuite,
  _In_  DWORD                     dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_  DWORD                     cbCipherLengths,
  _In_  DWORD                     dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6772e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6772e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6772e-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6772e-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6772e-108">Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="6772e-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="6772e-109">*dwProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6772e-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6772e-110">Uno de los valores del [**identificador de protocolo del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="6772e-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="6772e-111">*dwCipherSuite* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6772e-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6772e-112">Uno de los valores del [**identificador del conjunto de cifrado del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="6772e-112">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="6772e-113">*dwKeyType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6772e-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6772e-114">Uno de los valores del [**identificador de tipo de clave del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="6772e-114">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="6772e-115">En el caso de los tipos de clave que no son [*criptografía de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC), establezca este parámetro en cero.</span><span class="sxs-lookup"><span data-stu-id="6772e-115">For key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC), set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6772e-116">*pCipherLengths* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6772e-116">*pCipherLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6772e-117">Un puntero a un búfer para recibir la estructura de [**\_ \_ \_ longitudes de cifrado SSL de NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) .</span><span class="sxs-lookup"><span data-stu-id="6772e-117">A pointer to a buffer to receive the [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6772e-118">*cbCipherLengths* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6772e-118">*cbCipherLengths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6772e-119">La longitud, en bytes, del búfer al que apunta el parámetro *pCipherLengths* .</span><span class="sxs-lookup"><span data-stu-id="6772e-119">The length, in bytes, of the buffer pointed to by the *pCipherLengths* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6772e-120">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6772e-120">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6772e-121">Este parámetro se reserva para uso futuro y debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="6772e-121">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6772e-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6772e-122">Return value</span></span>

<span data-ttu-id="6772e-123">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="6772e-123">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="6772e-124">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6772e-124">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="6772e-125">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="6772e-125">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="6772e-126">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6772e-126">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="6772e-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="6772e-127">Description</span></span>                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6772e-128"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="6772e-128"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="6772e-129">El parámetro *hSslProvider* contiene un puntero que no es válido.</span><span class="sxs-lookup"><span data-stu-id="6772e-129">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="6772e-130"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="6772e-130"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="6772e-131">El parámetro *pCipherLengths* está establecido en **null** o la longitud del búfer especificada por *cbCipherLengths* es demasiado corta.</span><span class="sxs-lookup"><span data-stu-id="6772e-131">The *pCipherLengths* parameter is set to **NULL** or the buffer length specified by the *cbCipherLengths* is too short.</span></span><br/> |
| <dl> <span data-ttu-id="6772e-132"><dt>**NTE \_ \_Marcas no válidas**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="6772e-132"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="6772e-133">El parámetro *dwFlags* debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="6772e-133">The *dwFlags* parameter must be set to zero.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="6772e-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6772e-134">Remarks</span></span>

<span data-ttu-id="6772e-135">Se llama a la función **SslLookupCipherLengths** para las conversaciones del Protocolo de seguridad de la [*capa de transporte*](/windows/desktop/SecGloss/t-gly) (TLS) 1,1 o posteriores para consultar las longitudes de encabezado y finalizador del Protocolo, conjunto de cifrado y tipo de clave solicitados.</span><span class="sxs-lookup"><span data-stu-id="6772e-135">The **SslLookupCipherLengths** function is called for [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.1 or later conversations to query the header and trailer lengths for the requested protocol, cipher suite, and key type.</span></span>

## <a name="requirements"></a><span data-ttu-id="6772e-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6772e-136">Requirements</span></span>



| <span data-ttu-id="6772e-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="6772e-137">Requirement</span></span> | <span data-ttu-id="6772e-138">Value</span><span class="sxs-lookup"><span data-stu-id="6772e-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6772e-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6772e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6772e-140">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6772e-140">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6772e-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6772e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6772e-142">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6772e-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6772e-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6772e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="6772e-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="6772e-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="6772e-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6772e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6772e-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6772e-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

