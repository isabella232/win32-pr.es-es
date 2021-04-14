---
description: Limite el número de huesos que pueden influir en un vértice o limite la cantidad de influencia que puede tener un hueso en un vértice.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: 'Método ID3DX10SkinInfo:: Compact (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.Compact
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 379343688a1fd2ffe5ebd968dc984fa09faada7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424359"
---
# <a name="id3dx10skininfocompact-method"></a><span data-ttu-id="3081c-103">ID3DX10SkinInfo:: Compact (método)</span><span class="sxs-lookup"><span data-stu-id="3081c-103">ID3DX10SkinInfo::Compact method</span></span>

<span data-ttu-id="3081c-104">Limite el número de huesos que pueden influir en un vértice o limite la cantidad de influencia que puede tener un hueso en un vértice.</span><span class="sxs-lookup"><span data-stu-id="3081c-104">Limit the number of bones that can influence a vertex and/or limit the amount of influence a bone can have on a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="3081c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3081c-105">Syntax</span></span>


```C++
HRESULT Compact(
  [in] UINT  MaxPerVertexInfluences,
  [in] UINT  ScaleMode,
  [in] float MinWeight
);
```



## <a name="parameters"></a><span data-ttu-id="3081c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3081c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3081c-107">*MaxPerVertexInfluences* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3081c-107">*MaxPerVertexInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3081c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3081c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3081c-109">Número máximo de huesos que pueden influir en cualquier vértice determinado.</span><span class="sxs-lookup"><span data-stu-id="3081c-109">The maximum number of bones that can influence any given vertex.</span></span> <span data-ttu-id="3081c-110">Este valor se omite si es mayor que el valor devuelto por [**ID3DX10SkinInfo:: GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).</span><span class="sxs-lookup"><span data-stu-id="3081c-110">This value is ignored if it is greater than the value returned by [**ID3DX10SkinInfo::GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).</span></span>

</dd> <dt>

<span data-ttu-id="3081c-111">*ScaleMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3081c-111">*ScaleMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3081c-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3081c-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3081c-113">Marca que describe cómo escalar los pesos restantes en un vértice determinado después de que se hayan cortado algunos en MinWeight.</span><span class="sxs-lookup"><span data-stu-id="3081c-113">A flag describing how to scale the remaining weights on a given vertex after some have been chopped off by MinWeight.</span></span> <span data-ttu-id="3081c-114">Si D3DX10 \_ SKININFO \_ no \_ se especifica ningún ajuste de escala, no se reducirá el tamaño de los pesos.</span><span class="sxs-lookup"><span data-stu-id="3081c-114">If D3DX10\_SKININFO\_NO\_SCALING is specified, the weights will not be scaled at all.</span></span> <span data-ttu-id="3081c-115">Si \_ \_ se especifica D3DX10 SKININFO escalar \_ a \_ 1, los pesos mayores que MinWeight se escalarán verticalmente para que se agreguen hasta 1,0.</span><span class="sxs-lookup"><span data-stu-id="3081c-115">If D3DX10\_SKININFO\_SCALE\_TO\_1 is specified, the weights greater than MinWeight will be scaled up so that they add up to 1.0.</span></span> <span data-ttu-id="3081c-116">Si \_ \_ se especifica D3DX10 SKININFO Scale \_ to total, se reducirán \_ los pesos mayores que MinWeight para que se agreguen al total original.</span><span class="sxs-lookup"><span data-stu-id="3081c-116">If D3DX10\_SKININFO\_SCALE\_TO\_TOTAL is specified, the weights greater than MinWeight will be scaled up so that they add up to the original total.</span></span>

</dd> <dt>

<span data-ttu-id="3081c-117">*MinWeight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3081c-117">*MinWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3081c-118">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3081c-118">Type: **float**</span></span>

<span data-ttu-id="3081c-119">Porcentaje mínimo de influencia, o peso, que cualquier hueso puede tener en cualquier vértice.</span><span class="sxs-lookup"><span data-stu-id="3081c-119">The minimum percentage of influence, or weight, that any bone can have on any vertex.</span></span> <span data-ttu-id="3081c-120">Este valor debe estar comprendido entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="3081c-120">This value must be between 0 and 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3081c-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3081c-121">Return value</span></span>

<span data-ttu-id="3081c-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3081c-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3081c-123">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3081c-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3081c-124">Si se produce un error en el método, el valor devuelto puede ser: E \_ OUTOFMEMORY o e \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="3081c-124">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="3081c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3081c-125">Requirements</span></span>



| <span data-ttu-id="3081c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3081c-126">Requirement</span></span> | <span data-ttu-id="3081c-127">Value</span><span class="sxs-lookup"><span data-stu-id="3081c-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3081c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3081c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3081c-129"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3081c-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3081c-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3081c-130">Library</span></span><br/> | <dl> <span data-ttu-id="3081c-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3081c-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3081c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3081c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3081c-133">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="3081c-133">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="3081c-134">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="3081c-134">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
