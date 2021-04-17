---
description: Estadísticas de recursos recopiladas por el ResourceManager de D3DDEVINFO \_ cuando se usa el mecanismo de consulta asincrónica.
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: Estructura D3DRESOURCESTATS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCESTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f6f549011b9750f69187c0e0cbf34ec94764c9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717632"
---
# <a name="d3dresourcestats-structure"></a><span data-ttu-id="b21b3-103">Estructura D3DRESOURCESTATS</span><span class="sxs-lookup"><span data-stu-id="b21b3-103">D3DRESOURCESTATS structure</span></span>

<span data-ttu-id="b21b3-104">Estadísticas de recursos recopiladas por el [**\_ ResourceManager de D3DDEVINFO**](d3ddevinfo-resourcemanager.md) cuando se usa el mecanismo de consulta asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b21b3-104">Resource statistics gathered by the [**D3DDEVINFO\_ResourceManager**](d3ddevinfo-resourcemanager.md) when using the asynchronous query mechanism.</span></span>

## <a name="syntax"></a><span data-ttu-id="b21b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b21b3-105">Syntax</span></span>


```C++
typedef struct D3DRESOURCESTATS {
  BOOL  bThrashing;
  DWORD ApproxBytesDownloaded;
  DWORD NumEvicts;
  DWORD NumVidCreates;
  DWORD LastPri;
  DWORD NumUsed;
  DWORD NumUsedInVidMem;
  DWORD WorkingSet;
  DWORD WorkingSetBytes;
  DWORD TotalManaged;
  DWORD TotalBytes;
} D3DRESOURCESTATS, *LPD3DRESOURCESTATS;
```



## <a name="members"></a><span data-ttu-id="b21b3-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b21b3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b21b3-107">**bThrashing**</span><span class="sxs-lookup"><span data-stu-id="b21b3-107">**bThrashing**</span></span>
</dt> <dd>

<span data-ttu-id="b21b3-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b21b3-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b21b3-109">Indica si se está produciendo la paginación.</span><span class="sxs-lookup"><span data-stu-id="b21b3-109">Indicates if thrashing is occurring.</span></span>

</dd> <dt>

<span data-ttu-id="b21b3-110">**ApproxBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="b21b3-110">**ApproxBytesDownloaded**</span></span>
</dt> <dd>

<span data-ttu-id="b21b3-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b21b3-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b21b3-112">Número aproximado de bytes descargados por el administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="b21b3-112">Approximate number of bytes downloaded by the resource manager.</span></span>

</dd> <dt>

<span data-ttu-id="b21b3-113">**NumEvicts**</span><span class="sxs-lookup"><span data-stu-id="b21b3-113">**NumEvicts**</span></span>
</dt> <dd>

<span data-ttu-id="b21b3-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b21b3-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b21b3-115">Número de objetos expulsados.</span><span class="sxs-lookup"><span data-stu-id="b21b3-115">Number of objects evicted.</span></span>

</dd> <dt>

<span data-ttu-id="b21b3-116">**NumVidCreates**</span><span class="sxs-lookup"><span data-stu-id="b21b3-116">**NumVidCreates**</span></span>
</dt> <dd>

<span data-ttu-id="b21b3-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b21b3-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b21b3-118">Número de objetos creados en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b21b3-118">Number of objects created in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="b21b3-119">**LastPri**</span><span class="sxs-lookup"><span data-stu-id="b21b3-119">**LastPri**</span></span>
</dt> <dd>

<span data-ttu-id="b21b3-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b21b3-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b21b3-121">Prioridad del último objeto expulsado.</span><span class="sxs-lookup"><span data-stu-id="b21b3-121">Priority of last object evicted.</span></span>

</dd> <dt>

<span data-ttu-id="b21b3-122">**NumUsed**</span><span class="sxs-lookup"><span data-stu-id="b21b3-122">**NumUsed**</span></span>
</dt> <dd>

<span data-ttu-id="b21b3-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b21b3-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b21b3-124">Número de objetos establecidos en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b21b3-124">Number of objects set to the device.</span></span>

</dd> <dt>

<span data-ttu-id="b21b3-125">**NumUsedInVidMem**</span><span class="sxs-lookup"><span data-stu-id="b21b3-125">**NumUsedInVidMem**</span></span>
</dt> <dd>

<span data-ttu-id="b21b3-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b21b3-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b21b3-127">Número de objetos establecidos en el dispositivo, que ya están en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b21b3-127">Number of objects set to the device, which are already in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="b21b3-128">**WorkingSet**</span><span class="sxs-lookup"><span data-stu-id="b21b3-128">**WorkingSet**</span></span>
</dt> <dd>

<span data-ttu-id="b21b3-129">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b21b3-129">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b21b3-130">Número de objetos en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b21b3-130">Number of objects in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="b21b3-131">**WorkingSetBytes**</span><span class="sxs-lookup"><span data-stu-id="b21b3-131">**WorkingSetBytes**</span></span>
</dt> <dd>

<span data-ttu-id="b21b3-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b21b3-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b21b3-133">Número de bytes en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b21b3-133">Number of bytes in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="b21b3-134">**TotalManaged**</span><span class="sxs-lookup"><span data-stu-id="b21b3-134">**TotalManaged**</span></span>
</dt> <dd>

<span data-ttu-id="b21b3-135">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b21b3-135">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b21b3-136">Número total de objetos administrados.</span><span class="sxs-lookup"><span data-stu-id="b21b3-136">Total number of managed objects.</span></span>

</dd> <dt>

<span data-ttu-id="b21b3-137">**TotalBytes**</span><span class="sxs-lookup"><span data-stu-id="b21b3-137">**TotalBytes**</span></span>
</dt> <dd>

<span data-ttu-id="b21b3-138">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b21b3-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b21b3-139">Número total de bytes de objetos administrados.</span><span class="sxs-lookup"><span data-stu-id="b21b3-139">Total number of bytes of managed objects.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b21b3-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b21b3-140">Requirements</span></span>



| <span data-ttu-id="b21b3-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b21b3-141">Requirement</span></span> | <span data-ttu-id="b21b3-142">Value</span><span class="sxs-lookup"><span data-stu-id="b21b3-142">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b21b3-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b21b3-143">Header</span></span><br/> | <dl> <span data-ttu-id="b21b3-144"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b21b3-144"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b21b3-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="b21b3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b21b3-146">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="b21b3-146">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="b21b3-147">Notificación asincrónica (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b21b3-147">Asynchronous Notification (Direct3D 9)</span></span>](asynchronous-notification.md)
</dt> </dl>

 

 
