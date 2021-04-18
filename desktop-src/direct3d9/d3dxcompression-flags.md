---
description: Define el modo de compresión utilizado para almacenar los datos de conjuntos de animación comprimidos.
ms.assetid: 41592b71-52ba-4727-a885-fb10fc23c5f8
title: Enumeración D3DXCOMPRESSION_FLAGS (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOMPRESSION_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 6f912c44659d418d543194ba82a9d82f31e7ef08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718266"
---
# <a name="d3dxcompression_flags-enumeration"></a><span data-ttu-id="4b1f8-103">\_Enumeración de marcas D3DXCOMPRESSION</span><span class="sxs-lookup"><span data-stu-id="4b1f8-103">D3DXCOMPRESSION\_FLAGS enumeration</span></span>

<span data-ttu-id="4b1f8-104">Define el modo de compresión utilizado para almacenar los datos de conjuntos de animación comprimidos.</span><span class="sxs-lookup"><span data-stu-id="4b1f8-104">Defines the compression mode used for storing compressed animation set data.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b1f8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b1f8-105">Syntax</span></span>


```C++
typedef enum D3DXCOMPRESSION_FLAGS { 
  D3DXCOMPRESS_DEFAULT      = 0,
  D3DXCOMPRESS_STRONG       = 1,
  D3DXCOMPRESS_FORCE_DWORD  = 0x7fffffff
} D3DXCOMPRESSION_FLAGS, *LPD3DXCOMPRESSION_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="4b1f8-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="4b1f8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4b1f8-107"><span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**\_Valor predeterminado de D3DXCOMPRESS**</span><span class="sxs-lookup"><span data-stu-id="4b1f8-107"><span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="4b1f8-108">Implementa la compresión rápida.</span><span class="sxs-lookup"><span data-stu-id="4b1f8-108">Implements fast compression.</span></span>

</dd> <dt>

<span data-ttu-id="4b1f8-109"><span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS \_ Strong**</span><span class="sxs-lookup"><span data-stu-id="4b1f8-109"><span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS\_STRONG**</span></span>
</dt> <dd>

<span data-ttu-id="4b1f8-110">Implementa la compresión lenta.</span><span class="sxs-lookup"><span data-stu-id="4b1f8-110">Implements slow compression.</span></span> <span data-ttu-id="4b1f8-111">Normalmente da como resultado un conjunto de animaciones comprimidas de mejor calidad que si \_ se usa el valor predeterminado D3DXCOMPRESS.</span><span class="sxs-lookup"><span data-stu-id="4b1f8-111">Typically results in a better quality compressed animation set than if D3DXCOMPRESS\_DEFAULT is used.</span></span>

</dd> <dt>

<span data-ttu-id="4b1f8-112"><span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b1f8-112"><span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="4b1f8-113">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="4b1f8-113">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="4b1f8-114">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4b1f8-114">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="4b1f8-115">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4b1f8-115">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b1f8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b1f8-116">Requirements</span></span>



| <span data-ttu-id="4b1f8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b1f8-117">Requirement</span></span> | <span data-ttu-id="4b1f8-118">Value</span><span class="sxs-lookup"><span data-stu-id="4b1f8-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b1f8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b1f8-119">Header</span></span><br/> | <dl> <span data-ttu-id="4b1f8-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b1f8-120"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b1f8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b1f8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b1f8-122">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="4b1f8-122">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




