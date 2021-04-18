---
description: Crea una nueva malla y la rellena con los datos de una malla cargada previamente.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: 'ID3DX10Mesh:: CloneMesh (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CloneMesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0f007475ea9f6aeaa6dc0c01bbd721c4a5103adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718371"
---
# <a name="id3dx10meshclonemesh-method"></a><span data-ttu-id="02a62-103">ID3DX10Mesh:: CloneMesh (método)</span><span class="sxs-lookup"><span data-stu-id="02a62-103">ID3DX10Mesh::CloneMesh method</span></span>

<span data-ttu-id="02a62-104">Crea una nueva malla y la rellena con los datos de una malla cargada previamente.</span><span class="sxs-lookup"><span data-stu-id="02a62-104">Creates a new mesh and fills it with the data of a previously loaded mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="02a62-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02a62-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]        UINT                     Flags,
  [in]        LPCSTR                   pPosSemantic,
  [in]  const D3D10_INPUT_ELEMENT_DESC *pDesc,
  [in]        UINT                     DeclCount,
  [out]       ID3DX10Mesh              **ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="02a62-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02a62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02a62-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="02a62-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02a62-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02a62-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02a62-109">Marcas de creación que se van a aplicar a la nueva malla.</span><span class="sxs-lookup"><span data-stu-id="02a62-109">Creation flags to be applied to the new mesh.</span></span> <span data-ttu-id="02a62-110">Consulte [**D3DX10 \_ Mesh**](d3dx10-mesh.md).</span><span class="sxs-lookup"><span data-stu-id="02a62-110">See [**D3DX10\_MESH**](d3dx10-mesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="02a62-111">*pPosSemantic* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02a62-111">*pPosSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02a62-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02a62-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02a62-113">Nombre semántico para los datos de la posición.</span><span class="sxs-lookup"><span data-stu-id="02a62-113">The semantic name for the position data.</span></span>

</dd> <dt>

<span data-ttu-id="02a62-114">*pDesc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02a62-114">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02a62-115">Tipo: **\* const [**D3D10 \_ \_ \_ DESC del elemento de entrada**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)**</span><span class="sxs-lookup"><span data-stu-id="02a62-115">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="02a62-116">Matriz de \_ estructuras de Desc del elemento de entrada D3D10 \_ \_ , que describe el formato de vértice de la malla devuelta.</span><span class="sxs-lookup"><span data-stu-id="02a62-116">Array of D3D10\_INPUT\_ELEMENT\_DESC structures, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="02a62-117">Vea [**\_ Descripción del \_ elemento \_ de entrada D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="02a62-117">See [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span></span>

</dd> <dt>

<span data-ttu-id="02a62-118">*DeclCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02a62-118">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02a62-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02a62-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02a62-120">Número de elementos de la matriz pDesc.</span><span class="sxs-lookup"><span data-stu-id="02a62-120">The number of elements in the pDesc array.</span></span>

</dd> <dt>

<span data-ttu-id="02a62-121">*ppCloneMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="02a62-121">*ppCloneMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02a62-122">Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="02a62-122">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="02a62-123">La nueva malla.</span><span class="sxs-lookup"><span data-stu-id="02a62-123">The new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02a62-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02a62-124">Return value</span></span>

<span data-ttu-id="02a62-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="02a62-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="02a62-126">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="02a62-126">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02a62-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02a62-127">Requirements</span></span>



| <span data-ttu-id="02a62-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="02a62-128">Requirement</span></span> | <span data-ttu-id="02a62-129">Value</span><span class="sxs-lookup"><span data-stu-id="02a62-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02a62-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02a62-130">Header</span></span><br/>  | <dl> <span data-ttu-id="02a62-131"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="02a62-131"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="02a62-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02a62-132">Library</span></span><br/> | <dl> <span data-ttu-id="02a62-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02a62-133"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02a62-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="02a62-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a62-135">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="02a62-135">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="02a62-136">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="02a62-136">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
