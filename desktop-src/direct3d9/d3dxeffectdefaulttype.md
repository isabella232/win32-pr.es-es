---
description: Tipos de datos de efecto. Los datos están contenidos en el miembro pValue de D3DXEFFECTDEFAULT.
ms.assetid: d698ad6e-2ce2-48d6-90be-49bc08f172a9
title: Enumeración D3DXEFFECTDEFAULTTYPE (D3dx9mesh.h)
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
ms.openlocfilehash: 25b197503b4f709c376a80c1fde0a89f96656da330be6bd26a4b1ebc1c8f47a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119205"
---
# <a name="d3dxeffectdefaulttype-enumeration"></a>D3DXEFFECTDEFAULTTYPE (enumeración)

Tipos de datos de efecto. Los datos están contenidos en el miembro pValue de [**D3DXEFFECTDEFAULT.**](d3dxeffectdefault.md)

## <a name="syntax"></a>Syntax


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

<span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**CADENA D3DXEDT \_**
</dt> <dd>

El tipo de datos es una cadena de texto ASCII terminada en NULL.

</dd> <dt>

<span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**FLOTANTES D3DXEDT \_**
</dt> <dd>

El tipo de datos es una matriz de tipo float. NumBytes especifica el número de tipos float de la matriz en [**D3DXEFFECTDEFAULT.**](d3dxeffectdefault.md)

</dd> <dt>

<span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT \_ DWORD**
</dt> <dd>

El tipo de datos es DWORD.

</dd> <dt>

<span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT \_ FORCEDWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




