---
description: Aplica medianils a un búfer de textura flotante.
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: 'ID3DXTextureGutterHelper:: ApplyGuttersFloat (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00ee6eac7328ee5f6adceb5b3966c222509237b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718285"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a><span data-ttu-id="da4de-103">ID3DXTextureGutterHelper:: ApplyGuttersFloat (método)</span><span class="sxs-lookup"><span data-stu-id="da4de-103">ID3DXTextureGutterHelper::ApplyGuttersFloat method</span></span>

<span data-ttu-id="da4de-104">Aplica medianils a un búfer de textura flotante.</span><span class="sxs-lookup"><span data-stu-id="da4de-104">Applies gutters to a FLOAT texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="da4de-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da4de-105">Syntax</span></span>


```C++
HRESULT ApplyGuttersFloat(
  [in] FLOAT *pDataIn,
  [in] UINT  *NumCoeffs,
  [in] UINT  *Width,
  [in] UINT  *Height
);
```



## <a name="parameters"></a><span data-ttu-id="da4de-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da4de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da4de-107">*pDataIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da4de-107">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da4de-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="da4de-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="da4de-109">Puntero a un búfer de datos de textura flotante.</span><span class="sxs-lookup"><span data-stu-id="da4de-109">Pointer to a buffer of FLOAT texture data.</span></span>

</dd> <dt>

<span data-ttu-id="da4de-110">*NumCoeffs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da4de-110">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da4de-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="da4de-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="da4de-112">Número de escalas por canal de color utilizadas en la memoria para almacenar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="da4de-112">Number of scalars per color channel used in memory to store samples.</span></span> <span data-ttu-id="da4de-113">Cada textura contiene valores de NumCoeffs FLOAT.</span><span class="sxs-lookup"><span data-stu-id="da4de-113">Each texel contains NumCoeffs FLOAT values.</span></span>

</dd> <dt>

<span data-ttu-id="da4de-114">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="da4de-114">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da4de-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="da4de-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="da4de-116">Ancho de la textura, en píxeles, Obtenido de [**ID3DXTextureGutterHelper:: GetWidth**](id3dxtexturegutterhelper--getwidth.md).</span><span class="sxs-lookup"><span data-stu-id="da4de-116">Width of the texture, in pixels, obtained from [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md).</span></span>

</dd> <dt>

<span data-ttu-id="da4de-117">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="da4de-117">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da4de-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="da4de-118">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="da4de-119">Alto de la textura, en píxeles, Obtenido de [**ID3DXTextureGutterHelper:: getHeight**](id3dxtexturegutterhelper--getheight.md).</span><span class="sxs-lookup"><span data-stu-id="da4de-119">Height of the texture, in pixels, obtained from [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da4de-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da4de-120">Return value</span></span>

<span data-ttu-id="da4de-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="da4de-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="da4de-122">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="da4de-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="da4de-123">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="da4de-123">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="da4de-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da4de-124">Remarks</span></span>

<span data-ttu-id="da4de-125">La [**clase 2 textura**](id3dxtexturegutterhelper.md) se generan al volver a muestrear las clases 1 y 4 textura.</span><span class="sxs-lookup"><span data-stu-id="da4de-125">[**Class 2 texels**](id3dxtexturegutterhelper.md) are generated by resampling class 1 and 4 texels.</span></span>

## <a name="requirements"></a><span data-ttu-id="da4de-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da4de-126">Requirements</span></span>



| <span data-ttu-id="da4de-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="da4de-127">Requirement</span></span> | <span data-ttu-id="da4de-128">Value</span><span class="sxs-lookup"><span data-stu-id="da4de-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da4de-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da4de-129">Header</span></span><br/>  | <dl> <span data-ttu-id="da4de-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="da4de-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="da4de-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="da4de-131">Library</span></span><br/> | <dl> <span data-ttu-id="da4de-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da4de-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="da4de-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="da4de-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da4de-134">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="da4de-134">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
