---
description: Proporciona las siguientes sobrecargas de operador y conversiones de tipo para las estructuras D3DXPLANE.
ms.assetid: 05f80b68-fb2b-4fd7-94e9-e5b40968c4aa
title: Extensiones de D3DXPLANE (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 3ff8f68283cd81e6647fcdea480ac19b48547cab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717559"
---
# <a name="d3dxplane-extensions"></a>Extensiones de D3DXPLANE

Proporciona las siguientes sobrecargas de operador y conversiones de tipo para las estructuras [**D3DXPLANE**](d3dxplane.md) .

``` syntax
typedef struct D3DXPLANE
{
#ifdef __cplusplus
public:
    D3DXPLANE() {}
    D3DXPLANE( CONST FLOAT* );
    D3DXPLANE( CONST D3DXFLOAT16* );
    D3DXPLANE( FLOAT a, FLOAT b, FLOAT c, FLOAT d );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXPLANE& operator *= ( FLOAT );
    D3DXPLANE& operator /= ( FLOAT );

    // unary operators
    D3DXPLANE operator + () const;
    D3DXPLANE operator - () const;

    // binary operators
    D3DXPLANE operator * ( FLOAT ) const;
    D3DXPLANE operator / ( FLOAT ) const;

    friend D3DXPLANE operator * ( FLOAT, CONST D3DXPLANE& );

    BOOL operator == ( CONST D3DXPLANE& ) const;
    BOOL operator != ( CONST D3DXPLANE& ) const;

#endif //__cplusplus
    FLOAT a, b, c, d;
} D3DXPLANE, *LPD3DXPLANE;
```

Tipos derivados: \* LPD3DXPLANE

## <a name="remarks"></a>Observaciones

Para obtener más información sobre los miembros de la estructura, consulte [**D3DXPLANE**](d3dxplane.md).

Las sobrecargas de operador y las conversiones de tipo para esta estructura se implementan en d3dx9math. INL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




