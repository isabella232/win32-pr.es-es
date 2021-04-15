---
description: Establece las coordenadas de textura (u, v) de cada textura.
ms.assetid: b1f8f5d6-568f-4868-87c9-9d6b1034d898
title: 'ID3DXTextureGutterHelper:: SetTexelMap (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ee00394e81dadf147d54dffe0dc02199b2274e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708034"
---
# <a name="id3dxtexturegutterhelpersettexelmap-method"></a><span data-ttu-id="b2730-103">ID3DXTextureGutterHelper:: SetTexelMap (método)</span><span class="sxs-lookup"><span data-stu-id="b2730-103">ID3DXTextureGutterHelper::SetTexelMap method</span></span>

<span data-ttu-id="b2730-104">Establece las coordenadas de textura (u, v) de cada textura.</span><span class="sxs-lookup"><span data-stu-id="b2730-104">Sets the (u, v) texture coordinates of each texel.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2730-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2730-105">Syntax</span></span>


```C++
HRESULT SetTexelMap(
  [in] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a><span data-ttu-id="b2730-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2730-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2730-107">*pTexelData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2730-107">*pTexelData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2730-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="b2730-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="b2730-109">Puntero a la ubicación en coordenadas de textura de píxeles (u, v) donde se encuentra cada textura.</span><span class="sxs-lookup"><span data-stu-id="b2730-109">Pointer to the location in pixel (u, v) texture coordinates where each texel is located.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2730-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2730-110">Return value</span></span>

<span data-ttu-id="b2730-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2730-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2730-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b2730-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b2730-113">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="b2730-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="b2730-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2730-114">Requirements</span></span>



| <span data-ttu-id="b2730-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2730-115">Requirement</span></span> | <span data-ttu-id="b2730-116">Value</span><span class="sxs-lookup"><span data-stu-id="b2730-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2730-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2730-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b2730-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2730-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b2730-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2730-119">Library</span></span><br/> | <dl> <span data-ttu-id="b2730-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2730-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b2730-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2730-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2730-122">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="b2730-122">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




