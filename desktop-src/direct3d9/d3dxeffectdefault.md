---
description: Parámetros predeterminados de efecto.
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: Estructura D3DXEFFECTDEFAULT (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: fee415cbd7d8ec28daa079dd2f224949402a813b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072822"
---
# <a name="d3dxeffectdefault-structure"></a>D3DXEFFECTDEFAULT (estructura)

Parámetros predeterminados de efecto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXEFFECTDEFAULT {
  LPSTR                 pParamName;
  D3DXEFFECTDEFAULTTYPE Type;
  DWORD                 NumBytes;
  LPVOID                pValue;
} D3DXEFFECTDEFAULT, *LPD3DXEFFECTDEFAULT;
```



## <a name="members"></a>Members

<dl> <dt>

**pParamName**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Nombre del parámetro.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**

</dd> <dd>

Tipo de datos en pValue. Para obtener más información, [ **vea D3DXEFFECTDEFAULTTYPE.**](./d3dxeffectdefaulttype.md)

</dd> <dt>

**NumBytes**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño, en bytes, de los datos a los que apunta pValue.

</dd> <dt>

**pValue**
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntero a la ubicación de memoria que contiene los datos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de efecto](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
