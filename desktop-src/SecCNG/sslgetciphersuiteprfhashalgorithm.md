---
description: 'Devuelve el identificador del algoritmo Cryptography API: Next Generation (CNG) del algoritmo hash que se usa para la función pseudoaleatorios (PRF) del Protocolo de seguridad de la capa de transporte (TLS) para el protocolo de entrada, el conjunto de cifrado y el tipo de clave.'
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: Función SslGetCipherSuitePRFHashAlgorithm (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetCipherSuitePRFHashAlgorithm
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452cb7b36b20697a95b2c2abae7d8cd3b4180050
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669986"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a><span data-ttu-id="68099-103">SslGetCipherSuitePRFHashAlgorithm función)</span><span class="sxs-lookup"><span data-stu-id="68099-103">SslGetCipherSuitePRFHashAlgorithm function</span></span>

<span data-ttu-id="68099-104">La función **SslGetCipherSuitePRFHashAlgorithm** devuelve el identificador del algoritmo Cryptography API: Next Generation (CNG) del [*algoritmo hash*](/windows/desktop/SecGloss/h-gly) que se usa para la [*función pseudoaleatorios*](/windows/desktop/SecGloss/p-gly) (PRF) del Protocolo de seguridad de la [*capa de transporte*](/windows/desktop/SecGloss/t-gly) (TLS) para el protocolo de entrada, el conjunto de cifrado y el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="68099-104">The **SslGetCipherSuitePRFHashAlgorithm** function returns the Cryptography API: Next Generation (CNG) Algorithm Identifier of the [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) that is used for the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) [*pseudo-random function*](/windows/desktop/SecGloss/p-gly) (PRF) for the input protocol, cipher suite, and key type.</span></span>

## <a name="syntax"></a><span data-ttu-id="68099-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68099-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetCipherSuitePRFHashAlgorithm(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _Out_ WCHAR              szPRFHash[NCRYPT_SSL_MAX_NAME_SIZE],
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="68099-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68099-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68099-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68099-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68099-108">Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="68099-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="68099-109">*dwProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68099-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68099-110">Uno de los valores del [**identificador de protocolo del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="68099-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="68099-111">*dwCipherSuite* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68099-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68099-112">Uno de los valores del [**identificador del conjunto de cifrado del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="68099-112">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="68099-113">*dwKeyType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68099-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68099-114">Uno de los valores del [**identificador de tipo de clave del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="68099-114">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="68099-115">En el caso de los tipos de clave que no son [*criptografía de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC), establezca este parámetro en cero.</span><span class="sxs-lookup"><span data-stu-id="68099-115">For key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC), set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="68099-116">*szPRFHash* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="68099-116">*szPRFHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68099-117">Uno de los [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) para el hash que se utilizará para el PRF de TLS.</span><span class="sxs-lookup"><span data-stu-id="68099-117">One of the [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) for the hash that will be used for the TLS PRF.</span></span>

</dd> <dt>

<span data-ttu-id="68099-118">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68099-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68099-119">Este parámetro se reserva para uso futuro y debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="68099-119">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68099-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68099-120">Return value</span></span>

<span data-ttu-id="68099-121">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="68099-121">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="68099-122">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="68099-122">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="68099-123">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="68099-123">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="68099-124">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68099-124">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="68099-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="68099-125">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68099-126"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="68099-126"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="68099-127">El parámetro *hSslProvider* contiene un puntero que no es válido.</span><span class="sxs-lookup"><span data-stu-id="68099-127">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                |
| <dl> <span data-ttu-id="68099-128"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="68099-128"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="68099-129">El parámetro *szPRFHash* se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="68099-129">The *szPRFHash* parameter is set to **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="68099-130"><dt>**NTE \_ 0x80090029L no \_ compatible**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="68099-130"><dt>**NTE\_NOT\_SUPPORTED**</dt> <dt>0x80090029L</dt></span></span> </dl>     | <span data-ttu-id="68099-131">La función seleccionada no se admite en la versión especificada de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="68099-131">The selected function is not supported in the specified version of the interface.</span></span><br/> |
| <dl> <span data-ttu-id="68099-132"><dt>**NTE \_ \_Marcas no válidas**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="68099-132"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="68099-133">El parámetro *dwFlags* debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="68099-133">The *dwFlags* parameter must be set to zero.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="68099-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68099-134">Remarks</span></span>

<span data-ttu-id="68099-135">Se llama a esta función **SslGetCipherSuitePRFHashAlgorithm** para las conversaciones TLS 1,2 o posteriores con el fin de consultar el algoritmo hash que se usará en el PRF de TLS.</span><span class="sxs-lookup"><span data-stu-id="68099-135">This **SslGetCipherSuitePRFHashAlgorithm** function is called for TLS 1.2 or later conversations to query the hashing algorithm that will be used in the TLS PRF.</span></span>

## <a name="requirements"></a><span data-ttu-id="68099-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68099-136">Requirements</span></span>



| <span data-ttu-id="68099-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="68099-137">Requirement</span></span> | <span data-ttu-id="68099-138">Value</span><span class="sxs-lookup"><span data-stu-id="68099-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="68099-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68099-139">Minimum supported client</span></span><br/> | <span data-ttu-id="68099-140">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="68099-140">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="68099-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68099-141">Minimum supported server</span></span><br/> | <span data-ttu-id="68099-142">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="68099-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68099-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68099-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="68099-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="68099-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="68099-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68099-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68099-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68099-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

