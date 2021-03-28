---
title: Interfaz ID3DX11EffectMatrixVariable (D3dx11effect. h)
description: Una interfaz de matriz variable tiene acceso a una matriz.
ms.assetid: 44f30d1a-3ec1-49d7-92c0-475cf2fa4d2a
keywords:
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5c4c89a231d429fc0a1f8fecbcbb4d06db35cb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987042"
---
# <a name="id3dx11effectmatrixvariable-interface"></a><span data-ttu-id="eae24-105">Interfaz ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="eae24-105">ID3DX11EffectMatrixVariable interface</span></span>

<span data-ttu-id="eae24-106">Una interfaz de matriz variable tiene acceso a una matriz.</span><span class="sxs-lookup"><span data-stu-id="eae24-106">A matrix-variable interface accesses a matrix.</span></span>

## <a name="members"></a><span data-ttu-id="eae24-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="eae24-107">Members</span></span>

<span data-ttu-id="eae24-108">La interfaz **ID3DX11EffectMatrixVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="eae24-108">The **ID3DX11EffectMatrixVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="eae24-109">**ID3DX11EffectMatrixVariable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eae24-109">**ID3DX11EffectMatrixVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="eae24-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="eae24-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eae24-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="eae24-111">Methods</span></span>

<span data-ttu-id="eae24-112">La interfaz **ID3DX11EffectMatrixVariable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="eae24-112">The **ID3DX11EffectMatrixVariable** interface has these methods.</span></span>



| <span data-ttu-id="eae24-113">Método</span><span class="sxs-lookup"><span data-stu-id="eae24-113">Method</span></span>                                                                                 | <span data-ttu-id="eae24-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="eae24-114">Description</span></span>                                                       |
|:---------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="eae24-115">**GetMatrix**</span><span class="sxs-lookup"><span data-stu-id="eae24-115">**GetMatrix**</span></span>](id3dx11effectmatrixvariable-getmatrix.md)                             | <span data-ttu-id="eae24-116">Obtiene una matriz.</span><span class="sxs-lookup"><span data-stu-id="eae24-116">Get a matrix.</span></span><br/>                                          |
| [<span data-ttu-id="eae24-117">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="eae24-117">**GetMatrixArray**</span></span>](id3dx11effectmatrixvariable-getmatrixarray.md)                   | <span data-ttu-id="eae24-118">Obtiene una matriz de matrices.</span><span class="sxs-lookup"><span data-stu-id="eae24-118">Get an array of matrices.</span></span><br/>                              |
| [<span data-ttu-id="eae24-119">**GetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="eae24-119">**GetMatrixTranspose**</span></span>](id3dx11effectmatrixvariable-getmatrixtranspose.md)           | <span data-ttu-id="eae24-120">Transponer y obtener una matriz de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="eae24-120">Transpose and get a floating-point matrix.</span></span><br/>             |
| [<span data-ttu-id="eae24-121">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="eae24-121">**GetMatrixTransposeArray**</span></span>](id3dx11effectmatrixvariable-getmatrixtransposearray.md) | <span data-ttu-id="eae24-122">Transponer y obtener una matriz de matrices de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="eae24-122">Transpose and get an array of floating-point matrices.</span></span><br/> |
| [<span data-ttu-id="eae24-123">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="eae24-123">**SetMatrix**</span></span>](id3dx11effectmatrixvariable-setmatrix.md)                             | <span data-ttu-id="eae24-124">Establezca una matriz de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="eae24-124">Set a floating-point matrix.</span></span><br/>                           |
| [<span data-ttu-id="eae24-125">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="eae24-125">**SetMatrixArray**</span></span>](id3dx11effectmatrixvariable-setmatrixarray.md)                   | <span data-ttu-id="eae24-126">Establezca una matriz de matrices de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="eae24-126">Set an array of floating-point matrices.</span></span><br/>               |
| [<span data-ttu-id="eae24-127">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="eae24-127">**SetMatrixTranspose**</span></span>](id3dx11effectmatrixvariable-setmatrixtranspose.md)           | <span data-ttu-id="eae24-128">Transponer y establecer una matriz de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="eae24-128">Transpose and set a floating-point matrix.</span></span><br/>             |
| [<span data-ttu-id="eae24-129">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="eae24-129">**SetMatrixTransposeArray**</span></span>](id3dx11effectmatrixvariable-setmatrixtransposearray.md) | <span data-ttu-id="eae24-130">Transponer y establecer una matriz de matrices de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="eae24-130">Transpose and set an array of floating-point matrices.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eae24-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eae24-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eae24-132">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="eae24-132">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="eae24-133">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="eae24-133">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="eae24-134">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="eae24-134">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eae24-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eae24-135">Requirements</span></span>



| <span data-ttu-id="eae24-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="eae24-136">Requirement</span></span> | <span data-ttu-id="eae24-137">Value</span><span class="sxs-lookup"><span data-stu-id="eae24-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eae24-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eae24-138">Header</span></span><br/>  | <dl> <span data-ttu-id="eae24-139"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="eae24-139"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="eae24-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eae24-140">Library</span></span><br/> | <dl> <span data-ttu-id="eae24-141"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="eae24-141"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eae24-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="eae24-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eae24-143">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="eae24-143">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="eae24-144">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="eae24-144">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="eae24-145">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="eae24-145">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





