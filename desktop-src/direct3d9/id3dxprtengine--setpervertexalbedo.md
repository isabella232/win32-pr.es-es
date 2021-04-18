---
description: Establece un valor de Albedo para cada vértice de la malla, sobrescribiendo los valores de Albedo anteriores.
ms.assetid: 5220dfe3-8d41-480c-a850-b9aad3d2bb2f
title: 'ID3DXPRTEngine:: SetPerVertexAlbedo (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da7a33a79cc50963e87d0eff15baf22ee8d79ce3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649421"
---
# <a name="id3dxprtenginesetpervertexalbedo-method"></a><span data-ttu-id="12bed-103">ID3DXPRTEngine:: SetPerVertexAlbedo (método)</span><span class="sxs-lookup"><span data-stu-id="12bed-103">ID3DXPRTEngine::SetPerVertexAlbedo method</span></span>

<span data-ttu-id="12bed-104">Establece un valor de Albedo para cada vértice de la malla, sobrescribiendo los valores de Albedo anteriores.</span><span class="sxs-lookup"><span data-stu-id="12bed-104">Sets an albedo value for each mesh vertex, overwriting previous albedo values.</span></span>

## <a name="syntax"></a><span data-ttu-id="12bed-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12bed-105">Syntax</span></span>


```C++
HRESULT SetPerVertexAlbedo(
  [in] const VOID *pDataIn,
  [in]       UINT NumChannels,
  [in]       UINT Stride
);
```



## <a name="parameters"></a><span data-ttu-id="12bed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12bed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12bed-107">*pDataIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="12bed-107">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12bed-108">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="12bed-108">Type: **const VOID\***</span></span>

<span data-ttu-id="12bed-109">Puntero a FLOAT Albedo data del primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="12bed-109">Pointer to FLOAT albedo data of the first sample.</span></span>

</dd> <dt>

<span data-ttu-id="12bed-110">*NumChannels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="12bed-110">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12bed-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12bed-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12bed-112">Número de canales de color que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="12bed-112">Number of color channels to set.</span></span> <span data-ttu-id="12bed-113">Establézcalo en 1 para especificar materiales grises (R = G = B) o 3 para habilitar los efectos de sangrado de color.</span><span class="sxs-lookup"><span data-stu-id="12bed-113">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="12bed-114">*STRIDE* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="12bed-114">*Stride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12bed-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12bed-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12bed-116">STRIDE en bytes necesario para obtener el valor de albedo del siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="12bed-116">Stride in bytes needed to get to next sample's albedo value.</span></span> <span data-ttu-id="12bed-117">Vea [ancho frente a paso (Direct3D 9)](width-vs--pitch.md).</span><span class="sxs-lookup"><span data-stu-id="12bed-117">See [Width vs. Pitch (Direct3D 9)](width-vs--pitch.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12bed-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12bed-118">Return value</span></span>

<span data-ttu-id="12bed-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12bed-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12bed-120">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="12bed-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="12bed-121">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="12bed-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="12bed-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12bed-122">Requirements</span></span>



| <span data-ttu-id="12bed-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="12bed-123">Requirement</span></span> | <span data-ttu-id="12bed-124">Value</span><span class="sxs-lookup"><span data-stu-id="12bed-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12bed-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12bed-125">Header</span></span><br/>  | <dl> <span data-ttu-id="12bed-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="12bed-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="12bed-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12bed-127">Library</span></span><br/> | <dl> <span data-ttu-id="12bed-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12bed-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="12bed-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="12bed-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12bed-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="12bed-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
