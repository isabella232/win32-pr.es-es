---
description: Establezca los datos de representación del punto para la malla.
ms.assetid: 451a1ff0-68fa-48c4-b3f1-d41d7583cb3f
title: 'ID3DX10Mesh:: SetPointRepData (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetPointRepData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 65114c5411de7932e9cb71166fcf8554fa0bf7b6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718361"
---
# <a name="id3dx10meshsetpointrepdata-method"></a><span data-ttu-id="5854b-103">ID3DX10Mesh:: SetPointRepData (método)</span><span class="sxs-lookup"><span data-stu-id="5854b-103">ID3DX10Mesh::SetPointRepData method</span></span>

<span data-ttu-id="5854b-104">Establezca los datos de representación del punto para la malla.</span><span class="sxs-lookup"><span data-stu-id="5854b-104">Set the point rep data for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="5854b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5854b-105">Syntax</span></span>


```C++
HRESULT SetPointRepData(
  [in] const UINT *pPointReps
);
```



## <a name="parameters"></a><span data-ttu-id="5854b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5854b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5854b-107">*pPointReps* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5854b-107">*pPointReps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5854b-108">Tipo: **const [**uint**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5854b-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5854b-109">Datos de representación de punto que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="5854b-109">The point rep data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5854b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5854b-110">Return value</span></span>

<span data-ttu-id="5854b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5854b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5854b-112">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5854b-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5854b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5854b-113">Requirements</span></span>



| <span data-ttu-id="5854b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5854b-114">Requirement</span></span> | <span data-ttu-id="5854b-115">Value</span><span class="sxs-lookup"><span data-stu-id="5854b-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5854b-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5854b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5854b-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5854b-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5854b-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5854b-118">Library</span></span><br/> | <dl> <span data-ttu-id="5854b-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5854b-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5854b-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="5854b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5854b-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="5854b-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="5854b-122">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="5854b-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
