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
ms.openlocfilehash: 1e93e26933ad6b3829848e7e826d8d9685e9f141
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222863"
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

componente x del vector.

</dd> <dt>

**y**
</dt> <dd>

componente y del vector.

</dd> </dl>



## <a name="remarks"></a>Observaciones

Esta estructura se define en el ``D3DX\_DXGIFormatConvert.inl`` encabezado del SDK de DirectX (2010 de junio) para su uso desde C++. La versión más reciente de este encabezado en el paquete NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ya no lo define y se basa en [DirectX:: XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) en DirectXMath en su lugar.



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. INL</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras](format-conversion-structures.md)
</dt> <dt>

[Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
