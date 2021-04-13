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
# <a name="d3ddecltype-enumeration"></a>Enumeración D3DDECLTYPE

Define un tipo de datos de declaración de vértices.

## <a name="syntax"></a>Sintaxis


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE \_ FLOAT1**
</dt> <dd>

Float de un componente expandido a (float, 0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE \_ FLOAT2**
</dt> <dd>

Float de dos componentes expandido a (float, Float, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE \_ FLOAT3**
</dt> <dd>

Float de tres componentes expandido a (float, Float, Float, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE \_ FLOAT4**
</dt> <dd>

Float de cuatro componentes expandido a (float, Float, Float, float).

</dd> <dt>

<span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE \_ D3DCOLOR**
</dt> <dd>

Bytes sin signo de cuatro componentes y empaquetados asignados al intervalo de 0 a 1. La entrada es un [**D3DCOLOR**](d3dcolor.md) y se expande al orden RGBA.

</dd> <dt>

<span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE \_ UBYTE4**
</dt> <dd>

Bytes sin signo de cuatro componentes.

</dd> <dt>

<span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE \_ SHORT2**
</dt> <dd>

Los valores cortos con signo de dos componentes se expanden a (valor, valor, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE \_ SHORT4**
</dt> <dd>

El Short con signo de cuatro componentes se expande a (valor, valor, valor, valor).

</dd> <dt>

<span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE \_ UBYTE4N**
</dt> <dd>

Bytes de cuatro componentes con cada byte normalizado dividiendo con 255.0 f.

</dd> <dt>

<span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE \_ SHORT2N**
</dt> <dd>

Normalizado, de dos componentes, con signo corto, expandido a (primer Short/32767.0, segundo Short/32767.0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE \_ SHORT4N**
</dt> <dd>

Normalizado, de cuatro componentes, con signo corto, expandido a (primer Short/32767.0, segundo Short/32767.0, tercer Short/32767.0, cuarto Short/32767.0).

</dd> <dt>

<span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE \_ USHORT2N**
</dt> <dd>

Normalizado, dos componentes, sin signo corto, expandido a (primer Short/65535.0, Short Short/65535.0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE \_ USHORT4N**
</dt> <dd>

Normalizado, de cuatro componentes, sin signo corto, expandido a (primer Short/65535.0, segundo Short/65535.0, tercer Short/65535.0, cuarto Short/65535.0).

</dd> <dt>

<span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE \_ UDEC3**
</dt> <dd>

Formato de tres componentes, sin signo y 10 10 10 expandido a (valor, valor, valor, 1).

</dd> <dt>

<span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE \_ DEC3N**
</dt> <dd>

Formato de tres componentes, firmado, 10 10 10 normalizado y expandido a (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE \_ FLOAT16 \_ 2**
</dt> <dd>

Dos componentes, de 16 bits y de punto flotante expandidos a (valor, valor, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE \_ FLOAT16 \_ 4**
</dt> <dd>

Cuatro componentes, de 16 bits y de punto flotante expandidos a (valor, valor, valor, valor).

</dd> <dt>

<span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE \_ sin usar**
</dt> <dd>

El campo de tipo de la declaración no se utiliza. Está diseñado para su uso con D3DDECLMETHOD \_ UV y D3DDECLMETHOD \_ LOOKUPPRESAMPLED.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los datos de vértices se declaran con una matriz de estructuras [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) . Cada elemento de la matriz contiene un tipo de datos de declaración de vértices.

Use la herramienta Visor de mayúsculas de DirectX (DXCapsViewer.exe) para ver los tipos que se admiten en el dispositivo. Puede obtener esta herramienta y obtener información sobre ella desde el SDK de DirectX. Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DDECLMETHOD**](./d3ddeclmethod.md)
</dt> </dl>

 

 
