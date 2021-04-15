---
description: Establece un valor de la clase textura que indica la clase textura según la ubicación de cada textura.
ms.assetid: cb2e6afb-4b6a-4b01-aaa8-1fd2d1f2bfa1
title: 'ID3DXTextureGutterHelper:: SetGutterMap (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d3c0b7c7e33664f3e078eca82a6f39b1294992a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708035"
---
# <a name="id3dxtexturegutterhelpersetguttermap-method"></a><span data-ttu-id="6f76d-103">ID3DXTextureGutterHelper:: SetGutterMap (método)</span><span class="sxs-lookup"><span data-stu-id="6f76d-103">ID3DXTextureGutterHelper::SetGutterMap method</span></span>

<span data-ttu-id="6f76d-104">Establece un valor de la clase textura que indica la clase textura según la ubicación de cada textura.</span><span class="sxs-lookup"><span data-stu-id="6f76d-104">Sets a texel class value that indicates texel class according to each texel's location.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f76d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f76d-105">Syntax</span></span>


```C++
HRESULT SetGutterMap(
  [in] BYTE *pGutterData
);
```



## <a name="parameters"></a><span data-ttu-id="6f76d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f76d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f76d-107">*pGutterData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f76d-107">*pGutterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f76d-108">Tipo: **[ **byte**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f76d-108">Type: **[**BYTE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6f76d-109">Puntero a la clase textura.</span><span class="sxs-lookup"><span data-stu-id="6f76d-109">Pointer to the texel class.</span></span> <span data-ttu-id="6f76d-110">Las clases posibles de textura son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="6f76d-110">Possible texel classes are as follows.</span></span> <span data-ttu-id="6f76d-111">No hay ninguna clase textura 3.</span><span class="sxs-lookup"><span data-stu-id="6f76d-111">There is no texel class 3.</span></span>



| <span data-ttu-id="6f76d-112">Clase textura</span><span class="sxs-lookup"><span data-stu-id="6f76d-112">Texel Class</span></span> | <span data-ttu-id="6f76d-113">Ubicación de textura</span><span class="sxs-lookup"><span data-stu-id="6f76d-113">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f76d-114">0</span><span class="sxs-lookup"><span data-stu-id="6f76d-114">0</span></span>           | <span data-ttu-id="6f76d-115">Punto no válido; no se usará textura.</span><span class="sxs-lookup"><span data-stu-id="6f76d-115">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="6f76d-116">1</span><span class="sxs-lookup"><span data-stu-id="6f76d-116">1</span></span>           | <span data-ttu-id="6f76d-117">Triángulo interior.</span><span class="sxs-lookup"><span data-stu-id="6f76d-117">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6f76d-118">2</span><span class="sxs-lookup"><span data-stu-id="6f76d-118">2</span></span>           | <span data-ttu-id="6f76d-119">Encuadernación interior.</span><span class="sxs-lookup"><span data-stu-id="6f76d-119">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="6f76d-120">4</span><span class="sxs-lookup"><span data-stu-id="6f76d-120">4</span></span>           | <span data-ttu-id="6f76d-121">Encuadernación interior; textura se evaluará como un ejemplo completo en los métodos [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)o [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="6f76d-121">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f76d-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f76d-122">Return value</span></span>

<span data-ttu-id="6f76d-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6f76d-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6f76d-124">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6f76d-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6f76d-125">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="6f76d-125">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="6f76d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f76d-126">Requirements</span></span>



| <span data-ttu-id="6f76d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f76d-127">Requirement</span></span> | <span data-ttu-id="6f76d-128">Value</span><span class="sxs-lookup"><span data-stu-id="6f76d-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f76d-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f76d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6f76d-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f76d-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6f76d-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f76d-131">Library</span></span><br/> | <dl> <span data-ttu-id="6f76d-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f76d-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6f76d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f76d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f76d-134">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="6f76d-134">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
