---
description: Tipos de datos de efecto. Los datos están contenidos en el miembro de pValue de D3DXEFFECTDEFAULT.
ms.assetid: d698ad6e-2ce2-48d6-90be-49bc08f172a9
title: Enumeración D3DXEFFECTDEFAULTTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULTTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: ffd31167d712a8270011c061cd6328aa9214352e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698253"
---
# <a name="d3dxeffectdefaulttype-enumeration"></a>Enumeración D3DXEFFECTDEFAULTTYPE

Tipos de datos de efecto. Los datos están contenidos en el miembro de pValue de [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DXEFFECTDEFAULTTYPE { 
  D3DXEDT_STRING      = 1,
  D3DXEDT_FLOATS      = 2,
  D3DXEDT_DWORD       = 3,
  D3DXEDT_FORCEDWORD  = 0x7fffffff
} D3DXEFFECTDEFAULTTYPE, *LPD3DXEFFECTDEFAULTTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**\_Cadena D3DXEDT**
</dt> <dd>

El tipo de datos es una cadena de texto ASCII terminada en NULL.

</dd> <dt>

<span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT \_ flotantes**
</dt> <dd>

El tipo de datos es una matriz de tipo float. El número de tipos Float de la matriz se especifica mediante NumBytes en [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).

</dd> <dt>

<span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT \_ DWORD**
</dt> <dd>

El tipo de datos es un valor DWORD.

</dd> <dt>

<span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT \_ FORCEDWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




