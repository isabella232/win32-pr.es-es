---
title: Función FreeSoH (NapUtil. h)
description: Libera una estructura de datos SoH.
ms.assetid: 587acf64-31be-46c8-9d49-b5014c1a90ba
keywords:
- FreeSoH función NAP
topic_type:
- apiref
api_name:
- FreeSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28409c18bf9f673c78d6df2a224cb936223edddb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151091"
---
# <a name="freesoh-function"></a><span data-ttu-id="f3bd5-104">FreeSoH función)</span><span class="sxs-lookup"><span data-stu-id="f3bd5-104">FreeSoH function</span></span>

> [!Note]  
> <span data-ttu-id="f3bd5-105">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="f3bd5-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f3bd5-106">La función **FreeSoH** libera una estructura de datos **SOH** .</span><span class="sxs-lookup"><span data-stu-id="f3bd5-106">The **FreeSoH** function frees a **SoH** data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3bd5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3bd5-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeSoH(
  _In_ SoH *soh
);
```



## <a name="parameters"></a><span data-ttu-id="f3bd5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3bd5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3bd5-109">*SOH* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f3bd5-109">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bd5-110">Puntero a la estructura de datos [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="f3bd5-110">A pointer to the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3bd5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3bd5-111">Remarks</span></span>

<span data-ttu-id="f3bd5-112">Todas las interfaces COM que admite el sistema NAP usan reglas estándar de administración de memoria COM y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="f3bd5-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="f3bd5-113">El autor de la llamada asigna y libera los parámetros **in** .</span><span class="sxs-lookup"><span data-stu-id="f3bd5-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="f3bd5-114">El destinatario asigna los parámetros **out** y el llamador los libera mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="f3bd5-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="f3bd5-115">Los parámetros **in/out** son asignados por el autor de la llamada, liberados y reasignados por el destinatario y, en última instancia, liberados por el llamador, mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="f3bd5-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="f3bd5-116">Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.</span><span class="sxs-lookup"><span data-stu-id="f3bd5-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3bd5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3bd5-117">Requirements</span></span>



| <span data-ttu-id="f3bd5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3bd5-118">Requirement</span></span> | <span data-ttu-id="f3bd5-119">Value</span><span class="sxs-lookup"><span data-stu-id="f3bd5-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f3bd5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3bd5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f3bd5-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f3bd5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f3bd5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3bd5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f3bd5-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3bd5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f3bd5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3bd5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3bd5-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3bd5-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="f3bd5-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3bd5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3bd5-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3bd5-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





