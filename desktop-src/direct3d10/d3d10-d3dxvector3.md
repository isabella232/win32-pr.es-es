---
description: 'Estructura D3DXVECTOR3 (D3DX10Math.h): describe un vector de tres componentes que incluye sobrecargas de operador y conversión de tipos.'
ms.assetid: d170cd26-d705-4a31-82b3-f9ea070b6ca4
title: Estructura D3DXVECTOR3 (D3DX10Math.h)
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
ms.openlocfilehash: 7b43348b6b5683e9fe75c5340fd0c2cab5efe719
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102862"
---
# <a name="d3dxvector3-structure-d3dx10mathh"></a><span data-ttu-id="78e8c-103">Estructura D3DXVECTOR3 (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="78e8c-103">D3DXVECTOR3 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="78e8c-104">Describe un vector de tres componentes que incluye sobrecargas de operador y conversión de tipos.</span><span class="sxs-lookup"><span data-stu-id="78e8c-104">Describes a three-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="78e8c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78e8c-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR3 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
} D3DXVECTOR3, *LPD3DXVECTOR3;
```



## <a name="members"></a><span data-ttu-id="78e8c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="78e8c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="78e8c-107">**x**</span><span class="sxs-lookup"><span data-stu-id="78e8c-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="78e8c-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78e8c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="78e8c-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="78e8c-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="78e8c-110">**y**</span><span class="sxs-lookup"><span data-stu-id="78e8c-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="78e8c-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78e8c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="78e8c-112">Componente y.</span><span class="sxs-lookup"><span data-stu-id="78e8c-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="78e8c-113">**z**</span><span class="sxs-lookup"><span data-stu-id="78e8c-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="78e8c-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78e8c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="78e8c-115">Componente z.</span><span class="sxs-lookup"><span data-stu-id="78e8c-115">The z-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78e8c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="78e8c-116">Remarks</span></span>

<span data-ttu-id="78e8c-117">**D3DXVECTOR3 tiene** las siguientes extensiones de C++.</span><span class="sxs-lookup"><span data-stu-id="78e8c-117">**D3DXVECTOR3** has the following C++ extensions.</span></span>

### <a name="d3dxvector3-extensions"></a><span data-ttu-id="78e8c-118">Extensiones D3DXVECTOR3</span><span class="sxs-lookup"><span data-stu-id="78e8c-118">D3DXVECTOR3 Extensions</span></span>


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



## <a name="requirements"></a><span data-ttu-id="78e8c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78e8c-119">Requirements</span></span>



| <span data-ttu-id="78e8c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="78e8c-120">Requirement</span></span> | <span data-ttu-id="78e8c-121">Value</span><span class="sxs-lookup"><span data-stu-id="78e8c-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78e8c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78e8c-122">Header</span></span><br/> | <dl> <span data-ttu-id="78e8c-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="78e8c-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78e8c-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="78e8c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78e8c-125">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="78e8c-125">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
