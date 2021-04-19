---
title: Estructura XMUINT4
description: Describe un vector entero de 4D sin signo.
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
ms.openlocfilehash: 7e461d5b10f01f61de3fcfd721c4a6b1350c7d68
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222853"
---
# <a name="xmuint4-structure"></a>Estructura XMUINT4

Describe un vector entero de 4D sin signo.

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



## <a name="members"></a>Miembros

<dl> <dt>

**x**
</dt> <dd>

componente x del vector.

</dd> <dt>

**y**
</dt> <dd>

componente y del vector.

<dl> <dt>

**z**
</dt> <dd>

componente z del vector.

<dl> <dt>

**w**
</dt> <dd>

componente w del vector.

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a>Observaciones

Esta estructura se define en el ``D3DX\_DXGIFormatConvert.inl`` encabezado del SDK de DirectX (2010 de junio) para su uso desde C++. La versión más reciente de este encabezado en el paquete NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ya no lo define y se basa en [DirectX:: XMUINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint4) en DirectXMath en su lugar.




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
