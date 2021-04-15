---
description: Porcentaje de tiempo de procesamiento de datos en el controlador. Estas estadísticas pueden ayudar a identificar los casos en los que el controlador está esperando otros recursos.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: D3DDEVINFO_D3D9INTERFACETIMINGS estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9INTERFACETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dfd6303f3682e29090db41fa83b38fc67f99121e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649403"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a><span data-ttu-id="f51cf-104">D3DDEVINFO \_ estructura D3D9INTERFACETIMINGS</span><span class="sxs-lookup"><span data-stu-id="f51cf-104">D3DDEVINFO\_D3D9INTERFACETIMINGS structure</span></span>

<span data-ttu-id="f51cf-105">Porcentaje de tiempo de procesamiento de datos en el controlador.</span><span class="sxs-lookup"><span data-stu-id="f51cf-105">Percent of time processing data in the driver.</span></span> <span data-ttu-id="f51cf-106">Estas estadísticas pueden ayudar a identificar los casos en los que el controlador está esperando otros recursos.</span><span class="sxs-lookup"><span data-stu-id="f51cf-106">These statistics may help identify cases when the driver is waiting for other resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="f51cf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f51cf-107">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9INTERFACETIMINGS {
  FLOAT WaitingForGPUToUseApplicationResourceTimePercent;
  FLOAT WaitingForGPUToAcceptMoreCommandsTimePercent;
  FLOAT WaitingForGPUToStayWithinLatencyTimePercent;
  FLOAT WaitingForGPUExclusiveResourceTimePercent;
  FLOAT WaitingForGPUOtherTimePercent;
} D3DDEVINFO_D3D9INTERFACETIMINGS, *LPD3DDEVINFO_D3D9INTERFACETIMINGS;
```



## <a name="members"></a><span data-ttu-id="f51cf-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f51cf-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f51cf-109">**WaitingForGPUToUseApplicationResourceTimePercent**</span><span class="sxs-lookup"><span data-stu-id="f51cf-109">**WaitingForGPUToUseApplicationResourceTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="f51cf-110">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f51cf-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f51cf-111">Porcentaje de tiempo que el controlador invierte en esperar a que la GPU termine de usar un recurso bloqueado (no se especificó [D3DLOCK \_ DONOTWAIT](d3dlock.md) ).</span><span class="sxs-lookup"><span data-stu-id="f51cf-111">Percentage of time the driver spent waiting for the GPU to finish using a locked resource (and [D3DLOCK\_DONOTWAIT](d3dlock.md) wasn't specified).</span></span>

</dd> <dt>

<span data-ttu-id="f51cf-112">**WaitingForGPUToAcceptMoreCommandsTimePercent**</span><span class="sxs-lookup"><span data-stu-id="f51cf-112">**WaitingForGPUToAcceptMoreCommandsTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="f51cf-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f51cf-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f51cf-114">Porcentaje de tiempo que el controlador invierte en esperar a que la GPU termine de procesar algunos comandos antes de que el controlador pudiera enviar más.</span><span class="sxs-lookup"><span data-stu-id="f51cf-114">Percentage of time the driver spent waiting for the GPU to finish processing some commands before the driver could send more.</span></span> <span data-ttu-id="f51cf-115">Esto indica que el controlador se ha quedado sin espacio para enviar comandos a la GPU.</span><span class="sxs-lookup"><span data-stu-id="f51cf-115">This indicates the driver has run out of room to send commands to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="f51cf-116">**WaitingForGPUToStayWithinLatencyTimePercent**</span><span class="sxs-lookup"><span data-stu-id="f51cf-116">**WaitingForGPUToStayWithinLatencyTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="f51cf-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f51cf-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f51cf-118">Porcentaje de tiempo que el controlador invierte en esperar a que la latencia de la GPU se reduzca a menos de tres fotogramas de representación.</span><span class="sxs-lookup"><span data-stu-id="f51cf-118">Percentage of time the driver spent waiting for the GPU latency to reduce to less than three rendering frames.</span></span>

<span data-ttu-id="f51cf-119">Si una aplicación está limitada por GPU, el controlador debe detenerla hasta que la GPU se encuentre dentro de tres fotogramas.</span><span class="sxs-lookup"><span data-stu-id="f51cf-119">If an application is GPU-limited, the driver must stall the CPU until the GPU gets within three frames.</span></span> <span data-ttu-id="f51cf-120">Esto evita que una aplicación se incluya en la cola de llamadas de representación de muchos segundos, lo que puede aumentar drásticamente la latencia entre el momento en que el usuario introduce datos nuevos y el momento en que el usuario ve los resultados de dicha entrada.</span><span class="sxs-lookup"><span data-stu-id="f51cf-120">This prevents an application from queuing up many seconds' worth of rendering calls which may dramatically increase the latency between when the user inputs new data and when the user sees the results of that input.</span></span> <span data-ttu-id="f51cf-121">En general, el controlador puede realizar un seguimiento del número [**de veces que**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) se llama a para evitar poner en cola más de tres fotogramas de trabajo de representación.</span><span class="sxs-lookup"><span data-stu-id="f51cf-121">In general, the driver can track the number of times [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) is called to prevent queuing up more than three frames of rendering work.</span></span>

</dd> <dt>

<span data-ttu-id="f51cf-122">**WaitingForGPUExclusiveResourceTimePercent**</span><span class="sxs-lookup"><span data-stu-id="f51cf-122">**WaitingForGPUExclusiveResourceTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="f51cf-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f51cf-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f51cf-124">Porcentaje de tiempo que el controlador invierte en esperar un recurso que no se puede canalizar (se opera en paralelo).</span><span class="sxs-lookup"><span data-stu-id="f51cf-124">Percentage of time the driver spent waiting for a resource that cannot be pipelined (that is operated in parallel).</span></span> <span data-ttu-id="f51cf-125">Una aplicación puede querer evitar el uso de un recurso no canalizado por razones de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f51cf-125">An application may want to avoid using a non-pipelined resource for performance reasons.</span></span>

</dd> <dt>

<span data-ttu-id="f51cf-126">**WaitingForGPUOtherTimePercent**</span><span class="sxs-lookup"><span data-stu-id="f51cf-126">**WaitingForGPUOtherTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="f51cf-127">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f51cf-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f51cf-128">Porcentaje de tiempo que el controlador invierte en esperar a otro procesamiento de GPU.</span><span class="sxs-lookup"><span data-stu-id="f51cf-128">Percentage of time the driver spent waiting for other GPU processing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f51cf-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f51cf-129">Remarks</span></span>

<span data-ttu-id="f51cf-130">Estas métricas ayudan a identificar cuándo un controlador está esperando y qué está esperando.</span><span class="sxs-lookup"><span data-stu-id="f51cf-130">These metrics help identify when a driver is waiting and what it is waiting for.</span></span> <span data-ttu-id="f51cf-131">Los porcentajes altos no son necesariamente un problema.</span><span class="sxs-lookup"><span data-stu-id="f51cf-131">High percentages are not necessarily a problem.</span></span>

<span data-ttu-id="f51cf-132">Estas métricas globales del sistema pueden implementarse o no.</span><span class="sxs-lookup"><span data-stu-id="f51cf-132">These system-global metrics may or may not be implemented.</span></span> <span data-ttu-id="f51cf-133">En función del hardware específico, es posible que estas métricas no admitan varias consultas simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="f51cf-133">Depending on the specific hardware, these metrics may not support multiple queries simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="f51cf-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f51cf-134">Requirements</span></span>



| <span data-ttu-id="f51cf-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f51cf-135">Requirement</span></span> | <span data-ttu-id="f51cf-136">Value</span><span class="sxs-lookup"><span data-stu-id="f51cf-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f51cf-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f51cf-137">Header</span></span><br/> | <dl> <span data-ttu-id="f51cf-138"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f51cf-138"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f51cf-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="f51cf-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f51cf-140">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="f51cf-140">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="f51cf-141">**GetData**</span><span class="sxs-lookup"><span data-stu-id="f51cf-141">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
