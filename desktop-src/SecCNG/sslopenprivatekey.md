---
description: Abre un identificador para una clave privada.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: Función SslOpenPrivateKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenPrivateKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6fd5c10ce6385e377c72d21f4557d27d2345737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154089"
---
# <a name="sslopenprivatekey-function"></a><span data-ttu-id="de022-103">SslOpenPrivateKey función)</span><span class="sxs-lookup"><span data-stu-id="de022-103">SslOpenPrivateKey function</span></span>

<span data-ttu-id="de022-104">La función **SslOpenPrivateKey** abre un identificador para una [*clave privada*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="de022-104">The **SslOpenPrivateKey** function opens a handle to a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="de022-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de022-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslOpenPrivateKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phPrivateKey,
  _In_  PCCERT_CONTEXT     pCertContext,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="de022-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de022-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de022-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="de022-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de022-108">Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="de022-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="de022-109">*phPrivateKey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="de022-109">*phPrivateKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de022-110">Dirección de un búfer en el que se va a escribir el identificador de la clave privada.</span><span class="sxs-lookup"><span data-stu-id="de022-110">The address of a buffer in which to write the handle to the private key.</span></span>

<span data-ttu-id="de022-111">Cuando haya terminado de usar la clave, debe liberar *phPrivateKey* llamando a la función [**SslFreeObject**](sslfreeobject.md) .</span><span class="sxs-lookup"><span data-stu-id="de022-111">When you have finished using the key, you should free *phPrivateKey* by calling the [**SslFreeObject**](sslfreeobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="de022-112">*pCertContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="de022-112">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de022-113">Dirección del certificado del que se va a obtener la clave privada.</span><span class="sxs-lookup"><span data-stu-id="de022-113">The address of the certificate from which to obtain the private key.</span></span>

</dd> <dt>

<span data-ttu-id="de022-114">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="de022-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de022-115">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="de022-115">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de022-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de022-116">Return value</span></span>

<span data-ttu-id="de022-117">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="de022-117">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="de022-118">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="de022-118">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="de022-119">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="de022-119">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="de022-120">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de022-120">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="de022-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="de022-121">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="de022-122"><dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="de022-122"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="de022-123">No hay suficiente memoria disponible para asignar los búferes necesarios.</span><span class="sxs-lookup"><span data-stu-id="de022-123">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="de022-124"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="de022-124"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="de022-125">El identificador de *hSslProvider* no es válido.</span><span class="sxs-lookup"><span data-stu-id="de022-125">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="de022-126"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="de022-126"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="de022-127">El parámetro *phPrivateKey* o *pCertContext* es **null**.</span><span class="sxs-lookup"><span data-stu-id="de022-127">The *phPrivateKey* or *pCertContext* parameter is **NULL**.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="de022-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de022-128">Remarks</span></span>

<span data-ttu-id="de022-129">La clave privada obtenida forma parte de un [*par de claves pública y privada*](/windows/desktop/SecGloss/p-gly) dentro de un [*certificado*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="de022-129">The private key obtained is part of a [*public/private key pair*](/windows/desktop/SecGloss/p-gly) within a [*certificate*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="de022-130">Esta función simplemente extrae la clave privada del certificado especificado por el parámetro *pCertContext* .</span><span class="sxs-lookup"><span data-stu-id="de022-130">This function merely extracts the private key from the certificate specified by the *pCertContext* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="de022-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de022-131">Requirements</span></span>



| <span data-ttu-id="de022-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="de022-132">Requirement</span></span> | <span data-ttu-id="de022-133">Value</span><span class="sxs-lookup"><span data-stu-id="de022-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de022-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de022-134">Minimum supported client</span></span><br/> | <span data-ttu-id="de022-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="de022-135">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="de022-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de022-136">Minimum supported server</span></span><br/> | <span data-ttu-id="de022-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="de022-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="de022-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de022-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="de022-139"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="de022-139"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="de022-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="de022-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de022-141"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de022-141"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

