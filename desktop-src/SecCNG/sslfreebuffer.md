---
description: Se usa para liberar memoria asignada por una de las funciones del proveedor del Protocolo de Capa de sockets seguros (SSL).
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: Función SslFreeBuffer (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeBuffer
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bced83b52ddf37266f64ae0c2b8919902f30fff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083432"
---
# <a name="sslfreebuffer-function"></a><span data-ttu-id="5e8ae-103">SslFreeBuffer función)</span><span class="sxs-lookup"><span data-stu-id="5e8ae-103">SslFreeBuffer function</span></span>

<span data-ttu-id="5e8ae-104">La función **SslFreeBuffer** se usa para liberar memoria asignada por una de las funciones del proveedor del [*Protocolo capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="5e8ae-104">The **SslFreeBuffer** function is used to free memory that was allocated by one of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e8ae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e8ae-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a><span data-ttu-id="5e8ae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e8ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e8ae-107">*pvInput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e8ae-107">*pvInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e8ae-108">Puntero al búfer de memoria que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="5e8ae-108">A pointer to the memory buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e8ae-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e8ae-109">Return value</span></span>

<span data-ttu-id="5e8ae-110">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5e8ae-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="5e8ae-111">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="5e8ae-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="5e8ae-112">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e8ae-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="5e8ae-113">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e8ae-113">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="5e8ae-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e8ae-114">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e8ae-115"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="5e8ae-115"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="5e8ae-116">El parámetro *pdwProviderCount* o *ppProviderList* es **null**.</span><span class="sxs-lookup"><span data-stu-id="5e8ae-116">The *pdwProviderCount* or *ppProviderList* parameter is **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5e8ae-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e8ae-117">Requirements</span></span>



| <span data-ttu-id="5e8ae-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e8ae-118">Requirement</span></span> | <span data-ttu-id="5e8ae-119">Value</span><span class="sxs-lookup"><span data-stu-id="5e8ae-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e8ae-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e8ae-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5e8ae-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e8ae-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5e8ae-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e8ae-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5e8ae-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e8ae-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5e8ae-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e8ae-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e8ae-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e8ae-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="5e8ae-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e8ae-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e8ae-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e8ae-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

