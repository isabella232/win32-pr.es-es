---
description: Inicia el dibujo de cada una de las caras de un mapa de entorno.
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: 'ID3DXRenderToEnvMap:: facial (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 452933c0d85a7aad2987011796ff47eff41dc32b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821482"
---
# <a name="id3dxrendertoenvmapface-method"></a><span data-ttu-id="d78c8-103">ID3DXRenderToEnvMap:: facial (método)</span><span class="sxs-lookup"><span data-stu-id="d78c8-103">ID3DXRenderToEnvMap::Face method</span></span>

<span data-ttu-id="d78c8-104">Inicia el dibujo de cada una de las caras de un mapa de entorno.</span><span class="sxs-lookup"><span data-stu-id="d78c8-104">Initiate the drawing of each face of an environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="d78c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d78c8-105">Syntax</span></span>


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="d78c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d78c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d78c8-107">*Caras* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d78c8-107">*Face* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d78c8-108">Tipo: **[ **D3DCUBEMAP \_ caras**](./d3dcubemap-faces.md)**</span><span class="sxs-lookup"><span data-stu-id="d78c8-108">Type: **[**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md)**</span></span>

<span data-ttu-id="d78c8-109">Primera superficie del mapa de cubo del entorno.</span><span class="sxs-lookup"><span data-stu-id="d78c8-109">The first face of the environmental cube map.</span></span> <span data-ttu-id="d78c8-110">Vea [**\_ caras de D3DCUBEMAP**](./d3dcubemap-faces.md).</span><span class="sxs-lookup"><span data-stu-id="d78c8-110">See [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md).</span></span>

</dd> <dt>

<span data-ttu-id="d78c8-111">*MipFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d78c8-111">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d78c8-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d78c8-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d78c8-113">Combinación válida de una o más marcas [de \_ filtro de D3DX](d3dx-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="d78c8-113">A valid combination of one or more [D3DX\_FILTER](d3dx-filter.md) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d78c8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d78c8-114">Return value</span></span>

<span data-ttu-id="d78c8-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d78c8-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d78c8-116">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d78c8-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d78c8-117">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d78c8-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d78c8-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d78c8-118">Remarks</span></span>

<span data-ttu-id="d78c8-119">Se debe llamar a este método una vez para cada tipo de asignación de entorno.</span><span class="sxs-lookup"><span data-stu-id="d78c8-119">This method must be called once for each type of environment map.</span></span> <span data-ttu-id="d78c8-120">La única excepción es un mapa de entorno cúbico que requiere que se llame a este método seis veces, una vez para cada cara de D3DCUBEMAP \_ caras.</span><span class="sxs-lookup"><span data-stu-id="d78c8-120">The only exception is a cubic environment map which requires this method to be called six times, once for each face in D3DCUBEMAP\_FACES.</span></span> <span data-ttu-id="d78c8-121">Para obtener más información, vea [asignación de entorno (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="d78c8-121">For more information, see [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d78c8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d78c8-122">Requirements</span></span>



| <span data-ttu-id="d78c8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d78c8-123">Requirement</span></span> | <span data-ttu-id="d78c8-124">Value</span><span class="sxs-lookup"><span data-stu-id="d78c8-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d78c8-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d78c8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d78c8-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d78c8-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d78c8-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d78c8-127">Library</span></span><br/> | <dl> <span data-ttu-id="d78c8-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d78c8-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d78c8-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d78c8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d78c8-130">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="d78c8-130">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
