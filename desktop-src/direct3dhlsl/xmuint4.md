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
ms.openlocfilehash: 9f0b02ffe64e7b4c4479723b4e36abd87f6bd03b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986772"
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

 

 





