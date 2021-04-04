---
description: Tipo del objeto.
ms.assetid: ab405984-2ebc-4514-9400-bdb13676eda5
title: Enumeración D3DXPARAMETER_CLASS (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_CLASS
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: c42bfc9335c38de04ab484193a1e178a122f2210
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914701"
---
# <a name="d3dxparameter_class-enumeration"></a><span data-ttu-id="37a59-103">\_Enumeración de clases D3DXPARAMETER</span><span class="sxs-lookup"><span data-stu-id="37a59-103">D3DXPARAMETER\_CLASS enumeration</span></span>

<span data-ttu-id="37a59-104">Tipo del objeto.</span><span class="sxs-lookup"><span data-stu-id="37a59-104">The type of object.</span></span>

## <a name="syntax"></a><span data-ttu-id="37a59-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37a59-105">Syntax</span></span>


```C++
typedef enum D3DXPARAMETER_CLASS { 
  D3DXPC_SCALAR,
  D3DXPC_VECTOR,
  D3DXPC_MATRIX_ROWS,
  D3DXPC_MATRIX_COLUMNS,
  D3DXPC_OBJECT,
  D3DXPC_STRUCT,
  D3DXPC_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_CLASS, *LPD3DXPARAMETER_CLASS;
```



## <a name="constants"></a><span data-ttu-id="37a59-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="37a59-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="37a59-107"><span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**\_Escalar D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="37a59-107"><span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**D3DXPC\_SCALAR**</span></span>
</dt> <dd>

<span data-ttu-id="37a59-108">Constant es un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="37a59-108">Constant is a scalar.</span></span>

</dd> <dt>

<span data-ttu-id="37a59-109"><span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**\_Vector D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="37a59-109"><span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**D3DXPC\_VECTOR**</span></span>
</dt> <dd>

<span data-ttu-id="37a59-110">Constant es un vector.</span><span class="sxs-lookup"><span data-stu-id="37a59-110">Constant is a vector.</span></span>

</dd> <dt>

<span data-ttu-id="37a59-111"><span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**Filas de la \_ matriz D3DXPC \_**</span><span class="sxs-lookup"><span data-stu-id="37a59-111"><span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**D3DXPC\_MATRIX\_ROWS**</span></span>
</dt> <dd>

<span data-ttu-id="37a59-112">Constant es una matriz principal de fila.</span><span class="sxs-lookup"><span data-stu-id="37a59-112">Constant is a row major matrix.</span></span>

</dd> <dt>

<span data-ttu-id="37a59-113"><span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**Columnas de la \_ matriz D3DXPC \_**</span><span class="sxs-lookup"><span data-stu-id="37a59-113"><span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**D3DXPC\_MATRIX\_COLUMNS**</span></span>
</dt> <dd>

<span data-ttu-id="37a59-114">Constant es una matriz principal de columna.</span><span class="sxs-lookup"><span data-stu-id="37a59-114">Constant is a column major matrix.</span></span>

</dd> <dt>

<span data-ttu-id="37a59-115"><span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**\_Objeto D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="37a59-115"><span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**D3DXPC\_OBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="37a59-116">Constant es una textura, un sombreador o una cadena.</span><span class="sxs-lookup"><span data-stu-id="37a59-116">Constant is either a texture, shader, or a string.</span></span>

</dd> <dt>

<span data-ttu-id="37a59-117"><span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**\_Struct D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="37a59-117"><span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**D3DXPC\_STRUCT**</span></span>
</dt> <dd>

<span data-ttu-id="37a59-118">Constant es una estructura.</span><span class="sxs-lookup"><span data-stu-id="37a59-118">Constant is a structure.</span></span>

</dd> <dt>

<span data-ttu-id="37a59-119"><span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="37a59-119"><span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="37a59-120">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="37a59-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="37a59-121">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="37a59-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="37a59-122">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="37a59-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37a59-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37a59-123">Requirements</span></span>



| <span data-ttu-id="37a59-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="37a59-124">Requirement</span></span> | <span data-ttu-id="37a59-125">Value</span><span class="sxs-lookup"><span data-stu-id="37a59-125">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a59-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37a59-126">Header</span></span><br/> | <dl> <span data-ttu-id="37a59-127"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="37a59-127"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37a59-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="37a59-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37a59-129">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="37a59-129">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="37a59-130">**D3DXSHADER \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="37a59-130">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="37a59-131">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="37a59-131">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




