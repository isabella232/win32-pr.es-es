---
description: Tipo de datos del registro.
ms.assetid: b54530d3-4267-4b41-9a16-59d400ef3e18
title: Enumeración D3DXREGISTER_SET (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXREGISTER_SET
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 683b13d0b386fcdbc162293455e2beb11bc1ee85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707825"
---
# <a name="d3dxregister_set-enumeration"></a><span data-ttu-id="68632-103">\_Enumeración de conjuntos de D3DXREGISTER</span><span class="sxs-lookup"><span data-stu-id="68632-103">D3DXREGISTER\_SET enumeration</span></span>

<span data-ttu-id="68632-104">Tipo de datos del registro.</span><span class="sxs-lookup"><span data-stu-id="68632-104">Data type of the register.</span></span>

## <a name="syntax"></a><span data-ttu-id="68632-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68632-105">Syntax</span></span>


```C++
typedef enum _D3DXREGISTER_SET { 
  D3DXRS_BOOL,
  D3DXRS_INT4,
  D3DXRS_FLOAT4,
  D3DXRS_SAMPLER,
  D3DXRS_FORCE_DWORD  = 0x7fffffff
} D3DXREGISTER_SET, *LPD3DXREGISTER_SET;
```



## <a name="constants"></a><span data-ttu-id="68632-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="68632-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="68632-107"><span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**D3DXRS \_ bool**</span><span class="sxs-lookup"><span data-stu-id="68632-107"><span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**D3DXRS\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="68632-108">Valor booleano.</span><span class="sxs-lookup"><span data-stu-id="68632-108">Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="68632-109"><span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**D3DXRS \_ INT4**</span><span class="sxs-lookup"><span data-stu-id="68632-109"><span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**D3DXRS\_INT4**</span></span>
</dt> <dd>

<span data-ttu-id="68632-110">número entero 4D.</span><span class="sxs-lookup"><span data-stu-id="68632-110">4D integer number.</span></span>

</dd> <dt>

<span data-ttu-id="68632-111"><span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**D3DXRS \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="68632-111"><span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**D3DXRS\_FLOAT4**</span></span>
</dt> <dd>

<span data-ttu-id="68632-112">número de punto flotante 4D.</span><span class="sxs-lookup"><span data-stu-id="68632-112">4D floating-point number.</span></span>

</dd> <dt>

<span data-ttu-id="68632-113"><span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**Muestra de D3DXRS \_**</span><span class="sxs-lookup"><span data-stu-id="68632-113"><span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**D3DXRS\_SAMPLER**</span></span>
</dt> <dd>

<span data-ttu-id="68632-114">El registro contiene datos de muestra 4D.</span><span class="sxs-lookup"><span data-stu-id="68632-114">The register contains 4D sampler data.</span></span>

</dd> <dt>

<span data-ttu-id="68632-115"><span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="68632-115"><span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="68632-116">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="68632-116">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="68632-117">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="68632-117">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="68632-118">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="68632-118">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68632-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68632-119">Requirements</span></span>



| <span data-ttu-id="68632-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="68632-120">Requirement</span></span> | <span data-ttu-id="68632-121">Value</span><span class="sxs-lookup"><span data-stu-id="68632-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="68632-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68632-122">Header</span></span><br/> | <dl> <span data-ttu-id="68632-123"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="68632-123"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68632-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="68632-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68632-125">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="68632-125">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="68632-126">**D3DXSHADER \_ CONSTANTINFO**</span><span class="sxs-lookup"><span data-stu-id="68632-126">**D3DXSHADER\_CONSTANTINFO**</span></span>](d3dxshader-constantinfo.md)
</dt> <dt>

[<span data-ttu-id="68632-127">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="68632-127">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




