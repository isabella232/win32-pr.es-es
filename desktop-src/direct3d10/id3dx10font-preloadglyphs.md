---
description: Cargue una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: ID3DX10Font::P método reloadGlyphs (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadGlyphs
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fdb67b8a25912c6efc49ef27082d3b6b4e843b33
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707894"
---
# <a name="id3dx10fontpreloadglyphs-method"></a><span data-ttu-id="8af61-103">ID3DX10Font::P método reloadGlyphs</span><span class="sxs-lookup"><span data-stu-id="8af61-103">ID3DX10Font::PreloadGlyphs method</span></span>

<span data-ttu-id="8af61-104">Cargue una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8af61-104">Load a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8af61-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8af61-105">Syntax</span></span>


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="8af61-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8af61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8af61-107">*Primero* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8af61-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8af61-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8af61-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8af61-109">IDENTIFICADOR del primer glifo que se va a cargar en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8af61-109">ID of the first glyph to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="8af61-110">*Última* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8af61-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8af61-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8af61-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8af61-112">IDENTIFICADOR del último glifo que se va a cargar en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8af61-112">ID of the last glyph to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8af61-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8af61-113">Return value</span></span>

<span data-ttu-id="8af61-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8af61-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8af61-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8af61-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8af61-116">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="8af61-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="8af61-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8af61-117">Remarks</span></span>

<span data-ttu-id="8af61-118">Este método genera texturas que contienen los glifos de entrada.</span><span class="sxs-lookup"><span data-stu-id="8af61-118">This method generates textures that contain the input glyphs.</span></span> <span data-ttu-id="8af61-119">Los glifos se dibujan como una serie de triángulos.</span><span class="sxs-lookup"><span data-stu-id="8af61-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="8af61-120">Los glifos no se representarán en el dispositivo; ID3DX10Font: se debe llamar a:D rawText para representar los glifos.</span><span class="sxs-lookup"><span data-stu-id="8af61-120">Glyphs will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the glyphs.</span></span> <span data-ttu-id="8af61-121">Sin embargo, al precargar los glifos en la memoria de vídeo, ID3DX10Font::D rawText usarán prácticamente menos recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="8af61-121">However, by pre-loading glyphs into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="8af61-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8af61-122">Requirements</span></span>



| <span data-ttu-id="8af61-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8af61-123">Requirement</span></span> | <span data-ttu-id="8af61-124">Value</span><span class="sxs-lookup"><span data-stu-id="8af61-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8af61-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8af61-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8af61-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8af61-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8af61-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8af61-127">Library</span></span><br/> | <dl> <span data-ttu-id="8af61-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8af61-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8af61-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="8af61-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af61-130">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="8af61-130">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="8af61-131">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="8af61-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
