---
description: Establezca los datos de vértices en uno de los búferes de vértices de la malla.
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: 'ID3DX10Mesh:: SetVertexData (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetVertexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 68d54c6868e44517d42e0b53159f7a23ef45a05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698326"
---
# <a name="id3dx10meshsetvertexdata-method"></a><span data-ttu-id="689c5-103">ID3DX10Mesh:: SetVertexData (método)</span><span class="sxs-lookup"><span data-stu-id="689c5-103">ID3DX10Mesh::SetVertexData method</span></span>

<span data-ttu-id="689c5-104">Establezca los datos de vértices en uno de los búferes de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="689c5-104">Set vertex data into one of the mesh's vertex buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="689c5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="689c5-105">Syntax</span></span>


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a><span data-ttu-id="689c5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="689c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="689c5-107">*iBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="689c5-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="689c5-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="689c5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="689c5-109">Búfer de vértices que se va a rellenar con pData.</span><span class="sxs-lookup"><span data-stu-id="689c5-109">The vertex buffer to be filled with pData.</span></span>

</dd> <dt>

<span data-ttu-id="689c5-110">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="689c5-110">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="689c5-111">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="689c5-111">Type: **const void\***</span></span>

<span data-ttu-id="689c5-112">Datos de vértices que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="689c5-112">The vertex data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="689c5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="689c5-113">Return value</span></span>

<span data-ttu-id="689c5-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="689c5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="689c5-115">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="689c5-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="689c5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="689c5-116">Requirements</span></span>



| <span data-ttu-id="689c5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="689c5-117">Requirement</span></span> | <span data-ttu-id="689c5-118">Value</span><span class="sxs-lookup"><span data-stu-id="689c5-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="689c5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="689c5-119">Header</span></span><br/>  | <dl> <span data-ttu-id="689c5-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="689c5-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="689c5-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="689c5-121">Library</span></span><br/> | <dl> <span data-ttu-id="689c5-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="689c5-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="689c5-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="689c5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="689c5-124">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="689c5-124">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="689c5-125">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="689c5-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
