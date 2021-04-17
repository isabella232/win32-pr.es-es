---
description: Obtiene un identificador hash que se usa para los mensajes de protocolo de enlace hash.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: Función SslCreateHandshakeHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateHandshakeHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8affda999278ce2d4a740293a7532643a6c564ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666958"
---
# <a name="sslcreatehandshakehash-function"></a><span data-ttu-id="89ff9-103">SslCreateHandshakeHash función)</span><span class="sxs-lookup"><span data-stu-id="89ff9-103">SslCreateHandshakeHash function</span></span>

<span data-ttu-id="89ff9-104">La función **SslCreateHandshakeHash** obtiene un identificador hash que se usa para los mensajes de protocolo de enlace hash.</span><span class="sxs-lookup"><span data-stu-id="89ff9-104">The **SslCreateHandshakeHash** function obtains a hash handle that is used to hash handshake messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="89ff9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89ff9-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateHandshakeHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="89ff9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89ff9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89ff9-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89ff9-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ff9-108">Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="89ff9-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="89ff9-109">*phHandshakeHash* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="89ff9-109">*phHandshakeHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89ff9-110">Identificador hash que se puede pasar a otras funciones de proveedor SSL.</span><span class="sxs-lookup"><span data-stu-id="89ff9-110">A hash handle that can be passed to other SSL provider functions.</span></span>

</dd> <dt>

<span data-ttu-id="89ff9-111">*dwProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89ff9-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ff9-112">Uno de los valores del [**identificador de protocolo del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="89ff9-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

> [!Note]  
> <span data-ttu-id="89ff9-113">Esta función no se usa con el protocolo SSL 2,0.</span><span class="sxs-lookup"><span data-stu-id="89ff9-113">This function is not used with the SSL 2.0 protocol.</span></span>

 

</dd> <dt>

<span data-ttu-id="89ff9-114">*dwCipherSuite* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89ff9-114">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ff9-115">Uno de los valores del [**identificador del conjunto de cifrado del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="89ff9-115">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="89ff9-116">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89ff9-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ff9-117">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="89ff9-117">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89ff9-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89ff9-118">Return value</span></span>

<span data-ttu-id="89ff9-119">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="89ff9-119">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="89ff9-120">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="89ff9-120">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="89ff9-121">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="89ff9-121">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="89ff9-122">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89ff9-122">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="89ff9-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="89ff9-123">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="89ff9-124"><dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="89ff9-124"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="89ff9-125">No hay memoria suficiente para asignar el búfer hash.</span><span class="sxs-lookup"><span data-stu-id="89ff9-125">There is insufficient memory to allocate the hash buffer.</span></span><br/> |
| <dl> <span data-ttu-id="89ff9-126"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="89ff9-126"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="89ff9-127">El identificador de *hSslProvider* no es válido.</span><span class="sxs-lookup"><span data-stu-id="89ff9-127">The *hSslProvider* handle is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="89ff9-128"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="89ff9-128"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="89ff9-129">El valor de *phHandshakeHash* es NULL.</span><span class="sxs-lookup"><span data-stu-id="89ff9-129">The *phHandshakeHash* is null.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="89ff9-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89ff9-130">Remarks</span></span>

<span data-ttu-id="89ff9-131">La función **SslCreateHandshakeHash** es una de las tres funciones que se usan para generar un hash que se usará durante el protocolo de enlace SSL.</span><span class="sxs-lookup"><span data-stu-id="89ff9-131">The **SslCreateHandshakeHash** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="89ff9-132">Se llama a la función **SslCreateHandshakeHash** para obtener un identificador hash.</span><span class="sxs-lookup"><span data-stu-id="89ff9-132">The **SslCreateHandshakeHash** function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="89ff9-133">A la función [**SslHashHandshake**](sslhashhandshake.md) se le llama cualquier número de veces con el identificador hash para agregar datos al hash.</span><span class="sxs-lookup"><span data-stu-id="89ff9-133">The [**SslHashHandshake**](sslhashhandshake.md) function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="89ff9-134">Se llama a la función [**SslComputeFinishedHash**](sslcomputefinishedhash.md) con el identificador hash para obtener el Resumen de los datos con hash.</span><span class="sxs-lookup"><span data-stu-id="89ff9-134">The [**SslComputeFinishedHash**](sslcomputefinishedhash.md) function is called with the hash handle to obtain the digest of the hashed data.</span></span>

## <a name="requirements"></a><span data-ttu-id="89ff9-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89ff9-135">Requirements</span></span>



| <span data-ttu-id="89ff9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="89ff9-136">Requirement</span></span> | <span data-ttu-id="89ff9-137">Value</span><span class="sxs-lookup"><span data-stu-id="89ff9-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="89ff9-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89ff9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="89ff9-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="89ff9-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="89ff9-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89ff9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="89ff9-141">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="89ff9-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="89ff9-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89ff9-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="89ff9-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="89ff9-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="89ff9-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="89ff9-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89ff9-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89ff9-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

