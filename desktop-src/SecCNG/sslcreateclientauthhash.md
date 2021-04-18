---
description: Recupera un identificador para el hash del Protocolo de enlace que se utiliza para la autenticación del cliente.
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: Función SslCreateClientAuthHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4ac83d6d8aeea8429812d80b7bf66de7c87062a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666960"
---
# <a name="sslcreateclientauthhash-function"></a><span data-ttu-id="792cb-103">SslCreateClientAuthHash función)</span><span class="sxs-lookup"><span data-stu-id="792cb-103">SslCreateClientAuthHash function</span></span>

<span data-ttu-id="792cb-104">La función **SslCreateClientAuthHash** recupera un identificador para el [*hash*](/windows/desktop/SecGloss/h-gly) de protocolo de enlace que se usa para la autenticación del cliente.</span><span class="sxs-lookup"><span data-stu-id="792cb-104">The **SslCreateClientAuthHash** function retrieves a handle to the handshake [*hash*](/windows/desktop/SecGloss/h-gly) that is used for client authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="792cb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="792cb-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  LPCWSTR            pszHashAlgId,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="792cb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="792cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="792cb-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="792cb-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="792cb-108">Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="792cb-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="792cb-109">*phHandshakeHash* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="792cb-109">*phHandshakeHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="792cb-110">Puntero a una variable **de \_ \_ identificador hash de NCRYPT** para recibir el identificador hash.</span><span class="sxs-lookup"><span data-stu-id="792cb-110">A pointer to an **NCRYPT\_HASH\_HANDLE** variable to receive the hash handle.</span></span>

</dd> <dt>

<span data-ttu-id="792cb-111">*dwProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="792cb-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="792cb-112">Uno de los valores del [**identificador de protocolo del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="792cb-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="792cb-113">*dwCipherSuite* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="792cb-113">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="792cb-114">Uno de los valores del [**identificador del conjunto de cifrado del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="792cb-114">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="792cb-115">*pszHashAlgId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="792cb-115">*pszHashAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="792cb-116">Uno de los valores de los [**identificadores del algoritmo CNG**](cng-algorithm-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="792cb-116">One of the [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) values.</span></span>

</dd> <dt>

<span data-ttu-id="792cb-117">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="792cb-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="792cb-118">Este parámetro se reserva para uso futuro y debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="792cb-118">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="792cb-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="792cb-119">Return value</span></span>

<span data-ttu-id="792cb-120">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="792cb-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="792cb-121">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="792cb-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="792cb-122">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="792cb-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="792cb-123">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="792cb-123">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="792cb-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="792cb-124">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="792cb-125"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="792cb-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="792cb-126">El parámetro *hSslProvider* contiene un puntero que no es válido.</span><span class="sxs-lookup"><span data-stu-id="792cb-126">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                |
| <dl> <span data-ttu-id="792cb-127"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="792cb-127"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="792cb-128">El parámetro *phHandshakeHash* se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="792cb-128">The *phHandshakeHash* parameter is set to **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="792cb-129"><dt>**NTE \_ 0x80090029L no \_ compatible**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="792cb-129"><dt>**NTE\_NOT\_SUPPORTED**</dt> <dt>0x80090029L</dt></span></span> </dl>     | <span data-ttu-id="792cb-130">La función seleccionada no se admite en la versión especificada de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="792cb-130">The selected function is not supported in the specified version of the interface.</span></span><br/> |
| <dl> <span data-ttu-id="792cb-131"><dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="792cb-131"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="792cb-132">Memoria insuficiente para asignar búferes.</span><span class="sxs-lookup"><span data-stu-id="792cb-132">Insufficient memory to allocate buffers.</span></span><br/>                                          |
| <dl> <span data-ttu-id="792cb-133"><dt>**NTE \_ \_Marcas no válidas**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="792cb-133"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="792cb-134">El parámetro *dwFlags* debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="792cb-134">The *dwFlags* parameter must be set to zero.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="792cb-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="792cb-135">Remarks</span></span>

<span data-ttu-id="792cb-136">Se llama a la función **SslCreateClientAuthHash** para las conversaciones del Protocolo de seguridad de la [*capa de transporte*](/windows/desktop/SecGloss/t-gly) (TLS) 1,2 o una versión posterior para crear objetos hash que se utilizan para los mensajes de protocolo de enlace hash.</span><span class="sxs-lookup"><span data-stu-id="792cb-136">The **SslCreateClientAuthHash** function is called for [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.2 or later conversations to create hash objects that are used to hash handshake messages.</span></span> <span data-ttu-id="792cb-137">Se llama una vez para cada [*algoritmo hash*](/windows/desktop/SecGloss/h-gly) posible que se puede usar en la firma de autenticación del cliente.</span><span class="sxs-lookup"><span data-stu-id="792cb-137">It is called once for each possible [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) that can be used in the client authentication signature.</span></span>

## <a name="requirements"></a><span data-ttu-id="792cb-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="792cb-138">Requirements</span></span>



| <span data-ttu-id="792cb-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="792cb-139">Requirement</span></span> | <span data-ttu-id="792cb-140">Value</span><span class="sxs-lookup"><span data-stu-id="792cb-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="792cb-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="792cb-141">Minimum supported client</span></span><br/> | <span data-ttu-id="792cb-142">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="792cb-142">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="792cb-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="792cb-143">Minimum supported server</span></span><br/> | <span data-ttu-id="792cb-144">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="792cb-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="792cb-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="792cb-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="792cb-146"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="792cb-146"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="792cb-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="792cb-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="792cb-148"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="792cb-148"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

