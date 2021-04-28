---
description: 'Método ID3DXBaseMesh::GetAttributeTable: recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.'
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: Método ID3DXBaseMesh::GetAttributeTable (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f5d27de884f72b46db900487e26f1099bf30949
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115453"
---
# <a name="id3dxbasemeshgetattributetable-method"></a><span data-ttu-id="a0b4a-103">Método ID3DXBaseMesh::GetAttributeTable</span><span class="sxs-lookup"><span data-stu-id="a0b4a-103">ID3DXBaseMesh::GetAttributeTable method</span></span>

<span data-ttu-id="a0b4a-104">Recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.</span><span class="sxs-lookup"><span data-stu-id="a0b4a-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0b4a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0b4a-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="a0b4a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0b4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0b4a-107">*pAttribTable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a0b4a-107">*pAttribTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0b4a-108">Tipo: **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0b4a-108">Type: **[**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="a0b4a-109">Puntero a una matriz de [**estructuras D3DXATTRIBUTERANGE,**](d3dxattributerange.md) que representan las entradas de la tabla de atributos de la malla.</span><span class="sxs-lookup"><span data-stu-id="a0b4a-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="a0b4a-110">Especifique **NULL** para recuperar el valor de pAttribTableSize.</span><span class="sxs-lookup"><span data-stu-id="a0b4a-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="a0b4a-111">*pAttribTableSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a0b4a-111">*pAttribTableSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0b4a-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0b4a-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a0b4a-113">Puntero al número de entradas almacenadas en pAttribTable o a un valor que se va a rellenar con el número de entradas almacenadas en la tabla de atributos de la malla.</span><span class="sxs-lookup"><span data-stu-id="a0b4a-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0b4a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0b4a-114">Return value</span></span>

<span data-ttu-id="a0b4a-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0b4a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0b4a-116">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0b4a-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a0b4a-117">Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a0b4a-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0b4a-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a0b4a-118">Remarks</span></span>

<span data-ttu-id="a0b4a-119">[**Id3DXMesh::Optimize**](id3dxmesh--optimize.md) crea una tabla de atributos y pasa D3DXMESHOPT \_ ATTRSORT para el parámetro Flags.</span><span class="sxs-lookup"><span data-stu-id="a0b4a-119">An attribute table is created by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) and passing D3DXMESHOPT\_ATTRSORT for the Flags parameter.</span></span>

<span data-ttu-id="a0b4a-120">Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con diferentes texturas, estados de representación, materiales, entre otras.</span><span class="sxs-lookup"><span data-stu-id="a0b4a-120">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="a0b4a-121">Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla al no dibujar un identificador de atributo determinado al dibujar el marco.</span><span class="sxs-lookup"><span data-stu-id="a0b4a-121">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0b4a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0b4a-122">Requirements</span></span>



| <span data-ttu-id="a0b4a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0b4a-123">Requirement</span></span> | <span data-ttu-id="a0b4a-124">Value</span><span class="sxs-lookup"><span data-stu-id="a0b4a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b4a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0b4a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a0b4a-126"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="a0b4a-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a0b4a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0b4a-127">Library</span></span><br/> | <dl> <span data-ttu-id="a0b4a-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0b4a-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0b4a-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a0b4a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b4a-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="a0b4a-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
