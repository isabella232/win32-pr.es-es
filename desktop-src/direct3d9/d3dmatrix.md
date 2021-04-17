---
description: Describe una matriz.
ms.assetid: d6b98a32-e745-4724-b8ce-a81a3f5416f3
title: D3DMATRIX (D3D9Types. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718276"
---
# <a name="d3dmatrix"></a><span data-ttu-id="a9928-103">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="a9928-103">D3DMATRIX</span></span>

<span data-ttu-id="a9928-104">Describe una matriz.</span><span class="sxs-lookup"><span data-stu-id="a9928-104">Describes a matrix.</span></span>

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

<span data-ttu-id="a9928-105">Tipos derivados: \* LPD3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="a9928-105">Derived types: \*LPD3DMATRIX</span></span>

## <a name="members"></a><span data-ttu-id="a9928-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a9928-106">Members</span></span>



| <span data-ttu-id="a9928-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a9928-107">Item</span></span>                                                        | <span data-ttu-id="a9928-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9928-108">Description</span></span>                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9928-109"><span id="_ij"></span><span id="_IJ"></span>\_ij</span><span class="sxs-lookup"><span data-stu-id="a9928-109"><span id="_ij"></span><span id="_IJ"></span>\_ij</span></span><br/> | <span data-ttu-id="a9928-110">Matriz de puntos flotantes que representan una matriz 4x4, donde i es el número de fila y j es el número de columna.</span><span class="sxs-lookup"><span data-stu-id="a9928-110">An array of floats that represent a 4x4 matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="a9928-111">Por ejemplo, \_ 34 significa lo mismo que \[ ₃ ₄ \] , el componente de la tercera fila y la cuarta columna.</span><span class="sxs-lookup"><span data-stu-id="a9928-111">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a9928-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9928-112">Remarks</span></span>

<span data-ttu-id="a9928-113">En Direct3D, el \_ elemento 34 de una matriz de proyección no puede ser un número negativo.</span><span class="sxs-lookup"><span data-stu-id="a9928-113">In Direct3D, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="a9928-114">Si su aplicación necesita usar un valor negativo en esta ubicación, debe escalar toda la matriz de proyección en-1 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a9928-114">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9928-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9928-115">Requirements</span></span>



| <span data-ttu-id="a9928-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9928-116">Requirement</span></span> | <span data-ttu-id="a9928-117">Value</span><span class="sxs-lookup"><span data-stu-id="a9928-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9928-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9928-118">Header</span></span><br/> | <dl> <span data-ttu-id="a9928-119"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9928-119"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9928-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9928-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9928-121">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="a9928-121">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="a9928-122">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="a9928-122">**GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="a9928-123">**MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="a9928-123">**MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="a9928-124">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="a9928-124">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

<span data-ttu-id="a9928-125">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="a9928-125">**SetTransform**</span></span>
</dt> <dt>

[<span data-ttu-id="a9928-126">**D3DXMATRIX**</span><span class="sxs-lookup"><span data-stu-id="a9928-126">**D3DXMATRIX**</span></span>](d3dxmatrix.md)
</dt> <dt>

[<span data-ttu-id="a9928-127">Transformaciones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a9928-127">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
