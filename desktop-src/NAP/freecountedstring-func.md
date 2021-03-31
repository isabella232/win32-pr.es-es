---
title: Función FreeCountedString (NapUtil. h)
description: Libera una estructura de datos CountedString.
ms.assetid: d080d247-9339-474b-866e-b412e82dd35f
keywords:
- FreeCountedString función NAP
topic_type:
- apiref
api_name:
- FreeCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f732a069d19d6b8948854bd1fe2e23be070aa23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995953"
---
# <a name="freecountedstring-function"></a><span data-ttu-id="15066-104">FreeCountedString función)</span><span class="sxs-lookup"><span data-stu-id="15066-104">FreeCountedString function</span></span>

> [!Note]  
> <span data-ttu-id="15066-105">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="15066-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="15066-106">La función **FreeCountedString** libera una estructura de datos [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="15066-106">The **FreeCountedString** function frees a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="15066-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15066-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeCountedString(
  _In_ CountedString *countedString
);
```



## <a name="parameters"></a><span data-ttu-id="15066-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15066-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15066-109">*countedString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="15066-109">*countedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15066-110">Puntero a la estructura de datos [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="15066-110">A pointer to the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15066-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15066-111">Remarks</span></span>

<span data-ttu-id="15066-112">Todas las interfaces COM que admite el sistema NAP usan reglas estándar de administración de memoria COM y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="15066-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="15066-113">El autor de la llamada asigna y libera los parámetros **in** .</span><span class="sxs-lookup"><span data-stu-id="15066-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="15066-114">El destinatario asigna los parámetros **out** y el llamador los libera mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="15066-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="15066-115">Los parámetros **in/out** son asignados por el autor de la llamada, liberados y reasignados por el destinatario y, en última instancia, liberados por el llamador, mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="15066-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="15066-116">Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.</span><span class="sxs-lookup"><span data-stu-id="15066-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="15066-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15066-117">Requirements</span></span>



| <span data-ttu-id="15066-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="15066-118">Requirement</span></span> | <span data-ttu-id="15066-119">Value</span><span class="sxs-lookup"><span data-stu-id="15066-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="15066-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15066-120">Minimum supported client</span></span><br/> | <span data-ttu-id="15066-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="15066-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="15066-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15066-122">Minimum supported server</span></span><br/> | <span data-ttu-id="15066-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="15066-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="15066-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15066-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="15066-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="15066-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="15066-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15066-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15066-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15066-127"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15066-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="15066-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15066-129">**AllocCountedString**</span><span class="sxs-lookup"><span data-stu-id="15066-129">**AllocCountedString**</span></span>](alloccountedstring-func.md)
</dt> </dl>

 

 





