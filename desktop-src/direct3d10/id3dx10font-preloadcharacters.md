---
description: Cargar una serie de caracteres en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.
ms.assetid: 935a6248-e6b7-4fce-aaa7-b7f0c94c1f79
title: ID3DX10Font::P método reloadCharacters (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadCharacters
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fafa34d4a243e254e929f7c9a1d65d2a3fb9c8dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670237"
---
# <a name="id3dx10fontpreloadcharacters-method"></a><span data-ttu-id="a22e8-103">ID3DX10Font::P método reloadCharacters</span><span class="sxs-lookup"><span data-stu-id="a22e8-103">ID3DX10Font::PreloadCharacters method</span></span>

<span data-ttu-id="a22e8-104">Cargar una serie de caracteres en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a22e8-104">Load a series of characters into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a22e8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a22e8-105">Syntax</span></span>


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="a22e8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a22e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a22e8-107">*Primero* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a22e8-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a22e8-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a22e8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a22e8-109">IDENTIFICADOR del primer carácter que se va a cargar en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a22e8-109">ID of the first character to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="a22e8-110">*Última* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a22e8-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a22e8-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a22e8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a22e8-112">IDENTIFICADOR del último carácter que se va a cargar en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a22e8-112">ID of the last character to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a22e8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a22e8-113">Return value</span></span>

<span data-ttu-id="a22e8-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a22e8-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a22e8-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a22e8-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a22e8-116">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="a22e8-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="a22e8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a22e8-117">Remarks</span></span>

<span data-ttu-id="a22e8-118">Este método genera texturas que contienen glifos que representan los caracteres de entrada.</span><span class="sxs-lookup"><span data-stu-id="a22e8-118">This method generates textures containing glyphs that represent the input characters.</span></span> <span data-ttu-id="a22e8-119">Los glifos se dibujan como una serie de triángulos.</span><span class="sxs-lookup"><span data-stu-id="a22e8-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="a22e8-120">Los caracteres no se representarán en el dispositivo; ID3DX10Font: se debe llamar a:D rawText para representar los caracteres.</span><span class="sxs-lookup"><span data-stu-id="a22e8-120">Characters will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the characters.</span></span> <span data-ttu-id="a22e8-121">Sin embargo, al cargar previamente los caracteres en la memoria de vídeo, ID3DX10Font::D rawText usarán prácticamente menos recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="a22e8-121">However, by pre-loading characters into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="a22e8-122">Este método convierte internamente los caracteres en glifos mediante la función GDI [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a22e8-122">This method internally converts characters to glyphs using the GDI function [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="a22e8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a22e8-123">Requirements</span></span>



| <span data-ttu-id="a22e8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a22e8-124">Requirement</span></span> | <span data-ttu-id="a22e8-125">Value</span><span class="sxs-lookup"><span data-stu-id="a22e8-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a22e8-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a22e8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a22e8-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a22e8-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a22e8-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a22e8-128">Library</span></span><br/> | <dl> <span data-ttu-id="a22e8-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a22e8-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a22e8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a22e8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22e8-131">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="a22e8-131">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="a22e8-132">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="a22e8-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
