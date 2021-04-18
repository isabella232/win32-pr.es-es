---
description: Carga una serie de caracteres en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.
ms.assetid: bb49842e-99de-406b-bf4b-139d6499f96e
title: ID3DXFont::P método reloadCharacters (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadCharacters
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9262fcb386b9362093ad563bd851946fd2305c7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718483"
---
# <a name="id3dxfontpreloadcharacters-method"></a><span data-ttu-id="ae2f7-103">ID3DXFont::P método reloadCharacters</span><span class="sxs-lookup"><span data-stu-id="ae2f7-103">ID3DXFont::PreloadCharacters method</span></span>

<span data-ttu-id="ae2f7-104">Carga una serie de caracteres en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae2f7-104">Loads a series of characters into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae2f7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae2f7-105">Syntax</span></span>


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="ae2f7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae2f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae2f7-107">*Primero* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae2f7-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae2f7-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae2f7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae2f7-109">IDENTIFICADOR del primer carácter que se va a cargar en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae2f7-109">ID of the first character to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="ae2f7-110">*Última* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae2f7-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae2f7-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae2f7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae2f7-112">IDENTIFICADOR del último carácter que se va a cargar en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae2f7-112">ID of the last character to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae2f7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae2f7-113">Return value</span></span>

<span data-ttu-id="ae2f7-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae2f7-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae2f7-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ae2f7-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ae2f7-116">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="ae2f7-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae2f7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae2f7-117">Remarks</span></span>

<span data-ttu-id="ae2f7-118">Este método genera texturas que contienen glifos que representan los caracteres de entrada.</span><span class="sxs-lookup"><span data-stu-id="ae2f7-118">This method generates textures containing glyphs that represent the input characters.</span></span> <span data-ttu-id="ae2f7-119">Los glifos se dibujan como una serie de triángulos.</span><span class="sxs-lookup"><span data-stu-id="ae2f7-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="ae2f7-120">Los caracteres no se representarán en el dispositivo; También se debe llamar a [**DrawText**](id3dxfont--drawtext.md) para representar los caracteres.</span><span class="sxs-lookup"><span data-stu-id="ae2f7-120">Characters will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the characters.</span></span> <span data-ttu-id="ae2f7-121">Sin embargo, al cargar previamente los caracteres en la memoria de vídeo, **DrawText** usará prácticamente menos recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="ae2f7-121">However, by pre-loading characters into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="ae2f7-122">Este método convierte internamente los caracteres en glifos mediante la función GDI [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span><span class="sxs-lookup"><span data-stu-id="ae2f7-122">This method internally converts characters to glyphs using the GDI function [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2f7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae2f7-123">Requirements</span></span>



| <span data-ttu-id="ae2f7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae2f7-124">Requirement</span></span> | <span data-ttu-id="ae2f7-125">Value</span><span class="sxs-lookup"><span data-stu-id="ae2f7-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2f7-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae2f7-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ae2f7-127"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae2f7-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ae2f7-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ae2f7-128">Library</span></span><br/> | <dl> <span data-ttu-id="ae2f7-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae2f7-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ae2f7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae2f7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2f7-131">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="ae2f7-131">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
