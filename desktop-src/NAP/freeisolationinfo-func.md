---
title: Función FreeIsolationInfo (NapUtil. h)
description: Libera una estructura de datos IsolationInfo.
ms.assetid: 639cfa74-0823-4a19-9cbe-dd6f0a38e7eb
keywords:
- FreeIsolationInfo función NAP
topic_type:
- apiref
api_name:
- FreeIsolationInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ed154d35b32edab0f1a68d84f78c10cfd1cfe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676889"
---
# <a name="freeisolationinfo-function"></a><span data-ttu-id="aa439-104">FreeIsolationInfo función)</span><span class="sxs-lookup"><span data-stu-id="aa439-104">FreeIsolationInfo function</span></span>

> [!Note]  
> <span data-ttu-id="aa439-105">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="aa439-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="aa439-106">La función **FreeIsolationInfo** libera una estructura de datos [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) .</span><span class="sxs-lookup"><span data-stu-id="aa439-106">The **FreeIsolationInfo** function frees an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa439-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa439-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeIsolationInfo(
  _In_ IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="aa439-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa439-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa439-109">*isolationInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aa439-109">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa439-110">Puntero a la estructura de datos [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="aa439-110">A pointer to the [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa439-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa439-111">Remarks</span></span>

<span data-ttu-id="aa439-112">Todas las interfaces COM que admite el sistema NAP usan reglas estándar de administración de memoria COM y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="aa439-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="aa439-113">El autor de la llamada asigna y libera los parámetros **in** .</span><span class="sxs-lookup"><span data-stu-id="aa439-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="aa439-114">El destinatario asigna los parámetros **out** y el llamador los libera mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="aa439-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="aa439-115">Los parámetros **in/out** son asignados por el autor de la llamada, liberados y reasignados por el destinatario y, en última instancia, liberados por el llamador, mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="aa439-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="aa439-116">Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.</span><span class="sxs-lookup"><span data-stu-id="aa439-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa439-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa439-117">Requirements</span></span>



| <span data-ttu-id="aa439-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa439-118">Requirement</span></span> | <span data-ttu-id="aa439-119">Value</span><span class="sxs-lookup"><span data-stu-id="aa439-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aa439-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa439-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa439-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="aa439-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="aa439-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa439-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa439-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa439-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aa439-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa439-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa439-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa439-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="aa439-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa439-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa439-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa439-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





