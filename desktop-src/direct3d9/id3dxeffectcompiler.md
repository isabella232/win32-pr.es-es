---
description: La interfaz ID3DXEffectCompiler compila un efecto a partir de una función o de un sombreador de vértices.
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: Interfaz ID3DXEffectCompiler (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d69cbcd6c14bb3a874a382f46fe5aee6619b8168
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362468"
---
# <a name="id3dxeffectcompiler-interface"></a><span data-ttu-id="f712c-103">Interfaz ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="f712c-103">ID3DXEffectCompiler interface</span></span>

<span data-ttu-id="f712c-104">La interfaz **ID3DXEffectCompiler** compila un efecto a partir de una función o de un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="f712c-104">The **ID3DXEffectCompiler** interface compiles an effect from a function or from a vertex shader.</span></span>

## <a name="members"></a><span data-ttu-id="f712c-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="f712c-105">Members</span></span>

<span data-ttu-id="f712c-106">La interfaz **ID3DXEffectCompiler** hereda de [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="f712c-106">The **ID3DXEffectCompiler** interface inherits from [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span> <span data-ttu-id="f712c-107">**ID3DXEffectCompiler** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f712c-107">**ID3DXEffectCompiler** also has these types of members:</span></span>

-   [<span data-ttu-id="f712c-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="f712c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f712c-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="f712c-109">Methods</span></span>

<span data-ttu-id="f712c-110">La interfaz **ID3DXEffectCompiler** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f712c-110">The **ID3DXEffectCompiler** interface has these methods.</span></span>



| <span data-ttu-id="f712c-111">Método</span><span class="sxs-lookup"><span data-stu-id="f712c-111">Method</span></span>                                                      | <span data-ttu-id="f712c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f712c-112">Description</span></span>                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f712c-113">**CompileEffect**</span><span class="sxs-lookup"><span data-stu-id="f712c-113">**CompileEffect**</span></span>](id3dxeffectcompiler--compileeffect.md) | <span data-ttu-id="f712c-114">Compilar un efecto.</span><span class="sxs-lookup"><span data-stu-id="f712c-114">Compile an effect.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="f712c-115">**CompileShader**</span><span class="sxs-lookup"><span data-stu-id="f712c-115">**CompileShader**</span></span>](id3dxeffectcompiler--compileshader.md) | <span data-ttu-id="f712c-116">Compila un sombreador a partir de un efecto que contiene una o más funciones.</span><span class="sxs-lookup"><span data-stu-id="f712c-116">Compiles a shader from an effect that contains one or more functions.</span></span><br/>                                                            |
| [<span data-ttu-id="f712c-117">**GetLiteral**</span><span class="sxs-lookup"><span data-stu-id="f712c-117">**GetLiteral**</span></span>](id3dxeffectcompiler--getliteral.md)       | <span data-ttu-id="f712c-118">Obtiene un estado literal de un parámetro.</span><span class="sxs-lookup"><span data-stu-id="f712c-118">Gets a literal status of a parameter.</span></span> <span data-ttu-id="f712c-119">Un parámetro literal tiene un valor que no cambia durante la vigencia de un efecto.</span><span class="sxs-lookup"><span data-stu-id="f712c-119">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span><br/>      |
| [<span data-ttu-id="f712c-120">**SetLiteral**</span><span class="sxs-lookup"><span data-stu-id="f712c-120">**SetLiteral**</span></span>](id3dxeffectcompiler--setliteral.md)       | <span data-ttu-id="f712c-121">Alterna el estado literal de un parámetro.</span><span class="sxs-lookup"><span data-stu-id="f712c-121">Toggles the literal status of a parameter.</span></span> <span data-ttu-id="f712c-122">Un parámetro literal tiene un valor que no cambia durante la vigencia de un efecto.</span><span class="sxs-lookup"><span data-stu-id="f712c-122">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f712c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f712c-123">Remarks</span></span>

<span data-ttu-id="f712c-124">La interfaz ID3DXEffectCompiler se obtiene llamando a [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)o [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).</span><span class="sxs-lookup"><span data-stu-id="f712c-124">The ID3DXEffectCompiler interface is obtained by calling [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md), or [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).</span></span>

<span data-ttu-id="f712c-125">El tipo LPD3DXEFFECTCOMPILER se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="f712c-125">The LPD3DXEFFECTCOMPILER type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a><span data-ttu-id="f712c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f712c-126">Requirements</span></span>



| <span data-ttu-id="f712c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f712c-127">Requirement</span></span> | <span data-ttu-id="f712c-128">Value</span><span class="sxs-lookup"><span data-stu-id="f712c-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f712c-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f712c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f712c-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f712c-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f712c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f712c-131">Library</span></span><br/> | <dl> <span data-ttu-id="f712c-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f712c-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f712c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f712c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f712c-134">**ID3DXBaseEffect**</span><span class="sxs-lookup"><span data-stu-id="f712c-134">**ID3DXBaseEffect**</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="f712c-135">Interfaces de efectos</span><span class="sxs-lookup"><span data-stu-id="f712c-135">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f712c-136">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="f712c-136">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="f712c-137">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="f712c-137">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="f712c-138">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="f712c-138">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 




