---
title: CD3DX12_ROOT_CONSTANTS estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de constantes raíz D3D12 \_ .
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- Estructura de CD3DX12_ROOT_CONSTANTS
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_CONSTANTS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a1f81a429b083400adad60f316cc90c4ede1d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717604"
---
# <a name="cd3dx12_root_constants-structure"></a><span data-ttu-id="f208d-104">CD3DX12 \_ \_ estructura de constantes raíz</span><span class="sxs-lookup"><span data-stu-id="f208d-104">CD3DX12\_ROOT\_CONSTANTS structure</span></span>

<span data-ttu-id="f208d-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ constantes raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="f208d-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f208d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f208d-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_CONSTANTS  : public D3D12_ROOT_CONSTANTS{
       CD3DX12_ROOT_CONSTANTS();
       explicit CD3DX12_ROOT_CONSTANTS(const D3D12_ROOT_CONSTANTS &o);
       CD3DX12_ROOT_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="f208d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f208d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f208d-108">**\_Constantes raíz CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="f208d-108">**CD3DX12\_ROOT\_CONSTANTS()**</span></span>
</dt> <dd>

<span data-ttu-id="f208d-109">Crea una nueva instancia no inicializada de una \_ constante raíz CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="f208d-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_CONSTANTS.</span></span>

</dd> <dt>

<span data-ttu-id="f208d-110">**constantes de raíz CD3DX12 explícitas \_ \_ (constantes de raíz const D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="f208d-110">**explicit CD3DX12\_ROOT\_CONSTANTS(const D3D12\_ROOT\_CONSTANTS &o)**</span></span>
</dt> <dd>

<span data-ttu-id="f208d-111">Crea una nueva instancia de una \_ constante raíz CD3DX12 \_ , inicializada con el contenido de otra estructura [**de \_ \_ constantes raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="f208d-111">Creates a new instance of a CD3DX12\_ROOT\_CONSTANTS, initialized with the contents of another [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f208d-112">**\_Constantes raíz CD3DX12 \_ (uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="f208d-112">**CD3DX12\_ROOT\_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="f208d-113">Crea una nueva instancia de una \_ constante CD3DX12 raíz \_ , inicializando los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="f208d-113">Creates a new instance of a CD3DX12\_ROOT\_CONSTANTS, initializing the following parameters:</span></span>

<span data-ttu-id="f208d-114">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="f208d-114">UINT num32BitValues</span></span>

<span data-ttu-id="f208d-115">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="f208d-115">UINT shaderRegister</span></span>

<span data-ttu-id="f208d-116">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="f208d-116">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="f208d-117">**Init en línea (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="f208d-117">**inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="f208d-118">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="f208d-118">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="f208d-119">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="f208d-119">UINT num32BitValues</span></span>

<span data-ttu-id="f208d-120">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="f208d-120">UINT shaderRegister</span></span>

<span data-ttu-id="f208d-121">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="f208d-121">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="f208d-122">**Init inline init (D3D12 \_ root \_ constants &ROOTCONSTANTS, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="f208d-122">**static inline Init(D3D12\_ROOT\_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="f208d-123">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="f208d-123">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="f208d-124">[**D3D12 \_ \_Constantes raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants</span><span class="sxs-lookup"><span data-stu-id="f208d-124">[**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants</span></span>

<span data-ttu-id="f208d-125">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="f208d-125">UINT num32BitValues</span></span>

<span data-ttu-id="f208d-126">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="f208d-126">UINT shaderRegister</span></span>

<span data-ttu-id="f208d-127">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="f208d-127">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f208d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f208d-128">Requirements</span></span>



| <span data-ttu-id="f208d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f208d-129">Requirement</span></span> | <span data-ttu-id="f208d-130">Value</span><span class="sxs-lookup"><span data-stu-id="f208d-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f208d-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f208d-131">Header</span></span><br/> | <dl> <span data-ttu-id="f208d-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f208d-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f208d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f208d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f208d-134">**\_Constantes raíz \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="f208d-134">**D3D12\_ROOT\_CONSTANTS**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[<span data-ttu-id="f208d-135">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="f208d-135">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





