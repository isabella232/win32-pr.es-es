---
description: 'Método ID3DX10Mesh::SetAttributeTable: establece la tabla de atributos para una malla y el número de entradas almacenadas en la tabla.'
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: Método ID3DX10Mesh::SetAttributeTable (D3DX10.h)
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
ms.openlocfilehash: 4e06b181bb512e16e9caaa0d233ebbd3472bfcf8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084013"
---
# <a name="id3dx10meshsetattributetable-method"></a><span data-ttu-id="38fd6-103">Método ID3DX10Mesh::SetAttributeTable</span><span class="sxs-lookup"><span data-stu-id="38fd6-103">ID3DX10Mesh::SetAttributeTable method</span></span>

<span data-ttu-id="38fd6-104">Establece la tabla de atributos para una malla y el número de entradas almacenadas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="38fd6-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="38fd6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38fd6-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="38fd6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38fd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38fd6-107">*pAttribTable* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="38fd6-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38fd6-108">Tipo: **const [**D3DX10 \_ ATTRIBUTE \_ RANGE**](d3dx10-attribute-range.md) \***</span><span class="sxs-lookup"><span data-stu-id="38fd6-108">Type: **const [**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="38fd6-109">Puntero a una matriz de estructuras D3DX10 ATTRIBUTE RANGE, que representan \_ las entradas de la tabla de atributos de \_ malla.</span><span class="sxs-lookup"><span data-stu-id="38fd6-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="38fd6-110">*cAttribTableSize* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="38fd6-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38fd6-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38fd6-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38fd6-112">Número de atributos de la tabla de atributos de malla.</span><span class="sxs-lookup"><span data-stu-id="38fd6-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38fd6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38fd6-113">Return value</span></span>

<span data-ttu-id="38fd6-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38fd6-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38fd6-115">El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="38fd6-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="38fd6-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38fd6-116">Remarks</span></span>

<span data-ttu-id="38fd6-117">Si una aplicación realiza un seguimiento de la información de una tabla de atributos y reorganiza la tabla como resultado de cambios en atributos o caras, este método permite a la aplicación actualizar las tablas de atributos en lugar de llamar de nuevo a ID3DX10Mesh::Optimize.</span><span class="sxs-lookup"><span data-stu-id="38fd6-117">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling ID3DX10Mesh::Optimize again.</span></span>

## <a name="requirements"></a><span data-ttu-id="38fd6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38fd6-118">Requirements</span></span>



| <span data-ttu-id="38fd6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="38fd6-119">Requirement</span></span> | <span data-ttu-id="38fd6-120">Value</span><span class="sxs-lookup"><span data-stu-id="38fd6-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38fd6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38fd6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="38fd6-122"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="38fd6-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="38fd6-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38fd6-123">Library</span></span><br/> | <dl> <span data-ttu-id="38fd6-124"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="38fd6-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38fd6-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="38fd6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38fd6-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="38fd6-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="38fd6-127">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="38fd6-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
