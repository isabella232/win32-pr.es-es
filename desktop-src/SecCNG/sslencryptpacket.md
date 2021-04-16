---
description: Cifra un único paquete de protocolo de Capa de sockets seguros (SSL).
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: Función SslEncryptPacket (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEncryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e839b37e839fd09d5df5f9902474b7ce7c4c74a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649291"
---
# <a name="sslencryptpacket-function"></a><span data-ttu-id="cdade-103">SslEncryptPacket función)</span><span class="sxs-lookup"><span data-stu-id="cdade-103">SslEncryptPacket function</span></span>

<span data-ttu-id="cdade-104">La función **SslEncryptPacket** cifra un único paquete de [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="cdade-104">The **SslEncryptPacket** function encrypts a single [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdade-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cdade-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEncryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwContentType,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="cdade-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cdade-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdade-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cdade-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdade-108">Identificador de la instancia del proveedor del protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="cdade-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="cdade-109">*hKey* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cdade-109">*hKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdade-110">Identificador de la clave que se usa para cifrar el paquete.</span><span class="sxs-lookup"><span data-stu-id="cdade-110">The handle to the key that is used to encrypt the packet.</span></span>

</dd> <dt>

<span data-ttu-id="cdade-111">*pbInput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cdade-111">*pbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdade-112">Un puntero al búfer que contiene el paquete que se va a cifrar.</span><span class="sxs-lookup"><span data-stu-id="cdade-112">A pointer to the buffer that contains the packet to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="cdade-113">*cbInput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cdade-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdade-114">La longitud, en bytes, del búfer *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="cdade-114">The length, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cdade-115">*pbOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cdade-115">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdade-116">Un puntero a un búfer para recibir el paquete cifrado.</span><span class="sxs-lookup"><span data-stu-id="cdade-116">A pointer to a buffer to receive the encrypted packet.</span></span>

</dd> <dt>

<span data-ttu-id="cdade-117">*cbOutput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cdade-117">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdade-118">La longitud, bytes, del búfer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="cdade-118">The length, bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cdade-119">*pcbResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cdade-119">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdade-120">Número de bytes escritos en el búfer de *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="cdade-120">The number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cdade-121">*SequenceNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cdade-121">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdade-122">El número de secuencia que corresponde a este paquete.</span><span class="sxs-lookup"><span data-stu-id="cdade-122">The sequence number that corresponds to this packet.</span></span>

</dd> <dt>

<span data-ttu-id="cdade-123">*dwContentType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cdade-123">*dwContentType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdade-124">El tipo de contenido que corresponde a este paquete, que especifica el protocolo de nivel superior que se usa para procesar el paquete delimitado.</span><span class="sxs-lookup"><span data-stu-id="cdade-124">The content type that corresponds to this packet, which specifies the higher level protocol used to process the enclosed packet.</span></span>



| <span data-ttu-id="cdade-125">Value</span><span class="sxs-lookup"><span data-stu-id="cdade-125">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="cdade-126">Significado</span><span class="sxs-lookup"><span data-stu-id="cdade-126">Meaning</span></span>                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <span data-ttu-id="cdade-127"><dt>**CT \_ CAMBIAR \_ \_ especificación de cifrado**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="cdade-127"><dt>**CT\_CHANGE\_CIPHER\_SPEC**</dt> <dt>20</dt></span></span> </dl> | <span data-ttu-id="cdade-128">Indica un cambio en la estrategia de cifrado.</span><span class="sxs-lookup"><span data-stu-id="cdade-128">Indicates a change in the ciphering strategy.</span></span><br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <span data-ttu-id="cdade-129"><dt>**CT \_ ALERTA**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="cdade-129"><dt>**CT\_ALERT**</dt> <dt>21</dt></span></span> </dl>                                          | <span data-ttu-id="cdade-130">Indica que el paquete incluido contiene una alerta.</span><span class="sxs-lookup"><span data-stu-id="cdade-130">Indicates that the enclosed packet contains an alert.</span></span><br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <span data-ttu-id="cdade-131"><dt>**CT \_ Protocolo de enlace**</dt> <dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="cdade-131"><dt>**CT\_HANDSHAKE**</dt> <dt>22</dt></span></span> </dl>                              | <span data-ttu-id="cdade-132">Indica que el paquete incluido es parte del Protocolo de enlace.</span><span class="sxs-lookup"><span data-stu-id="cdade-132">Indicates that the enclosed packet is part of the handshake protocol.</span></span><br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <span data-ttu-id="cdade-133"><dt>**CT \_ APPLICATIONDATA**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="cdade-133"><dt>**CT\_APPLICATIONDATA**</dt> <dt>23</dt></span></span> </dl>            | <span data-ttu-id="cdade-134">Indica que el paquete contiene datos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdade-134">Indicates that the packet contains application data.</span></span><br/>                  |



 

</dd> <dt>

<span data-ttu-id="cdade-135">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cdade-135">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdade-136">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cdade-136">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdade-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cdade-137">Return value</span></span>

<span data-ttu-id="cdade-138">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="cdade-138">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="cdade-139">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="cdade-139">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="cdade-140">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="cdade-140">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="cdade-141">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cdade-141">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="cdade-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdade-142">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="cdade-143"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="cdade-143"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="cdade-144">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="cdade-144">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cdade-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdade-145">Requirements</span></span>



| <span data-ttu-id="cdade-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdade-146">Requirement</span></span> | <span data-ttu-id="cdade-147">Value</span><span class="sxs-lookup"><span data-stu-id="cdade-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdade-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdade-148">Minimum supported client</span></span><br/> | <span data-ttu-id="cdade-149">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cdade-149">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cdade-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdade-150">Minimum supported server</span></span><br/> | <span data-ttu-id="cdade-151">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cdade-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cdade-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cdade-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdade-153"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdade-153"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="cdade-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cdade-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdade-155"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdade-155"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

