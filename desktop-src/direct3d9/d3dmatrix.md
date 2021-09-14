---
description: Describe una matriz.
ms.assetid: d6b98a32-e745-4724-b8ce-a81a3f5416f3
title: D3DMATRIX (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6b4339d2e44e1add46103bae58ad3e02c8a6509b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970992"
---
# <a name="d3dmatrix"></a>D3DMATRIX

Describe una matriz.

``` syntax
typedef struct _D3DMATRIX {
    union {
        struct {
            float        _11, _12, _13, _14;
            float        _21, _22, _23, _24;
            float        _31, _32, _33, _34;
            float        _41, _42, _43, _44;

        };
        float m[4][4];
    };
} D3DMATRIX;
```

Tipos derivados: \* LPD3DMATRIX

## <a name="members"></a>Members



| Elemento                                                        | Descripción                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_ij"></span><span id="_IJ"></span>\_Ij<br/> | Matriz de flotantes que representan una matriz de 4x4, donde i es el número de fila y j es el número de columna. Por ejemplo, 34 significa lo mismo que a₃₄ , el componente de \_ la tercera fila y la cuarta \[ \] columna.<br/> |



 

## <a name="remarks"></a>Observaciones

En Direct3D, el \_ elemento 34 de una matriz de proyección no puede ser un número negativo. Si la aplicación necesita usar un valor negativo en esta ubicación, debe escalar toda la matriz de proyección en -1 en su lugar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[**MultiplyTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

**SetTransform**
</dt> <dt>

[**D3DXMATRIX**](d3dxmatrix.md)
</dt> <dt>

[Transformaciones (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
