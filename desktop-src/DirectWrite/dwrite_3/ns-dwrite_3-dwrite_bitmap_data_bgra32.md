---
UID: NS:dwrite_3.DWRITE_BITMAP_DATA_BGRA32
title: DWRITE_BITMAP_DATA_BGRA32 (dwrite_3.h)
description: Representa los datos de mapa de bits en formato BGRA32.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_BITMAP_DATA_BGRA32
- dwrite_3/DWRITE_BITMAP_DATA_BGRA32
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_3.h
api_name:
- DWRITE_BITMAP_DATA_BGRA32
ms.openlocfilehash: 813f3601cac03dcf477fa40f6db5105e075029ab
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548930"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a><span data-ttu-id="345f5-103">DWRITE_BITMAP_DATA_BGRA32 estructura (dwrite_3.h)</span><span class="sxs-lookup"><span data-stu-id="345f5-103">DWRITE_BITMAP_DATA_BGRA32 structure (dwrite_3.h)</span></span>

<span data-ttu-id="345f5-104">Representa los datos de mapa de bits en formato BGRA32.</span><span class="sxs-lookup"><span data-stu-id="345f5-104">Represents bitmap data in BGRA32 format.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="345f5-105">Esta API está disponible como parte de la implementación de DWriteCore de [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="345f5-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="345f5-106">DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="345f5-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="345f5-107">Para obtener más información y ejemplos de código, vea [Introducción a DWriteCore.](../dwritecore-overview.md)</span><span class="sxs-lookup"><span data-stu-id="345f5-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="345f5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="345f5-108">Syntax</span></span>

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a><span data-ttu-id="345f5-109">Members</span><span class="sxs-lookup"><span data-stu-id="345f5-109">Members</span></span>

`width`

<span data-ttu-id="345f5-110">Tipo: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="345f5-110">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="345f5-111">Ancho, en píxeles, del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="345f5-111">The width, in pixels, of the bitmap.</span></span>


`height`

<span data-ttu-id="345f5-112">Tipo: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="345f5-112">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="345f5-113">Alto, en píxeles, del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="345f5-113">The height, in pixels, of the bitmap.</span></span>


`pixels`

<span data-ttu-id="345f5-114">Tipo: \_ Tamaño del campo \_ \_ (ancho \* alto)**[UINT32](../../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="345f5-114">Type: \_Field\_size\_(width \* height)**[UINT32](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="345f5-115">Puntero a la ubicación de los valores de bits del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="345f5-115">A pointer to the location of the bit values for the bitmap.</span></span>


## <a name="examples"></a><span data-ttu-id="345f5-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="345f5-116">Examples</span></span>

<span data-ttu-id="345f5-117">Consulte el [tema de información general de DWriteCore](../dwritecore-overview.md) y la aplicación de ejemplo [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="345f5-117">See the [DWriteCore overview](../dwritecore-overview.md) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="345f5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="345f5-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="345f5-119">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="345f5-119">**Minimum supported client**</span></span> | <span data-ttu-id="345f5-120">Windows 10, Project Project Project [Aplicaciones Win32]</span><span class="sxs-lookup"><span data-stu-id="345f5-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="345f5-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="345f5-121">**Header**</span></span> | <span data-ttu-id="345f5-122">dwrite_3.h (incluir dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="345f5-122">dwrite_3.h (include dwrite_core.h)</span></span> |