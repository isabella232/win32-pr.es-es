---
description: Matriz 4x4 que contiene métodos y sobrecargas de operador.
ms.assetid: c354d28b-bb08-41c5-bb59-90a912181f0f
title: Estructura D3DXMATRIX (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIX
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: cae887e2e9a8782cdc7ba159db203c929006c58a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698372"
---
# <a name="d3dxmatrix-structure-d3dx10mathh"></a><span data-ttu-id="0ef02-103">Estructura D3DXMATRIX (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="0ef02-103">D3DXMATRIX structure (D3DX10Math.h)</span></span>

<span data-ttu-id="0ef02-104">Matriz 4x4 que contiene métodos y sobrecargas de operador.</span><span class="sxs-lookup"><span data-stu-id="0ef02-104">A 4x4 matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef02-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ef02-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a><span data-ttu-id="0ef02-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ef02-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0ef02-107">**\_ij**</span><span class="sxs-lookup"><span data-stu-id="0ef02-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="0ef02-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ef02-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0ef02-109">El componente (i, j) de la matriz, donde i es el número de fila y j es el número de columna.</span><span class="sxs-lookup"><span data-stu-id="0ef02-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="0ef02-110">Por ejemplo, \_ 34 significa lo mismo que \[ ₃ ₄ \] , el componente de la tercera fila y la cuarta columna.</span><span class="sxs-lookup"><span data-stu-id="0ef02-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ef02-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ef02-111">Remarks</span></span>

<span data-ttu-id="0ef02-112">Los programadores de C no pueden usar la estructura D3DXMATRIX, deben usar la estructura D3DMATRIX.</span><span class="sxs-lookup"><span data-stu-id="0ef02-112">C programmers cannot use the D3DXMATRIX structure, they must use the D3DMATRIX structure.</span></span> <span data-ttu-id="0ef02-113">Los programadores de C++ pueden aprovechar las ventajas de los constructores sobrecargados y los operadores de asignación, unario y binario (incluida la igualdad).</span><span class="sxs-lookup"><span data-stu-id="0ef02-113">C++ programmers can take advantage of overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

<span data-ttu-id="0ef02-114">En D3DX, el \_ elemento 34 de una matriz de proyección no puede ser un número negativo.</span><span class="sxs-lookup"><span data-stu-id="0ef02-114">In D3DX, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="0ef02-115">Si su aplicación necesita usar un valor negativo en esta ubicación, debe escalar toda la matriz de proyección en-1 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0ef02-115">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

### <a name="d3dxmatrix-extensions"></a><span data-ttu-id="0ef02-116">Extensiones de D3DXMATRIX</span><span class="sxs-lookup"><span data-stu-id="0ef02-116">D3DXMATRIX Extensions</span></span>

<span data-ttu-id="0ef02-117">**D3DXMATRIX** tiene las siguientes extensiones de C++.</span><span class="sxs-lookup"><span data-stu-id="0ef02-117">**D3DXMATRIX** has the following C++ extensions.</span></span>


```
#ifdef __cplusplus
typedef struct D3DXMATRIX : public D3DMATRIX
{
public:
    D3DXMATRIX() {};
    D3DXMATRIX( CONST FLOAT * );
    D3DXMATRIX( CONST D3DMATRIX& );
    D3DXMATRIX( CONST D3DXFLOAT16 * );
    D3DXMATRIX( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );


    // access grants
    FLOAT& operator () ( UINT Row, UINT Col );
    FLOAT  operator () ( UINT Row, UINT Col ) const;

    // casting operators
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXMATRIX& operator *= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator += ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator -= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator *= ( FLOAT );
    D3DXMATRIX& operator /= ( FLOAT );

    // unary operators
    D3DXMATRIX operator + () const;
    D3DXMATRIX operator - () const;

    // binary operators
    D3DXMATRIX operator * ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator + ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator - ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator * ( FLOAT ) const;
    D3DXMATRIX operator / ( FLOAT ) const;

    friend D3DXMATRIX operator * ( FLOAT, CONST D3DXMATRIX& );

    BOOL operator == ( CONST D3DXMATRIX& ) const;
    BOOL operator != ( CONST D3DXMATRIX& ) const;

} D3DXMATRIX, *LPD3DXMATRIX;

#else //!__cplusplus
typedef struct _D3DMATRIX D3DXMATRIX, *LPD3DXMATRIX;
#endif //!__cplusplus
        
```



## <a name="requirements"></a><span data-ttu-id="0ef02-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ef02-118">Requirements</span></span>



| <span data-ttu-id="0ef02-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ef02-119">Requirement</span></span> | <span data-ttu-id="0ef02-120">Value</span><span class="sxs-lookup"><span data-stu-id="0ef02-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef02-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ef02-121">Header</span></span><br/> | <dl> <span data-ttu-id="0ef02-122"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ef02-122"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef02-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ef02-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef02-124">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="0ef02-124">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
