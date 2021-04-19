---
description: Aplica los datos de medianil de textura almacenados a un búfer de textura de ID3DXPRTBuffer.
ms.assetid: 05cc0709-543a-4df5-980a-8549451d396b
title: 'ID3DXPRTBuffer:: EvalGH (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.EvalGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23896ff2514db7b5e12b164ea0c0a763b5d1d3b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708118"
---
# <a name="id3dxprtbufferevalgh-method"></a><span data-ttu-id="59cb5-103">ID3DXPRTBuffer:: EvalGH (método)</span><span class="sxs-lookup"><span data-stu-id="59cb5-103">ID3DXPRTBuffer::EvalGH method</span></span>

<span data-ttu-id="59cb5-104">Aplica los datos de medianil de textura almacenados a un búfer de textura de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="59cb5-104">Applies stored texture gutter data to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="59cb5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59cb5-105">Syntax</span></span>


```C++
HRESULT EvalGH();
```



## <a name="parameters"></a><span data-ttu-id="59cb5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59cb5-106">Parameters</span></span>

<span data-ttu-id="59cb5-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="59cb5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59cb5-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59cb5-108">Return value</span></span>

<span data-ttu-id="59cb5-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59cb5-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59cb5-110">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59cb5-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="59cb5-111">Si se produce un error en el método, se devolverá el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="59cb5-111">If the method fails, the following value will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="59cb5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59cb5-112">Remarks</span></span>

<span data-ttu-id="59cb5-113">Este método realiza una llamada interna a [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) para recuperar y aplicar los datos de medianil de textura.</span><span class="sxs-lookup"><span data-stu-id="59cb5-113">This method makes an internal call to [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) to retrieve and apply texture gutter data.</span></span>

## <a name="requirements"></a><span data-ttu-id="59cb5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59cb5-114">Requirements</span></span>



| <span data-ttu-id="59cb5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="59cb5-115">Requirement</span></span> | <span data-ttu-id="59cb5-116">Value</span><span class="sxs-lookup"><span data-stu-id="59cb5-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59cb5-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59cb5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="59cb5-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="59cb5-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="59cb5-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59cb5-119">Library</span></span><br/> | <dl> <span data-ttu-id="59cb5-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59cb5-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="59cb5-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="59cb5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59cb5-122">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="59cb5-122">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 




