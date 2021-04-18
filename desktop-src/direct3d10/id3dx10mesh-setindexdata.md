---
description: Establecer los datos de índice de la malla.
ms.assetid: f3e7e166-94b5-45f6-9d43-8d7e32b7b523
title: 'ID3DX10Mesh:: SetIndexData (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetIndexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f561a4109fbab2163b2ec51e95b45a618da5b6d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718363"
---
# <a name="id3dx10meshsetindexdata-method"></a><span data-ttu-id="3a900-103">ID3DX10Mesh:: SetIndexData (método)</span><span class="sxs-lookup"><span data-stu-id="3a900-103">ID3DX10Mesh::SetIndexData method</span></span>

<span data-ttu-id="3a900-104">Establecer los datos de índice de la malla.</span><span class="sxs-lookup"><span data-stu-id="3a900-104">Set the mesh's index data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a900-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a900-105">Syntax</span></span>


```C++
HRESULT SetIndexData(
  [in] const void *pData,
  [in]       UINT cIndices
);
```



## <a name="parameters"></a><span data-ttu-id="3a900-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a900-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a900-107">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a900-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a900-108">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="3a900-108">Type: **const void\***</span></span>

<span data-ttu-id="3a900-109">Los datos del índice.</span><span class="sxs-lookup"><span data-stu-id="3a900-109">The index data.</span></span>

</dd> <dt>

<span data-ttu-id="3a900-110">*cIndices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a900-110">*cIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a900-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a900-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a900-112">Número de índices en pData.</span><span class="sxs-lookup"><span data-stu-id="3a900-112">The number of indices in pData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a900-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a900-113">Return value</span></span>

<span data-ttu-id="3a900-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a900-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a900-115">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3a900-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a900-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a900-116">Requirements</span></span>



| <span data-ttu-id="3a900-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a900-117">Requirement</span></span> | <span data-ttu-id="3a900-118">Value</span><span class="sxs-lookup"><span data-stu-id="3a900-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a900-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a900-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3a900-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a900-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a900-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a900-121">Library</span></span><br/> | <dl> <span data-ttu-id="3a900-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a900-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a900-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a900-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a900-124">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="3a900-124">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="3a900-125">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="3a900-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
