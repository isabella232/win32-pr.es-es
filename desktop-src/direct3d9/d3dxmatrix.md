---
description: 'Estructura D3DXMATRIX (D3dx9math.h): matriz de 4x4 que contiene métodos y sobrecargas de operador.'
ms.assetid: 0911088b-50cf-4c4a-996e-351386fc359b
title: Estructura D3DXMATRIX (D3dx9math.h)
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
- d3dx9math.h
ms.openlocfilehash: fad44c13f7b856270fe6475f9e099f6e1714e064
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094223"
---
# <a name="d3dxmatrix-structure-d3dx9mathh"></a><span data-ttu-id="12bea-103">Estructura D3DXMATRIX (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="12bea-103">D3DXMATRIX structure (D3dx9math.h)</span></span>

<span data-ttu-id="12bea-104">Matriz 4x4 que contiene métodos y sobrecargas de operador.</span><span class="sxs-lookup"><span data-stu-id="12bea-104">A 4x4 matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="12bea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12bea-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a><span data-ttu-id="12bea-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="12bea-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="12bea-107">**\_Ij**</span><span class="sxs-lookup"><span data-stu-id="12bea-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="12bea-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12bea-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12bea-109">Componente (i, j) de la matriz, donde i es el número de fila y j es el número de columna.</span><span class="sxs-lookup"><span data-stu-id="12bea-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="12bea-110">Por ejemplo, 34 significa lo mismo que a₃₄ , el componente de \_ la tercera fila y la cuarta \[ \] columna.</span><span class="sxs-lookup"><span data-stu-id="12bea-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12bea-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="12bea-111">Remarks</span></span>

<span data-ttu-id="12bea-112">Los programadores de C no pueden usar la estructura D3DXMATRIX, deben usar la estructura [**D3DMATRIX.**](d3dmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="12bea-112">C programmers cannot use the D3DXMATRIX structure, they must use the [**D3DMATRIX**](d3dmatrix.md) structure.</span></span> <span data-ttu-id="12bea-113">Los programadores de C++ pueden aprovechar los constructores sobrecargados y los operadores de asignación, unario y binario (incluida la igualdad).</span><span class="sxs-lookup"><span data-stu-id="12bea-113">C++ programmers can take advantage of overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

<span data-ttu-id="12bea-114">En D3DX, el \_ elemento 34 de una matriz de proyección no puede ser un número negativo.</span><span class="sxs-lookup"><span data-stu-id="12bea-114">In D3DX, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="12bea-115">Si la aplicación necesita usar un valor negativo en esta ubicación, debe escalar toda la matriz de proyección en -1 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="12bea-115">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

### <a name="d3dxmatrix-extensions"></a><span data-ttu-id="12bea-116">Extensiones D3DXMATRIX</span><span class="sxs-lookup"><span data-stu-id="12bea-116">D3DXMATRIX Extensions</span></span>

<span data-ttu-id="12bea-117">**D3DXMATRIX** tiene las siguientes extensiones de C++.</span><span class="sxs-lookup"><span data-stu-id="12bea-117">**D3DXMATRIX** has the following C++ extensions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="12bea-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12bea-118">Requirements</span></span>



| <span data-ttu-id="12bea-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="12bea-119">Requirement</span></span> | <span data-ttu-id="12bea-120">Value</span><span class="sxs-lookup"><span data-stu-id="12bea-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12bea-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12bea-121">Header</span></span><br/> | <dl> <span data-ttu-id="12bea-122"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="12bea-122"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12bea-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="12bea-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12bea-124">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="12bea-124">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="12bea-125">**D3DMATRIX**</span><span class="sxs-lookup"><span data-stu-id="12bea-125">**D3DMATRIX**</span></span>](d3dmatrix.md)
</dt> </dl>

 

 
