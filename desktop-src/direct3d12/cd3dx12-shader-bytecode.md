---
title: CD3DX12_SHADER_BYTECODE estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de código de bytes del sombreador D3D12 \_ .
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- Estructura de CD3DX12_SHADER_BYTECODE
topic_type:
- apiref
api_name:
- CD3DX12_SHADER_BYTECODE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227c18913492d6533b08f49f5761fab1b93e97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717597"
---
# <a name="cd3dx12_shader_bytecode-structure"></a><span data-ttu-id="58332-104">CD3DX12 \_ estructura de código de byte del sombreador \_</span><span class="sxs-lookup"><span data-stu-id="58332-104">CD3DX12\_SHADER\_BYTECODE structure</span></span>

<span data-ttu-id="58332-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ código de \_ bytes del sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="58332-105">A helper structure to enable easy initialization of a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="58332-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58332-106">Syntax</span></span>


```C++
struct CD3DX12_SHADER_BYTECODE  : public D3D12_SHADER_BYTECODE{
   CD3DX12_SHADER_BYTECODE();
   explicit CD3DX12_SHADER_BYTECODE(const D3D12_SHADER_BYTECODE &o);
   CD3DX12_SHADER_BYTECODE(ID3DBlob* pShaderBlob);
   CD3DX12_SHADER_BYTECODE(const void* _pShaderBytecode, SIZE_T bytecodeLength);
   operator const D3D12_SHADER_BYTECODE&() const;
};
```



## <a name="members"></a><span data-ttu-id="58332-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="58332-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="58332-108">**\_ \_ Código de bytes del sombreador CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="58332-108">**CD3DX12\_SHADER\_BYTECODE()**</span></span>
</dt> <dd>

<span data-ttu-id="58332-109">Crea una nueva instancia no inicializada de un \_ código de bytes de sombreador CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="58332-109">Creates a new, uninitialized, instance of a CD3DX12\_SHADER\_BYTECODE.</span></span>

</dd> <dt>

<span data-ttu-id="58332-110">**código de \_ bytes del sombreador CD3DX12 explícito \_ (const D3D12 \_ sombreador de \_ bytes &o)**</span><span class="sxs-lookup"><span data-stu-id="58332-110">**explicit CD3DX12\_SHADER\_BYTECODE(const D3D12\_SHADER\_BYTECODE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="58332-111">Crea una nueva instancia de un \_ código de bytes de sombreador CD3DX12 \_ , inicializada con el contenido de otra estructura de [**código de \_ \_ bytes del sombreador de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="58332-111">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initialized with the contents of another [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="58332-112">**\_Código de bytes del sombreador de CD3DX12 \_ (ID3DBlob \* pShaderBlob)**</span><span class="sxs-lookup"><span data-stu-id="58332-112">**CD3DX12\_SHADER\_BYTECODE(ID3DBlob\* pShaderBlob)**</span></span>
</dt> <dd>

<span data-ttu-id="58332-113">Crea una nueva instancia de un \_ código de bytes de sombreador CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="58332-113">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initializing the following parameters:</span></span>

<span data-ttu-id="58332-114">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* pShaderBlob</span><span class="sxs-lookup"><span data-stu-id="58332-114">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))\* pShaderBlob</span></span>

</dd> <dt>

<span data-ttu-id="58332-115">**\_ \_ Código de bytes del sombreador CD3DX12 (const void \* \_ PShaderBytecode, size \_ T bytecodeLength)**</span><span class="sxs-lookup"><span data-stu-id="58332-115">**CD3DX12\_SHADER\_BYTECODE(const void\* \_pShaderBytecode, SIZE\_T bytecodeLength)**</span></span>
</dt> <dd>

<span data-ttu-id="58332-116">Crea una nueva instancia de un \_ código de bytes de sombreador CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="58332-116">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initializing the following parameters:</span></span>

<span data-ttu-id="58332-117">void \* \_ pShaderBytecode</span><span class="sxs-lookup"><span data-stu-id="58332-117">void\* \_pShaderBytecode</span></span>

<span data-ttu-id="58332-118">TAMAÑO \_ T bytecodeLength</span><span class="sxs-lookup"><span data-stu-id="58332-118">SIZE\_T bytecodeLength</span></span>

</dd> <dt>

<span data-ttu-id="58332-119">**operador const D3D12 \_ código de \_ byte del sombreador& () Const**</span><span class="sxs-lookup"><span data-stu-id="58332-119">**operator const D3D12\_SHADER\_BYTECODE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="58332-120">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="58332-120">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58332-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58332-121">Requirements</span></span>



| <span data-ttu-id="58332-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="58332-122">Requirement</span></span> | <span data-ttu-id="58332-123">Value</span><span class="sxs-lookup"><span data-stu-id="58332-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="58332-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58332-124">Header</span></span><br/> | <dl> <span data-ttu-id="58332-125"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="58332-125"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58332-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="58332-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58332-127">**\_Código de bytes del sombreador D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="58332-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[<span data-ttu-id="58332-128">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="58332-128">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

