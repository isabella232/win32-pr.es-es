---
description: Destruye el subárbol de fotogramas bajo la raíz, incluida la raíz.
ms.assetid: 0bbb529f-01d8-430b-a72b-4af5f7a71253
title: Función D3DXFrameDestroy (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameDestroy
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1c0809ff61abec6f55564ca17a116ad4c826bca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718207"
---
# <a name="d3dxframedestroy-function"></a><span data-ttu-id="62b5d-103">D3DXFrameDestroy función)</span><span class="sxs-lookup"><span data-stu-id="62b5d-103">D3DXFrameDestroy function</span></span>

<span data-ttu-id="62b5d-104">Destruye el subárbol de fotogramas bajo la raíz, incluida la raíz.</span><span class="sxs-lookup"><span data-stu-id="62b5d-104">Destroys the subtree of frames under the root, including the root.</span></span>

## <a name="syntax"></a><span data-ttu-id="62b5d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62b5d-105">Syntax</span></span>


```C++
HRESULT D3DXFrameDestroy(
  _In_ LPD3DXFRAME             pFrameRoot,
  _In_ LPD3DXALLOCATEHIERARCHY pAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="62b5d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62b5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62b5d-107">*pFrameRoot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62b5d-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62b5d-108">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="62b5d-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="62b5d-109">Puntero al nodo raíz.</span><span class="sxs-lookup"><span data-stu-id="62b5d-109">Pointer to the root node.</span></span>

</dd> <dt>

<span data-ttu-id="62b5d-110">*pAlloc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62b5d-110">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62b5d-111">Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="62b5d-111">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="62b5d-112">Interfaz de asignación usada para desasignar nodos de la jerarquía de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="62b5d-112">Allocation interface used to deallocate nodes of the frame hierarchy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62b5d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62b5d-113">Return value</span></span>

<span data-ttu-id="62b5d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62b5d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62b5d-115">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="62b5d-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="62b5d-116">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="62b5d-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="62b5d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62b5d-117">Requirements</span></span>



| <span data-ttu-id="62b5d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="62b5d-118">Requirement</span></span> | <span data-ttu-id="62b5d-119">Value</span><span class="sxs-lookup"><span data-stu-id="62b5d-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62b5d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62b5d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="62b5d-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="62b5d-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="62b5d-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62b5d-122">Library</span></span><br/> | <dl> <span data-ttu-id="62b5d-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62b5d-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="62b5d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="62b5d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b5d-125">Funciones de animación</span><span class="sxs-lookup"><span data-stu-id="62b5d-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




