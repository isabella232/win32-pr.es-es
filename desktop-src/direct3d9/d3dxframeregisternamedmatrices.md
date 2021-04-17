---
description: Dada una jerarquía de fotogramas, registra todas las matrices con nombre en el mezclador de animaciones.
ms.assetid: df0560c2-4417-4d54-94c8-031521b32189
title: Función D3DXFrameRegisterNamedMatrices (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameRegisterNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8496f467e668939c5d5aa0e90266ab012d436038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718204"
---
# <a name="d3dxframeregisternamedmatrices-function"></a><span data-ttu-id="8a338-103">D3DXFrameRegisterNamedMatrices función)</span><span class="sxs-lookup"><span data-stu-id="8a338-103">D3DXFrameRegisterNamedMatrices function</span></span>

<span data-ttu-id="8a338-104">Dada una jerarquía de fotogramas, registra todas las matrices con nombre en el mezclador de animaciones.</span><span class="sxs-lookup"><span data-stu-id="8a338-104">Given a frame hierarchy, registers all the named matrices in the animation mixer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a338-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a338-105">Syntax</span></span>


```C++
HRESULT D3DXFrameRegisterNamedMatrices(
  _In_ LPD3DXFRAME               pFrameRoot,
  _In_ LPD3DXANIMATIONCONTROLLER pAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="8a338-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a338-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a338-107">*pFrameRoot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a338-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a338-108">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="8a338-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="8a338-109">Nodo de nivel superior de la jerarquía de Marcos.</span><span class="sxs-lookup"><span data-stu-id="8a338-109">The top level node in the frame hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="8a338-110">*pAnimController* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a338-110">*pAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a338-111">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="8a338-111">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="8a338-112">Puntero al objeto de controlador de animación.</span><span class="sxs-lookup"><span data-stu-id="8a338-112">Pointer to the animation controller object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a338-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a338-113">Return value</span></span>

<span data-ttu-id="8a338-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8a338-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8a338-115">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a338-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8a338-116">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8a338-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a338-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a338-117">Requirements</span></span>



| <span data-ttu-id="8a338-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a338-118">Requirement</span></span> | <span data-ttu-id="8a338-119">Value</span><span class="sxs-lookup"><span data-stu-id="8a338-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a338-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a338-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8a338-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a338-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8a338-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a338-122">Library</span></span><br/> | <dl> <span data-ttu-id="8a338-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a338-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8a338-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a338-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a338-125">Funciones de animación</span><span class="sxs-lookup"><span data-stu-id="8a338-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




