---
title: Estructura XMUINT4
description: Describe un vector entero 4D sin signo.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- HLSL de la estructura XMUINT4
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e424b4e5fd1c97f5aec01571d887b54dbb143b7
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549900"
---
# <a name="xmuint4-structure"></a>Estructura XMUINT4

Describe un vector entero 4D sin signo.

## <a name="syntax"></a>Sintaxis


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a>Members

<dl> <dt>

**x**
</dt> <dd>

Componente x del vector.

</dd> <dt>

**y**
</dt> <dd>

Componente y del vector.

<dl> <dt>

**Z**
</dt> <dd>

Componente z del vector.

<dl> <dt>

**w**
</dt> <dd>

w-component del vector.

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a>Comentarios

Esta estructura se define en el encabezado del ``D3DX\_DXGIFormatConvert.inl`` SDK de DirectX (junio de 2010) para su uso desde C++. La versión más reciente de este encabezado en el paquete NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ya no lo define y se basa en [DirectX::XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) en DirectXMath en su lugar.




## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras](format-conversion-structures.md)
</dt> <dt>

[Desempaquetar y empaquetar DXGI \_ FORMAT para In-Place de imágenes](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>