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
# <a name="d3dxplane-extensions"></a><span data-ttu-id="cf80f-103">Extensiones de D3DXPLANE</span><span class="sxs-lookup"><span data-stu-id="cf80f-103">D3DXPLANE Extensions</span></span>

<span data-ttu-id="cf80f-104">Proporciona las siguientes sobrecargas de operador y conversiones de tipo para las estructuras [**D3DXPLANE**](d3dxplane.md) .</span><span class="sxs-lookup"><span data-stu-id="cf80f-104">Supplies the following operator overloads and type casts for [**D3DXPLANE**](d3dxplane.md) structures.</span></span>

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

<span data-ttu-id="cf80f-105">Tipos derivados: \* LPD3DXPLANE</span><span class="sxs-lookup"><span data-stu-id="cf80f-105">Derived types: \*LPD3DXPLANE</span></span>

## <a name="remarks"></a><span data-ttu-id="cf80f-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf80f-106">Remarks</span></span>

<span data-ttu-id="cf80f-107">Para obtener más información sobre los miembros de la estructura, consulte [**D3DXPLANE**](d3dxplane.md).</span><span class="sxs-lookup"><span data-stu-id="cf80f-107">For more information about structure members, refer to [**D3DXPLANE**](d3dxplane.md).</span></span>

<span data-ttu-id="cf80f-108">Las sobrecargas de operador y las conversiones de tipo para esta estructura se implementan en d3dx9math. INL.</span><span class="sxs-lookup"><span data-stu-id="cf80f-108">Operator overloads and type casts for this structure are implemented in d3dx9math.inl.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf80f-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf80f-109">Requirements</span></span>



| <span data-ttu-id="cf80f-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf80f-110">Requirement</span></span> | <span data-ttu-id="cf80f-111">Value</span><span class="sxs-lookup"><span data-stu-id="cf80f-111">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf80f-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf80f-112">Header</span></span><br/> | <dl> <span data-ttu-id="cf80f-113"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf80f-113"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf80f-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf80f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf80f-115">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="cf80f-115">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




