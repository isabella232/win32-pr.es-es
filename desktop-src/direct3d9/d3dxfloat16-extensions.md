---
description: Proporciona sobrecargas de operador y conversión de tipos para estructuras D3DXFLOAT16.
ms.assetid: d287efb5-d15e-46dc-924d-012e1a108efc
title: Extensiones D3DXFLOAT16 (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 63b3dfa3ae42ead2088193c42b2eef86c05ebb82c04d4a07162fb26970c5d29c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526149"
---
# <a name="d3dxfloat16-extensions"></a>Extensiones D3DXFLOAT16

Proporciona sobrecargas de operador y conversión de tipos [**para estructuras D3DXFLOAT16.**](d3dxfloat16.md)

``` syntax
typedef struct D3DXFLOAT16
{
#ifdef __cplusplus
public:
    D3DXFLOAT16() {};
    D3DXFLOAT16( FLOAT );
    D3DXFLOAT16( CONST D3DXFLOAT16& );

    // casting
    operator FLOAT ();

    // binary operators
    BOOL operator == ( CONST D3DXFLOAT16& ) const;
    BOOL operator != ( CONST D3DXFLOAT16& ) const;

protected:
#endif //__cplusplus
    WORD value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```

Tipos derivados: \* LPD3DXFLOAT16

## <a name="members"></a>Miembros

Para obtener más información sobre los miembros de estructura, consulte D3DXFLOAT16.

## <a name="remarks"></a>Comentarios

Las sobrecargas de operador y las conversión de tipos para esta estructura se implementan en d3dx9math.inl.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




