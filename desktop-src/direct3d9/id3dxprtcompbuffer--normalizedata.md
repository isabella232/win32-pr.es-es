---
description: Normaliza todos los pesos del análisis de componentes principales (PCA) para que estén entre-1 y 1. Los vectores de base se modifican para reflejar esta normalización.
ms.assetid: f1c87049-a1ec-452e-b556-a2dc95324d5d
title: 'ID3DXPRTCompBuffer:: NormalizeData (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.NormalizeData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9a69dacb25d04b56a14e27a43487911e56a038ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718453"
---
# <a name="id3dxprtcompbuffernormalizedata-method"></a><span data-ttu-id="fc54e-104">ID3DXPRTCompBuffer:: NormalizeData (método)</span><span class="sxs-lookup"><span data-stu-id="fc54e-104">ID3DXPRTCompBuffer::NormalizeData method</span></span>

<span data-ttu-id="fc54e-105">Normaliza todos los pesos del análisis de componentes principales (PCA) para que estén entre-1 y 1.</span><span class="sxs-lookup"><span data-stu-id="fc54e-105">Normalizes all principal component analysis (PCA) weights so that they are between -1 and 1.</span></span> <span data-ttu-id="fc54e-106">Los vectores de base se modifican para reflejar esta normalización.</span><span class="sxs-lookup"><span data-stu-id="fc54e-106">Basis vectors are modified to reflect this normalization.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc54e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc54e-107">Syntax</span></span>


```C++
HRESULT NormalizeData();
```



## <a name="parameters"></a><span data-ttu-id="fc54e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc54e-108">Parameters</span></span>

<span data-ttu-id="fc54e-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fc54e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc54e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc54e-110">Return value</span></span>

<span data-ttu-id="fc54e-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc54e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc54e-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fc54e-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fc54e-113">Si se produce un error en el método, se devolverá el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="fc54e-113">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc54e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc54e-114">Requirements</span></span>



| <span data-ttu-id="fc54e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc54e-115">Requirement</span></span> | <span data-ttu-id="fc54e-116">Value</span><span class="sxs-lookup"><span data-stu-id="fc54e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc54e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc54e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fc54e-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc54e-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fc54e-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc54e-119">Library</span></span><br/> | <dl> <span data-ttu-id="fc54e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc54e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fc54e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc54e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc54e-122">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="fc54e-122">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 




