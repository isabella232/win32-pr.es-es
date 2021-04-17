---
description: Establecer los datos de adyacencia de la malla.
ms.assetid: 67d51ce0-7fe2-484d-9874-f1fa59632d59
title: 'ID3DX10Mesh:: SetAdjacencyData (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAdjacencyData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6fabced002caf424fa1fcbcefcb3b326b0c71f7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718365"
---
# <a name="id3dx10meshsetadjacencydata-method"></a><span data-ttu-id="bfcc4-103">ID3DX10Mesh:: SetAdjacencyData (método)</span><span class="sxs-lookup"><span data-stu-id="bfcc4-103">ID3DX10Mesh::SetAdjacencyData method</span></span>

<span data-ttu-id="bfcc4-104">Establecer los datos de adyacencia de la malla.</span><span class="sxs-lookup"><span data-stu-id="bfcc4-104">Set the mesh's adjacency data.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfcc4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfcc4-105">Syntax</span></span>


```C++
HRESULT SetAdjacencyData(
  [in] const UINT *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="bfcc4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfcc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfcc4-107">*pAdjacency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bfcc4-107">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfcc4-108">Tipo: **const [**uint**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="bfcc4-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bfcc4-109">Datos de adyacencia que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="bfcc4-109">The adjacency data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfcc4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfcc4-110">Return value</span></span>

<span data-ttu-id="bfcc4-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bfcc4-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bfcc4-112">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bfcc4-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfcc4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfcc4-113">Requirements</span></span>



| <span data-ttu-id="bfcc4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfcc4-114">Requirement</span></span> | <span data-ttu-id="bfcc4-115">Value</span><span class="sxs-lookup"><span data-stu-id="bfcc4-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfcc4-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfcc4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bfcc4-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfcc4-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="bfcc4-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfcc4-118">Library</span></span><br/> | <dl> <span data-ttu-id="bfcc4-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfcc4-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfcc4-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfcc4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfcc4-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="bfcc4-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="bfcc4-122">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="bfcc4-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
