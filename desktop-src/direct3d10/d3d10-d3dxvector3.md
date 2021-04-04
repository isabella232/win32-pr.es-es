---
description: Describe un vector de tres componentes, que incluye sobrecargas de operador y conversiones de tipo.
ms.assetid: d170cd26-d705-4a31-82b3-f9ea070b6ca4
title: Estructura D3DXVECTOR3 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR3
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: fd971b594d854aea92229e75186bf5d8a55c73ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821378"
---
# <a name="d3dxvector3-structure-d3dx10mathh"></a><span data-ttu-id="4c2d0-103">Estructura D3DXVECTOR3 (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="4c2d0-103">D3DXVECTOR3 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="4c2d0-104">Describe un vector de tres componentes, que incluye sobrecargas de operador y conversiones de tipo.</span><span class="sxs-lookup"><span data-stu-id="4c2d0-104">Describes a three-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c2d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c2d0-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR3 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
} D3DXVECTOR3, *LPD3DXVECTOR3;
```



## <a name="members"></a><span data-ttu-id="4c2d0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="4c2d0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4c2d0-107">**x**</span><span class="sxs-lookup"><span data-stu-id="4c2d0-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="4c2d0-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c2d0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4c2d0-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="4c2d0-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="4c2d0-110">**y**</span><span class="sxs-lookup"><span data-stu-id="4c2d0-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="4c2d0-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c2d0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4c2d0-112">Componente y.</span><span class="sxs-lookup"><span data-stu-id="4c2d0-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="4c2d0-113">**z**</span><span class="sxs-lookup"><span data-stu-id="4c2d0-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="4c2d0-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c2d0-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4c2d0-115">Componente z.</span><span class="sxs-lookup"><span data-stu-id="4c2d0-115">The z-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c2d0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c2d0-116">Remarks</span></span>

<span data-ttu-id="4c2d0-117">**D3DXVECTOR3** tiene las siguientes extensiones de C++.</span><span class="sxs-lookup"><span data-stu-id="4c2d0-117">**D3DXVECTOR3** has the following C++ extensions.</span></span>

### <a name="d3dxvector3-extensions"></a><span data-ttu-id="4c2d0-118">Extensiones de D3DXVECTOR3</span><span class="sxs-lookup"><span data-stu-id="4c2d0-118">D3DXVECTOR3 Extensions</span></span>


```
#ifdef __cplusplus
typedef struct D3DXVECTOR3 : public D3DVECTOR
{
public:
    D3DXVECTOR3() {};
    D3DXVECTOR3( CONST FLOAT * );
    D3DXVECTOR3( CONST D3DVECTOR& );
    D3DXVECTOR3( CONST D3DXFLOAT16 * );
    D3DXVECTOR3( FLOAT x, FLOAT y, FLOAT z );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR3& operator += ( CONST D3DXVECTOR3& );
    D3DXVECTOR3& operator -= ( CONST D3DXVECTOR3& );
    D3DXVECTOR3& operator *= ( FLOAT );
    D3DXVECTOR3& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR3 operator + () const;
    D3DXVECTOR3 operator - () const;

    // binary operators
    D3DXVECTOR3 operator + ( CONST D3DXVECTOR3& ) const;
    D3DXVECTOR3 operator - ( CONST D3DXVECTOR3& ) const;
    D3DXVECTOR3 operator * ( FLOAT ) const;
    D3DXVECTOR3 operator / ( FLOAT ) const;

    friend D3DXVECTOR3 operator * ( FLOAT, CONST struct D3DXVECTOR3& );

    BOOL operator == ( CONST D3DXVECTOR3& ) const;
    BOOL operator != ( CONST D3DXVECTOR3& ) const;

} D3DXVECTOR3, *LPD3DXVECTOR3;

#else //!__cplusplus
typedef struct _D3DVECTOR D3DXVECTOR3, *LPD3DXVECTOR3;
#endif //!__cplusplus
        
```



## <a name="requirements"></a><span data-ttu-id="4c2d0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c2d0-119">Requirements</span></span>



| <span data-ttu-id="4c2d0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c2d0-120">Requirement</span></span> | <span data-ttu-id="4c2d0-121">Value</span><span class="sxs-lookup"><span data-stu-id="4c2d0-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c2d0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c2d0-122">Header</span></span><br/> | <dl> <span data-ttu-id="4c2d0-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c2d0-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c2d0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c2d0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c2d0-125">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="4c2d0-125">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
