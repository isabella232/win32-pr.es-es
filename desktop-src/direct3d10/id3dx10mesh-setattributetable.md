---
description: Establece la tabla de atributos de una malla y el número de entradas almacenadas en la tabla.
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: 'ID3DX10Mesh:: SetAttributeTable (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 808349b3f7456ebf3f8e1c3a7f9fdf2236db4beb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280415"
---
# <a name="id3dx10meshsetattributetable-method"></a><span data-ttu-id="b1752-103">ID3DX10Mesh:: SetAttributeTable (método)</span><span class="sxs-lookup"><span data-stu-id="b1752-103">ID3DX10Mesh::SetAttributeTable method</span></span>

<span data-ttu-id="b1752-104">Establece la tabla de atributos de una malla y el número de entradas almacenadas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="b1752-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1752-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1752-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="b1752-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1752-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1752-107">*pAttribTable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1752-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1752-108">Tipo: **\* [**intervalo de \_ atributo \_ const D3DX10**](d3dx10-attribute-range.md)**</span><span class="sxs-lookup"><span data-stu-id="b1752-108">Type: **const [**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="b1752-109">Puntero a una matriz de estructuras de intervalos de atributos de D3DX10 \_ \_ , que representa las entradas de la tabla de atributos de malla.</span><span class="sxs-lookup"><span data-stu-id="b1752-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="b1752-110">*cAttribTableSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1752-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1752-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1752-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1752-112">Número de atributos en la tabla de atributos de malla.</span><span class="sxs-lookup"><span data-stu-id="b1752-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1752-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1752-113">Return value</span></span>

<span data-ttu-id="b1752-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1752-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1752-115">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b1752-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1752-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1752-116">Remarks</span></span>

<span data-ttu-id="b1752-117">Si una aplicación realiza un seguimiento de la información en una tabla de atributos y reorganiza la tabla como resultado de los cambios en los atributos o caras, este método permite que la aplicación actualice las tablas de atributos en lugar de volver a llamar a ID3DX10Mesh:: Optimize.</span><span class="sxs-lookup"><span data-stu-id="b1752-117">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling ID3DX10Mesh::Optimize again.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1752-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1752-118">Requirements</span></span>



| <span data-ttu-id="b1752-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1752-119">Requirement</span></span> | <span data-ttu-id="b1752-120">Value</span><span class="sxs-lookup"><span data-stu-id="b1752-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1752-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1752-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b1752-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1752-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1752-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1752-123">Library</span></span><br/> | <dl> <span data-ttu-id="b1752-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1752-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1752-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1752-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1752-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="b1752-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="b1752-127">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="b1752-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
