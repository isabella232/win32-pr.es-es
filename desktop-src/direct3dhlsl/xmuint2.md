---
title: Estructura XMUINT2
description: Describe un vector entero 2D sin signo.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- Estructura HLSL de XMUINT2
topic_type:
- apiref
api_name:
- XMUINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71168d08b8a91e09429a6f4e004c48c699635414
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966415"
---
# <a name="xmuint2-structure"></a>Estructura XMUINT2

Describe un vector entero 2D sin signo.

## <a name="syntax"></a>Sintaxis


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
```



## <a name="members"></a>Members

<dl> <dt>

**x**
</dt> <dd>

componente x del vector.

</dd> <dt>

**y**
</dt> <dd>

Componente y del vector.

</dd> </dl>



## <a name="remarks"></a>Observaciones

Esta estructura se define en el encabezado ``D3DX\_DXGIFormatConvert.inl`` del SDK de DirectX (junio de 2010) para su uso desde C++. La versión más reciente de este encabezado en el paquete de NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ya no lo define y se basa en [DirectX::XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) en DirectXMath en su lugar.



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras](format-conversion-structures.md)
</dt> <dt>

[Desempaquetar y empaquetar DXGI \_ FORMAT para la edición In-Place imágenes](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>