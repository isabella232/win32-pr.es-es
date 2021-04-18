---
description: Recibe un valor de la clase textura que indica la clase textura según la ubicación de cada textura.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: 'ID3DXTextureGutterHelper:: GetGutterMap (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d973e716c598eaceaf7f75e6694a35691df4266
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649419"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a><span data-ttu-id="40000-103">ID3DXTextureGutterHelper:: GetGutterMap (método)</span><span class="sxs-lookup"><span data-stu-id="40000-103">ID3DXTextureGutterHelper::GetGutterMap method</span></span>

<span data-ttu-id="40000-104">Recibe un valor de la clase textura que indica la clase textura según la ubicación de cada textura.</span><span class="sxs-lookup"><span data-stu-id="40000-104">Receives a texel class value that indicates texel class according to each texel's location.</span></span>

## <a name="syntax"></a><span data-ttu-id="40000-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40000-105">Syntax</span></span>


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a><span data-ttu-id="40000-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40000-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40000-107">*pGutterData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="40000-107">*pGutterData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="40000-108">Tipo: **[ **byte**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="40000-108">Type: **[**BYTE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="40000-109">Puntero a la clase textura.</span><span class="sxs-lookup"><span data-stu-id="40000-109">Pointer to the texel class.</span></span> <span data-ttu-id="40000-110">Las clases posibles de textura son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="40000-110">Possible texel classes are as follows.</span></span> <span data-ttu-id="40000-111">No hay ninguna clase textura 3.</span><span class="sxs-lookup"><span data-stu-id="40000-111">There is no texel class 3.</span></span>



| <span data-ttu-id="40000-112">Clase textura</span><span class="sxs-lookup"><span data-stu-id="40000-112">Texel Class</span></span> | <span data-ttu-id="40000-113">Ubicación de textura</span><span class="sxs-lookup"><span data-stu-id="40000-113">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40000-114">0</span><span class="sxs-lookup"><span data-stu-id="40000-114">0</span></span>           | <span data-ttu-id="40000-115">Punto no válido; no se usará textura.</span><span class="sxs-lookup"><span data-stu-id="40000-115">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="40000-116">1</span><span class="sxs-lookup"><span data-stu-id="40000-116">1</span></span>           | <span data-ttu-id="40000-117">Triángulo interior.</span><span class="sxs-lookup"><span data-stu-id="40000-117">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="40000-118">2</span><span class="sxs-lookup"><span data-stu-id="40000-118">2</span></span>           | <span data-ttu-id="40000-119">Encuadernación interior.</span><span class="sxs-lookup"><span data-stu-id="40000-119">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="40000-120">4</span><span class="sxs-lookup"><span data-stu-id="40000-120">4</span></span>           | <span data-ttu-id="40000-121">Encuadernación interior; textura se evaluará como un ejemplo completo en los métodos [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)o [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="40000-121">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40000-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40000-122">Return value</span></span>

<span data-ttu-id="40000-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="40000-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="40000-124">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="40000-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="40000-125">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="40000-125">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="40000-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40000-126">Remarks</span></span>

<span data-ttu-id="40000-127">La aplicación debe asignar y administrar pGutterData, con un tamaño dado por:</span><span class="sxs-lookup"><span data-stu-id="40000-127">The application must allocate and manage pGutterData, with size given by:</span></span>


```
texture width * texture height * sizeof(BYTE)
```



<span data-ttu-id="40000-128">[**ID3DXTextureGutterHelper:: GetWidth**](id3dxtexturegutterhelper--getwidth.md) y [**ID3DXTextureGutterHelper:: getHeight**](id3dxtexturegutterhelper--getheight.md)devuelven el ancho y el alto de la textura.</span><span class="sxs-lookup"><span data-stu-id="40000-128">Texture width and height are returned by [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md) and [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40000-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40000-129">Requirements</span></span>



| <span data-ttu-id="40000-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="40000-130">Requirement</span></span> | <span data-ttu-id="40000-131">Value</span><span class="sxs-lookup"><span data-stu-id="40000-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40000-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40000-132">Header</span></span><br/>  | <dl> <span data-ttu-id="40000-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="40000-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="40000-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40000-134">Library</span></span><br/> | <dl> <span data-ttu-id="40000-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40000-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="40000-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="40000-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40000-137">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="40000-137">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
