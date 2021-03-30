---
description: Cargue texto con formato en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo. Este método admite cadenas ANSI y Unicode.
ms.assetid: 0e5380fc-7a01-4e09-9c18-22087be56780
title: ID3DX10Font::P método reloadText (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7294fb7e86b3532960a34a15e1118dc33f748f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280339"
---
# <a name="id3dx10fontpreloadtext-method"></a><span data-ttu-id="73815-104">ID3DX10Font::P método reloadText</span><span class="sxs-lookup"><span data-stu-id="73815-104">ID3DX10Font::PreloadText method</span></span>

<span data-ttu-id="73815-105">Cargue texto con formato en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73815-105">Load formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="73815-106">Este método admite cadenas ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="73815-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="73815-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73815-107">Syntax</span></span>


```C++
HRESULT PreloadText(
  [in] LPCSTR pString,
  [in] INT    Count
);
```



## <a name="parameters"></a><span data-ttu-id="73815-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73815-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73815-109">*pString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73815-109">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73815-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73815-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73815-111">Puntero a una cadena de caracteres que se va a cargar en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="73815-111">Pointer to a string of characters to be loaded into video memory.</span></span> <span data-ttu-id="73815-112">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR; de lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="73815-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR; otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="73815-113">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="73815-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="73815-114">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73815-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73815-115">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73815-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73815-116">Número de caracteres de la cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="73815-116">Number of characters in the text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73815-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73815-117">Return value</span></span>

<span data-ttu-id="73815-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="73815-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="73815-119">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="73815-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="73815-120">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="73815-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="73815-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73815-121">Remarks</span></span>

<span data-ttu-id="73815-122">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="73815-122">The compiler setting also determines the function version.</span></span> <span data-ttu-id="73815-123">Si se define Unicode, la llamada de función se resuelve como PreloadTextW.</span><span class="sxs-lookup"><span data-stu-id="73815-123">If Unicode is defined, the function call resolves to PreloadTextW.</span></span> <span data-ttu-id="73815-124">De lo contrario, la llamada de función se resuelve como PreloadTextA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="73815-124">Otherwise, the function call resolves to PreloadTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="73815-125">Este método genera texturas que contienen glifos que representan el texto de entrada.</span><span class="sxs-lookup"><span data-stu-id="73815-125">This method generates textures that contain glyphs that represent the input text.</span></span> <span data-ttu-id="73815-126">Los glifos se dibujan como una serie de triángulos.</span><span class="sxs-lookup"><span data-stu-id="73815-126">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="73815-127">El texto no se representará en el dispositivo; ID3DX10Font: se debe llamar a:D rawText para representar el texto.</span><span class="sxs-lookup"><span data-stu-id="73815-127">Text will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the text.</span></span> <span data-ttu-id="73815-128">Sin embargo, al cargar previamente texto en la memoria de vídeo, ID3DX10Font::D rawText usarán de forma significativa menos recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="73815-128">However, by preloading text into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="73815-129">Este método convierte internamente los caracteres en glifos mediante la función GDI [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73815-129">This method internally converts characters to glyphs using the GDI function [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="73815-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73815-130">Requirements</span></span>



| <span data-ttu-id="73815-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="73815-131">Requirement</span></span> | <span data-ttu-id="73815-132">Value</span><span class="sxs-lookup"><span data-stu-id="73815-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73815-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73815-133">Header</span></span><br/>  | <dl> <span data-ttu-id="73815-134"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="73815-134"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="73815-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73815-135">Library</span></span><br/> | <dl> <span data-ttu-id="73815-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73815-136"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73815-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="73815-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73815-138">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="73815-138">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="73815-139">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="73815-139">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
