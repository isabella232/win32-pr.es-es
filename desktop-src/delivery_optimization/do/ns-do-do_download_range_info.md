---
title: Estructura de DO_DOWNLOAD_RANGE_INFO
description: Identifica una matriz de intervalos de bytes que se van a descargar de un archivo.
keywords:
- Estructura de DO_DOWNLOAD_RANGE_INFO
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE_INFO
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 01628ea29895012f60552e696b7f68854f426f8d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104420041"
---
# <a name="do_download_range_info-structure"></a><span data-ttu-id="54c79-104">Estructura de DO_DOWNLOAD_RANGE_INFO</span><span class="sxs-lookup"><span data-stu-id="54c79-104">DO_DOWNLOAD_RANGE_INFO structure</span></span>

<span data-ttu-id="54c79-105">La estructura **DO_DOWNLOAD_RANGE_INFO** identifica una matriz de intervalos de bytes que se van a descargar de un archivo.</span><span class="sxs-lookup"><span data-stu-id="54c79-105">The **DO_DOWNLOAD_RANGE_INFO** structure identifies an array of ranges of bytes to download from a file.</span></span> <span data-ttu-id="54c79-106">Normalmente se pasa como argumento opcional a la función **IDODownload:: Start** .</span><span class="sxs-lookup"><span data-stu-id="54c79-106">It is typically passed as an optional argument to the **IDODownload::Start** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="54c79-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54c79-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a><span data-ttu-id="54c79-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="54c79-108">Members</span></span>

`RangeCount`

<span data-ttu-id="54c79-109">Número de elementos de intervalos.</span><span class="sxs-lookup"><span data-stu-id="54c79-109">Number of elements in Ranges.</span></span>

`Ranges`

<span data-ttu-id="54c79-110">Matriz de una o varias estructuras de **DO_DOWNLOAD_RANGE** que especifican los intervalos que se van a descargar.</span><span class="sxs-lookup"><span data-stu-id="54c79-110">Array of one or more **DO_DOWNLOAD_RANGE** structures that specify the ranges to download.</span></span>

## <a name="requirements"></a><span data-ttu-id="54c79-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54c79-111">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="54c79-112">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="54c79-112">**Minimum supported client**</span></span> | <span data-ttu-id="54c79-113">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="54c79-113">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="54c79-114">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="54c79-114">**Minimum supported server**</span></span> | <span data-ttu-id="54c79-115">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="54c79-115">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="54c79-116">**Header**</span><span class="sxs-lookup"><span data-stu-id="54c79-116">**Header**</span></span> | <span data-ttu-id="54c79-117">Do. h</span><span class="sxs-lookup"><span data-stu-id="54c79-117">Do.h</span></span> |
