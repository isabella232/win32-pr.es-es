---
description: La función ExpertReallocMemory aumenta o reduce la cantidad de memoria asignada por Monitor de red.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: Función ExpertReallocMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertReallocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8f562443f9ca66def7e053f5958b17e70af50140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652369"
---
# <a name="expertreallocmemory-function"></a><span data-ttu-id="8ff29-103">ExpertReallocMemory función)</span><span class="sxs-lookup"><span data-stu-id="8ff29-103">ExpertReallocMemory function</span></span>

<span data-ttu-id="8ff29-104">La función **ExpertReallocMemory** aumenta o reduce la cantidad de memoria asignada por monitor de red.</span><span class="sxs-lookup"><span data-stu-id="8ff29-104">The **ExpertReallocMemory** function increases or decreases the amount of memory allocated by Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ff29-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ff29-105">Syntax</span></span>


```C++
LPVOID WINAPI ExpertReallocMemory(
  _In_  HEXPERTKEY hExpertKey,
  _In_  LPVOID     pOriginalMemory,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a><span data-ttu-id="8ff29-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ff29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ff29-107">*hExpertKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ff29-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff29-108">Identificador único que se pasa al experto en [**Ejecutar**](run.md) o [**configurar**](configure.md).</span><span class="sxs-lookup"><span data-stu-id="8ff29-108">Unique identifier passed to the expert at [**Run**](run.md) or [**Configure**](configure.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ff29-109">*pOriginalMemory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ff29-109">*pOriginalMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff29-110">Puntero a la memoria asignada por Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="8ff29-110">Pointer to the memory allocated by Network Monitor.</span></span> <span data-ttu-id="8ff29-111">El puntero *pOriginalMemory* puede ser devuelto por una llamada anterior a [**ExpertAllocMemory**](expertallocmemory.md) o **ExpertReallocMemory**.</span><span class="sxs-lookup"><span data-stu-id="8ff29-111">The *pOriginalMemory* pointer can be returned by a previous call to [**ExpertAllocMemory**](expertallocmemory.md) or **ExpertReallocMemory**.</span></span>

</dd> <dt>

<span data-ttu-id="8ff29-112">*nBytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ff29-112">*nBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff29-113">Tamaño de la memoria reasignada.</span><span class="sxs-lookup"><span data-stu-id="8ff29-113">Size of reallocated memory.</span></span>

</dd> <dt>

<span data-ttu-id="8ff29-114">*perror* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8ff29-114">*pError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff29-115">En la devolución, un código de error si se produce un error en la función.</span><span class="sxs-lookup"><span data-stu-id="8ff29-115">On return, an error code if the function fails.</span></span> <span data-ttu-id="8ff29-116">Si el código de error es NMERR \_ Expert \_ Terminate, el experto debe limpiar y volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8ff29-116">If the error code is NMERR\_EXPERT\_TERMINATE, the expert must clean up and return immediately.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ff29-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ff29-117">Return value</span></span>

<span data-ttu-id="8ff29-118">Si la función se realiza correctamente, el valor devuelto es un puntero a la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="8ff29-118">If the function is successful, the return value is a pointer to the allocated memory.</span></span>

<span data-ttu-id="8ff29-119">Si la función no se realiza correctamente, el valor devuelto es **null** y el *perror* (si es un valor distinto de **null** ) indica el motivo del error.</span><span class="sxs-lookup"><span data-stu-id="8ff29-119">If the function is unsuccessful, the return value is **NULL**, and *pError* (if it is a non-**NULL** value) indicates the reason for the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ff29-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ff29-120">Remarks</span></span>

<span data-ttu-id="8ff29-121">Es importante tener en cuenta que un experto debe usar las funciones de asignación de memoria Monitor de red para la administración de memoria.</span><span class="sxs-lookup"><span data-stu-id="8ff29-121">It is important to note that an expert should use the Network Monitor memory allocation functions for memory management.</span></span> <span data-ttu-id="8ff29-122">Si se produce un error en el experto durante el tiempo de ejecución, el uso de estas funciones permitirá a Monitor de red liberar la memoria que ha asignado.</span><span class="sxs-lookup"><span data-stu-id="8ff29-122">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ff29-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ff29-123">Requirements</span></span>



| <span data-ttu-id="8ff29-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ff29-124">Requirement</span></span> | <span data-ttu-id="8ff29-125">Value</span><span class="sxs-lookup"><span data-stu-id="8ff29-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff29-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ff29-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8ff29-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8ff29-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8ff29-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ff29-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8ff29-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8ff29-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8ff29-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ff29-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ff29-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ff29-131"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="8ff29-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ff29-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="8ff29-133"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ff29-133"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8ff29-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ff29-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ff29-135"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ff29-135"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




