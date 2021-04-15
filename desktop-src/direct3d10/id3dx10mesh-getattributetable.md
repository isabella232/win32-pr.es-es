---
description: Recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: 'ID3DX10Mesh:: GetAttributeTable (método) (D3DX10. h)'
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
ms.openlocfilehash: 4ff00f3c5d036b3b463bc7c6622de75361b196e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707988"
---
# <a name="id3dx10meshgetattributetable-method"></a><span data-ttu-id="e0603-103">ID3DX10Mesh:: GetAttributeTable (método)</span><span class="sxs-lookup"><span data-stu-id="e0603-103">ID3DX10Mesh::GetAttributeTable method</span></span>

<span data-ttu-id="e0603-104">Recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.</span><span class="sxs-lookup"><span data-stu-id="e0603-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0603-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0603-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="e0603-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0603-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0603-107">*pAttribTable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0603-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0603-108">Tipo: **[ **\_ \_ intervalo del atributo D3DX10**](d3dx10-attribute-range.md)\***</span><span class="sxs-lookup"><span data-stu-id="e0603-108">Type: **[**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="e0603-109">Puntero a una matriz de estructuras de intervalo de atributos de D3DX10 \_ \_ , que representa las entradas de la tabla de atributos de la malla.</span><span class="sxs-lookup"><span data-stu-id="e0603-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="e0603-110">Especifique **null** para recuperar el valor de pAttribTableSize.</span><span class="sxs-lookup"><span data-stu-id="e0603-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="e0603-111">*pAttribTableSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0603-111">*pAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0603-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e0603-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e0603-113">Puntero al número de entradas almacenadas en pAttribTable o un valor que se va a rellenar con el número de entradas almacenadas en la tabla de atributos de la malla.</span><span class="sxs-lookup"><span data-stu-id="e0603-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0603-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0603-114">Return value</span></span>

<span data-ttu-id="e0603-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0603-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0603-116">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e0603-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e0603-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0603-117">Remarks</span></span>

<span data-ttu-id="e0603-118">Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con distintas texturas, Estados de representación, materiales, etc.</span><span class="sxs-lookup"><span data-stu-id="e0603-118">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="e0603-119">Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla sin dibujar un identificador de atributo determinado al dibujar el marco.</span><span class="sxs-lookup"><span data-stu-id="e0603-119">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0603-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0603-120">Requirements</span></span>



| <span data-ttu-id="e0603-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0603-121">Requirement</span></span> | <span data-ttu-id="e0603-122">Value</span><span class="sxs-lookup"><span data-stu-id="e0603-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0603-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0603-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e0603-124"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0603-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0603-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0603-125">Library</span></span><br/> | <dl> <span data-ttu-id="e0603-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0603-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0603-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0603-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0603-128">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="e0603-128">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="e0603-129">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="e0603-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
