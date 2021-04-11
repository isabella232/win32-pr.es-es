---
description: Este método permite al usuario cambiar la declaración de la malla sin cambiar el diseño de los datos del búfer de vértices. La llamada solo es válida si los formatos de declaración anterior y nuevo tienen el mismo tamaño de vértice.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: 'ID3DXBaseMesh:: UpdateSemantics (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UpdateSemantics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e31a6fe424d085467bfa795c7ce7b2d445a1f69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083739"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a><span data-ttu-id="b5d56-104">ID3DXBaseMesh:: UpdateSemantics (método)</span><span class="sxs-lookup"><span data-stu-id="b5d56-104">ID3DXBaseMesh::UpdateSemantics method</span></span>

<span data-ttu-id="b5d56-105">Este método permite al usuario cambiar la declaración de la malla sin cambiar el diseño de los datos del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="b5d56-105">This method allows the user to change the mesh declaration without changing the data layout of the vertex buffer.</span></span> <span data-ttu-id="b5d56-106">La llamada solo es válida si los formatos de declaración anterior y nuevo tienen el mismo tamaño de vértice.</span><span class="sxs-lookup"><span data-stu-id="b5d56-106">The call is valid only if the old and new declaration formats have the same vertex size.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d56-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5d56-107">Syntax</span></span>


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="b5d56-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5d56-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5d56-109">*Declaración* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="b5d56-109">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d56-110">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="b5d56-110">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="b5d56-111">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que describe el formato de vértice de los vértices de malla.</span><span class="sxs-lookup"><span data-stu-id="b5d56-111">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="b5d56-112">El límite superior de esta matriz de declarador es el [**tamaño máximo de \_ FVF \_ decl \_**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="b5d56-112">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5d56-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5d56-113">Return value</span></span>

<span data-ttu-id="b5d56-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5d56-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5d56-115">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5d56-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b5d56-116">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b5d56-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5d56-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5d56-117">Remarks</span></span>

<span data-ttu-id="b5d56-118">[**ID3DXBaseMesh:: CloneMesh**](id3dxbasemesh--clonemesh.md) se usa para volver a formatear y cambiar el diseño de los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="b5d56-118">[**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="b5d56-119">Por ejemplo, úselo para agregar espacio para las normales, coordenadas de textura, colores, pesos, etc., que no estaban presentes antes.</span><span class="sxs-lookup"><span data-stu-id="b5d56-119">For example, use it to to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="b5d56-120">**ID3DXBaseMesh:: UpdateSemantics** es un método para actualizar la declaración de vértices con información semántica diferente, sin cambiar el diseño del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="b5d56-120">**ID3DXBaseMesh::UpdateSemantics** is a method for updating the vertex declaration with different semantic information, without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="b5d56-121">Por ejemplo, úselo para cambiar la etiqueta de una coordenada de textura 3D como binormalización o tangente, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="b5d56-121">For example, use it to relabel a 3D texture coordinate as a binormal or tangent, or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d56-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5d56-122">Requirements</span></span>



| <span data-ttu-id="b5d56-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5d56-123">Requirement</span></span> | <span data-ttu-id="b5d56-124">Value</span><span class="sxs-lookup"><span data-stu-id="b5d56-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d56-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5d56-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b5d56-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5d56-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b5d56-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5d56-127">Library</span></span><br/> | <dl> <span data-ttu-id="b5d56-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5d56-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5d56-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5d56-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d56-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="b5d56-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="b5d56-131">**ID3DXBaseMesh::CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="b5d56-131">**ID3DXBaseMesh::CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[<span data-ttu-id="b5d56-132">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="b5d56-132">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
