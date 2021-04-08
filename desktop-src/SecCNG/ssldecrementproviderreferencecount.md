---
description: Disminuye las referencias al proveedor del Protocolo de Capa de sockets seguros (SSL).
ms.assetid: 67bfa4b5-c02c-4a76-871d-93f3bf4e3602
title: Función SslDecrementProviderReferenceCount (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4d3fe072c02f22b713115dd5191b0b5e0cedbb37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001646"
---
# <a name="ssldecrementproviderreferencecount-function"></a><span data-ttu-id="56cfc-103">SslDecrementProviderReferenceCount función)</span><span class="sxs-lookup"><span data-stu-id="56cfc-103">SslDecrementProviderReferenceCount function</span></span>

<span data-ttu-id="56cfc-104">La función **SslDecrementProviderReferenceCount** reduce las referencias al proveedor del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="56cfc-104">The **SslDecrementProviderReferenceCount** function decrements the references to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="56cfc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56cfc-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslDecrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a><span data-ttu-id="56cfc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56cfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56cfc-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="56cfc-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56cfc-108">Identificador de la instancia del proveedor del protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="56cfc-108">The handle of the SSL protocol provider instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56cfc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56cfc-109">Return value</span></span>

<span data-ttu-id="56cfc-110">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="56cfc-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="56cfc-111">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="56cfc-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="56cfc-112">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="56cfc-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="56cfc-113">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56cfc-113">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="56cfc-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="56cfc-114">Description</span></span>                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="56cfc-115"><dt> **Estado \_ \_ identificador no válido**</dt> <dt>0xC0000008L</dt></span><span class="sxs-lookup"><span data-stu-id="56cfc-115"><dt>**STATUS\_INVALID\_HANDLE** </dt> <dt>0xC0000008L</dt></span></span> </dl> | <span data-ttu-id="56cfc-116">El identificador del proveedor SSL no es válido.</span><span class="sxs-lookup"><span data-stu-id="56cfc-116">The SSL provider handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="56cfc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56cfc-117">Requirements</span></span>



| <span data-ttu-id="56cfc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="56cfc-118">Requirement</span></span> | <span data-ttu-id="56cfc-119">Value</span><span class="sxs-lookup"><span data-stu-id="56cfc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="56cfc-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56cfc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="56cfc-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="56cfc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="56cfc-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56cfc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="56cfc-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="56cfc-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="56cfc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56cfc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="56cfc-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="56cfc-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="56cfc-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="56cfc-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56cfc-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56cfc-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

