---
title: Método ID3DX11EffectDepthStencilVariable UndoSetDepthStencilState (D3dx11effect. h)
description: Revierte un estado de estarcido de profundidad establecido previamente.
ms.assetid: 558bc777-a520-4235-84d3-db2d9f1ce4b6
keywords:
- Método UndoSetDepthStencilState Direct3D 11
- Método UndoSetDepthStencilState Direct3D 11, interfaz ID3DX11EffectDepthStencilVariable
- Interfaz ID3DX11EffectDepthStencilVariable Direct3D 11, método UndoSetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.UndoSetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd44d486d2613406617f0534046c54818267dd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998647"
---
# <a name="id3dx11effectdepthstencilvariableundosetdepthstencilstate-method"></a><span data-ttu-id="594a8-106">ID3DX11EffectDepthStencilVariable:: UndoSetDepthStencilState (método)</span><span class="sxs-lookup"><span data-stu-id="594a8-106">ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState method</span></span>

<span data-ttu-id="594a8-107">Revierte un estado de estarcido de profundidad establecido previamente.</span><span class="sxs-lookup"><span data-stu-id="594a8-107">Reverts a previously set depth stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="594a8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="594a8-108">Syntax</span></span>


```C++
HRESULT UndoSetDepthStencilState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="594a8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="594a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="594a8-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="594a8-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="594a8-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="594a8-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="594a8-112">Índice en una matriz de interfaces de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="594a8-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="594a8-113">Si solo hay una interfaz de estarcido de profundidad, use 0.</span><span class="sxs-lookup"><span data-stu-id="594a8-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="594a8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="594a8-114">Return value</span></span>

<span data-ttu-id="594a8-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="594a8-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="594a8-116">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="594a8-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="594a8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="594a8-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="594a8-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="594a8-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="594a8-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="594a8-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="594a8-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="594a8-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="594a8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="594a8-121">Requirements</span></span>



| <span data-ttu-id="594a8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="594a8-122">Requirement</span></span> | <span data-ttu-id="594a8-123">Value</span><span class="sxs-lookup"><span data-stu-id="594a8-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="594a8-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="594a8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="594a8-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="594a8-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="594a8-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="594a8-126">Library</span></span><br/> | <dl> <span data-ttu-id="594a8-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="594a8-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="594a8-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="594a8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="594a8-129">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="594a8-129">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

