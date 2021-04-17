---
description: Calcula el bloque de claves utilizado por el protocolo de autenticación extensible (EAP).
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: Función SslComputeEapKeyBlock (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeEapKeyBlock
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: d46c1284b208975126067ff295507b51def9133b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666961"
---
# <a name="sslcomputeeapkeyblock-function"></a><span data-ttu-id="cf0d5-103">SslComputeEapKeyBlock función)</span><span class="sxs-lookup"><span data-stu-id="cf0d5-103">SslComputeEapKeyBlock function</span></span>

<span data-ttu-id="cf0d5-104">La función **SslComputeEapKeyBlock** calcula el bloque de claves que usa el protocolo de autenticación extensible (EAP).</span><span class="sxs-lookup"><span data-stu-id="cf0d5-104">The **SslComputeEapKeyBlock** function computes the key block used by the Extensible Authentication Protocol (EAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf0d5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf0d5-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeEapKeyBlock(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hMasterKey,
  _In_      PBYTE              pbRandoms,
  _In_      DWORD              cbRandoms,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="cf0d5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf0d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf0d5-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf0d5-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf0d5-108">Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="cf0d5-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="cf0d5-109">*hMasterKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf0d5-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf0d5-110">Identificador del objeto de [*clave maestra*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="cf0d5-110">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="cf0d5-111">*pbRandoms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf0d5-111">*pbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf0d5-112">Un puntero a un búfer que contiene una concatenación de los valores aleatorios de cliente \_ y \_ de servidor de la sesión SSL.</span><span class="sxs-lookup"><span data-stu-id="cf0d5-112">A pointer to a buffer that contains a concatenation of the client\_random and server\_random values of the SSL session.</span></span>

</dd> <dt>

<span data-ttu-id="cf0d5-113">*cbRandoms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf0d5-113">*cbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf0d5-114">La longitud, en bytes, del búfer *pbRandoms* .</span><span class="sxs-lookup"><span data-stu-id="cf0d5-114">The length, in bytes, of the *pbRandoms* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cf0d5-115">*pbOutput* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cf0d5-115">*pbOutput* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cf0d5-116">La dirección de un búfer que recibe el BLOB de clave.</span><span class="sxs-lookup"><span data-stu-id="cf0d5-116">The address of a buffer that receives the key BLOB.</span></span> <span data-ttu-id="cf0d5-117">El parámetro *cbOutput* contiene el tamaño de este búfer.</span><span class="sxs-lookup"><span data-stu-id="cf0d5-117">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="cf0d5-118">Si este parámetro es **null**, esta función colocará el tamaño necesario, en bytes, en el **valor DWORD** al que apunta el parámetro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="cf0d5-118">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cf0d5-119">*cbOutput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf0d5-119">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf0d5-120">La longitud, en bytes, del búfer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="cf0d5-120">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cf0d5-121">*pcbResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cf0d5-121">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf0d5-122">Un puntero a un valor **DWORD** que especifica la longitud, en bytes, del hash escrito en el búfer de *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="cf0d5-122">A pointer to a **DWORD** value that specifies the length, in bytes, of the hash written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cf0d5-123">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf0d5-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf0d5-124">Establezca en **\_ marca de \_ servidor \_ SSL NCRYPT** para indicar que se trata de una llamada de servidor.</span><span class="sxs-lookup"><span data-stu-id="cf0d5-124">Set to **NCRYPT\_SSL\_SERVER\_FLAG** to indicate that this is a server call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf0d5-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf0d5-125">Return value</span></span>

<span data-ttu-id="cf0d5-126">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="cf0d5-126">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="cf0d5-127">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="cf0d5-127">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="cf0d5-128">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf0d5-128">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="cf0d5-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf0d5-129">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="cf0d5-130"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="cf0d5-130"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="cf0d5-131">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="cf0d5-131">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cf0d5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf0d5-132">Requirements</span></span>



| <span data-ttu-id="cf0d5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf0d5-133">Requirement</span></span> | <span data-ttu-id="cf0d5-134">Value</span><span class="sxs-lookup"><span data-stu-id="cf0d5-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0d5-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf0d5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cf0d5-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cf0d5-136">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cf0d5-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf0d5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cf0d5-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf0d5-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cf0d5-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf0d5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf0d5-140"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf0d5-140"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="cf0d5-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cf0d5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf0d5-142"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf0d5-142"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

