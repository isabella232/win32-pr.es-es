---
description: Preparar un dispositivo para dibujar sprites.
ms.assetid: cffe5ac3-eeee-4ece-afcc-04a476b75863
title: 'ID3DX10Sprite:: Begin (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Begin
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ede2995f72eb1200e68f035119643a362e15701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280412"
---
# <a name="id3dx10spritebegin-method"></a><span data-ttu-id="ade51-103">ID3DX10Sprite:: Begin (método)</span><span class="sxs-lookup"><span data-stu-id="ade51-103">ID3DX10Sprite::Begin method</span></span>

<span data-ttu-id="ade51-104">Preparar un dispositivo para dibujar sprites.</span><span class="sxs-lookup"><span data-stu-id="ade51-104">Prepare a device for drawing sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="ade51-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ade51-105">Syntax</span></span>


```C++
HRESULT Begin(
  [in] UINT flags
);
```



## <a name="parameters"></a><span data-ttu-id="ade51-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ade51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ade51-107">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ade51-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ade51-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ade51-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ade51-109">Marcas que controlan cómo se dibujarán los sprites.</span><span class="sxs-lookup"><span data-stu-id="ade51-109">Flags that control how the sprites will be drawn.</span></span> <span data-ttu-id="ade51-110">Vea [**D3DX10 \_ Sprite \_ Flag**](d3dx10-sprite-flag.md).</span><span class="sxs-lookup"><span data-stu-id="ade51-110">See [**D3DX10\_SPRITE\_FLAG**](d3dx10-sprite-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ade51-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ade51-111">Return value</span></span>

<span data-ttu-id="ade51-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ade51-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ade51-113">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ade51-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ade51-114">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ade51-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ade51-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ade51-115">Remarks</span></span>

<span data-ttu-id="ade51-116">Cada llamada a Begin debe coincidir con una llamada a [**ID3DX10Sprite:: end**](id3dx10sprite-end.md).</span><span class="sxs-lookup"><span data-stu-id="ade51-116">Every call to Begin must be matched with a call to [**ID3DX10Sprite::End**](id3dx10sprite-end.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ade51-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ade51-117">Requirements</span></span>



| <span data-ttu-id="ade51-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ade51-118">Requirement</span></span> | <span data-ttu-id="ade51-119">Value</span><span class="sxs-lookup"><span data-stu-id="ade51-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ade51-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ade51-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ade51-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ade51-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ade51-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ade51-122">Library</span></span><br/> | <dl> <span data-ttu-id="ade51-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ade51-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ade51-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ade51-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ade51-125">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="ade51-125">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="ade51-126">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="ade51-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
