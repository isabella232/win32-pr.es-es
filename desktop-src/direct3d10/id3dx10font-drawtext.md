---
description: Dibujar texto con formato. Este método admite cadenas ANSI y Unicode.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: ID3DX10Font::D método rawText (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.DrawText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5fa23684be1b63cfbd8e3d07d3578d87fdfbf46a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698266"
---
# <a name="id3dx10fontdrawtext-method"></a><span data-ttu-id="65a4f-104">ID3DX10Font::D método rawText</span><span class="sxs-lookup"><span data-stu-id="65a4f-104">ID3DX10Font::DrawText method</span></span>

<span data-ttu-id="65a4f-105">Dibujar texto con formato.</span><span class="sxs-lookup"><span data-stu-id="65a4f-105">Draw formatted text.</span></span> <span data-ttu-id="65a4f-106">Este método admite cadenas ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="65a4f-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="65a4f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65a4f-107">Syntax</span></span>


```C++
INT DrawText(
  [in] LPD3DX10SPRITE pSprite,
  [in] LPCTSTR        pString,
  [in] INT            Count,
  [in] LPRECT         pRect,
  [in] UINT           Format,
  [in] D3DXCOLOR      Color
);
```



## <a name="parameters"></a><span data-ttu-id="65a4f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65a4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65a4f-109">*pSprite* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65a4f-109">*pSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a4f-110">Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**</span><span class="sxs-lookup"><span data-stu-id="65a4f-110">Type: **[**LPD3DX10SPRITE**](id3dx10sprite.md)**</span></span>

<span data-ttu-id="65a4f-111">Puntero a un objeto ID3DX10Sprite que contiene la cadena que desea dibujar.</span><span class="sxs-lookup"><span data-stu-id="65a4f-111">Pointer to an ID3DX10Sprite object that contains the string you wish to draw.</span></span> <span data-ttu-id="65a4f-112">Puede ser **null**, en cuyo caso Direct3D presentará la cadena con su propio objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="65a4f-112">Can be **NULL**, in which case Direct3D will render the string with its own sprite object.</span></span> <span data-ttu-id="65a4f-113">Para mejorar la eficacia, se debe especificar un objeto Sprite si ID3DX10Font::D rawText se va a llamar más de una vez en una fila.</span><span class="sxs-lookup"><span data-stu-id="65a4f-113">To improve efficiency, a sprite object should be specified if ID3DX10Font::DrawText is to be called more than once in a row.</span></span>

</dd> <dt>

<span data-ttu-id="65a4f-114">*pString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65a4f-114">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a4f-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65a4f-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65a4f-116">Puntero a una cadena que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="65a4f-116">Pointer to a string to draw.</span></span> <span data-ttu-id="65a4f-117">Si se define Unicode, este tipo de parámetro se resuelve en un LPCWSTR; de lo contrario, el tipo se resuelve como un LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="65a4f-117">If UNICODE is defined, this parameter type resolves to an LPCWSTR, otherwise, the type resolves to an LPCSTR.</span></span> <span data-ttu-id="65a4f-118">Si el parámetro Count es-1, la cadena debe terminar en **null** .</span><span class="sxs-lookup"><span data-stu-id="65a4f-118">If the Count parameter is -1, the string must be **NULL** terminated.</span></span>

</dd> <dt>

<span data-ttu-id="65a4f-119">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65a4f-119">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a4f-120">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65a4f-120">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65a4f-121">Número de caracteres de la cadena.</span><span class="sxs-lookup"><span data-stu-id="65a4f-121">The number of characters in the string.</span></span> <span data-ttu-id="65a4f-122">Si Count es-1, se supone que el parámetro pString es un puntero a un Sprite que contiene una cadena terminada en NULL y ID3DX10Font::D rawText calcula el recuento de caracteres automáticamente.</span><span class="sxs-lookup"><span data-stu-id="65a4f-122">If Count is -1, then the pString parameter is assumed to be a pointer to a sprite containing a NULL-terminated string and ID3DX10Font::DrawText computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="65a4f-123">*pRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65a4f-123">*pRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a4f-124">Tipo: **LPRECT**</span><span class="sxs-lookup"><span data-stu-id="65a4f-124">Type: **LPRECT**</span></span>

<span data-ttu-id="65a4f-125">Puntero a una estructura [Rect](/previous-versions//ms536136(v=vs.85)) que contiene el rectángulo, en coordenadas lógicas, en la que se va a dar formato al texto.</span><span class="sxs-lookup"><span data-stu-id="65a4f-125">Pointer to a [RECT](/previous-versions//ms536136(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span> <span data-ttu-id="65a4f-126">Como con cualquier objeto RECT, el valor de la coordenada del lado derecho del rectángulo debe ser mayor que el del lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="65a4f-126">As with any RECT object, the coordinate value of the rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="65a4f-127">Del mismo modo, el valor de la coordenada de la parte inferior debe ser mayor que el de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="65a4f-127">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

</dd> <dt>

<span data-ttu-id="65a4f-128">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65a4f-128">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a4f-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65a4f-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65a4f-130">Especifique el método para dar formato al texto.</span><span class="sxs-lookup"><span data-stu-id="65a4f-130">Specify the method of formatting the text.</span></span> <span data-ttu-id="65a4f-131">Puede ser cualquier combinación de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="65a4f-131">It can be any combination of the following values:</span></span>



| <span data-ttu-id="65a4f-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="65a4f-132">Item</span></span>                                                                                      | <span data-ttu-id="65a4f-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="65a4f-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65a4f-134"><span id="DT_BOTTOM"></span><span id="dt_bottom"></span>\_inferior DT</span><span class="sxs-lookup"><span data-stu-id="65a4f-134"><span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT\_BOTTOM</span></span><br/>             | <span data-ttu-id="65a4f-135">Justifique el texto en la parte inferior del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="65a4f-135">Justify the text to the bottom of the rectangle.</span></span> <span data-ttu-id="65a4f-136">Este valor se debe combinar con DT \_ SINGLELINE.</span><span class="sxs-lookup"><span data-stu-id="65a4f-136">This value must be combined with DT\_SINGLELINE.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="65a4f-137"><span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT \_ CALCRECT</span><span class="sxs-lookup"><span data-stu-id="65a4f-137"><span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT\_CALCRECT</span></span><br/>       | <span data-ttu-id="65a4f-138">Indique a DrawText que calcule automáticamente el ancho y el alto del rectángulo en función de la longitud de la cadena que indica que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="65a4f-138">Tell DrawText to automatically calculate the width and height of the rectangle based on the length of the string you tell it to draw.</span></span> <span data-ttu-id="65a4f-139">Si hay varias líneas de texto, ID3DX10Font::D rawText usa el ancho del rectángulo al que apunta el parámetro pRect y extiende la base del rectángulo para enlazar la última línea de texto.</span><span class="sxs-lookup"><span data-stu-id="65a4f-139">If there are multiple lines of text, ID3DX10Font::DrawText uses the width of the rectangle pointed to by the pRect parameter and extends the base of the rectangle to bound the last line of text.</span></span> <span data-ttu-id="65a4f-140">Si solo hay una línea de texto, ID3DX10Font::D rawText modifica el lado derecho del rectángulo de modo que delimita el último carácter de la línea.</span><span class="sxs-lookup"><span data-stu-id="65a4f-140">If there is only one line of text, ID3DX10Font::DrawText modifies the right side of the rectangle so that it bounds the last character in the line.</span></span> <span data-ttu-id="65a4f-141">En cualquier caso, ID3DX10Font::D rawText devuelve el alto del texto con formato, pero no dibuja el texto.</span><span class="sxs-lookup"><span data-stu-id="65a4f-141">In either case, ID3DX10Font::DrawText returns the height of the formatted text but does not draw the text.</span></span><br/> |
| <span data-ttu-id="65a4f-142"><span id="DT_CENTER"></span><span id="dt_center"></span>\_Centro DT</span><span class="sxs-lookup"><span data-stu-id="65a4f-142"><span id="DT_CENTER"></span><span id="dt_center"></span>DT\_CENTER</span></span><br/>             | <span data-ttu-id="65a4f-143">Centrar el texto horizontalmente en el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="65a4f-143">Center text horizontally in the rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="65a4f-144"><span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT \_ EXPANDTABS</span><span class="sxs-lookup"><span data-stu-id="65a4f-144"><span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT\_EXPANDTABS</span></span><br/> | <span data-ttu-id="65a4f-145">Expandir caracteres de tabulación.</span><span class="sxs-lookup"><span data-stu-id="65a4f-145">Expand tab characters.</span></span> <span data-ttu-id="65a4f-146">El número de caracteres predeterminado por tabulación es ocho.</span><span class="sxs-lookup"><span data-stu-id="65a4f-146">The default number of characters per tab is eight.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="65a4f-147"><span id="DT_LEFT"></span><span id="dt_left"></span>DT a la \_ izquierda</span><span class="sxs-lookup"><span data-stu-id="65a4f-147"><span id="DT_LEFT"></span><span id="dt_left"></span>DT\_LEFT</span></span><br/>                   | <span data-ttu-id="65a4f-148">Alinear el texto a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="65a4f-148">Align text to the left.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="65a4f-149"><span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT \_ NOclip</span><span class="sxs-lookup"><span data-stu-id="65a4f-149"><span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT\_NOCLIP</span></span><br/>             | <span data-ttu-id="65a4f-150">Dibuja sin recortes.</span><span class="sxs-lookup"><span data-stu-id="65a4f-150">Draw without clipping.</span></span> <span data-ttu-id="65a4f-151">ID3DX10Font::D rawText es algo más rápido cuando \_ se usa DT noclip.</span><span class="sxs-lookup"><span data-stu-id="65a4f-151">ID3DX10Font::DrawText is somewhat faster when DT\_NOCLIP is used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="65a4f-152"><span id="DT_RIGHT"></span><span id="dt_right"></span>\_derecho DT</span><span class="sxs-lookup"><span data-stu-id="65a4f-152"><span id="DT_RIGHT"></span><span id="dt_right"></span>DT\_RIGHT</span></span><br/>                | <span data-ttu-id="65a4f-153">Alinear el texto a la derecha.</span><span class="sxs-lookup"><span data-stu-id="65a4f-153">Align text to the right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="65a4f-154"><span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT \_ RTLREADING</span><span class="sxs-lookup"><span data-stu-id="65a4f-154"><span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT\_RTLREADING</span></span><br/> | <span data-ttu-id="65a4f-155">Muestra texto en orden de lectura de derecha a izquierda para el texto bidireccional cuando se selecciona una fuente hebreo o árabe.</span><span class="sxs-lookup"><span data-stu-id="65a4f-155">Display text in right-to-left reading order for bidirectional text when a Hebrew or Arabic font is selected.</span></span> <span data-ttu-id="65a4f-156">El orden de lectura predeterminado para todo el texto es de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="65a4f-156">The default reading order for all text is left-to-right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="65a4f-157"><span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ SINGLELINE</span><span class="sxs-lookup"><span data-stu-id="65a4f-157"><span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT\_SINGLELINE</span></span><br/> | <span data-ttu-id="65a4f-158">Mostrar texto solo en una sola línea.</span><span class="sxs-lookup"><span data-stu-id="65a4f-158">Display text on a single line only.</span></span> <span data-ttu-id="65a4f-159">Los retornos de carro y los saltos de línea no interrumpen la línea.</span><span class="sxs-lookup"><span data-stu-id="65a4f-159">Carriage returns and line feeds do not break the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="65a4f-160"><span id="DT_TOP"></span><span id="dt_top"></span>\_superior DT</span><span class="sxs-lookup"><span data-stu-id="65a4f-160"><span id="DT_TOP"></span><span id="dt_top"></span>DT\_TOP</span></span><br/>                      | <span data-ttu-id="65a4f-161">Texto que justifica la parte superior.</span><span class="sxs-lookup"><span data-stu-id="65a4f-161">Top-justify text.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="65a4f-162"><span id="DT_VCENTER"></span><span id="dt_vcenter"></span>\_vCenter DT</span><span class="sxs-lookup"><span data-stu-id="65a4f-162"><span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT\_VCENTER</span></span><br/>          | <span data-ttu-id="65a4f-163">Centrar el texto verticalmente (solo una línea).</span><span class="sxs-lookup"><span data-stu-id="65a4f-163">Center text vertically (single line only).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="65a4f-164"><span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT \_ WORDBREAK</span><span class="sxs-lookup"><span data-stu-id="65a4f-164"><span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT\_WORDBREAK</span></span><br/>    | <span data-ttu-id="65a4f-165">Romper palabras.</span><span class="sxs-lookup"><span data-stu-id="65a4f-165">Break words.</span></span> <span data-ttu-id="65a4f-166">Las líneas se dividen automáticamente entre palabras si una palabra se extiende más allá del borde del rectángulo especificado por el parámetro pRect.</span><span class="sxs-lookup"><span data-stu-id="65a4f-166">Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the pRect parameter.</span></span> <span data-ttu-id="65a4f-167">Una secuencia de retorno de carro/avance de línea también rompe la línea.</span><span class="sxs-lookup"><span data-stu-id="65a4f-167">A carriage return/line feed sequence also breaks the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="65a4f-168">*Color* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="65a4f-168">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a4f-169">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="65a4f-169">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="65a4f-170">Color del texto.</span><span class="sxs-lookup"><span data-stu-id="65a4f-170">Color of the text.</span></span> <span data-ttu-id="65a4f-171">Vea [**D3DXCOLOR**](d3d10-d3dxcolor.md).</span><span class="sxs-lookup"><span data-stu-id="65a4f-171">See [**D3DXCOLOR**](d3d10-d3dxcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65a4f-172">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65a4f-172">Return value</span></span>

<span data-ttu-id="65a4f-173">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65a4f-173">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65a4f-174">Si la función se ejecuta correctamente, el valor devuelto es el alto del texto en unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="65a4f-174">If the function succeeds, the return value is the height of the text in logical units.</span></span> <span data-ttu-id="65a4f-175">Si \_ se especifica dt vCenter o DT \_ Bottom, el valor devuelto es el desplazamiento de pRect (superior a la parte inferior) del texto dibujado.</span><span class="sxs-lookup"><span data-stu-id="65a4f-175">If DT\_VCENTER or DT\_BOTTOM is specified, the return value is the offset from pRect (top to the bottom) of the drawn text.</span></span> <span data-ttu-id="65a4f-176">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="65a4f-176">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="65a4f-177">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65a4f-177">Remarks</span></span>

<span data-ttu-id="65a4f-178">Los parámetros de este método son muy similares a los de la función [DrawText de GDI](/previous-versions//ms533909(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="65a4f-178">The parameters of this method are very similar to those of the [GDI DrawText](/previous-versions//ms533909(v=vs.85)) function.</span></span>

<span data-ttu-id="65a4f-179">Este método admite cadenas ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="65a4f-179">This method supports both ANSI and Unicode strings.</span></span>

<span data-ttu-id="65a4f-180">A menos \_ que se use el formato DT noclip, este método recorta el texto para que no aparezca fuera del rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="65a4f-180">Unless the DT\_NOCLIP format is used, this method clips the text so that it does not appear outside the specified rectangle.</span></span> <span data-ttu-id="65a4f-181">Se supone que todo el formato tiene varias líneas a menos que \_ se especifique el formato DT SINGLELINE.</span><span class="sxs-lookup"><span data-stu-id="65a4f-181">All formatting is assumed to have multiple lines unless the DT\_SINGLELINE format is specified.</span></span>

<span data-ttu-id="65a4f-182">Si la fuente seleccionada es demasiado grande para el rectángulo, este método no intenta sustituir una fuente menor.</span><span class="sxs-lookup"><span data-stu-id="65a4f-182">If the selected font is too large for the rectangle, this method does not attempt to substitute a smaller font.</span></span>

<span data-ttu-id="65a4f-183">Este método solo admite fuentes cuyo escape y orientación son cero.</span><span class="sxs-lookup"><span data-stu-id="65a4f-183">This method supports only fonts whose escapement and orientation are both zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="65a4f-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65a4f-184">Requirements</span></span>



| <span data-ttu-id="65a4f-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="65a4f-185">Requirement</span></span> | <span data-ttu-id="65a4f-186">Value</span><span class="sxs-lookup"><span data-stu-id="65a4f-186">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65a4f-187">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65a4f-187">Header</span></span><br/>  | <dl> <span data-ttu-id="65a4f-188"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="65a4f-188"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="65a4f-189">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65a4f-189">Library</span></span><br/> | <dl> <span data-ttu-id="65a4f-190"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65a4f-190"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65a4f-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="65a4f-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65a4f-192">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="65a4f-192">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="65a4f-193">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="65a4f-193">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
