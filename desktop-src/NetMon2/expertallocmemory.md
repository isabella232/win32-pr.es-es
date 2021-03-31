---
description: La función ExpertAllocMemory asigna memoria para el experto.
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: Función ExpertAllocMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertAllocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b30aba5e2b448df141d0c82e6ec5a2b0d9b3303f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808731"
---
# <a name="expertallocmemory-function"></a><span data-ttu-id="9d5ed-103">ExpertAllocMemory función)</span><span class="sxs-lookup"><span data-stu-id="9d5ed-103">ExpertAllocMemory function</span></span>

<span data-ttu-id="9d5ed-104">La función **ExpertAllocMemory** asigna memoria para el experto.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-104">The **ExpertAllocMemory** function allocates memory for the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d5ed-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d5ed-105">Syntax</span></span>


```C++
LPVOID WINAPI ExpertAllocMemory(
        HEXPERTKEY hExpertKey,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a><span data-ttu-id="9d5ed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d5ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d5ed-107">*hExpertKey*</span><span class="sxs-lookup"><span data-stu-id="9d5ed-107">*hExpertKey*</span></span> 
</dt> <dd>

<span data-ttu-id="9d5ed-108">Identificador de experto único.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-108">Unique expert identifier.</span></span> <span data-ttu-id="9d5ed-109">Monitor de red pasa *hExpertKey* al experto cuando llama a la función [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="9d5ed-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="9d5ed-110">*nBytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d5ed-110">*nBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5ed-111">Memoria asignada, medida en bytes.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-111">Allocated memory, measured in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9d5ed-112">*perror* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9d5ed-112">*pError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5ed-113">Indicador de error.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-113">Error indicator.</span></span> <span data-ttu-id="9d5ed-114">Si se produce un error en la función, el parámetro *nBytes* contiene el código de error.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-114">If the function fails, the *nBytes* parameter contains the error code.</span></span> <span data-ttu-id="9d5ed-115">Si el código de error es NMERR \_ Expert \_ Terminate, el experto debe limpiar y volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-115">If the error code is NMERR\_EXPERT\_TERMINATE, the expert must clean-up and return immediately.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d5ed-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d5ed-116">Return value</span></span>

<span data-ttu-id="9d5ed-117">Si la función se realiza correctamente, el valor devuelto es un puntero a la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-117">If the function is successful, the return value is a pointer to the allocated memory.</span></span>

<span data-ttu-id="9d5ed-118">Si la función no se realiza correctamente, el valor devuelto es **null** y el *perror* proporciona un código de error que indica la razón del error.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-118">If the function is unsuccessful, the return value is **NULL**, and *pError* provides an error code that indicates the reason for the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d5ed-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d5ed-119">Remarks</span></span>

<span data-ttu-id="9d5ed-120">Es importante tener en cuenta que un experto debe usar las funciones de asignación de memoria Monitor de red (incluido [ExpertReallocMemory](expertreallocmemory.md)) para la administración de memoria.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-120">It is important to note that an expert should use the Network Monitor memory allocation functions (including [ExpertReallocMemory](expertreallocmemory.md)) for memory management.</span></span> <span data-ttu-id="9d5ed-121">Si se produce un error en el experto durante el tiempo de ejecución, el uso de estas funciones permitirá a Monitor de red liberar la memoria que ha asignado.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-121">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d5ed-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d5ed-122">Requirements</span></span>



| <span data-ttu-id="9d5ed-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d5ed-123">Requirement</span></span> | <span data-ttu-id="9d5ed-124">Value</span><span class="sxs-lookup"><span data-stu-id="9d5ed-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5ed-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d5ed-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9d5ed-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9d5ed-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9d5ed-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d5ed-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9d5ed-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9d5ed-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9d5ed-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d5ed-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d5ed-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d5ed-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9d5ed-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d5ed-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d5ed-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d5ed-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9d5ed-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9d5ed-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d5ed-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d5ed-134"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




