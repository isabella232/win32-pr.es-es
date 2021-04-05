---
description: Descifra un único paquete de protocolo de Capa de sockets seguros (SSL).
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: Función SslDecryptPacket (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cd568596b7e780242c0ff8d9c522a9e1758c60b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001643"
---
# <a name="ssldecryptpacket-function"></a><span data-ttu-id="f9570-103">SslDecryptPacket función)</span><span class="sxs-lookup"><span data-stu-id="f9570-103">SslDecryptPacket function</span></span>

<span data-ttu-id="f9570-104">la función **SslDecryptPacket** descifra un único paquete de [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="f9570-104">the **SslDecryptPacket** function decrypts a single [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9570-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9570-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslDecryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f9570-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9570-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9570-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f9570-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9570-108">Identificador de la instancia del proveedor del protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="f9570-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="f9570-109">*hKey* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f9570-109">*hKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9570-110">Identificador de la clave que se usa para descifrar el paquete.</span><span class="sxs-lookup"><span data-stu-id="f9570-110">The handle to the key that is used to decrypt the packet.</span></span>

</dd> <dt>

<span data-ttu-id="f9570-111">*pbInput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f9570-111">*pbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9570-112">Un puntero al búfer que contiene el paquete que se va a descifrar.</span><span class="sxs-lookup"><span data-stu-id="f9570-112">A pointer to the buffer that contains the packet to be decrypted.</span></span>

</dd> <dt>

<span data-ttu-id="f9570-113">*cbInput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f9570-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9570-114">La longitud, en bytes, del búfer *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="f9570-114">The length, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f9570-115">*pbOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9570-115">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9570-116">Un puntero a un búfer para que contenga el paquete descifrado.</span><span class="sxs-lookup"><span data-stu-id="f9570-116">A pointer to a buffer to contain the decrypted packet.</span></span>

</dd> <dt>

<span data-ttu-id="f9570-117">*cbOutput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f9570-117">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9570-118">La longitud, bytes, del búfer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="f9570-118">The length, bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f9570-119">*pcbResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9570-119">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9570-120">Número de bytes escritos en el búfer de *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="f9570-120">The number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f9570-121">*SequenceNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f9570-121">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9570-122">El número de secuencia que corresponde a este paquete.</span><span class="sxs-lookup"><span data-stu-id="f9570-122">The sequence number that corresponds to this packet.</span></span>

</dd> <dt>

<span data-ttu-id="f9570-123">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f9570-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9570-124">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f9570-124">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9570-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9570-125">Return value</span></span>

<span data-ttu-id="f9570-126">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="f9570-126">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="f9570-127">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="f9570-127">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="f9570-128">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="f9570-128">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="f9570-129">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9570-129">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="f9570-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9570-130">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="f9570-131"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="f9570-131"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="f9570-132">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="f9570-132">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9570-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9570-133">Remarks</span></span>

<span data-ttu-id="f9570-134">La longitud del paquete puede ser cero, por ejemplo, cuando se descifra un mensaje "HelloRequest".</span><span class="sxs-lookup"><span data-stu-id="f9570-134">The length of the packet can be zero, such as when a "HelloRequest" message is decrypted.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9570-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9570-135">Requirements</span></span>



| <span data-ttu-id="f9570-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9570-136">Requirement</span></span> | <span data-ttu-id="f9570-137">Value</span><span class="sxs-lookup"><span data-stu-id="f9570-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9570-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9570-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f9570-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f9570-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f9570-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9570-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f9570-141">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9570-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f9570-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9570-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9570-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9570-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="f9570-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9570-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9570-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9570-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

