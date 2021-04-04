---
description: Comprueba la firma especificada utilizando el hash proporcionado y la clave pública.
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: Función SslVerifySignature (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslVerifySignature
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cb2a50a7f16062f271a89b6061e3f2fa2dd16685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907827"
---
# <a name="sslverifysignature-function"></a><span data-ttu-id="edd6a-103">SslVerifySignature función)</span><span class="sxs-lookup"><span data-stu-id="edd6a-103">SslVerifySignature function</span></span>

<span data-ttu-id="edd6a-104">La función **SslVerifySignature** comprueba la firma especificada mediante el [*hash*](/windows/desktop/SecGloss/h-gly) proporcionado y la [*clave pública*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="edd6a-104">The **SslVerifySignature** function verifies the specified signature by using the supplied [*hash*](/windows/desktop/SecGloss/h-gly) and the [*public key*](/windows/desktop/SecGloss/p-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="edd6a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edd6a-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslVerifySignature(
  _In_ NCRYPT_PROV_HANDLE hSslProvider,
  _In_ NCRYPT_KEY_HANDLE  hPublicKey,
  _In_ PBYTE              pbHashValue,
  _In_ DWORD              cbHashValue,
  _In_ PBYTE              pbSignature,
  _In_ DWORD              cbSignature,
  _In_ DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="edd6a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edd6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edd6a-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edd6a-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd6a-108">Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="edd6a-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="edd6a-109">*hPublicKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edd6a-109">*hPublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd6a-110">Identificador de la clave pública.</span><span class="sxs-lookup"><span data-stu-id="edd6a-110">The handle to the public key.</span></span>

</dd> <dt>

<span data-ttu-id="edd6a-111">*pbHashValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edd6a-111">*pbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd6a-112">Un puntero a un búfer que contiene el hash que se va a utilizar para comprobar la firma.</span><span class="sxs-lookup"><span data-stu-id="edd6a-112">A pointer to a buffer that contains the hash to use to verify the signature.</span></span>

</dd> <dt>

<span data-ttu-id="edd6a-113">*cbHashValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edd6a-113">*cbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd6a-114">Tamaño, en bytes, del búfer *pbHashValue* .</span><span class="sxs-lookup"><span data-stu-id="edd6a-114">The size, in bytes, of the *pbHashValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="edd6a-115">*pbSignature* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edd6a-115">*pbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd6a-116">Puntero a un búfer que contiene la firma que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="edd6a-116">A pointer to a buffer that contains the signature to verify.</span></span>

</dd> <dt>

<span data-ttu-id="edd6a-117">*cbSignature* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edd6a-117">*cbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd6a-118">Tamaño, en bytes, del búfer *pbSignature* .</span><span class="sxs-lookup"><span data-stu-id="edd6a-118">The size, in bytes, of the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="edd6a-119">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edd6a-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd6a-120">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="edd6a-120">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edd6a-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edd6a-121">Return value</span></span>

<span data-ttu-id="edd6a-122">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="edd6a-122">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="edd6a-123">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="edd6a-123">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="edd6a-124">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="edd6a-124">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="edd6a-125">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edd6a-125">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="edd6a-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="edd6a-126">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="edd6a-127"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="edd6a-127"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="edd6a-128">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="edd6a-128">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="edd6a-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edd6a-129">Remarks</span></span>

<span data-ttu-id="edd6a-130">Windows no llama actualmente a la función **SslVerifySignature** .</span><span class="sxs-lookup"><span data-stu-id="edd6a-130">The **SslVerifySignature** function is not currently called by Windows.</span></span> <span data-ttu-id="edd6a-131">Esta función es una parte necesaria de la interfaz del proveedor SSL y debe implementarse completamente para garantizar la compatibilidad con versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="edd6a-131">This function is a required part of the SSL Provider interface and should be fully implemented to ensure forward compatibility.</span></span>

<span data-ttu-id="edd6a-132">Las implementaciones actuales del lado servidor de la conexión del Protocolo de seguridad de la [*capa de transporte*](/windows/desktop/SecGloss/t-gly) (TLS) llaman a la función [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) durante la autenticación del cliente para procesar el mensaje de comprobación de certificado.</span><span class="sxs-lookup"><span data-stu-id="edd6a-132">Current implementations of the server side of the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) connection call the [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) function during the client authentication to process the certificate verify message.</span></span>

## <a name="requirements"></a><span data-ttu-id="edd6a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edd6a-133">Requirements</span></span>



| <span data-ttu-id="edd6a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="edd6a-134">Requirement</span></span> | <span data-ttu-id="edd6a-135">Value</span><span class="sxs-lookup"><span data-stu-id="edd6a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd6a-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edd6a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="edd6a-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="edd6a-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="edd6a-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edd6a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="edd6a-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="edd6a-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="edd6a-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edd6a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="edd6a-141"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="edd6a-141"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="edd6a-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="edd6a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edd6a-143"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edd6a-143"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

