---
title: Estructura XMINT2
description: Describe un vector entero 2D.
ms.assetid: 651f62f8-577d-4356-9bbc-0d4a9ca8fb01
keywords:
- HLSL de la estructura XMINT2
topic_type:
- apiref
api_name:
- XMINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc613cd87b212ca21aacf1744b7789bd49732a555630d5cfc6051eaab2b3d10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484185"
---
# <a name="xmint2-structure"></a>Estructura XMINT2

Describe un vector entero 2D.

## <a name="syntax"></a>Sintaxis


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
```



## <a name="members"></a>Miembros

<dl> <dt>

**x**
</dt> <dd>

Componente x del vector.

</dd> <dt>

**y**
</dt> <dd>

Componente y del vector.

</dd> </dl>



## <a name="remarks"></a>Comentarios

Esta estructura se define en el encabezado ``D3DX\_DXGIFormatConvert.inl`` del SDK de DirectX (junio de 2010) para su uso desde C++. La versión más reciente de este encabezado en el paquete de NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ya no lo define y se basa en [DirectX::XMINT2](/windows/win32/api/directxmath/ns-directxmath-xmint2) en DirectXMath en su lugar.



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras](format-conversion-structures.md)
</dt> <dt>

[Desempaquetar y empaquetar DXGI \_ FORMAT para la edición In-Place imágenes](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>