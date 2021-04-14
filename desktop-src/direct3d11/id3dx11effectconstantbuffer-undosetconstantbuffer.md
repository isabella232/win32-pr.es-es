---
title: Método ID3DX11EffectConstantBuffer UndoSetConstantBuffer (D3dx11effect. h)
description: Revierte un búfer de constantes previamente establecido.
ms.assetid: 6c5e1256-3a92-4bfe-8614-f09d627bc3db
keywords:
- Método UndoSetConstantBuffer Direct3D 11
- Método UndoSetConstantBuffer Direct3D 11, interfaz ID3DX11EffectConstantBuffer
- Interfaz ID3DX11EffectConstantBuffer Direct3D 11, método UndoSetConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.UndoSetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c95a26f1ea92d5bfe1975e3fe4dc1961046e5535
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424491"
---
# <a name="id3dx11effectconstantbufferundosetconstantbuffer-method"></a><span data-ttu-id="7ec9b-106">ID3DX11EffectConstantBuffer:: UndoSetConstantBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="7ec9b-106">ID3DX11EffectConstantBuffer::UndoSetConstantBuffer method</span></span>

<span data-ttu-id="7ec9b-107">Revierte un búfer de constantes previamente establecido.</span><span class="sxs-lookup"><span data-stu-id="7ec9b-107">Reverts a previously set constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec9b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ec9b-108">Syntax</span></span>


```C++
HRESULT UndoSetConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="7ec9b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ec9b-109">Parameters</span></span>

<span data-ttu-id="7ec9b-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7ec9b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7ec9b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ec9b-111">Return value</span></span>

<span data-ttu-id="7ec9b-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ec9b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ec9b-113">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7ec9b-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ec9b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ec9b-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7ec9b-115">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="7ec9b-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7ec9b-116">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="7ec9b-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7ec9b-117">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7ec9b-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ec9b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ec9b-118">Requirements</span></span>



| <span data-ttu-id="7ec9b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ec9b-119">Requirement</span></span> | <span data-ttu-id="7ec9b-120">Value</span><span class="sxs-lookup"><span data-stu-id="7ec9b-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec9b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ec9b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7ec9b-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ec9b-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7ec9b-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ec9b-123">Library</span></span><br/> | <dl> <span data-ttu-id="7ec9b-124"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="7ec9b-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ec9b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ec9b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec9b-126">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="7ec9b-126">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





