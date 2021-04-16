---
title: CD3DX12_CLEAR_VALUE estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de valores sin cifrar D3D12 \_ .
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- Estructura de CD3DX12_CLEAR_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_CLEAR_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9dc7afc62c6e9a3e229e6f5bdc4287bf4b85a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649389"
---
# <a name="cd3dx12_clear_value-structure"></a><span data-ttu-id="9aae9-104">CD3DX12 \_ estructura de valor sin borrar \_</span><span class="sxs-lookup"><span data-stu-id="9aae9-104">CD3DX12\_CLEAR\_VALUE structure</span></span>

<span data-ttu-id="9aae9-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ valores sin cifrar D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .</span><span class="sxs-lookup"><span data-stu-id="9aae9-105">A helper structure to enable easy initialization of a [**D3D12\_CLEAR\_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aae9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9aae9-106">Syntax</span></span>


```C++
struct CD3DX12_CLEAR_VALUE  : public D3D12_CLEAR_VALUE{
   CD3DX12_CLEAR_VALUE();
   explicit CD3DX12_CLEAR_VALUE(const D3D12_CLEAR_VALUE &o);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, const FLOAT color[ 4 ]);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, FLOAT depth, UINT8 stencil);
   operator const D3D12_CLEAR_VALUE&() const;
};
```



## <a name="members"></a><span data-ttu-id="9aae9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9aae9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9aae9-108">**CD3DX12 \_ Borrar \_ valor ()**</span><span class="sxs-lookup"><span data-stu-id="9aae9-108">**CD3DX12\_CLEAR\_VALUE()**</span></span>
</dt> <dd>

<span data-ttu-id="9aae9-109">Crea una nueva instancia no inicializada de un \_ valor Clear de CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="9aae9-109">Creates a new, uninitialized, instance of a CD3DX12\_CLEAR\_VALUE.</span></span>

</dd> <dt>

<span data-ttu-id="9aae9-110">**valor Clear de CD3DX12 explícito \_ \_ (const D3D12 \_ Clear \_ Value &o)**</span><span class="sxs-lookup"><span data-stu-id="9aae9-110">**explicit CD3DX12\_CLEAR\_VALUE(const D3D12\_CLEAR\_VALUE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="9aae9-111">Crea una nueva instancia de un valor de CD3DX12 \_ Clear \_ , inicializado con el contenido de otra estructura [**D3D12 \_ Clear \_ Value**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .</span><span class="sxs-lookup"><span data-stu-id="9aae9-111">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initialized with the contents of another [**D3D12\_CLEAR\_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9aae9-112">**CD3DX12 \_ Clear \_ Value ( \_ formato de formato de DXGI, const float color \[ 4 \] )**</span><span class="sxs-lookup"><span data-stu-id="9aae9-112">**CD3DX12\_CLEAR\_VALUE(DXGI\_FORMAT format, const FLOAT color\[ 4 \])**</span></span>
</dt> <dd>

<span data-ttu-id="9aae9-113">Crea una nueva instancia de un valor de CD3DX12 \_ Clear \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="9aae9-113">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initializing the following parameters:</span></span>

<span data-ttu-id="9aae9-114">[**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato</span><span class="sxs-lookup"><span data-stu-id="9aae9-114">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="9aae9-115">Color FLOAT \[ 4 \]</span><span class="sxs-lookup"><span data-stu-id="9aae9-115">FLOAT color\[ 4 \]</span></span>

</dd> <dt>

<span data-ttu-id="9aae9-116">**CD3DX12 \_ Clear \_ Value ( \_ formato de formato de DXGI, profundidad de Float, Galería de símbolos UINT8)**</span><span class="sxs-lookup"><span data-stu-id="9aae9-116">**CD3DX12\_CLEAR\_VALUE(DXGI\_FORMAT format, FLOAT depth, UINT8 stencil)**</span></span>
</dt> <dd>

<span data-ttu-id="9aae9-117">Crea una nueva instancia de un valor de CD3DX12 \_ Clear \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="9aae9-117">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initializing the following parameters:</span></span>

<span data-ttu-id="9aae9-118">[**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato</span><span class="sxs-lookup"><span data-stu-id="9aae9-118">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="9aae9-119">Profundidad de FLOAT</span><span class="sxs-lookup"><span data-stu-id="9aae9-119">FLOAT depth</span></span>

<span data-ttu-id="9aae9-120">Galería de símbolos UINT8</span><span class="sxs-lookup"><span data-stu-id="9aae9-120">UINT8 stencil</span></span>

</dd> <dt>

<span data-ttu-id="9aae9-121">**Operator const D3D12 \_ Clear \_ Value& () Const**</span><span class="sxs-lookup"><span data-stu-id="9aae9-121">**operator const D3D12\_CLEAR\_VALUE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="9aae9-122">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="9aae9-122">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9aae9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aae9-123">Requirements</span></span>



| <span data-ttu-id="9aae9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aae9-124">Requirement</span></span> | <span data-ttu-id="9aae9-125">Value</span><span class="sxs-lookup"><span data-stu-id="9aae9-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9aae9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9aae9-126">Header</span></span><br/> | <dl> <span data-ttu-id="9aae9-127"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aae9-127"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aae9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9aae9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aae9-129">**D3D12 \_ Borrar \_ valor**</span><span class="sxs-lookup"><span data-stu-id="9aae9-129">**D3D12\_CLEAR\_VALUE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[<span data-ttu-id="9aae9-130">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="9aae9-130">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

