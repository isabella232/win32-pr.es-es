---
description: Establece las propiedades de material de la malla en la escena 3D. Use este método para especificar parámetros de dispersión de subsuperficie.
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: 'ID3DXPRTEngine:: SetMeshMaterials (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMeshMaterials
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c90ae72cab5d7a20c2c65b940d28a9b57902d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362736"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a><span data-ttu-id="3b68c-104">ID3DXPRTEngine:: SetMeshMaterials (método)</span><span class="sxs-lookup"><span data-stu-id="3b68c-104">ID3DXPRTEngine::SetMeshMaterials method</span></span>

<span data-ttu-id="3b68c-105">Establece las propiedades de material de la malla en la escena 3D.</span><span class="sxs-lookup"><span data-stu-id="3b68c-105">Sets mesh material properties in the 3D scene.</span></span> <span data-ttu-id="3b68c-106">Use este método para especificar parámetros de dispersión de subsuperficie.</span><span class="sxs-lookup"><span data-stu-id="3b68c-106">Use this method to specify subsurface scattering parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b68c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b68c-107">Syntax</span></span>


```C++
HRESULT SetMeshMaterials(
  [in] const D3DXSHMATERIAL **ppMaterials,
  [in]       UINT           NumMeshes,
  [in]       UINT           NumChannels,
  [in]       BOOL           bSetAlbedo,
  [in]       FLOAT          fLengthScale
);
```



## <a name="parameters"></a><span data-ttu-id="3b68c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b68c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b68c-109">*ppMaterials* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b68c-109">*ppMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b68c-110">Tipo: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="3b68c-110">Type: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md)\*\***</span></span>

<span data-ttu-id="3b68c-111">Dirección de un puntero a propiedades de material de malla deseadas.</span><span class="sxs-lookup"><span data-stu-id="3b68c-111">Address of a pointer to desired mesh material properties.</span></span> <span data-ttu-id="3b68c-112">Vea [**D3DXSHMATERIAL**](d3dxshmaterial.md).</span><span class="sxs-lookup"><span data-stu-id="3b68c-112">See [**D3DXSHMATERIAL**](d3dxshmaterial.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b68c-113">*NumMeshes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b68c-113">*NumMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b68c-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b68c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b68c-115">Índice de la malla en la que se van a establecer las propiedades del material.</span><span class="sxs-lookup"><span data-stu-id="3b68c-115">Index of the mesh on which to set material properties.</span></span>

</dd> <dt>

<span data-ttu-id="3b68c-116">*NumChannels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b68c-116">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b68c-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b68c-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b68c-118">Número de canales de color que se van a establecer en la malla.</span><span class="sxs-lookup"><span data-stu-id="3b68c-118">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="3b68c-119">Establézcalo en 1 para especificar materiales grises (R = G = B) o 3 para habilitar los efectos de sangrado de color.</span><span class="sxs-lookup"><span data-stu-id="3b68c-119">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span> <span data-ttu-id="3b68c-120">Si piensa cambiar este parámetro, establezca primero Albedo con otro método como [**ID3DXPRTEngine:: SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) o [**ID3DXPRTEngine:: SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).</span><span class="sxs-lookup"><span data-stu-id="3b68c-120">If you intend to change this parameter, first set the albedo using another method such as [**ID3DXPRTEngine::SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) or [**ID3DXPRTEngine::SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b68c-121">*bSetAlbedo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b68c-121">*bSetAlbedo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b68c-122">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b68c-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b68c-123">Si **es true**, establece el albedo de la malla en ppMaterials y sobrescribe todos los valores de textura y albedo de vértice existentes.</span><span class="sxs-lookup"><span data-stu-id="3b68c-123">If **TRUE**, sets the albedo of the mesh to ppMaterials, overwriting all existing texel and vertex albedo values.</span></span> <span data-ttu-id="3b68c-124">Si **es false**, conserva todos los valores de textura y albedo de vértice existentes establecidos por otros métodos. NumChannels debe coincidir con el parámetro NumChannels que se usa para crear el búfer en [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) o [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).</span><span class="sxs-lookup"><span data-stu-id="3b68c-124">If **FALSE**, preserves all existing texel and vertex albedo values set by other methods; NumChannels must match the NumChannels parameter used to create the buffer in [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) or [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b68c-125">*fLengthScale* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b68c-125">*fLengthScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b68c-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b68c-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b68c-127">Escala de la escena 3D relativa a un cubo de 1 mm.</span><span class="sxs-lookup"><span data-stu-id="3b68c-127">Scale of the 3D scene relative to a 1-mm cube.</span></span> <span data-ttu-id="3b68c-128">Se usa para los cálculos de dispersión de subsuperficies.</span><span class="sxs-lookup"><span data-stu-id="3b68c-128">Used for subsurface scattering computations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b68c-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b68c-129">Return value</span></span>

<span data-ttu-id="3b68c-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b68c-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b68c-131">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3b68c-131">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3b68c-132">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3b68c-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b68c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b68c-133">Requirements</span></span>



| <span data-ttu-id="3b68c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b68c-134">Requirement</span></span> | <span data-ttu-id="3b68c-135">Value</span><span class="sxs-lookup"><span data-stu-id="3b68c-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b68c-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b68c-136">Header</span></span><br/>  | <dl> <span data-ttu-id="3b68c-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b68c-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3b68c-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b68c-138">Library</span></span><br/> | <dl> <span data-ttu-id="3b68c-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b68c-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3b68c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b68c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b68c-141">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="3b68c-141">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
