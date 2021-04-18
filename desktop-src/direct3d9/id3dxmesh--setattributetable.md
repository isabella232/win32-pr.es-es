---
description: Establece la tabla de atributos de una malla y el número de entradas almacenadas en la tabla.
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: 'ID3DXMesh:: SetAttributeTable (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.SetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 17ae3458bffd05114415a92538a8ce8ef2cc847e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707784"
---
# <a name="id3dxmeshsetattributetable-method"></a><span data-ttu-id="f00d5-103">ID3DXMesh:: SetAttributeTable (método)</span><span class="sxs-lookup"><span data-stu-id="f00d5-103">ID3DXMesh::SetAttributeTable method</span></span>

<span data-ttu-id="f00d5-104">Establece la tabla de atributos de una malla y el número de entradas almacenadas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="f00d5-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="f00d5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f00d5-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="f00d5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f00d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f00d5-107">*pAttribTable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f00d5-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f00d5-108">Tipo: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***</span><span class="sxs-lookup"><span data-stu-id="f00d5-108">Type: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="f00d5-109">Puntero a una matriz de estructuras [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) que representa las entradas de la tabla de atributos de malla.</span><span class="sxs-lookup"><span data-stu-id="f00d5-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="f00d5-110">*cAttribTableSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f00d5-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f00d5-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f00d5-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f00d5-112">Número de atributos en la tabla de atributos de malla.</span><span class="sxs-lookup"><span data-stu-id="f00d5-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f00d5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f00d5-113">Return value</span></span>

<span data-ttu-id="f00d5-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f00d5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f00d5-115">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f00d5-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f00d5-116">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f00d5-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f00d5-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f00d5-117">Remarks</span></span>

<span data-ttu-id="f00d5-118">Si una aplicación realiza un seguimiento de la información en una tabla de atributos y reorganiza la tabla como resultado de los cambios en los atributos o caras, este método permite que la aplicación actualice las tablas de atributos en lugar de volver a llamar a [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) .</span><span class="sxs-lookup"><span data-stu-id="f00d5-118">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) again.</span></span>

## <a name="requirements"></a><span data-ttu-id="f00d5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f00d5-119">Requirements</span></span>



| <span data-ttu-id="f00d5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f00d5-120">Requirement</span></span> | <span data-ttu-id="f00d5-121">Value</span><span class="sxs-lookup"><span data-stu-id="f00d5-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f00d5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f00d5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f00d5-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f00d5-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f00d5-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f00d5-124">Library</span></span><br/> | <dl> <span data-ttu-id="f00d5-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f00d5-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f00d5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f00d5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f00d5-127">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="f00d5-127">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="f00d5-128">**ID3DXMesh::LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="f00d5-128">**ID3DXMesh::LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

<span data-ttu-id="f00d5-129">**ID3DXMesh::LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="f00d5-129">**ID3DXMesh::LockAttributeBuffer**</span></span>
</dt> </dl>

 

 
