---
description: Firma un hash mediante la clave privada especificada.
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: Función SslSignHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslSignHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 339d0a27cb987557ff90cbd0f489813edb357b77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497224"
---
# <a name="sslsignhash-function"></a><span data-ttu-id="b9ea3-103">SslSignHash función)</span><span class="sxs-lookup"><span data-stu-id="b9ea3-103">SslSignHash function</span></span>

<span data-ttu-id="b9ea3-104">La función **SslSignHash** firma un [*hash*](/windows/desktop/SecGloss/h-gly) mediante la [*clave privada*](/windows/desktop/SecGloss/p-gly)especificada.</span><span class="sxs-lookup"><span data-stu-id="b9ea3-104">The **SslSignHash** function signs a [*hash*](/windows/desktop/SecGloss/h-gly) by using the specified [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="b9ea3-105">El proceso de firma se realiza en el servidor.</span><span class="sxs-lookup"><span data-stu-id="b9ea3-105">The signing process is performed on the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ea3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9ea3-106">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslSignHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  PBYTE              pbHashValue,
  _In_  DWORD              cbHashValue,
  _Out_ PBYTE              pbSignature,
  _In_  DWORD              cbSignature,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b9ea3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9ea3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9ea3-108">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9ea3-108">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ea3-109">Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="b9ea3-109">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="b9ea3-110">*hPrivateKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9ea3-110">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ea3-111">Identificador de la clave privada que se va a utilizar para firmar el hash.</span><span class="sxs-lookup"><span data-stu-id="b9ea3-111">The handle to the private key to use to sign the hash.</span></span>

</dd> <dt>

<span data-ttu-id="b9ea3-112">*pbHashValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9ea3-112">*pbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ea3-113">Un puntero a un búfer que contiene el hash que se va a firmar.</span><span class="sxs-lookup"><span data-stu-id="b9ea3-113">A pointer to a buffer that contains the hash to sign.</span></span>

</dd> <dt>

<span data-ttu-id="b9ea3-114">*cbHashValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9ea3-114">*cbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ea3-115">Tamaño, en bytes, del búfer *pbHashValue* .</span><span class="sxs-lookup"><span data-stu-id="b9ea3-115">The size, in bytes, of the *pbHashValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b9ea3-116">*pbSignature* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b9ea3-116">*pbSignature* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ea3-117">Dirección de un búfer que recibe la firma del hash.</span><span class="sxs-lookup"><span data-stu-id="b9ea3-117">The address of a buffer that receives the signature of the hash.</span></span> <span data-ttu-id="b9ea3-118">El parámetro *cbSignature* contiene el tamaño de este búfer.</span><span class="sxs-lookup"><span data-stu-id="b9ea3-118">The *cbSignature* parameter contains the size of this buffer.</span></span> <span data-ttu-id="b9ea3-119">Para determinar el tamaño del búfer necesario, establezca el parámetro *pbSignature* en **null**.</span><span class="sxs-lookup"><span data-stu-id="b9ea3-119">To determine the required sized size of the buffer, set the *pbSignature* parameter to **NULL**.</span></span> <span data-ttu-id="b9ea3-120">El tamaño necesario del búfer se devolverá en el parámetro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="b9ea3-120">The required size of the buffer will be returned in the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b9ea3-121">*cbSignature* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9ea3-121">*cbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ea3-122">Tamaño, en bytes, del búfer *pbSignature* .</span><span class="sxs-lookup"><span data-stu-id="b9ea3-122">The size, in bytes, of the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b9ea3-123">*pcbResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b9ea3-123">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ea3-124">Un puntero a un valor que, al finalizar, contiene el número real de bytes escritos en el búfer de *pbSignature* .</span><span class="sxs-lookup"><span data-stu-id="b9ea3-124">A pointer to a value that, upon completion, contains the actual number of bytes written to the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b9ea3-125">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9ea3-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ea3-126">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b9ea3-126">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9ea3-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9ea3-127">Return value</span></span>

<span data-ttu-id="b9ea3-128">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="b9ea3-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="b9ea3-129">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b9ea3-129">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="b9ea3-130">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="b9ea3-130">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="b9ea3-131">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9ea3-131">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="b9ea3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9ea3-132">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="b9ea3-133"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="b9ea3-133"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="b9ea3-134">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="b9ea3-134">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b9ea3-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9ea3-135">Requirements</span></span>



| <span data-ttu-id="b9ea3-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9ea3-136">Requirement</span></span> | <span data-ttu-id="b9ea3-137">Value</span><span class="sxs-lookup"><span data-stu-id="b9ea3-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ea3-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9ea3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b9ea3-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b9ea3-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b9ea3-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9ea3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b9ea3-141">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9ea3-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b9ea3-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9ea3-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9ea3-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9ea3-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="b9ea3-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b9ea3-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9ea3-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9ea3-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

