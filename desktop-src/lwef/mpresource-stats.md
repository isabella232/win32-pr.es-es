---
title: MPRESOURCE_STATS estructura (MpClient. h)
description: Estadísticas relacionadas con recursos.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- MPRESOURCE_STATS estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPRESOURCE_STATS características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPRESOURCE_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afbe1ce6734aabd1093f7acd886af757c51ed83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491549"
---
# <a name="mpresource_stats-structure"></a><span data-ttu-id="9e64a-105">MPRESOURCE ( \_ estructura de estadísticas)</span><span class="sxs-lookup"><span data-stu-id="9e64a-105">MPRESOURCE\_STATS structure</span></span>

<span data-ttu-id="9e64a-106">Estadísticas relacionadas con recursos.</span><span class="sxs-lookup"><span data-stu-id="9e64a-106">Resource-related statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e64a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e64a-107">Syntax</span></span>


```C++
typedef struct tagMPRESOURCE_STATS {
  DWORD  PPMProgress;
  UINT64 ProcessCount;
  UINT64 FileCount;
  UINT64 FileBytesCount;
  UINT64 RegKeyCount;
  UINT64 Reserved[4];
} MPRESOURCE_STATS, *PMPRESOURCE_STATS;
```



## <a name="members"></a><span data-ttu-id="9e64a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9e64a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9e64a-109">**PPMProgress**</span><span class="sxs-lookup"><span data-stu-id="9e64a-109">**PPMProgress**</span></span>
</dt> <dd>

<span data-ttu-id="9e64a-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9e64a-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9e64a-111">Progreso aproximado para el examen en ppm (partes por millón).</span><span class="sxs-lookup"><span data-stu-id="9e64a-111">Approximate progress for scan in ppm (parts per million).</span></span> <span data-ttu-id="9e64a-112">Establezca en **MPPROGRESS \_ no válido** si la información de progreso no está disponible.</span><span class="sxs-lookup"><span data-stu-id="9e64a-112">Set to **MPPROGRESS\_INVALID** if progress information is not available.</span></span>

</dd> <dt>

<span data-ttu-id="9e64a-113">**ProcessCount**</span><span class="sxs-lookup"><span data-stu-id="9e64a-113">**ProcessCount**</span></span>
</dt> <dd>

<span data-ttu-id="9e64a-114">Tipo: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="9e64a-114">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="9e64a-115">Número de procesos examinados.</span><span class="sxs-lookup"><span data-stu-id="9e64a-115">Number of processes scanned.</span></span>

</dd> <dt>

<span data-ttu-id="9e64a-116">**FileCount**</span><span class="sxs-lookup"><span data-stu-id="9e64a-116">**FileCount**</span></span>
</dt> <dd>

<span data-ttu-id="9e64a-117">Tipo: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="9e64a-117">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="9e64a-118">Número de archivos examinados.</span><span class="sxs-lookup"><span data-stu-id="9e64a-118">Number of files scanned.</span></span>

</dd> <dt>

<span data-ttu-id="9e64a-119">**FileBytesCount**</span><span class="sxs-lookup"><span data-stu-id="9e64a-119">**FileBytesCount**</span></span>
</dt> <dd>

<span data-ttu-id="9e64a-120">Tipo: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="9e64a-120">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="9e64a-121">Número de bytes examinados para los archivos.</span><span class="sxs-lookup"><span data-stu-id="9e64a-121">Number of bytes scanned for files.</span></span>

</dd> <dt>

<span data-ttu-id="9e64a-122">**RegKeyCount**</span><span class="sxs-lookup"><span data-stu-id="9e64a-122">**RegKeyCount**</span></span>
</dt> <dd>

<span data-ttu-id="9e64a-123">Tipo: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="9e64a-123">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="9e64a-124">Número de RegKeys examinados.</span><span class="sxs-lookup"><span data-stu-id="9e64a-124">Number of RegKeys scanned.</span></span>

</dd> <dt>

<span data-ttu-id="9e64a-125">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="9e64a-125">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="9e64a-126">Tipo: **UINT64 \[ 4 \]**</span><span class="sxs-lookup"><span data-stu-id="9e64a-126">Type: **UINT64\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="9e64a-127">Campos reservados para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="9e64a-127">Fields reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e64a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e64a-128">Requirements</span></span>



| <span data-ttu-id="9e64a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e64a-129">Requirement</span></span> | <span data-ttu-id="9e64a-130">Value</span><span class="sxs-lookup"><span data-stu-id="9e64a-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e64a-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e64a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9e64a-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e64a-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9e64a-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e64a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9e64a-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e64a-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e64a-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e64a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e64a-136"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e64a-136"><dt>MpClient.h</dt></span></span> </dl> |



 

 





