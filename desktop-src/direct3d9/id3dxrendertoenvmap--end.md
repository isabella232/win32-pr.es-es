---
description: Restaure todos los destinos de representación y, si es necesario, componga todas las caras representadas en la superficie del mapa del entorno.
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: 'ID3DXRenderToEnvMap:: end (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20e62a9d794738ae81ae84a665165f6034958f0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362512"
---
# <a name="id3dxrendertoenvmapend-method"></a><span data-ttu-id="c1aa8-103">ID3DXRenderToEnvMap:: end (método)</span><span class="sxs-lookup"><span data-stu-id="c1aa8-103">ID3DXRenderToEnvMap::End method</span></span>

<span data-ttu-id="c1aa8-104">Restaure todos los destinos de representación y, si es necesario, componga todas las caras representadas en la superficie del mapa del entorno.</span><span class="sxs-lookup"><span data-stu-id="c1aa8-104">Restore all render targets and, if needed, compose all the rendered faces into the environment map surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1aa8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1aa8-105">Syntax</span></span>


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="c1aa8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1aa8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1aa8-107">*MipFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1aa8-107">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1aa8-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1aa8-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1aa8-109">Combinación válida de una o más marcas [de \_ filtro de D3DX](d3dx-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="c1aa8-109">A valid combination of one or more [D3DX\_FILTER](d3dx-filter.md) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1aa8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1aa8-110">Return value</span></span>

<span data-ttu-id="c1aa8-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c1aa8-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c1aa8-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c1aa8-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c1aa8-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c1aa8-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1aa8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1aa8-114">Requirements</span></span>



| <span data-ttu-id="c1aa8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1aa8-115">Requirement</span></span> | <span data-ttu-id="c1aa8-116">Value</span><span class="sxs-lookup"><span data-stu-id="c1aa8-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1aa8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1aa8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c1aa8-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa8-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c1aa8-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1aa8-119">Library</span></span><br/> | <dl> <span data-ttu-id="c1aa8-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa8-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1aa8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1aa8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1aa8-122">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="c1aa8-122">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="c1aa8-123">**ID3DXRenderToEnvMap:: facial**</span><span class="sxs-lookup"><span data-stu-id="c1aa8-123">**ID3DXRenderToEnvMap::Face**</span></span>](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 
