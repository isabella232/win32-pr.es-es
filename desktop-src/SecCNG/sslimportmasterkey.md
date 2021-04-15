---
description: Realiza una operación de intercambio de claves del Protocolo de Capa de sockets seguros de servidor (SSL).
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: Función SslImportMasterKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e21c4cd0f6e51662124e02881b82c905dba68c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648382"
---
# <a name="sslimportmasterkey-function"></a><span data-ttu-id="2bd00-103">SslImportMasterKey función)</span><span class="sxs-lookup"><span data-stu-id="2bd00-103">SslImportMasterKey function</span></span>

<span data-ttu-id="2bd00-104">La función **SslImportMasterKey** realiza una operación de intercambio de claves del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) de servidor (SSL).</span><span class="sxs-lookup"><span data-stu-id="2bd00-104">The **SslImportMasterKey** function performs a server-side [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) key exchange operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bd00-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2bd00-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslImportMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  PBYTE              pbEncryptedKey,
  _In_  DWORD              cbEncryptedKey,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2bd00-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bd00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bd00-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2bd00-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd00-108">Identificador de la instancia del proveedor del protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="2bd00-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="2bd00-109">*hPrivateKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2bd00-109">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd00-110">Identificador de la [*clave privada*](/windows/desktop/SecGloss/p-gly) utilizada en el intercambio.</span><span class="sxs-lookup"><span data-stu-id="2bd00-110">The handle to the [*private key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="2bd00-111">*phMasterKey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2bd00-111">*phMasterKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd00-112">Puntero al identificador para recibir la [*clave maestra*](/windows/desktop/SecGloss/m-gly).</span><span class="sxs-lookup"><span data-stu-id="2bd00-112">A pointer to the handle to receive the [*master key*](/windows/desktop/SecGloss/m-gly).</span></span>

</dd> <dt>

<span data-ttu-id="2bd00-113">*dwProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2bd00-113">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd00-114">Uno de los valores del [**identificador de protocolo del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="2bd00-114">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="2bd00-115">*dwCipherSuite* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2bd00-115">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd00-116">Uno de los valores de los [**identificadores del conjunto de cifrado del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="2bd00-116">One of the [**CNG SSL Provider Cipher Suite Identifiers**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="2bd00-117">*pParameterList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2bd00-117">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd00-118">Puntero a una matriz de búferes de [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contienen información utilizada como parte de la operación de intercambio de claves.</span><span class="sxs-lookup"><span data-stu-id="2bd00-118">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="2bd00-119">El conjunto preciso de búferes depende del protocolo y el conjunto de cifrado que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="2bd00-119">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="2bd00-120">Como mínimo, la lista contendrá búferes que contengan los valores aleatorios proporcionados por el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="2bd00-120">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="2bd00-121">*pbEncryptedKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2bd00-121">*pbEncryptedKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd00-122">Un puntero a un búfer que contiene la clave secreta maestra precifrada cifrada con la [*clave pública*](/windows/desktop/SecGloss/p-gly) del servidor.</span><span class="sxs-lookup"><span data-stu-id="2bd00-122">A pointer to a buffer that contains the encrypted premaster secret key encrypted with the [*public key*](/windows/desktop/SecGloss/p-gly) of the server.</span></span>

</dd> <dt>

<span data-ttu-id="2bd00-123">*cbEncryptedKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2bd00-123">*cbEncryptedKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd00-124">Tamaño, en bytes, del búfer *pbEncryptedKey* .</span><span class="sxs-lookup"><span data-stu-id="2bd00-124">The size, in bytes, of the *pbEncryptedKey* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2bd00-125">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2bd00-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd00-126">Establezca este parámetro en **la \_ \_ \_ marca de servidor SSL NCRYPT** para indicar que se trata de una llamada de servidor.</span><span class="sxs-lookup"><span data-stu-id="2bd00-126">Set this parameter to **NCRYPT\_SSL\_SERVER\_FLAG** to indicate that this is a server call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bd00-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bd00-127">Return value</span></span>

<span data-ttu-id="2bd00-128">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="2bd00-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="2bd00-129">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="2bd00-129">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="2bd00-130">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="2bd00-130">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="2bd00-131">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bd00-131">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="2bd00-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bd00-132">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2bd00-133"><dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="2bd00-133"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="2bd00-134">No hay suficiente memoria disponible para asignar los búferes necesarios.</span><span class="sxs-lookup"><span data-stu-id="2bd00-134">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="2bd00-135"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="2bd00-135"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="2bd00-136">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="2bd00-136">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="2bd00-137"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="2bd00-137"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="2bd00-138">El parámetro *phMasterKey* es **null**.</span><span class="sxs-lookup"><span data-stu-id="2bd00-138">The *phMasterKey* parameter is **NULL**.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="2bd00-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2bd00-139">Remarks</span></span>

<span data-ttu-id="2bd00-140">Esta función descifra el secreto principal previo, calcula el secreto principal SSL y devuelve un identificador de este objeto al llamador.</span><span class="sxs-lookup"><span data-stu-id="2bd00-140">This function decrypts the premaster secret, computes the SSL master secret, and returns a handle to this object to the caller.</span></span> <span data-ttu-id="2bd00-141">Esta clave maestra se puede usar para derivar la clave de sesión SSL y finalizar el protocolo de enlace SSL.</span><span class="sxs-lookup"><span data-stu-id="2bd00-141">This master key can then be used to derive the SSL session key and finish the SSL handshake.</span></span>

> [!Note]  
> <span data-ttu-id="2bd00-142">Esta función se usa cuando se utiliza el algoritmo de intercambio de claves [*RSA*](/windows/desktop/SecGloss/r-gly) .</span><span class="sxs-lookup"><span data-stu-id="2bd00-142">This function is used when the [*RSA*](/windows/desktop/SecGloss/r-gly) key exchange algorithm is being used.</span></span> <span data-ttu-id="2bd00-143">Cuando se usa [*DH*](/windows/desktop/SecGloss/d-gly) , el código de servidor llama a [**SslGenerateMasterKey**](sslgeneratemasterkey.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="2bd00-143">When [*DH*](/windows/desktop/SecGloss/d-gly) is used, then the server code calls [**SslGenerateMasterKey**](sslgeneratemasterkey.md) instead.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2bd00-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bd00-144">Requirements</span></span>



| <span data-ttu-id="2bd00-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bd00-145">Requirement</span></span> | <span data-ttu-id="2bd00-146">Value</span><span class="sxs-lookup"><span data-stu-id="2bd00-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd00-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bd00-147">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd00-148">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2bd00-148">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2bd00-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bd00-149">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd00-150">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2bd00-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2bd00-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bd00-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bd00-152"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bd00-152"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="2bd00-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2bd00-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bd00-154"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bd00-154"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

