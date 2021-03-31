---
description: Carga texto con formato en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo. Este método admite cadenas ANSI y Unicode.
ms.assetid: f2a4e9f5-87c5-46c0-965d-ce1535a6921d
title: ID3DXFont::P método reloadText (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 958979e3008cf9ae0b79e2de3591635187df0f12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157248"
---
# <a name="id3dxfontpreloadtext-method"></a><span data-ttu-id="d207c-104">ID3DXFont::P método reloadText</span><span class="sxs-lookup"><span data-stu-id="d207c-104">ID3DXFont::PreloadText method</span></span>

<span data-ttu-id="d207c-105">Carga texto con formato en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d207c-105">Loads formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="d207c-106">Este método admite cadenas ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="d207c-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="d207c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d207c-107">Syntax</span></span>


```C++
HRESULT PreloadText(
  [in] LPCTSTR *pString,
  [in] INT     Count
);
```



## <a name="parameters"></a><span data-ttu-id="d207c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d207c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d207c-109">*pString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d207c-109">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d207c-110">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d207c-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d207c-111">Puntero a una cadena de caracteres que se va a cargar en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d207c-111">Pointer to a string of characters to be loaded into video memory.</span></span> <span data-ttu-id="d207c-112">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR; de lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="d207c-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR; otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="d207c-113">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="d207c-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d207c-114">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d207c-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d207c-115">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d207c-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d207c-116">Número de caracteres de la cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="d207c-116">Number of characters in the text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d207c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d207c-117">Return value</span></span>

<span data-ttu-id="d207c-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d207c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d207c-119">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d207c-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d207c-120">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="d207c-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="d207c-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d207c-121">Remarks</span></span>

<span data-ttu-id="d207c-122">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="d207c-122">The compiler setting also determines the function version.</span></span> <span data-ttu-id="d207c-123">Si se define Unicode, la llamada de función se resuelve como PreloadTextW.</span><span class="sxs-lookup"><span data-stu-id="d207c-123">If Unicode is defined, the function call resolves to PreloadTextW.</span></span> <span data-ttu-id="d207c-124">De lo contrario, la llamada de función se resuelve como PreloadTextA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="d207c-124">Otherwise, the function call resolves to PreloadTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="d207c-125">Este método genera texturas que contienen glifos que representan el texto de entrada.</span><span class="sxs-lookup"><span data-stu-id="d207c-125">This method generates textures that contain glyphs that represent the input text.</span></span> <span data-ttu-id="d207c-126">Los glifos se dibujan como una serie de triángulos.</span><span class="sxs-lookup"><span data-stu-id="d207c-126">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="d207c-127">El texto no se representará en el dispositivo; También se debe llamar a [**DrawText**](id3dxfont--drawtext.md) para representar el texto.</span><span class="sxs-lookup"><span data-stu-id="d207c-127">Text will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the text.</span></span> <span data-ttu-id="d207c-128">Sin embargo, al cargar previamente texto en la memoria de vídeo, **DrawText** usará prácticamente menos recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="d207c-128">However, by preloading text into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="d207c-129">Este método convierte internamente los caracteres en glifos mediante la función GDI [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span><span class="sxs-lookup"><span data-stu-id="d207c-129">This method internally converts characters to glyphs using the GDI function [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span></span>

## <a name="requirements"></a><span data-ttu-id="d207c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d207c-130">Requirements</span></span>



| <span data-ttu-id="d207c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d207c-131">Requirement</span></span> | <span data-ttu-id="d207c-132">Value</span><span class="sxs-lookup"><span data-stu-id="d207c-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d207c-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d207c-133">Header</span></span><br/>  | <dl> <span data-ttu-id="d207c-134"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d207c-134"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d207c-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d207c-135">Library</span></span><br/> | <dl> <span data-ttu-id="d207c-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d207c-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d207c-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="d207c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d207c-138">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="d207c-138">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
