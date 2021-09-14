---
description: Describe una función utilizada por un efecto.
ms.assetid: 5d9deb82-7fe5-4408-8a6a-b34ecd97e8ba
title: D3DXFUNCTION_DESC estructura (D3dx9effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFUNCTION_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: ec53cae4689ebc1795937012259b2e219630568b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072782"
---
# <a name="d3dxfunction_desc-structure"></a>D3DXFUNCTION \_ DESC (estructura)

Describe una función utilizada por un efecto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXFUNCTION_DESC {
  LPCSTR Name;
  UINT   Annotations;
} D3DXFUNCTION_DESC, *LPD3DXFUNCTION_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de la función.

</dd> <dt>

**Anotaciones**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Sin usar. [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md)siempre establecerá este miembro en cero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de efecto](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
