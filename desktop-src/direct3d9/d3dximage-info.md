---
description: 'D3DXIMAGE_INFO estructura: devuelve una descripción del contenido original de un archivo de imagen.'
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: D3DXIMAGE_INFO estructura (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_INFO
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: be70cc88645e0aac6734907c6a97f2d4bb104c99
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090543"
---
# <a name="d3dximage_info-structure"></a><span data-ttu-id="ebc2c-103">D3DXIMAGE \_ INFO (estructura)</span><span class="sxs-lookup"><span data-stu-id="ebc2c-103">D3DXIMAGE\_INFO structure</span></span>

<span data-ttu-id="ebc2c-104">Devuelve una descripción del contenido original de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebc2c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ebc2c-105">Syntax</span></span>


```C++
typedef struct D3DXIMAGE_INFO {
  UINT                 Width;
  UINT                 Height;
  UINT                 Depth;
  UINT                 MipLevels;
  D3DFORMAT            Format;
  D3DRESOURCETYPE      ResourceType;
  D3DXIMAGE_FILEFORMAT ImageFileFormat;
} D3DXIMAGE_INFO, *LPD3DXIMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="ebc2c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ebc2c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ebc2c-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="ebc2c-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="ebc2c-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ebc2c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ebc2c-109">Ancho de la imagen original en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ebc2c-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="ebc2c-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="ebc2c-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ebc2c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ebc2c-112">Alto de la imagen original en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ebc2c-113">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="ebc2c-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="ebc2c-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ebc2c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ebc2c-115">Profundidad de la imagen original en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ebc2c-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="ebc2c-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="ebc2c-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ebc2c-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ebc2c-118">Número de niveles de mip en la imagen original.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-118">Number of mip levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="ebc2c-119">**Format**</span><span class="sxs-lookup"><span data-stu-id="ebc2c-119">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="ebc2c-120">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ebc2c-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ebc2c-121">Valor del tipo [enumerado D3DFORMAT](d3dformat.md) que describe más de cerca los datos de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-121">A value from the [D3DFORMAT](d3dformat.md) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="ebc2c-122">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="ebc2c-122">**ResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="ebc2c-123">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="ebc2c-123">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ebc2c-124">Representa el tipo de la textura almacenada en el archivo.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-124">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="ebc2c-125">Es D3DRTYPE \_ TEXTURE, D3DRTYPE \_ VOLUMETEXTURE o D3DRTYPE \_ CubeTexture.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-125">It is either D3DRTYPE\_TEXTURE, D3DRTYPE\_VOLUMETEXTURE, or D3DRTYPE\_CubeTexture.</span></span>

</dd> <dt>

<span data-ttu-id="ebc2c-126">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="ebc2c-126">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ebc2c-127">Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ebc2c-127">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ebc2c-128">Representa el formato del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-128">Represents the format of the image file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ebc2c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebc2c-129">Requirements</span></span>



| <span data-ttu-id="ebc2c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebc2c-130">Requirement</span></span> | <span data-ttu-id="ebc2c-131">Value</span><span class="sxs-lookup"><span data-stu-id="ebc2c-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc2c-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebc2c-132">Header</span></span><br/> | <dl> <span data-ttu-id="ebc2c-133"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="ebc2c-133"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebc2c-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ebc2c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebc2c-135">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="ebc2c-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
