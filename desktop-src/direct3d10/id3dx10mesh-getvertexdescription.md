---
description: Acceda a la descripción del vértice pasada en D3DX10CreateMesh. La descripción del vértice describe el diseño de los búferes de vértices de la malla.
ms.assetid: e4a4a98a-e131-414c-ad98-21288ff0c61b
title: 'ID3DX10Mesh:: GetVertexDescription (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexDescription
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 01888ea83f43e37951b48e03916f18af1ec6ddb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003827"
---
# <a name="id3dx10meshgetvertexdescription-method"></a><span data-ttu-id="63f8f-104">ID3DX10Mesh:: GetVertexDescription (método)</span><span class="sxs-lookup"><span data-stu-id="63f8f-104">ID3DX10Mesh::GetVertexDescription method</span></span>

<span data-ttu-id="63f8f-105">Acceda a la descripción del vértice pasada en [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md).</span><span class="sxs-lookup"><span data-stu-id="63f8f-105">Access the vertex description passed into [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md).</span></span> <span data-ttu-id="63f8f-106">La descripción del vértice describe el diseño de los búferes de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="63f8f-106">The vertex description describes the layout of the mesh's vertex buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="63f8f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63f8f-107">Syntax</span></span>


```C++
HRESULT GetVertexDescription(
  [out] const D3D10_INPUT_ELEMENT_DESC **ppDesc,
  [in]        UINT                     *pDeclCount
);
```



## <a name="parameters"></a><span data-ttu-id="63f8f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63f8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63f8f-109">*ppDesc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="63f8f-109">*ppDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63f8f-110">Tipo: **const [**D3D10 \_ \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \* \* del elemento de entrada**</span><span class="sxs-lookup"><span data-stu-id="63f8f-110">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\*\***</span></span>

<span data-ttu-id="63f8f-111">Matriz de elementos de entrada que describen el diseño de los búferes de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="63f8f-111">Array of input elements that describe the layout of the mesh's vertex buffers.</span></span> <span data-ttu-id="63f8f-112">Vea [**\_ Descripción del \_ elemento \_ de entrada D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="63f8f-112">See [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span></span>

</dd> <dt>

<span data-ttu-id="63f8f-113">*pDeclCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63f8f-113">*pDeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63f8f-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="63f8f-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="63f8f-115">El número de elementos de entrada en ppDesc.</span><span class="sxs-lookup"><span data-stu-id="63f8f-115">The number of input elements in ppDesc.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63f8f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63f8f-116">Return value</span></span>

<span data-ttu-id="63f8f-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="63f8f-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="63f8f-118">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="63f8f-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="63f8f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63f8f-119">Requirements</span></span>



| <span data-ttu-id="63f8f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="63f8f-120">Requirement</span></span> | <span data-ttu-id="63f8f-121">Value</span><span class="sxs-lookup"><span data-stu-id="63f8f-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63f8f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63f8f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="63f8f-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="63f8f-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="63f8f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63f8f-124">Library</span></span><br/> | <dl> <span data-ttu-id="63f8f-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63f8f-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63f8f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="63f8f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63f8f-127">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="63f8f-127">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="63f8f-128">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="63f8f-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
