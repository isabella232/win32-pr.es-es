---
description: Crea un objeto Mesh mediante un declarador.
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: Función D3DX10CreateMesh (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateMesh
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2b00addb152fe18db448364fcc784c2044b10d23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689893"
---
# <a name="d3dx10createmesh-function"></a><span data-ttu-id="6f9e6-103">D3DX10CreateMesh función)</span><span class="sxs-lookup"><span data-stu-id="6f9e6-103">D3DX10CreateMesh function</span></span>

<span data-ttu-id="6f9e6-104">Crea un objeto Mesh mediante un declarador.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f9e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f9e6-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateMesh(
  _In_        ID3D10Device             *pDevice,
  _In_  const D3D10_INPUT_ELEMENT_DESC *pDeclaration,
  _In_        UINT                     DeclCount,
  _In_        LPCSTR                   pPositionSemantic,
  _In_        UINT                     VertexCount,
  _In_        UINT                     FaceCount,
  _In_        UINT                     Options,
  _Out_       ID3DX10Mesh              **ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="6f9e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f9e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f9e6-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f9e6-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9e6-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="6f9e6-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="6f9e6-109">Puntero a una [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), el objeto de dispositivo que se va a asociar a la malla.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-109">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6f9e6-110">*pDeclaration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f9e6-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9e6-111">Tipo: **\* const [**D3D10 \_ \_ \_ DESC del elemento de entrada**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)**</span><span class="sxs-lookup"><span data-stu-id="6f9e6-111">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="6f9e6-112">Matriz de [**elementos \_ \_ \_ DESC del elemento de entrada D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) , que describe el formato de vértice de la malla devuelta.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-112">Array of [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="6f9e6-113">Este parámetro debe asignarse directamente a un formato de vértice flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="6f9e6-113">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="6f9e6-114">*DeclCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f9e6-114">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9e6-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f9e6-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f9e6-116">Número de elementos de pDeclaration.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-116">The number of elements in pDeclaration.</span></span>

</dd> <dt>

<span data-ttu-id="6f9e6-117">*pPositionSemantic* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f9e6-117">*pPositionSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9e6-118">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f9e6-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f9e6-119">Semántica que identifica qué parte de la declaración de vértice contiene información de posición.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-119">Semantic that identifies which part of the vertex declaration contains position information.</span></span>

</dd> <dt>

<span data-ttu-id="6f9e6-120">*VertexCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f9e6-120">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9e6-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f9e6-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f9e6-122">Número de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-122">Number of vertices for the mesh.</span></span> <span data-ttu-id="6f9e6-123">Este parámetro debe ser mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-123">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="6f9e6-124">*FaceCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f9e6-124">*FaceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9e6-125">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f9e6-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f9e6-126">Número de caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-126">Number of faces for the mesh.</span></span> <span data-ttu-id="6f9e6-127">El intervalo válido para este número es mayor que 0 y uno menos que el valor DWORD máximo (normalmente 65534), ya que el último índice está reservado.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-127">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6f9e6-128">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6f9e6-128">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9e6-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f9e6-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f9e6-130">Combinación de una o varias marcas de la [**\_ malla D3DX10**](d3dx10-mesh.md), especificando las opciones de la malla.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-130">Combination of one or more flags from the [**D3DX10\_MESH**](d3dx10-mesh.md), specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6f9e6-131">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6f9e6-131">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9e6-132">Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6f9e6-132">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="6f9e6-133">Dirección de un puntero a una [**interfaz ID3DX10Mesh**](id3dx10mesh.md)que representa el objeto de malla creado.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-133">Address of a pointer to an [**ID3DX10Mesh Interface**](id3dx10mesh.md), representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f9e6-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f9e6-134">Return value</span></span>

<span data-ttu-id="6f9e6-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6f9e6-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6f9e6-136">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6f9e6-137">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f9e6-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f9e6-138">Requirements</span></span>



| <span data-ttu-id="6f9e6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f9e6-139">Requirement</span></span> | <span data-ttu-id="6f9e6-140">Value</span><span class="sxs-lookup"><span data-stu-id="6f9e6-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f9e6-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f9e6-141">Header</span></span><br/>  | <dl> <span data-ttu-id="6f9e6-142"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f9e6-142"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6f9e6-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f9e6-143">Library</span></span><br/> | <dl> <span data-ttu-id="6f9e6-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f9e6-144"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6f9e6-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f9e6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f9e6-146">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="6f9e6-146">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="6f9e6-147">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="6f9e6-147">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
