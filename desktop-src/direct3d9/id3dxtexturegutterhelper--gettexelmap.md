---
description: Recupera las coordenadas de textura (u, v) de cada textura.
ms.assetid: 7d8eecf8-6344-4a48-8338-b92ebb0ab2ef
title: 'ID3DXTextureGutterHelper:: GetTexelMap (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af401eaa98ac4255b15961477b1ba2316e29edf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362599"
---
# <a name="id3dxtexturegutterhelpergettexelmap-method"></a><span data-ttu-id="5ece7-103">ID3DXTextureGutterHelper:: GetTexelMap (método)</span><span class="sxs-lookup"><span data-stu-id="5ece7-103">ID3DXTextureGutterHelper::GetTexelMap method</span></span>

<span data-ttu-id="5ece7-104">Recupera las coordenadas de textura (u, v) de cada textura.</span><span class="sxs-lookup"><span data-stu-id="5ece7-104">Retrieves the (u, v) texture coordinates of each texel.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ece7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ece7-105">Syntax</span></span>


```C++
HRESULT GetTexelMap(
  [out] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a><span data-ttu-id="5ece7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ece7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ece7-107">*pTexelData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5ece7-107">*pTexelData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ece7-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ece7-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="5ece7-109">Puntero a la ubicación en coordenadas de textura de píxeles (u, v) donde se encuentra cada textura.</span><span class="sxs-lookup"><span data-stu-id="5ece7-109">Pointer to the location in pixel (u, v) texture coordinates where each texel is located.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ece7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ece7-110">Return value</span></span>

<span data-ttu-id="5ece7-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ece7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ece7-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5ece7-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5ece7-113">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="5ece7-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="5ece7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ece7-114">Remarks</span></span>

<span data-ttu-id="5ece7-115">En el caso de las [**clases 2 y 4 textura**](id3dxtexturegutterhelper.md), las coordenadas de textura (u, v) devueltas se corresponden con el punto más cercano del triángulo más cercano.</span><span class="sxs-lookup"><span data-stu-id="5ece7-115">For [**class 2 and 4 texels**](id3dxtexturegutterhelper.md), the returned (u, v) texture coordinates correspond to the closest point on the closest triangle.</span></span>

<span data-ttu-id="5ece7-116">La aplicación debe asignar y administrar pTexelData.</span><span class="sxs-lookup"><span data-stu-id="5ece7-116">The application must allocate and manage pTexelData.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ece7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ece7-117">Requirements</span></span>



| <span data-ttu-id="5ece7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ece7-118">Requirement</span></span> | <span data-ttu-id="5ece7-119">Value</span><span class="sxs-lookup"><span data-stu-id="5ece7-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ece7-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ece7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5ece7-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ece7-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5ece7-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ece7-122">Library</span></span><br/> | <dl> <span data-ttu-id="5ece7-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ece7-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5ece7-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ece7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ece7-125">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="5ece7-125">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




