---
description: Describe la ubicación del archivo de include.
ms.assetid: a15d363e-0d82-44a9-816b-edf2f60540b3
title: D3DXINCLUDE_TYPE enumeración (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINCLUDE_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 51a4ed41203a9f78ee5fef747f088e9def9033c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969784"
---
# <a name="d3dxinclude_type-enumeration"></a>D3DXINCLUDE \_ TYPE (enumeración)

Describe la ubicación del archivo de include.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DXINCLUDE_TYPE { 
  D3DXINC_LOCAL        = 0,
  D3DXINC_SYSTEM       = 1,
  D3DXINC_FORCE_DWORD  = 0x7fffffff
} D3DXINCLUDE_TYPE, *LPD3DXINCLUDE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC \_ LOCAL**
</dt> <dd>

Busque en el proyecto local el archivo de incluir.

</dd> <dt>

<span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**D3DXINC \_ SYSTEM**
</dt> <dd>

Busque en la ruta de acceso del sistema el archivo de incluir.

</dd> <dt>

<span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




