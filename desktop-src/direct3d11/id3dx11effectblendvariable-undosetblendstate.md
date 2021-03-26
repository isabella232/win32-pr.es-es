---
title: Método ID3DX11EffectBlendVariable UndoSetBlendState (D3dx11effect. h)
description: Revierte un estado de Blend establecido previamente.
ms.assetid: 375c225b-558f-4ad0-81e7-62eff3e28cf1
keywords:
- Método UndoSetBlendState Direct3D 11
- Método UndoSetBlendState Direct3D 11, interfaz ID3DX11EffectBlendVariable
- Interfaz ID3DX11EffectBlendVariable Direct3D 11, método UndoSetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.UndoSetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e117eafa9b6379b2240cf491809c58d8600d840f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998592"
---
# <a name="id3dx11effectblendvariableundosetblendstate-method"></a><span data-ttu-id="f93b5-106">ID3DX11EffectBlendVariable:: UndoSetBlendState (método)</span><span class="sxs-lookup"><span data-stu-id="f93b5-106">ID3DX11EffectBlendVariable::UndoSetBlendState method</span></span>

<span data-ttu-id="f93b5-107">Revierte un estado de Blend establecido previamente.</span><span class="sxs-lookup"><span data-stu-id="f93b5-107">Reverts a previously set blend-state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f93b5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f93b5-108">Syntax</span></span>


```C++
HRESULT UndoSetBlendState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="f93b5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f93b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f93b5-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="f93b5-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="f93b5-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f93b5-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f93b5-112">Índice en una matriz de interfaces de estado de mezcla.</span><span class="sxs-lookup"><span data-stu-id="f93b5-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="f93b5-113">Si solo hay una interfaz de estado de mezcla, use 0.</span><span class="sxs-lookup"><span data-stu-id="f93b5-113">If there is only one blend-state interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f93b5-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f93b5-114">Return value</span></span>

<span data-ttu-id="f93b5-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f93b5-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f93b5-116">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f93b5-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f93b5-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f93b5-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f93b5-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="f93b5-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f93b5-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="f93b5-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f93b5-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f93b5-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f93b5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f93b5-121">Requirements</span></span>



| <span data-ttu-id="f93b5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f93b5-122">Requirement</span></span> | <span data-ttu-id="f93b5-123">Value</span><span class="sxs-lookup"><span data-stu-id="f93b5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f93b5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f93b5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f93b5-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f93b5-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f93b5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f93b5-126">Library</span></span><br/> | <dl> <span data-ttu-id="f93b5-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="f93b5-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f93b5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f93b5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f93b5-129">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="f93b5-129">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

