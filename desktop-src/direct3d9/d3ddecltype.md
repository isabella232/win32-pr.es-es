---
description: Define un tipo de datos de declaración de vértices.
ms.assetid: 993fc7e4-4752-4bce-82d0-0a034fdc69c0
title: Enumeración D3DDECLTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3edb3f936772a7265c627f10eeb7aeb4f461701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362475"
---
# <a name="d3ddecltype-enumeration"></a><span data-ttu-id="8e6ef-103">Enumeración D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="8e6ef-103">D3DDECLTYPE enumeration</span></span>

<span data-ttu-id="8e6ef-104">Define un tipo de datos de declaración de vértices.</span><span class="sxs-lookup"><span data-stu-id="8e6ef-104">Defines a vertex declaration data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e6ef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e6ef-105">Syntax</span></span>


```C++
typedef enum D3DDECLTYPE { 
  D3DDECLTYPE_FLOAT1     = 0,
  D3DDECLTYPE_FLOAT2     = 1,
  D3DDECLTYPE_FLOAT3     = 2,
  D3DDECLTYPE_FLOAT4     = 3,
  D3DDECLTYPE_D3DCOLOR   = 4,
  D3DDECLTYPE_UBYTE4     = 5,
  D3DDECLTYPE_SHORT2     = 6,
  D3DDECLTYPE_SHORT4     = 7,
  D3DDECLTYPE_UBYTE4N    = 8,
  D3DDECLTYPE_SHORT2N    = 9,
  D3DDECLTYPE_SHORT4N    = 10,
  D3DDECLTYPE_USHORT2N   = 11,
  D3DDECLTYPE_USHORT4N   = 12,
  D3DDECLTYPE_UDEC3      = 13,
  D3DDECLTYPE_DEC3N      = 14,
  D3DDECLTYPE_FLOAT16_2  = 15,
  D3DDECLTYPE_FLOAT16_4  = 16,
  D3DDECLTYPE_UNUSED     = 17
} D3DDECLTYPE, *LPD3DDECLTYPE;
```



## <a name="constants"></a><span data-ttu-id="8e6ef-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="8e6ef-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8e6ef-107"><span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE \_ FLOAT1**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-107"><span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE\_FLOAT1**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-108">Float de un componente expandido a (float, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-108">One-component float expanded to (float, 0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-109"><span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-109"><span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE\_FLOAT2**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-110">Float de dos componentes expandido a (float, Float, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-110">Two-component float expanded to (float, float, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-111"><span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-111"><span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE\_FLOAT3**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-112">Float de tres componentes expandido a (float, Float, Float, 1).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-112">Three-component float expanded to (float, float, float, 1).</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-113"><span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-113"><span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE\_FLOAT4**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-114">Float de cuatro componentes expandido a (float, Float, Float, float).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-114">Four-component float expanded to (float, float, float, float).</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-115"><span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE \_ D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-115"><span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE\_D3DCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-116">Bytes sin signo de cuatro componentes y empaquetados asignados al intervalo de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="8e6ef-116">Four-component, packed, unsigned bytes mapped to 0 to 1 range.</span></span> <span data-ttu-id="8e6ef-117">La entrada es un [**D3DCOLOR**](d3dcolor.md) y se expande al orden RGBA.</span><span class="sxs-lookup"><span data-stu-id="8e6ef-117">Input is a [**D3DCOLOR**](d3dcolor.md) and is expanded to RGBA order.</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-118"><span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE \_ UBYTE4**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-118"><span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE\_UBYTE4**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-119">Bytes sin signo de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="8e6ef-119">Four-component, unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-120"><span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE \_ SHORT2**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-120"><span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE\_SHORT2**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-121">Los valores cortos con signo de dos componentes se expanden a (valor, valor, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-121">Two-component, signed short expanded to (value, value, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-122"><span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE \_ SHORT4**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-122"><span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE\_SHORT4**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-123">El Short con signo de cuatro componentes se expande a (valor, valor, valor, valor).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-123">Four-component, signed short expanded to (value, value, value, value).</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-124"><span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE \_ UBYTE4N**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-124"><span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE\_UBYTE4N**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-125">Bytes de cuatro componentes con cada byte normalizado dividiendo con 255.0 f.</span><span class="sxs-lookup"><span data-stu-id="8e6ef-125">Four-component byte with each byte normalized by dividing with 255.0f.</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-126"><span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE \_ SHORT2N**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-126"><span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE\_SHORT2N**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-127">Normalizado, de dos componentes, con signo corto, expandido a (primer Short/32767.0, segundo Short/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-127">Normalized, two-component, signed short, expanded to (first short/32767.0, second short/32767.0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-128"><span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE \_ SHORT4N**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-128"><span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE\_SHORT4N**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-129">Normalizado, de cuatro componentes, con signo corto, expandido a (primer Short/32767.0, segundo Short/32767.0, tercer Short/32767.0, cuarto Short/32767.0).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-129">Normalized, four-component, signed short, expanded to (first short/32767.0, second short/32767.0, third short/32767.0, fourth short/32767.0).</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-130"><span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE \_ USHORT2N**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-130"><span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE\_USHORT2N**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-131">Normalizado, dos componentes, sin signo corto, expandido a (primer Short/65535.0, Short Short/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-131">Normalized, two-component, unsigned short, expanded to (first short/65535.0, short short/65535.0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-132"><span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE \_ USHORT4N**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-132"><span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE\_USHORT4N**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-133">Normalizado, de cuatro componentes, sin signo corto, expandido a (primer Short/65535.0, segundo Short/65535.0, tercer Short/65535.0, cuarto Short/65535.0).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-133">Normalized, four-component, unsigned short, expanded to (first short/65535.0, second short/65535.0, third short/65535.0, fourth short/65535.0).</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-134"><span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE \_ UDEC3**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-134"><span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE\_UDEC3**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-135">Formato de tres componentes, sin signo y 10 10 10 expandido a (valor, valor, valor, 1).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-135">Three-component, unsigned, 10 10 10 format expanded to (value, value, value, 1).</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-136"><span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE \_ DEC3N**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-136"><span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE\_DEC3N**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-137">Formato de tres componentes, firmado, 10 10 10 normalizado y expandido a (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-137">Three-component, signed, 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-138"><span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE \_ FLOAT16 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-138"><span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE\_FLOAT16\_2**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-139">Dos componentes, de 16 bits y de punto flotante expandidos a (valor, valor, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-139">Two-component, 16-bit, floating point expanded to (value, value, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-140"><span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE \_ FLOAT16 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-140"><span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE\_FLOAT16\_4**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-141">Cuatro componentes, de 16 bits y de punto flotante expandidos a (valor, valor, valor, valor).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-141">Four-component, 16-bit, floating point expanded to (value, value, value, value).</span></span>

</dd> <dt>

<span data-ttu-id="8e6ef-142"><span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE \_ sin usar**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-142"><span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="8e6ef-143">El campo de tipo de la declaración no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8e6ef-143">Type field in the declaration is unused.</span></span> <span data-ttu-id="8e6ef-144">Está diseñado para su uso con D3DDECLMETHOD \_ UV y D3DDECLMETHOD \_ LOOKUPPRESAMPLED.</span><span class="sxs-lookup"><span data-stu-id="8e6ef-144">This is designed for use with D3DDECLMETHOD\_UV and D3DDECLMETHOD\_LOOKUPPRESAMPLED.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e6ef-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e6ef-145">Remarks</span></span>

<span data-ttu-id="8e6ef-146">Los datos de vértices se declaran con una matriz de estructuras [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="8e6ef-146">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="8e6ef-147">Cada elemento de la matriz contiene un tipo de datos de declaración de vértices.</span><span class="sxs-lookup"><span data-stu-id="8e6ef-147">Each element in the array contains a vertex declaration data type.</span></span>

<span data-ttu-id="8e6ef-148">Use la herramienta Visor de mayúsculas de DirectX (DXCapsViewer.exe) para ver los tipos que se admiten en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e6ef-148">Use the DirectX Caps Viewer Tool (DXCapsViewer.exe) to see which types are supported on your device.</span></span> <span data-ttu-id="8e6ef-149">Puede obtener esta herramienta y obtener información sobre ella desde el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="8e6ef-149">You can get this tool and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="8e6ef-150">Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="8e6ef-150">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e6ef-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e6ef-151">Requirements</span></span>



| <span data-ttu-id="8e6ef-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e6ef-152">Requirement</span></span> | <span data-ttu-id="8e6ef-153">Value</span><span class="sxs-lookup"><span data-stu-id="8e6ef-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e6ef-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e6ef-154">Header</span></span><br/> | <dl> <span data-ttu-id="8e6ef-155"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e6ef-155"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e6ef-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e6ef-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e6ef-157">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="8e6ef-157">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="8e6ef-158">**D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="8e6ef-158">**D3DDECLMETHOD**</span></span>](./d3ddeclmethod.md)
</dt> </dl>

 

 
