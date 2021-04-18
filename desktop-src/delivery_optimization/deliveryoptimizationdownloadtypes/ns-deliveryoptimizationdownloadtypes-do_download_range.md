---
title: Estructura de DO_DOWNLOAD_RANGE
description: Identifica un intervalo único de bytes que se va a descargar de un archivo.
keywords:
- Estructura de DO_DOWNLOAD_RANGE
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0f328565c80350a05cbfb23f178ea3580586f326
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105720111"
---
# <a name="do_download_range-structure"></a><span data-ttu-id="228b1-104">Estructura de DO_DOWNLOAD_RANGE</span><span class="sxs-lookup"><span data-stu-id="228b1-104">DO_DOWNLOAD_RANGE structure</span></span>

<span data-ttu-id="228b1-105">La estructura **DO_DOWNLOAD_RANGE** identifica un intervalo único de bytes que se va a descargar de un archivo.</span><span class="sxs-lookup"><span data-stu-id="228b1-105">The **DO_DOWNLOAD_RANGE** structure identifies a single range of bytes to download from a file.</span></span> <span data-ttu-id="228b1-106">La estructura de **DO_DOWNLOAD_RANGE** se incluye en **DO_DOWNLOAD_RANGES_INFO** estructura para proporcionar una matriz de intervalos que descargar.</span><span class="sxs-lookup"><span data-stu-id="228b1-106">The **DO_DOWNLOAD_RANGE** structure is included within **DO_DOWNLOAD_RANGES_INFO** structure to provide an array of ranges to download.</span></span>

## <a name="syntax"></a><span data-ttu-id="228b1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="228b1-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a><span data-ttu-id="228b1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="228b1-108">Members</span></span>

`Offset`

<span data-ttu-id="228b1-109">Desplazamiento de base cero al principio del intervalo de bytes que se va a descargar de un archivo.</span><span class="sxs-lookup"><span data-stu-id="228b1-109">Zero-based offset to the beginning of the range of bytes to download from a file.</span></span>

`Length`

<span data-ttu-id="228b1-110">Longitud del intervalo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="228b1-110">The length of the range, in bytes.</span></span> <span data-ttu-id="228b1-111">No especifique una longitud de cero bytes.</span><span class="sxs-lookup"><span data-stu-id="228b1-111">Do not specify a zero-byte length.</span></span> <span data-ttu-id="228b1-112">Para indicar que el intervalo se extiende hasta el final del archivo, especifique **DO_LENGTH_TO_EOF**.</span><span class="sxs-lookup"><span data-stu-id="228b1-112">To indicate that the range extends to the end of the file, specify **DO_LENGTH_TO_EOF**.</span></span>

## <a name="requirements"></a><span data-ttu-id="228b1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="228b1-113">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="228b1-114">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="228b1-114">**Minimum supported client**</span></span> | <span data-ttu-id="228b1-115">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="228b1-115">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="228b1-116">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="228b1-116">**Minimum supported server**</span></span> | <span data-ttu-id="228b1-117">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="228b1-117">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="228b1-118">**Header**</span><span class="sxs-lookup"><span data-stu-id="228b1-118">**Header**</span></span> | <span data-ttu-id="228b1-119">DeliveryOptimizationDownloadTypes. h</span><span class="sxs-lookup"><span data-stu-id="228b1-119">DeliveryOptimizationDownloadTypes.h</span></span> |
