---
title: Estructura XMINT4
description: Describe un vector entero 4D.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- HLSL de la estructura XMINT4
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead9e7da8d48025c456ae6e57b0ffe64cdb00f46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970444"
---
# <a name="xmint4-structure"></a>Estructura XMINT4

Describe un vector entero 4D.

## <a name="syntax"></a>Sintaxis


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
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

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="remarks"></a>Observaciones

Esta estructura se define en el encabezado ``D3DX\_DXGIFormatConvert.inl`` del SDK de DirectX (junio de 2010) para su uso desde C++. La versión más reciente de este encabezado en el paquete [microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet ya no lo define y se basa en [DirectX::XMINT4](/windows/win32/api/directxmath/ns-directxmath-xmint4) en DirectXMath en su lugar.



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras](format-conversion-structures.md)
</dt> <dt>

[Desempaquetar y empaquetar DXGI \_ FORMAT para la edición In-Place imágenes](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>