---
description: 'Método ID3DX10Mesh::GetAttributeTable: recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.'
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: Método ID3DX10Mesh::GetAttributeTable (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e7fc503af1a290b27fea81d0c2aba6b84393323b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084003"
---
# <a name="id3dx10meshgetattributetable-method"></a><span data-ttu-id="4a63a-103">Método ID3DX10Mesh::GetAttributeTable</span><span class="sxs-lookup"><span data-stu-id="4a63a-103">ID3DX10Mesh::GetAttributeTable method</span></span>

<span data-ttu-id="4a63a-104">Recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.</span><span class="sxs-lookup"><span data-stu-id="4a63a-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a63a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a63a-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="4a63a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a63a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a63a-107">*pAttribTable* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4a63a-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a63a-108">Tipo: **[ **D3DX10 \_ ATTRIBUTE \_ RANGE**](d3dx10-attribute-range.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a63a-108">Type: **[**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="4a63a-109">Puntero a una matriz de estructuras D3DX10 ATTRIBUTE RANGE, que representan las entradas de la \_ tabla de atributos de la \_ malla.</span><span class="sxs-lookup"><span data-stu-id="4a63a-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="4a63a-110">Especifique **NULL** para recuperar el valor de pAttribTableSize.</span><span class="sxs-lookup"><span data-stu-id="4a63a-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="4a63a-111">*pAttribTableSize* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4a63a-111">*pAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a63a-112">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a63a-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4a63a-113">Puntero al número de entradas almacenadas en pAttribTable o un valor que se va a rellenar con el número de entradas almacenadas en la tabla de atributos de la malla.</span><span class="sxs-lookup"><span data-stu-id="4a63a-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a63a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a63a-114">Return value</span></span>

<span data-ttu-id="4a63a-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4a63a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4a63a-116">El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="4a63a-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4a63a-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a63a-117">Remarks</span></span>

<span data-ttu-id="4a63a-118">Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con diferentes texturas, estados de representación, materiales, entre otras.</span><span class="sxs-lookup"><span data-stu-id="4a63a-118">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="4a63a-119">Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla no dibujando un identificador de atributo determinado al dibujar el marco.</span><span class="sxs-lookup"><span data-stu-id="4a63a-119">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a63a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a63a-120">Requirements</span></span>



| <span data-ttu-id="4a63a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a63a-121">Requirement</span></span> | <span data-ttu-id="4a63a-122">Value</span><span class="sxs-lookup"><span data-stu-id="4a63a-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a63a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a63a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4a63a-124"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="4a63a-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a63a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a63a-125">Library</span></span><br/> | <dl> <span data-ttu-id="4a63a-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a63a-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a63a-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4a63a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a63a-128">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="4a63a-128">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="4a63a-129">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="4a63a-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
