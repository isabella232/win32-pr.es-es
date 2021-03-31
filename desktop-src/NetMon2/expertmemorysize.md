---
description: La función ExpertMemorySize devuelve la cantidad de memoria asignada por la función ExpertAllocMemory.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: Función ExpertMemorySize (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertMemorySize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57c83bc3e9535550086c9732b33a71a357e4da42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907675"
---
# <a name="expertmemorysize-function"></a><span data-ttu-id="0796a-103">ExpertMemorySize función)</span><span class="sxs-lookup"><span data-stu-id="0796a-103">ExpertMemorySize function</span></span>

<span data-ttu-id="0796a-104">La función **ExpertMemorySize** devuelve la cantidad de memoria asignada por la función [ExpertAllocMemory](expertallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="0796a-104">The **ExpertMemorySize** function returns the amount of memory allocated by the [ExpertAllocMemory](expertallocmemory.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="0796a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0796a-105">Syntax</span></span>


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a><span data-ttu-id="0796a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0796a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0796a-107">*hExpertKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0796a-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0796a-108">Identificador de experto único.</span><span class="sxs-lookup"><span data-stu-id="0796a-108">Unique expert identifier.</span></span> <span data-ttu-id="0796a-109">Monitor de red pasa *hExpertKey* al experto cuando llama a la función [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="0796a-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="0796a-110">*pOriginalMemory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0796a-110">*pOriginalMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0796a-111">Puntero a la dirección de memoria del experto asignado por [ExpertAllocMemory](expertallocmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0796a-111">Pointer to the memory address of the expert allocated by [ExpertAllocMemory](expertallocmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0796a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0796a-112">Return value</span></span>

<span data-ttu-id="0796a-113">La función devuelve la cantidad de memoria asignada en bytes.</span><span class="sxs-lookup"><span data-stu-id="0796a-113">The function returns the amount of allocated memory   in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="0796a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0796a-114">Remarks</span></span>

<span data-ttu-id="0796a-115">Para obtener información sobre el tipo de datos de **tamaño \_ T** que devuelve **ExpertMemorySize** , vea tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="0796a-115">For information on the **SIZE\_T** data type that **ExpertMemorySize** returns, see Data Types.</span></span>

## <a name="requirements"></a><span data-ttu-id="0796a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0796a-116">Requirements</span></span>



| <span data-ttu-id="0796a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0796a-117">Requirement</span></span> | <span data-ttu-id="0796a-118">Value</span><span class="sxs-lookup"><span data-stu-id="0796a-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0796a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0796a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0796a-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0796a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0796a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0796a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0796a-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0796a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0796a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0796a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0796a-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0796a-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0796a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0796a-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="0796a-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0796a-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0796a-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0796a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0796a-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0796a-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




