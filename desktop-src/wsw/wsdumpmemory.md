---
title: Función WsDumpMemory (WebServicesDebug. h)
description: Esta función vuelca todas las asignaciones de memoria en la consola.
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- Servicios Web de la función WsDumpMemory para Windows
topic_type:
- apiref
api_name:
- WsDumpMemory
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70af8d34b3ee04a9db4128ce1063bd31e81306eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996866"
---
# <a name="wsdumpmemory-function"></a><span data-ttu-id="06624-104">WsDumpMemory función)</span><span class="sxs-lookup"><span data-stu-id="06624-104">WsDumpMemory function</span></span>

<span data-ttu-id="06624-105">Esta función vuelca todas las asignaciones de memoria en la consola.</span><span class="sxs-lookup"><span data-stu-id="06624-105">This function dumps all memory allocations to the console.</span></span>

> [!Note]  
> <span data-ttu-id="06624-106">Esta función es solo para depurar.</span><span class="sxs-lookup"><span data-stu-id="06624-106">This function is for DEBUG ONLY.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="06624-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06624-107">Syntax</span></span>


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a><span data-ttu-id="06624-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06624-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06624-109">*error* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="06624-109">*error* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06624-110">Un puntero a un objeto de [ \_ error de WS](ws-error.md) en el que se debe almacenar información adicional sobre el error si se produce un error en la función.</span><span class="sxs-lookup"><span data-stu-id="06624-110">A pointer to a [WS\_ERROR](ws-error.md) object where additional information about the error should be stored if the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06624-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06624-111">Return value</span></span>

<span data-ttu-id="06624-112">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="06624-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06624-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06624-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="06624-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06624-114">Requirements</span></span>



| <span data-ttu-id="06624-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="06624-115">Requirement</span></span> | <span data-ttu-id="06624-116">Value</span><span class="sxs-lookup"><span data-stu-id="06624-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="06624-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06624-117">Minimum supported client</span></span><br/> | <span data-ttu-id="06624-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="06624-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                             |
| <span data-ttu-id="06624-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06624-119">Minimum supported server</span></span><br/> | <span data-ttu-id="06624-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="06624-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="06624-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06624-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="06624-122"><dt>WebServicesDebug. h</dt></span><span class="sxs-lookup"><span data-stu-id="06624-122"><dt>WebServicesDebug.h</dt></span></span> </dl> |



 

 





