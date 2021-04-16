---
description: Devolución de llamada que notifica al host de las fases de canalización de la información de malla devuelta por la solicitud asociada.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback:: MeshDataVertCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E75EDE35-AC8E-4452-B79B-860C39B156F0
api_name:
- IPipeLineStagesCallback.MeshDataVertCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3c878851b0c3cfe32128d766f4dcb35a7437579d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537192"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span data-ttu-id="07e3a-103"><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>IPipeLineStagesCallback:: MeshDataVertCallback (método)</span><span class="sxs-lookup"><span data-stu-id="07e3a-103"><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>IPipeLineStagesCallback::MeshDataVertCallback method</span></span>

<span data-ttu-id="07e3a-104">Devolución de llamada que notifica al host de las fases de canalización de la información de malla devuelta por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="07e3a-104">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="07e3a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07e3a-105">Syntax</span></span>


```C++
HRESULT MeshDataVertCallback(
   UINT                         numVertices,
   UINT                         numBufferLayoutEntries,
   MeshDataBufferLayoutEntry [] count1_entries,
   UINT                         stride,
   UINT                         numVBBytes,
   BYTE []                      count4_pVBData,
   UINT                         numIBBytes,
   BYTE []                      count6_pIBData,
   UINT                         indexSize,
   UINT                         IBOffset,
   UINT                         baseVertex,
   UINT                         minVertex,
   BOOL                         IBIndexesVB,
   UINT                         numIndices,
   UINT                         topology
);
```

## <a name="parameters"></a><span data-ttu-id="07e3a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07e3a-106">Parameters</span></span>

<span data-ttu-id="07e3a-107">*numVertices* </span><span class="sxs-lookup"><span data-stu-id="07e3a-107">*numVertices* </span></span>  
<span data-ttu-id="07e3a-108">El número de vértices de los resultados.</span><span class="sxs-lookup"><span data-stu-id="07e3a-108">The number of vertices in the results.</span></span>

<span data-ttu-id="07e3a-109">*numBufferLayoutEntries* </span><span class="sxs-lookup"><span data-stu-id="07e3a-109">*numBufferLayoutEntries* </span></span>  
<span data-ttu-id="07e3a-110">El número de entradas de diseño de búfer en los resultados.</span><span class="sxs-lookup"><span data-stu-id="07e3a-110">The number of buffer layout entries in the results.</span></span>

<span data-ttu-id="07e3a-111">*entradas de count1 \_* </span><span class="sxs-lookup"><span data-stu-id="07e3a-111">*count1\_entries* </span></span>  
<span data-ttu-id="07e3a-112">El diseño del búfer es completo.</span><span class="sxs-lookup"><span data-stu-id="07e3a-112">The buffer layout entires.</span></span> <span data-ttu-id="07e3a-113">Estos describen la firma de salida del sombreador.</span><span class="sxs-lookup"><span data-stu-id="07e3a-113">These describe the shader output signature.</span></span>

<span data-ttu-id="07e3a-114">*STRI* </span><span class="sxs-lookup"><span data-stu-id="07e3a-114">*stride* </span></span>  
<span data-ttu-id="07e3a-115">Tamaño (STRIDE) de un fragmento de salida completo.</span><span class="sxs-lookup"><span data-stu-id="07e3a-115">The size (stride) of an entire output chunk.</span></span>

<span data-ttu-id="07e3a-116">*numVBBytes* </span><span class="sxs-lookup"><span data-stu-id="07e3a-116">*numVBBytes* </span></span>  
<span data-ttu-id="07e3a-117">Tamaño del búfer de vértices en bytes.</span><span class="sxs-lookup"><span data-stu-id="07e3a-117">The size of the vertex buffer in bytes.</span></span>

<span data-ttu-id="07e3a-118">*count4 \_ pVBData* </span><span class="sxs-lookup"><span data-stu-id="07e3a-118">*count4\_pVBData* </span></span>  
<span data-ttu-id="07e3a-119">Búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="07e3a-119">The vertex buffer.</span></span>

<span data-ttu-id="07e3a-120">*numIBBytes* </span><span class="sxs-lookup"><span data-stu-id="07e3a-120">*numIBBytes* </span></span>  
<span data-ttu-id="07e3a-121">Tamaño del búfer de índice en bytes.</span><span class="sxs-lookup"><span data-stu-id="07e3a-121">The size of the index buffer in bytes.</span></span>

<span data-ttu-id="07e3a-122">*count6 \_ pIBData* </span><span class="sxs-lookup"><span data-stu-id="07e3a-122">*count6\_pIBData* </span></span>  
<span data-ttu-id="07e3a-123">Búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="07e3a-123">The index buffer.</span></span>

<span data-ttu-id="07e3a-124">*indexSize* </span><span class="sxs-lookup"><span data-stu-id="07e3a-124">*indexSize* </span></span>  
<span data-ttu-id="07e3a-125">Tamaño de cada índice en bytes.</span><span class="sxs-lookup"><span data-stu-id="07e3a-125">The size of each index in bytes.</span></span>

<span data-ttu-id="07e3a-126">*IBOffset* </span><span class="sxs-lookup"><span data-stu-id="07e3a-126">*IBOffset* </span></span>  
<span data-ttu-id="07e3a-127">Desplazamiento en el búfer de índice que especifica dónde se deben empezar a usar los índices.</span><span class="sxs-lookup"><span data-stu-id="07e3a-127">An offset into the index buffer that specifies where indices should start being used.</span></span>

<span data-ttu-id="07e3a-128">*baseVertex* </span><span class="sxs-lookup"><span data-stu-id="07e3a-128">*baseVertex* </span></span>  
<span data-ttu-id="07e3a-129">Desplazamiento en el búfer de vértice que especifica dónde se deben empezar a usar los vértices.</span><span class="sxs-lookup"><span data-stu-id="07e3a-129">An offset into the vertex buffer that specifies where vertices should start being used.</span></span>

<span data-ttu-id="07e3a-130">*minVertex*</span><span class="sxs-lookup"><span data-stu-id="07e3a-130">*minVertex*</span></span>   

<span data-ttu-id="07e3a-131">*IBIndexesVB* </span><span class="sxs-lookup"><span data-stu-id="07e3a-131">*IBIndexesVB* </span></span>  
<span data-ttu-id="07e3a-132">True cuando se utiliza el búfer de índice; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="07e3a-132">true when the index buffer is used; otherwise false.</span></span>

<span data-ttu-id="07e3a-133">*numIndices* </span><span class="sxs-lookup"><span data-stu-id="07e3a-133">*numIndices* </span></span>  
<span data-ttu-id="07e3a-134">Número de índices usados.</span><span class="sxs-lookup"><span data-stu-id="07e3a-134">The number of indices used.</span></span>

<span data-ttu-id="07e3a-135">*topología* </span><span class="sxs-lookup"><span data-stu-id="07e3a-135">*topology* </span></span>  
<span data-ttu-id="07e3a-136">Topolology del sombreador.</span><span class="sxs-lookup"><span data-stu-id="07e3a-136">The topolology of the shader.</span></span> <span data-ttu-id="07e3a-137">Esto no es necesariamente el mismo que la topología de la llamada a Draw asociada.</span><span class="sxs-lookup"><span data-stu-id="07e3a-137">This is not necessarily the same as the topology of the associated draw call.</span></span>

## <a name="return-value"></a><span data-ttu-id="07e3a-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07e3a-138">Return value</span></span>

<span data-ttu-id="07e3a-139">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="07e3a-139">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="07e3a-140">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07e3a-140">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="07e3a-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07e3a-141">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="07e3a-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07e3a-142">Header</span></span></p></td><td><span data-ttu-id="07e3a-143">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="07e3a-143">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="07e3a-144"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="07e3a-144"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="07e3a-145">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="07e3a-145">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
