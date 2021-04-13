---
title: Método ID3DX11EffectVariable GetParentConstantBuffer (D3dx11effect. h)
description: Obtiene un búfer de constantes. | Método ID3DX11EffectVariable GetParentConstantBuffer (D3dx11effect. h)
ms.assetid: 43b46b05-951e-4c52-8bc7-4bb5f657ea78
keywords:
- Método GetParentConstantBuffer Direct3D 11
- Método GetParentConstantBuffer Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, método GetParentConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetParentConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa424b91b72dca5539fd0f96a1380e86d1f23f58
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998725"
---
# <a name="id3dx11effectvariablegetparentconstantbuffer-method"></a><span data-ttu-id="ec357-107">ID3DX11EffectVariable:: GetParentConstantBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="ec357-107">ID3DX11EffectVariable::GetParentConstantBuffer method</span></span>

<span data-ttu-id="ec357-108">Obtiene un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="ec357-108">Get a constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec357-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec357-109">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetParentConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="ec357-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec357-110">Parameters</span></span>

<span data-ttu-id="ec357-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ec357-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec357-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec357-112">Return value</span></span>

<span data-ttu-id="ec357-113">Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ec357-113">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="ec357-114">Un puntero a un [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ec357-114">A pointer to a [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ec357-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec357-115">Remarks</span></span>

<span data-ttu-id="ec357-116">Las variables de efecto son de lectura o escritura en un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="ec357-116">Effect variables are read-from or written-to a constant buffer.</span></span>

> [!Note]  
> <span data-ttu-id="ec357-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="ec357-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ec357-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="ec357-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ec357-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ec357-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ec357-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec357-120">Requirements</span></span>



| <span data-ttu-id="ec357-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec357-121">Requirement</span></span> | <span data-ttu-id="ec357-122">Value</span><span class="sxs-lookup"><span data-stu-id="ec357-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec357-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec357-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ec357-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec357-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ec357-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec357-125">Library</span></span><br/> | <dl> <span data-ttu-id="ec357-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="ec357-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec357-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec357-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec357-128">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="ec357-128">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





