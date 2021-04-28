---
description: 'Estructura D3DXVECTOR2 (D3dx9math.h): describe un vector de dos componentes que incluye sobrecargas de operador y conversión de tipos.'
ms.assetid: e61ec1c8-00b5-491f-8fb1-be97218f6c68
title: Estructura D3DXVECTOR2 (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR2
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 79f66c0e9130a320042c9b914bad47e5f02f0d8a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097613"
---
# <a name="d3dxvector2-structure-d3dx9mathh"></a><span data-ttu-id="df4f0-103">Estructura D3DXVECTOR2 (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="df4f0-103">D3DXVECTOR2 structure (D3dx9math.h)</span></span>

<span data-ttu-id="df4f0-104">Describe un vector de dos componentes que incluye sobrecargas de operador y conversión de tipos.</span><span class="sxs-lookup"><span data-stu-id="df4f0-104">Describes a two-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="df4f0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df4f0-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR2 {
  FLOAT x;
  FLOAT y;
} D3DXVECTOR2, *LPD3DXVECTOR2;
```



## <a name="members"></a><span data-ttu-id="df4f0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="df4f0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="df4f0-107">**x**</span><span class="sxs-lookup"><span data-stu-id="df4f0-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="df4f0-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df4f0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="df4f0-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="df4f0-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="df4f0-110">**y**</span><span class="sxs-lookup"><span data-stu-id="df4f0-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="df4f0-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df4f0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="df4f0-112">Componente y.</span><span class="sxs-lookup"><span data-stu-id="df4f0-112">The y-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df4f0-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="df4f0-113">Remarks</span></span>

### <a name="d3dxvector2-extensions"></a><span data-ttu-id="df4f0-114">Extensiones D3DXVECTOR2</span><span class="sxs-lookup"><span data-stu-id="df4f0-114">D3DXVECTOR2 Extensions</span></span>

<span data-ttu-id="df4f0-115">D3DXVECTOR2 tiene las siguientes extensiones de C++.</span><span class="sxs-lookup"><span data-stu-id="df4f0-115">D3DXVECTOR2 has the following C++ extensions.</span></span>


```
typedef struct D3DXVECTOR2
{
#ifdef __cplusplus
public:
    D3DXVECTOR2() {};
    D3DXVECTOR2( CONST FLOAT * );
    D3DXVECTOR2( CONST D3DXFLOAT16 * );
    D3DXVECTOR2( FLOAT x, FLOAT y );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR2& operator += ( CONST D3DXVECTOR2& );
    D3DXVECTOR2& operator -= ( CONST D3DXVECTOR2& );
    D3DXVECTOR2& operator *= ( FLOAT );
    D3DXVECTOR2& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR2 operator + () const;
    D3DXVECTOR2 operator - () const;

    // binary operators
    D3DXVECTOR2 operator + ( CONST D3DXVECTOR2& ) const;
    D3DXVECTOR2 operator - ( CONST D3DXVECTOR2& ) const;
    D3DXVECTOR2 operator * ( FLOAT ) const;
    D3DXVECTOR2 operator / ( FLOAT ) const;

    friend D3DXVECTOR2 operator * ( FLOAT, CONST D3DXVECTOR2& );

    BOOL operator == ( CONST D3DXVECTOR2& ) const;
    BOOL operator != ( CONST D3DXVECTOR2& ) const;


public:
#endif //__cplusplus
    FLOAT x, y;
} D3DXVECTOR2, *LPD3DXVECTOR2;

typedef struct D3DXVECTOR2_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR2_16F() {};
    D3DXVECTOR2_16F( CONST FLOAT * );
    D3DXVECTOR2_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR2_16F( CONST D3DXFLOAT16 &x, CONST D3DXFLOAT16 &y );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR2_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR2_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y;

} D3DXVECTOR2_16F, *LPD3DXVECTOR2_16F;
        
```



## <a name="requirements"></a><span data-ttu-id="df4f0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df4f0-116">Requirements</span></span>



| <span data-ttu-id="df4f0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="df4f0-117">Requirement</span></span> | <span data-ttu-id="df4f0-118">Value</span><span class="sxs-lookup"><span data-stu-id="df4f0-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df4f0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df4f0-119">Header</span></span><br/> | <dl> <span data-ttu-id="df4f0-120"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="df4f0-120"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df4f0-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="df4f0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df4f0-122">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="df4f0-122">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
