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
ms.openlocfilehash: ad36eb8fe691330b471db0b7e8b5378f3e7614db
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955058"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a><span data-ttu-id="b8c5a-103">DWRITE_BITMAP_DATA_BGRA32 estructura (dwrite_3.h)</span><span class="sxs-lookup"><span data-stu-id="b8c5a-103">DWRITE_BITMAP_DATA_BGRA32 structure (dwrite_3.h)</span></span>

<span data-ttu-id="b8c5a-104">Representa los datos de mapa de bits en formato BGRA32.</span><span class="sxs-lookup"><span data-stu-id="b8c5a-104">Represents bitmap data in BGRA32 format.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8c5a-105">Esta API está disponible como parte de la implementación de DWriteCore [de DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="b8c5a-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="b8c5a-106">DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="b8c5a-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="b8c5a-107">Para obtener más información y ejemplos de código, vea [Introducción a DWriteCore.](/windows/win32/directwrite/dwritecore-overview)</span><span class="sxs-lookup"><span data-stu-id="b8c5a-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8c5a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8c5a-108">Syntax</span></span>

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a><span data-ttu-id="b8c5a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b8c5a-109">Members</span></span>

`width`

<span data-ttu-id="b8c5a-110">Tipo: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8c5a-110">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8c5a-111">Ancho, en píxeles, del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="b8c5a-111">The width, in pixels, of the bitmap.</span></span>


`height`

<span data-ttu-id="b8c5a-112">Tipo: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8c5a-112">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8c5a-113">Alto, en píxeles, del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="b8c5a-113">The height, in pixels, of the bitmap.</span></span>


`pixels`

<span data-ttu-id="b8c5a-114">Tipo: \_ Tamaño del campo \_ \_ (ancho \* alto)**[UINT32](../../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8c5a-114">Type: \_Field\_size\_(width \* height)**[UINT32](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b8c5a-115">Puntero a la ubicación de los valores de bits del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="b8c5a-115">A pointer to the location of the bit values for the bitmap.</span></span>


## <a name="examples"></a><span data-ttu-id="b8c5a-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b8c5a-116">Examples</span></span>

<span data-ttu-id="b8c5a-117">Consulte el tema [de información general de DWriteCore](/windows/win32/directwrite/dwritecore-overview) y la aplicación de ejemplo [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="b8c5a-117">See the [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8c5a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8c5a-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b8c5a-119">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="b8c5a-119">**Minimum supported client**</span></span> | <span data-ttu-id="b8c5a-120">Windows 10, Project Project Project [Aplicaciones Win32]</span><span class="sxs-lookup"><span data-stu-id="b8c5a-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="b8c5a-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="b8c5a-121">**Header**</span></span> | <span data-ttu-id="b8c5a-122">dwrite_3.h (incluir dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="b8c5a-122">dwrite_3.h (include dwrite_core.h)</span></span> |