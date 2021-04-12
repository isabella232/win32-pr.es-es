---
description: Matriz de 4x4, de 16 bytes alineada que contiene métodos y sobrecargas de operador.
ms.assetid: d9e9c1cc-7555-4011-a4b4-8cce20404841
title: Estructura D3DXMATRIXA16 (D3DX10Math. h)
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
- D3DX10Math.h
ms.openlocfilehash: a33b5efa0e5e714c0b161fed8191702066a44b01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280472"
---
# <a name="d3dxmatrixa16-structure-d3dx10mathh"></a><span data-ttu-id="ee24b-103">Estructura D3DXMATRIXA16 (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="ee24b-103">D3DXMATRIXA16 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="ee24b-104">Matriz de 4x4, de 16 bytes alineada que contiene métodos y sobrecargas de operador.</span><span class="sxs-lookup"><span data-stu-id="ee24b-104">A 4x4, 16-byte-aligned matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee24b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee24b-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a><span data-ttu-id="ee24b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ee24b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ee24b-107">**\_ij**</span><span class="sxs-lookup"><span data-stu-id="ee24b-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="ee24b-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee24b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ee24b-109">El componente (i, j) de la matriz, donde i es el número de fila y j es el número de columna.</span><span class="sxs-lookup"><span data-stu-id="ee24b-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="ee24b-110">Por ejemplo, \_ 34 significa lo mismo que \[ ₃ ₄ \] , el componente de la tercera fila y la cuarta columna.</span><span class="sxs-lookup"><span data-stu-id="ee24b-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee24b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee24b-111">Remarks</span></span>

<span data-ttu-id="ee24b-112">Una matriz alineada de 16 bytes, cuando se usa en las funciones matemáticas de D3DX, se ha optimizado para mejorar el rendimiento de los procesadores Intel Pentium 4.</span><span class="sxs-lookup"><span data-stu-id="ee24b-112">A 16-byte aligned matrix, when used by D3DX math functions, has been optimized for improved performance on Intel Pentium 4 processors.</span></span> <span data-ttu-id="ee24b-113">Las matrices se alinean independientemente de dónde se crean: en la pila del programa, en el montón o en el ámbito global.</span><span class="sxs-lookup"><span data-stu-id="ee24b-113">Matrices are aligned independent of where they are created: on the program stack, in the heap, or in global scope.</span></span> <span data-ttu-id="ee24b-114">La alineación se logra mediante \_ \_ declspec (Align (16)), que funciona con Visual C++ .net y con Visual C++ 6,0 solo cuando se instala el paquete de procesadores.</span><span class="sxs-lookup"><span data-stu-id="ee24b-114">Alignment is accomplished using \_\_declspec(align(16)), which works with Visual C++ .NET and with Visual C++ 6.0 only when the processor pack is installed.</span></span> <span data-ttu-id="ee24b-115">Desafortunadamente, no hay ninguna manera de detectar el paquete de procesadores, por lo que la alineación de bytes está activada de forma predeterminada solo con Visual C++ .NET.</span><span class="sxs-lookup"><span data-stu-id="ee24b-115">Unfortunately, there is no way to detect the processor pack, so byte alignment is turned on by default only with Visual C++ .NET.</span></span>

<span data-ttu-id="ee24b-116">Los vectores y cuaterniones no están alineados en bytes en D3DX.</span><span class="sxs-lookup"><span data-stu-id="ee24b-116">Vectors and quaternions are not byte aligned in D3DX.</span></span> <span data-ttu-id="ee24b-117">Al usar vectores y cuaterniones con funciones matemáticas de D3DX, use \_ declspec (Align (16)) para generar vectores alineados de bytes y cuaterniones, ya que se realizarán de forma mucho mejor.</span><span class="sxs-lookup"><span data-stu-id="ee24b-117">When using vectors and quaternions with D3DX math functions, use \_declspec(align(16)) to generate byte aligned vectors and quaternions, because they will perform significantly better.</span></span> <span data-ttu-id="ee24b-118">\_Aquí se muestra la definición de declspec.</span><span class="sxs-lookup"><span data-stu-id="ee24b-118">The definition of \_declspec is shown here.</span></span>


```
#define D3DX_ALIGN16 __declspec(align(16))
```



<span data-ttu-id="ee24b-119">Otros compiladores interpretan **D3DXMATRIXA16** como [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="ee24b-119">Other compilers interpret **D3DXMATRIXA16** as [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span> <span data-ttu-id="ee24b-120">El uso de esta estructura en un compilador que no alinee realmente la matriz puede ser problemático, ya que no expondrá errores que omitan la alineación.</span><span class="sxs-lookup"><span data-stu-id="ee24b-120">Using this structure on a compiler that does not actually align the matrix can be problematic because it will not expose bugs that ignore alignment.</span></span> <span data-ttu-id="ee24b-121">Por ejemplo, si un objeto **D3DXMATRIXA16** está dentro de una estructura o una clase, se puede hacer un [memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) con un empaquetado estrecho (omitiendo los límites de 16 bytes).</span><span class="sxs-lookup"><span data-stu-id="ee24b-121">For example, if a **D3DXMATRIXA16** object is inside a structure or class, a [memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) might be done with tight packing (ignoring 16-byte boundaries).</span></span> <span data-ttu-id="ee24b-122">Esto provocaría saltos de compilación si el compilador estuviera en algún momento agregar alineación de matriz.</span><span class="sxs-lookup"><span data-stu-id="ee24b-122">This would cause build breaks if the compiler were to sometime add matrix aligning.</span></span>

### <a name="d3dxmatrixa16-extensions"></a><span data-ttu-id="ee24b-123">Extensiones de D3DXMATRIXA16</span><span class="sxs-lookup"><span data-stu-id="ee24b-123">D3DXMATRIXA16 Extensions</span></span>

<span data-ttu-id="ee24b-124">**D3DXMATRIXA16** tiene las siguientes extensiones de C++.</span><span class="sxs-lookup"><span data-stu-id="ee24b-124">**D3DXMATRIXA16** has the following C++ extensions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ee24b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee24b-125">Requirements</span></span>



| <span data-ttu-id="ee24b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee24b-126">Requirement</span></span> | <span data-ttu-id="ee24b-127">Value</span><span class="sxs-lookup"><span data-stu-id="ee24b-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee24b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee24b-128">Header</span></span><br/> | <dl> <span data-ttu-id="ee24b-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee24b-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee24b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee24b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee24b-131">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="ee24b-131">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
