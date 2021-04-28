---
description: 'Estructura D3DXMATRIXA16 (D3dx9math.h): matriz alineada en 4x4 y 16 bytes que contiene métodos y sobrecargas de operadores.'
ms.assetid: c7082fe5-f98b-4ab7-b8c2-7cdbab4848ad
title: Estructura D3DXMATRIXA16 (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIXA16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 7bb14f23d041ec2634b9710d5620382d8b93da2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094213"
---
# <a name="d3dxmatrixa16-structure-d3dx9mathh"></a><span data-ttu-id="3da40-103">Estructura D3DXMATRIXA16 (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="3da40-103">D3DXMATRIXA16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="3da40-104">Matriz de 4x4 y 16 bytes alineada que contiene métodos y sobrecargas de operadores.</span><span class="sxs-lookup"><span data-stu-id="3da40-104">A 4x4, 16-byte-aligned matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="3da40-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3da40-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a><span data-ttu-id="3da40-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3da40-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3da40-107">**\_Ij**</span><span class="sxs-lookup"><span data-stu-id="3da40-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="3da40-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3da40-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3da40-109">Componente (i, j) de la matriz, donde i es el número de fila y j es el número de columna.</span><span class="sxs-lookup"><span data-stu-id="3da40-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="3da40-110">Por ejemplo, 34 significa lo mismo que a₃₄ , el componente de \_ la tercera fila y la cuarta \[ \] columna.</span><span class="sxs-lookup"><span data-stu-id="3da40-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3da40-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3da40-111">Remarks</span></span>

<span data-ttu-id="3da40-112">Una matriz alineada de 16 bytes, cuando la usan las funciones matemáticas D3DX, se ha optimizado para mejorar el rendimiento en procesadores Intel Pentium 4.</span><span class="sxs-lookup"><span data-stu-id="3da40-112">A 16-byte aligned matrix, when used by D3DX math functions, has been optimized for improved performance on Intel Pentium 4 processors.</span></span> <span data-ttu-id="3da40-113">Las matrices se alinean independientemente de dónde se creen: en la pila del programa, en el montón o en el ámbito global.</span><span class="sxs-lookup"><span data-stu-id="3da40-113">Matrices are aligned independent of where they are created: on the program stack, in the heap, or in global scope.</span></span> <span data-ttu-id="3da40-114">La alineación se realiza mediante \_ \_ declspec(align(16)), que funciona con Visual C++ .NET y con Visual C++ 6.0 solo cuando se instala el paquete de procesador.</span><span class="sxs-lookup"><span data-stu-id="3da40-114">Alignment is accomplished using \_\_declspec(align(16)), which works with Visual C++ .NET and with Visual C++ 6.0 only when the processor pack is installed.</span></span> <span data-ttu-id="3da40-115">Desafortunadamente, no hay ninguna manera de detectar el paquete de procesador, por lo que la alineación de bytes está activada de forma predeterminada solo con Visual C++ .NET.</span><span class="sxs-lookup"><span data-stu-id="3da40-115">Unfortunately, there is no way to detect the processor pack, so byte alignment is turned on by default only with Visual C++ .NET.</span></span>

<span data-ttu-id="3da40-116">Los vectores y cuaterniones no están alineados en bytes en D3DX.</span><span class="sxs-lookup"><span data-stu-id="3da40-116">Vectors and quaternions are not byte aligned in D3DX.</span></span> <span data-ttu-id="3da40-117">Al usar vectores y cuaterniones con funciones matemáticas D3DX, use declspec(align(16)) para generar vectores y cuaterniones alineados con bytes, ya que tendrán un rendimiento considerablemente \_ mejor.</span><span class="sxs-lookup"><span data-stu-id="3da40-117">When using vectors and quaternions with D3DX math functions, use \_declspec(align(16)) to generate byte aligned vectors and quaternions, because they will perform significantly better.</span></span> <span data-ttu-id="3da40-118">La definición \_ de declspec se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="3da40-118">The definition of \_declspec is shown here.</span></span>


```
#define D3DX_ALIGN16 __declspec(align(16))
```



<span data-ttu-id="3da40-119">Otros compiladores interpretan D3DXMATRIXA16 como D3DXMATRIX.</span><span class="sxs-lookup"><span data-stu-id="3da40-119">Other compilers interpret D3DXMATRIXA16 as D3DXMATRIX.</span></span> <span data-ttu-id="3da40-120">El uso de esta estructura en un compilador que no alinea realmente la matriz puede ser problemático porque no expondrá errores que omiten la alineación.</span><span class="sxs-lookup"><span data-stu-id="3da40-120">Using this structure on a compiler that does not actually align the matrix can be problematic because it will not expose bugs that ignore alignment.</span></span> <span data-ttu-id="3da40-121">Por ejemplo, si un objeto D3DXMATRIXA16 está dentro de una estructura o clase, se podría realizar [**una memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) con empaquetado estricto (omitiendo los límites de 16 bytes).</span><span class="sxs-lookup"><span data-stu-id="3da40-121">For example, if a D3DXMATRIXA16 object is inside a structure or class, a [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) might be done with tight packing (ignoring 16-byte boundaries).</span></span> <span data-ttu-id="3da40-122">Esto provocaría interrupciones de compilación si el compilador agregara alguna vez la alineación de la matriz.</span><span class="sxs-lookup"><span data-stu-id="3da40-122">This would cause build breaks if the compiler were to sometime add matrix aligning.</span></span>

### <a name="d3dxmatrixa16"></a><span data-ttu-id="3da40-123">D3DXMATRIXA16</span><span class="sxs-lookup"><span data-stu-id="3da40-123">D3DXMATRIXA16</span></span>

<span data-ttu-id="3da40-124">**D3DXMATRIXA16 tiene** las siguientes extensiones de C++.</span><span class="sxs-lookup"><span data-stu-id="3da40-124">**D3DXMATRIXA16** has the following C++ extensions.</span></span>


```
typedef struct _D3DXMATRIXA16 : public D3DXMATRIX
{
    _D3DXMATRIXA16();
    _D3DXMATRIXA16( CONST FLOAT * f);
    _D3DXMATRIXA16( CONST D3DMATRIX& m);
    _D3DXMATRIXA16( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                    FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                    FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                    FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );
    void* operator new(size_t s);
    void* operator new[](size_t s);

    // The two operators below are not virtual operators. If you cast
    //   to D3DXMATRIX, do not delete using them
    void operator delete(void* p);
    void operator delete[](void* p);

    struct _D3DXMATRIXA16& operator=(CONST D3DXMATRIX& rhs);
} _D3DXMATRIXA16;

typedef D3DX_ALIGN16 _D3DXMATRIXA16 D3DXMATRIXA16, *LPD3DXMATRIXA16;
        
```



## <a name="requirements"></a><span data-ttu-id="3da40-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3da40-125">Requirements</span></span>



| <span data-ttu-id="3da40-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3da40-126">Requirement</span></span> | <span data-ttu-id="3da40-127">Value</span><span class="sxs-lookup"><span data-stu-id="3da40-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3da40-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3da40-128">Header</span></span><br/> | <dl> <span data-ttu-id="3da40-129"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="3da40-129"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3da40-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3da40-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da40-131">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="3da40-131">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="3da40-132">**D3DXMATRIX**</span><span class="sxs-lookup"><span data-stu-id="3da40-132">**D3DXMATRIX**</span></span>](d3dxmatrix.md)
</dt> </dl>

 

 
