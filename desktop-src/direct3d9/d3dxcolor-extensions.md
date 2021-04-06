---
description: Proporciona las siguientes sobrecargas de operador y conversiones de tipo para las estructuras D3DXCOLOR.
ms.assetid: 89780c6f-c78b-4ebe-876a-6dbc37b598ef
title: Extensiones de D3DXCOLOR (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 7f457332f371b2c452a465c5b831774488301c6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914765"
---
# <a name="d3dxcolor-extensions"></a><span data-ttu-id="fd695-103">Extensiones de D3DXCOLOR</span><span class="sxs-lookup"><span data-stu-id="fd695-103">D3DXCOLOR Extensions</span></span>

<span data-ttu-id="fd695-104">Proporciona las siguientes sobrecargas de operador y conversiones de tipo para las estructuras [**D3DXCOLOR**](d3dxcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="fd695-104">Supplies the following operator overloads and type casts for [**D3DXCOLOR**](d3dxcolor.md) structures.</span></span>

``` syntax
typedef struct D3DXCOLOR
{
#ifdef __cplusplus
public:
    D3DXCOLOR() {}
    D3DXCOLOR( DWORD argb );
    D3DXCOLOR( CONST FLOAT * );
    D3DXCOLOR( CONST D3DXFLOAT16 * );
    D3DXCOLOR( CONST D3DCOLORVALUE& );
    D3DXCOLOR( FLOAT r, FLOAT g, FLOAT b, FLOAT a );

    // casting
    operator DWORD () const;

    operator FLOAT* ();
    operator CONST FLOAT* () const;

    operator D3DCOLORVALUE* ();
    operator CONST D3DCOLORVALUE* () const;

    operator D3DCOLORVALUE& ();
    operator CONST D3DCOLORVALUE& () const;

    // assignment operators
    D3DXCOLOR& operator += ( CONST D3DXCOLOR& );
    D3DXCOLOR& operator -= ( CONST D3DXCOLOR& );
    D3DXCOLOR& operator *= ( FLOAT );
    D3DXCOLOR& operator /= ( FLOAT );

    // unary operators
    D3DXCOLOR operator + () const;
    D3DXCOLOR operator - () const;

    // binary operators
    D3DXCOLOR operator + ( CONST D3DXCOLOR& ) const;
    D3DXCOLOR operator - ( CONST D3DXCOLOR& ) const;
    D3DXCOLOR operator * ( FLOAT ) const;
    D3DXCOLOR operator / ( FLOAT ) const;

    friend D3DXCOLOR operator * ( FLOAT, CONST D3DXCOLOR& );

    BOOL operator == ( CONST D3DXCOLOR& ) const;
    BOOL operator != ( CONST D3DXCOLOR& ) const;

#endif //__cplusplus
    FLOAT r, g, b, a;
} D3DXCOLOR, *LPD3DXCOLOR;
```

<span data-ttu-id="fd695-105">Tipos derivados: \* LPD3DXCOLOR</span><span class="sxs-lookup"><span data-stu-id="fd695-105">Derived types: \*LPD3DXCOLOR</span></span>

## <a name="members"></a><span data-ttu-id="fd695-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd695-106">Members</span></span>

<span data-ttu-id="fd695-107">Para obtener más información sobre los miembros de la estructura, consulte [**D3DXCOLOR**](d3dxcolor.md).</span><span class="sxs-lookup"><span data-stu-id="fd695-107">For more information about structure members, refer to [**D3DXCOLOR**](d3dxcolor.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd695-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd695-108">Remarks</span></span>

<span data-ttu-id="fd695-109">Las sobrecargas de operador y las conversiones de tipo para esta estructura se implementan en d3dx9math. INL.</span><span class="sxs-lookup"><span data-stu-id="fd695-109">Operator overloads and type casts for this structure are implemented in d3dx9math.inl.</span></span>

> [!Note]  
> <span data-ttu-id="fd695-110">El constructor D3DXCOLOR () se bloquea en tiempo de ejecución cuando se ejecuta en modo de depuración en Microsoft Visual Studio 2010 con la opción del compilador de [comprobaciones de errores en tiempo de ejecución (/RTCc)](/previous-versions/visualstudio/visual-studio-2010/8wtf2dfz(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="fd695-110">The D3DXCOLOR() constructor crashes at runtime when you run it in debug mode in Microsoft Visual Studio 2010 with the [Run-Time Error Checks (/RTCc)](/previous-versions/visualstudio/visual-studio-2010/8wtf2dfz(v=vs.100)) compiler option.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fd695-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd695-111">Requirements</span></span>



| <span data-ttu-id="fd695-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd695-112">Requirement</span></span> | <span data-ttu-id="fd695-113">Value</span><span class="sxs-lookup"><span data-stu-id="fd695-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd695-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd695-114">Header</span></span><br/> | <dl> <span data-ttu-id="fd695-115"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd695-115"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd695-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd695-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd695-117">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="fd695-117">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
