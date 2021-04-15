---
description: Incrementa el recuento de referencias a una instancia del proveedor de protocolo Capa de sockets seguros (SSL).
ms.assetid: 67e7b8b4-b073-4936-b1e0-3fc7c1c011a2
title: Función SslIncrementProviderReferenceCount (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslIncrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 862697035d978db082c303c6e1df6f2a444d8be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669909"
---
# <a name="sslincrementproviderreferencecount-function"></a><span data-ttu-id="0361d-103">SslIncrementProviderReferenceCount función)</span><span class="sxs-lookup"><span data-stu-id="0361d-103">SslIncrementProviderReferenceCount function</span></span>

<span data-ttu-id="0361d-104">La función **SslIncrementProviderReferenceCount** incrementa el recuento de referencias a una instancia del proveedor de [*Protocolo capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="0361d-104">The **SslIncrementProviderReferenceCount** function increments the reference count to a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="0361d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0361d-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslIncrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a><span data-ttu-id="0361d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0361d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0361d-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0361d-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0361d-108">Identificador de la instancia del proveedor del protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="0361d-108">The handle to the SSL protocol provider instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0361d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0361d-109">Return value</span></span>

<span data-ttu-id="0361d-110">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="0361d-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="0361d-111">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="0361d-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="0361d-112">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="0361d-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="0361d-113">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0361d-113">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="0361d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0361d-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="0361d-115"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="0361d-115"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="0361d-116">El identificador de *hSslProvider* no es válido.</span><span class="sxs-lookup"><span data-stu-id="0361d-116">The *hSslProvider* handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0361d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0361d-117">Requirements</span></span>



| <span data-ttu-id="0361d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0361d-118">Requirement</span></span> | <span data-ttu-id="0361d-119">Value</span><span class="sxs-lookup"><span data-stu-id="0361d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0361d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0361d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0361d-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0361d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0361d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0361d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0361d-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0361d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0361d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0361d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0361d-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="0361d-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="0361d-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0361d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0361d-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0361d-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

