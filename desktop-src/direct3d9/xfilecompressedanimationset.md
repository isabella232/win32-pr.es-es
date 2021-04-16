---
description: Identifica los datos de animación de fotogramas clave comprimidos.
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: Estructura XFILECOMPRESSEDANIMATIONSET (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XFILECOMPRESSEDANIMATIONSET
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 240cac57c9c0d123203ee4599c14092df1327f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689868"
---
# <a name="xfilecompressedanimationset-structure"></a><span data-ttu-id="c1ebe-103">Estructura XFILECOMPRESSEDANIMATIONSET</span><span class="sxs-lookup"><span data-stu-id="c1ebe-103">XFILECOMPRESSEDANIMATIONSET structure</span></span>

<span data-ttu-id="c1ebe-104">Identifica los datos de animación de fotogramas clave comprimidos.</span><span class="sxs-lookup"><span data-stu-id="c1ebe-104">Identifies compressed key frame animation data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1ebe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1ebe-105">Syntax</span></span>


```C++
typedef struct XFILECOMPRESSEDANIMATIONSET {
  DWORD CompressedBlockSize;
  FLOAT TicksPerSec;
  DWORD PlaybackType;
  DWORD BufferLength;
} XFILECOMPRESSEDANIMATIONSET, *LPXFILECOMPRESSEDANIMATIONSET;
```



## <a name="members"></a><span data-ttu-id="c1ebe-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c1ebe-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1ebe-107">**CompressedBlockSize**</span><span class="sxs-lookup"><span data-stu-id="c1ebe-107">**CompressedBlockSize**</span></span>
</dt> <dd>

<span data-ttu-id="c1ebe-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1ebe-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1ebe-109">Tamaño total, en bytes, de los datos comprimidos en el búfer de datos de animación de fotogramas clave comprimidos.</span><span class="sxs-lookup"><span data-stu-id="c1ebe-109">Total size, in bytes, of the compressed data in the compressed key frame animation data buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c1ebe-110">**TicksPerSec**</span><span class="sxs-lookup"><span data-stu-id="c1ebe-110">**TicksPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="c1ebe-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1ebe-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1ebe-112">Número de TICs de fotogramas clave de animación que se producen por segundo.</span><span class="sxs-lookup"><span data-stu-id="c1ebe-112">Number of animation key frame ticks that occur per second.</span></span>

</dd> <dt>

<span data-ttu-id="c1ebe-113">**PlaybackType**</span><span class="sxs-lookup"><span data-stu-id="c1ebe-113">**PlaybackType**</span></span>
</dt> <dd>

<span data-ttu-id="c1ebe-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1ebe-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1ebe-115">Tipo del bucle de reproducción establecido de la animación.</span><span class="sxs-lookup"><span data-stu-id="c1ebe-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="c1ebe-116">Consulte [**\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="c1ebe-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1ebe-117">**BufferLength**</span><span class="sxs-lookup"><span data-stu-id="c1ebe-117">**BufferLength**</span></span>
</dt> <dd>

<span data-ttu-id="c1ebe-118">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1ebe-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1ebe-119">Tamaño mínimo del búfer, en bytes, necesario para contener datos de animación de fotogramas clave comprimidos.</span><span class="sxs-lookup"><span data-stu-id="c1ebe-119">Minimum buffer size, in bytes, required to hold compressed key frame animation data.</span></span> <span data-ttu-id="c1ebe-120">El valor es igual a ((CompressedBlockSize + 3)/4).</span><span class="sxs-lookup"><span data-stu-id="c1ebe-120">Value is equal to ( ( CompressedBlockSize + 3 ) / 4 ).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1ebe-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1ebe-121">Requirements</span></span>



| <span data-ttu-id="c1ebe-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1ebe-122">Requirement</span></span> | <span data-ttu-id="c1ebe-123">Value</span><span class="sxs-lookup"><span data-stu-id="c1ebe-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1ebe-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1ebe-124">Header</span></span><br/> | <dl> <span data-ttu-id="c1ebe-125"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1ebe-125"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1ebe-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1ebe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1ebe-127">Estructuras de archivos de D3DX X</span><span class="sxs-lookup"><span data-stu-id="c1ebe-127">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="c1ebe-128">**ID3DXCompressedAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="c1ebe-128">**ID3DXCompressedAnimationSet**</span></span>](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
