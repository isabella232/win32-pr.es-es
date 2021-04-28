---
description: 'Método ID3DXMesh::SetAttributeTable: establece la tabla de atributos para una malla y el número de entradas almacenadas en la tabla.'
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: Método ID3DXMesh::SetAttributeTable (D3DX9Mesh.h)
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
ms.openlocfilehash: a4cdb503e934ca00b41482601b59266eee750365
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093353"
---
# <a name="id3dxmeshsetattributetable-method"></a><span data-ttu-id="c1714-103">Método ID3DXMesh::SetAttributeTable</span><span class="sxs-lookup"><span data-stu-id="c1714-103">ID3DXMesh::SetAttributeTable method</span></span>

<span data-ttu-id="c1714-104">Establece la tabla de atributos para una malla y el número de entradas almacenadas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="c1714-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1714-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1714-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="c1714-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1714-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1714-107">*pAttribTable* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c1714-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1714-108">Tipo: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***</span><span class="sxs-lookup"><span data-stu-id="c1714-108">Type: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="c1714-109">Puntero a una matriz de [**estructuras D3DXATTRIBUTERANGE,**](d3dxattributerange.md) que representa las entradas de la tabla de atributos de malla.</span><span class="sxs-lookup"><span data-stu-id="c1714-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="c1714-110">*cAttribTableSize* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c1714-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1714-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1714-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1714-112">Número de atributos de la tabla de atributos de malla.</span><span class="sxs-lookup"><span data-stu-id="c1714-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1714-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1714-113">Return value</span></span>

<span data-ttu-id="c1714-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c1714-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c1714-115">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c1714-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c1714-116">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c1714-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1714-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1714-117">Remarks</span></span>

<span data-ttu-id="c1714-118">Si una aplicación realiza un seguimiento de la información de una tabla de atributos y reorganiza la tabla como resultado de cambios en atributos o caras, este método permite a la aplicación actualizar las tablas de atributos en lugar de llamar de nuevo a [**ID3DXMesh::Optimize.**](id3dxmesh--optimize.md)</span><span class="sxs-lookup"><span data-stu-id="c1714-118">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) again.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1714-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1714-119">Requirements</span></span>



| <span data-ttu-id="c1714-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1714-120">Requirement</span></span> | <span data-ttu-id="c1714-121">Value</span><span class="sxs-lookup"><span data-stu-id="c1714-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1714-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1714-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c1714-123"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="c1714-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c1714-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1714-124">Library</span></span><br/> | <dl> <span data-ttu-id="c1714-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1714-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1714-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c1714-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1714-127">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="c1714-127">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="c1714-128">**ID3DXMesh::LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="c1714-128">**ID3DXMesh::LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

<span data-ttu-id="c1714-129">**ID3DXMesh::LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="c1714-129">**ID3DXMesh::LockAttributeBuffer**</span></span>
</dt> </dl>

 

 
