---
description: Calcula la clave secreta maestra del Protocolo de Capa de sockets seguros (SSL).
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: Función SslGenerateMasterKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ae8b357743cabf652721d3666c177990568718e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424075"
---
# <a name="sslgeneratemasterkey-function"></a><span data-ttu-id="5e3db-103">SslGenerateMasterKey función)</span><span class="sxs-lookup"><span data-stu-id="5e3db-103">SslGenerateMasterKey function</span></span>

<span data-ttu-id="5e3db-104">La función **SslGenerateMasterKey** calcula la clave secreta maestra del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="5e3db-104">The **SslGenerateMasterKey** function computes the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) master secret key.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e3db-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e3db-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGenerateMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  NCRYPT_KEY_HANDLE  hPublicKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5e3db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e3db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e3db-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e3db-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3db-108">Identificador de la instancia del proveedor del protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="5e3db-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="5e3db-109">*hPrivateKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e3db-109">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3db-110">Identificador de la [*clave privada*](/windows/desktop/SecGloss/p-gly) utilizada en el intercambio.</span><span class="sxs-lookup"><span data-stu-id="5e3db-110">The handle to the [*private key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="5e3db-111">*hPublicKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e3db-111">*hPublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3db-112">Identificador de la [*clave pública*](/windows/desktop/SecGloss/p-gly) que se usa en el intercambio.</span><span class="sxs-lookup"><span data-stu-id="5e3db-112">The handle to the [*public key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="5e3db-113">*phMasterKey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5e3db-113">*phMasterKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3db-114">Puntero al identificador de la [*clave maestra*](/windows/desktop/SecGloss/m-gly)generada.</span><span class="sxs-lookup"><span data-stu-id="5e3db-114">A pointer to the handle to the generated [*master key*](/windows/desktop/SecGloss/m-gly).</span></span>

</dd> <dt>

<span data-ttu-id="5e3db-115">*dwProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e3db-115">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3db-116">Uno de los valores del [**identificador de protocolo del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e3db-116">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="5e3db-117">*dwCipherSuite* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e3db-117">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3db-118">Uno de los valores del [**identificador del conjunto de cifrado del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e3db-118">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="5e3db-119">*pParameterList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e3db-119">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3db-120">Puntero a una matriz de búferes de [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contienen información utilizada como parte de la operación de intercambio de claves.</span><span class="sxs-lookup"><span data-stu-id="5e3db-120">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="5e3db-121">El conjunto preciso de búferes depende del protocolo y el conjunto de cifrado que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5e3db-121">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="5e3db-122">Como mínimo, la lista contendrá búferes que contengan los valores aleatorios proporcionados por el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="5e3db-122">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="5e3db-123">*pbOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5e3db-123">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3db-124">Dirección de un búfer que recibe el secreto principal precifrado cifrado con la clave pública del servidor.</span><span class="sxs-lookup"><span data-stu-id="5e3db-124">The address of a buffer that receives the premaster secret encrypted with the public key of the server.</span></span> <span data-ttu-id="5e3db-125">El parámetro *cbOutput* contiene el tamaño de este búfer.</span><span class="sxs-lookup"><span data-stu-id="5e3db-125">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="5e3db-126">Si este parámetro es **null**, esta función devuelve el tamaño necesario, en bytes, en el **valor DWORD** al que apunta el parámetro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="5e3db-126">If this parameter is **NULL**, this function returns the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="5e3db-127">Este búfer se usa al realizar un intercambio de claves RSA.</span><span class="sxs-lookup"><span data-stu-id="5e3db-127">This buffer is used when performing a RSA key exchange.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e3db-128">*cbOutput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e3db-128">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3db-129">Tamaño, en bytes, del búfer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="5e3db-129">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5e3db-130">*pcbResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5e3db-130">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3db-131">Un puntero a un valor **DWORD** en el que se colocará el número de bytes escritos en el búfer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="5e3db-131">A pointer to a **DWORD** value in which to place number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5e3db-132">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e3db-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3db-133">Especifica si esta función se usa para el intercambio de claves del lado cliente o el servidor.</span><span class="sxs-lookup"><span data-stu-id="5e3db-133">Specifies whether this function is being used for client-side or server-side key exchange.</span></span>



| <span data-ttu-id="5e3db-134">Value</span><span class="sxs-lookup"><span data-stu-id="5e3db-134">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="5e3db-135">Significado</span><span class="sxs-lookup"><span data-stu-id="5e3db-135">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <span data-ttu-id="5e3db-136"><dt>**NCRYPT \_ \_ \_ Marca de cliente SSL**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="5e3db-136"><dt>**NCRYPT\_SSL\_CLIENT\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="5e3db-137">Especifica un intercambio de claves del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="5e3db-137">Specifies a client-side key exchange.</span></span><br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <span data-ttu-id="5e3db-138"><dt>**NCRYPT \_ \_ \_ Marca de servidor SSL**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="5e3db-138"><dt>**NCRYPT\_SSL\_SERVER\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="5e3db-139">Especifica un intercambio de claves del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="5e3db-139">Specifies a server-side key exchange.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e3db-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e3db-140">Return value</span></span>

<span data-ttu-id="5e3db-141">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5e3db-141">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="5e3db-142">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="5e3db-142">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="5e3db-143">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e3db-143">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="5e3db-144">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e3db-144">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="5e3db-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e3db-145">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e3db-146"><dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="5e3db-146"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="5e3db-147">No hay suficiente memoria disponible para asignar los búferes necesarios.</span><span class="sxs-lookup"><span data-stu-id="5e3db-147">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="5e3db-148"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="5e3db-148"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="5e3db-149">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="5e3db-149">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="5e3db-150"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="5e3db-150"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="5e3db-151">El parámetro *phMasterKey* o *hPublicKey* no es válido.</span><span class="sxs-lookup"><span data-stu-id="5e3db-151">The *phMasterKey* or *hPublicKey* parameter is not valid.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="5e3db-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e3db-152">Requirements</span></span>



| <span data-ttu-id="5e3db-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e3db-153">Requirement</span></span> | <span data-ttu-id="5e3db-154">Value</span><span class="sxs-lookup"><span data-stu-id="5e3db-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e3db-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e3db-155">Minimum supported client</span></span><br/> | <span data-ttu-id="5e3db-156">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e3db-156">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5e3db-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e3db-157">Minimum supported server</span></span><br/> | <span data-ttu-id="5e3db-158">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e3db-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5e3db-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e3db-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e3db-160"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e3db-160"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="5e3db-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e3db-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e3db-162"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e3db-162"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

