---
title: CD3DX12_RT_FORMAT_ARRAY estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de \_ matriz de formato D3D12 RT \_ .
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- Estructura de CD3DX12_RT_FORMAT_ARRAY
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05b7ae9e51d2d6b2a43f45dc83bda2074f6b734
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718486"
---
# <a name="cd3dx12_rt_format_array-structure"></a><span data-ttu-id="3ba8c-104">Estructura de la matriz de formato CD3DX12 \_ RT \_ \_</span><span class="sxs-lookup"><span data-stu-id="3ba8c-104">CD3DX12\_RT\_FORMAT\_ARRAY structure</span></span>

<span data-ttu-id="3ba8c-105">Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ matriz de \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="3ba8c-105">A helper structure to enable easy initialization of a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ba8c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ba8c-106">Syntax</span></span>


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a><span data-ttu-id="3ba8c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3ba8c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3ba8c-108">**\_Matriz de formato CD3DX12 RT \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="3ba8c-108">**CD3DX12\_RT\_FORMAT\_ARRAY()**</span></span>
</dt> <dd>

<span data-ttu-id="3ba8c-109">Crea una nueva instancia no inicializada de una \_ matriz de formato RT de CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3ba8c-109">Creates a new, uninitialized, instance of a CD3DX12\_RT\_FORMAT\_ARRAY.</span></span>

</dd> <dt>

<span data-ttu-id="3ba8c-110">**matriz de \_ formato RT CD3DX12 explícita \_ \_ (const D3D12 \_ RT \_ format \_ array& o)**</span><span class="sxs-lookup"><span data-stu-id="3ba8c-110">**explicit CD3DX12\_RT\_FORMAT\_ARRAY(const D3D12\_RT\_FORMAT\_ARRAY& o)**</span></span>
</dt> <dd>

<span data-ttu-id="3ba8c-111">Crea una nueva instancia de una \_ matriz de formato CD3DX12 RT \_ \_ , inicializada con los valores copiados de una estructura de [**\_ \_ \_ matriz de formato D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="3ba8c-111">Creates a new instance of a CD3DX12\_RT\_FORMAT\_ARRAY, initialized with values copied from a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3ba8c-112">**matriz de \_ formato RT CD3DX12 explícita \_ \_ (const DXGI \_ format \* pFormats, uint NumFormats)**</span><span class="sxs-lookup"><span data-stu-id="3ba8c-112">**explicit CD3DX12\_RT\_FORMAT\_ARRAY(const DXGI\_FORMAT\* pFormats, UINT NumFormats)**</span></span>
</dt> <dd>

<span data-ttu-id="3ba8c-113">Crea una nueva instancia de una \_ matriz de formato CD3DX12 RT \_ \_ , inicializada con los valores pasados en la lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="3ba8c-113">Creates a new instance of a CD3DX12\_RT\_FORMAT\_ARRAY, initialized with the values passed in the parameter list.</span></span> <span data-ttu-id="3ba8c-114">El contenido de la matriz especificado por el parámetro *pFormats* se copia en la matriz de miembros **RTFormats**.</span><span class="sxs-lookup"><span data-stu-id="3ba8c-114">Contents of the array specified by the *pFormats* parameter are copied into the member array **RTFormats**.</span></span> <span data-ttu-id="3ba8c-115">Se supone que la matriz especificada por *pFormats* tiene el mismo tamaño que **RTFormats**.</span><span class="sxs-lookup"><span data-stu-id="3ba8c-115">The array specified by *pFormats* is assumed to have the same size as **RTFormats**.</span></span>

</dd> <dt>

<span data-ttu-id="3ba8c-116">**Operator const D3D12 \_ RT \_ FORMAT \_ array& () Const**</span><span class="sxs-lookup"><span data-stu-id="3ba8c-116">**operator const D3D12\_RT\_FORMAT\_ARRAY&() const**</span></span>
</dt> <dd>

<span data-ttu-id="3ba8c-117">Conversión implícita a una estructura de [**\_ matriz de \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="3ba8c-117">Implicit conversion to a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span> <span data-ttu-id="3ba8c-118">Dado que \_ \_ \_ la matriz de formato D3D12 RT es el tipo subyacente de la \_ Galería de símbolos de profundidad CD3DX12 \_ \_ DESC1, el objeto simplemente se devuelve como una referencia de matriz de formato const D3D12 \_ RT \_ \_ a sí misma.</span><span class="sxs-lookup"><span data-stu-id="3ba8c-118">Because D3D12\_RT\_FORMAT\_ARRAY is the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, the object is simply returned as a const D3D12\_RT\_FORMAT\_ARRAY reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ba8c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ba8c-119">Requirements</span></span>



| <span data-ttu-id="3ba8c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ba8c-120">Requirement</span></span> | <span data-ttu-id="3ba8c-121">Value</span><span class="sxs-lookup"><span data-stu-id="3ba8c-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba8c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ba8c-122">Header</span></span><br/> | <dl> <span data-ttu-id="3ba8c-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ba8c-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ba8c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ba8c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba8c-125">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="3ba8c-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="3ba8c-126">**\_Matriz de \_ formato D3D12 RT \_**</span><span class="sxs-lookup"><span data-stu-id="3ba8c-126">**D3D12\_RT\_FORMAT\_ARRAY**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





