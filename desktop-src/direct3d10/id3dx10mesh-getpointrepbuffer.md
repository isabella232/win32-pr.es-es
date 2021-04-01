---
description: Obtiene el búfer del representante de puntos de la malla.
ms.assetid: 4be7bee5-15ea-496f-83c2-a3a9bafd97c6
title: 'ID3DX10Mesh:: GetPointRepBuffer (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetPointRepBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 131094792f35b21fd230b66bda6a43fb104b65ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157196"
---
# <a name="id3dx10meshgetpointrepbuffer-method"></a><span data-ttu-id="21004-103">ID3DX10Mesh:: GetPointRepBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="21004-103">ID3DX10Mesh::GetPointRepBuffer method</span></span>

<span data-ttu-id="21004-104">Obtiene el búfer del representante de puntos de la malla.</span><span class="sxs-lookup"><span data-stu-id="21004-104">Get the mesh's point rep buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="21004-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21004-105">Syntax</span></span>


```C++
HRESULT GetPointRepBuffer(
  [out] ID3DX10MeshBuffer **ppPointReps
);
```



## <a name="parameters"></a><span data-ttu-id="21004-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21004-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21004-107">*ppPointReps* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="21004-107">*ppPointReps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21004-108">Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="21004-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="21004-109">Puntero a un búfer de malla que contiene los datos del representante de puntos de la malla.</span><span class="sxs-lookup"><span data-stu-id="21004-109">Pointer to a mesh buffer containing the mesh's point rep data.</span></span> <span data-ttu-id="21004-110">Vea [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="21004-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21004-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21004-111">Return value</span></span>

<span data-ttu-id="21004-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21004-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21004-113">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="21004-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21004-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21004-114">Requirements</span></span>



| <span data-ttu-id="21004-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="21004-115">Requirement</span></span> | <span data-ttu-id="21004-116">Value</span><span class="sxs-lookup"><span data-stu-id="21004-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21004-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21004-117">Header</span></span><br/>  | <dl> <span data-ttu-id="21004-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="21004-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="21004-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="21004-119">Library</span></span><br/> | <dl> <span data-ttu-id="21004-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21004-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21004-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="21004-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21004-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="21004-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="21004-123">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="21004-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




