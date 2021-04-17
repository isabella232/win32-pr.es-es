---
description: La función ExpertFreeMemory libera la memoria adquirida por las llamadas a las funciones ExpertAllocMemory y ExpertReallocMemory.
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: Función ExpertFreeMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertFreeMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: cc26056a3ec3e8820c363d97f92c7eb382cd0622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666299"
---
# <a name="expertfreememory-function"></a><span data-ttu-id="f3aad-103">ExpertFreeMemory función)</span><span class="sxs-lookup"><span data-stu-id="f3aad-103">ExpertFreeMemory function</span></span>

<span data-ttu-id="f3aad-104">La función **ExpertFreeMemory** libera la memoria adquirida por las llamadas a las funciones [**ExpertAllocMemory**](expertallocmemory.md) y [**ExpertReallocMemory**](expertreallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="f3aad-104">The **ExpertFreeMemory** function frees memory acquired by calls to the [**ExpertAllocMemory**](expertallocmemory.md) and [**ExpertReallocMemory**](expertreallocmemory.md) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3aad-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3aad-105">Syntax</span></span>


```C++
SIZE_T WINAPI ExpertFreeMemory(
       HEXPERTKEY hExpertKey,
  _In_ LPVOID     pMemory
);
```



## <a name="parameters"></a><span data-ttu-id="f3aad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3aad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3aad-107">*hExpertKey*</span><span class="sxs-lookup"><span data-stu-id="f3aad-107">*hExpertKey*</span></span> 
</dt> <dd>

<span data-ttu-id="f3aad-108">Identificador de experto único.</span><span class="sxs-lookup"><span data-stu-id="f3aad-108">Unique expert identifier.</span></span> <span data-ttu-id="f3aad-109">Monitor de red pasa *hExpertKey* al experto cuando llama a la función [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="f3aad-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f3aad-110">*pMemory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3aad-110">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3aad-111">Puntero a la memoria que Monitor de red asigna.</span><span class="sxs-lookup"><span data-stu-id="f3aad-111">Pointer to the memory that Network Monitor allocates.</span></span> <span data-ttu-id="f3aad-112">El puntero *pMemory* puede ser devuelto por una llamada anterior a [**ExpertAllocMemory**](expertallocmemory.md) o [**ExpertReallocMemory**](expertreallocmemory.md).</span><span class="sxs-lookup"><span data-stu-id="f3aad-112">The *pMemory* pointer can be returned by a previous call to [**ExpertAllocMemory**](expertallocmemory.md) or [**ExpertReallocMemory**](expertreallocmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3aad-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3aad-113">Return value</span></span>

<span data-ttu-id="f3aad-114">Si la función se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="f3aad-114">If the function is successful.</span></span> <span data-ttu-id="f3aad-115">el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="f3aad-115">the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f3aad-116">Si la función no se realiza correctamente, el valor devuelto indica la razón del error.</span><span class="sxs-lookup"><span data-stu-id="f3aad-116">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="f3aad-117">Si el valor devuelto es NMERR \_ Expert \_ Terminate, el experto limpia y devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f3aad-117">If the return value is NMERR\_EXPERT\_TERMINATE, the expert immediately cleans up and returns.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3aad-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3aad-118">Remarks</span></span>

<span data-ttu-id="f3aad-119">Es importante tener en cuenta que un experto debe usar las funciones de asignación de memoria Monitor de red para la administración de memoria.</span><span class="sxs-lookup"><span data-stu-id="f3aad-119">It is important to note that an expert should use the Network Monitor memory allocation functions for memory management.</span></span> <span data-ttu-id="f3aad-120">Si se produce un error en el experto durante el tiempo de ejecución, el uso de estas funciones permitirá a Monitor de red liberar la memoria que ha asignado.</span><span class="sxs-lookup"><span data-stu-id="f3aad-120">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3aad-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3aad-121">Requirements</span></span>



| <span data-ttu-id="f3aad-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3aad-122">Requirement</span></span> | <span data-ttu-id="f3aad-123">Value</span><span class="sxs-lookup"><span data-stu-id="f3aad-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f3aad-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3aad-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f3aad-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f3aad-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f3aad-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3aad-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f3aad-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f3aad-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f3aad-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3aad-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3aad-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3aad-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f3aad-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3aad-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f3aad-131"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3aad-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f3aad-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3aad-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3aad-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3aad-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




