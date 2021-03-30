---
description: Dibuja texto con formato. Este método admite cadenas ANSI y Unicode.
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: ID3DXFont::D método rawText (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.DrawText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 96636c372ee48d516286935f03d80b8e9815ffc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280312"
---
# <a name="id3dxfontdrawtext-method"></a><span data-ttu-id="458b1-104">ID3DXFont::D método rawText</span><span class="sxs-lookup"><span data-stu-id="458b1-104">ID3DXFont::DrawText method</span></span>

<span data-ttu-id="458b1-105">Dibuja texto con formato.</span><span class="sxs-lookup"><span data-stu-id="458b1-105">Draws formatted text.</span></span> <span data-ttu-id="458b1-106">Este método admite cadenas ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="458b1-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="458b1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="458b1-107">Syntax</span></span>


```C++
INT DrawText(
  [in] LPD3DXSPRITE pSprite,
  [in] LPCTSTR      pString,
  [in] INT          Count,
  [in] LPRECT       pRect,
  [in] DWORD        Format,
  [in] D3DCOLOR     Color
);
```



## <a name="parameters"></a><span data-ttu-id="458b1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="458b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="458b1-109">*pSprite* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="458b1-109">*pSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="458b1-110">Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)**</span><span class="sxs-lookup"><span data-stu-id="458b1-110">Type: **[**LPD3DXSPRITE**](id3dxsprite.md)**</span></span>

<span data-ttu-id="458b1-111">Puntero a un objeto [**ID3DXSprite**](id3dxsprite.md) que contiene la cadena.</span><span class="sxs-lookup"><span data-stu-id="458b1-111">Pointer to an [**ID3DXSprite**](id3dxsprite.md) object that contains the string.</span></span> <span data-ttu-id="458b1-112">Puede ser **null**, en cuyo caso Direct3D presentará la cadena con su propio objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="458b1-112">Can be **NULL**, in which case Direct3D will render the string with its own sprite object.</span></span> <span data-ttu-id="458b1-113">Para mejorar la eficacia, se debe especificar un objeto Sprite si se va a llamar a **DrawText** más de una vez en una fila.</span><span class="sxs-lookup"><span data-stu-id="458b1-113">To improve efficiency, a sprite object should be specified if **DrawText** is to be called more than once in a row.</span></span>

</dd> <dt>

<span data-ttu-id="458b1-114">*pString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="458b1-114">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="458b1-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="458b1-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="458b1-116">Puntero a una cadena que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="458b1-116">Pointer to a string to draw.</span></span> <span data-ttu-id="458b1-117">Si el parámetro Count es-1, la cadena debe terminar en NULL.</span><span class="sxs-lookup"><span data-stu-id="458b1-117">If the Count parameter is -1, the string must be null-terminated.</span></span>

</dd> <dt>

<span data-ttu-id="458b1-118">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="458b1-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="458b1-119">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="458b1-119">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="458b1-120">Especifica el número de caracteres de la cadena.</span><span class="sxs-lookup"><span data-stu-id="458b1-120">Specifies the number of characters in the string.</span></span> <span data-ttu-id="458b1-121">Si Count es-1, se supone que el parámetro pString es un puntero a una cadena terminada en NULL y **DrawText** calcula el recuento de caracteres automáticamente.</span><span class="sxs-lookup"><span data-stu-id="458b1-121">If Count is -1, then the pString parameter is assumed to be a pointer to a null-terminated string and **DrawText** computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="458b1-122">*pRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="458b1-122">*pRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="458b1-123">Tipo: **[ **LPRECT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="458b1-123">Type: **[**LPRECT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="458b1-124">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene el rectángulo, en coordenadas lógicas, en la que se va a dar formato al texto.</span><span class="sxs-lookup"><span data-stu-id="458b1-124">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span> <span data-ttu-id="458b1-125">El valor de la coordenada del lado derecho del rectángulo debe ser mayor que el del lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="458b1-125">The coordinate value of the rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="458b1-126">Del mismo modo, el valor de la coordenada de la parte inferior debe ser mayor que el de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="458b1-126">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

</dd> <dt>

<span data-ttu-id="458b1-127">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="458b1-127">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="458b1-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="458b1-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="458b1-129">Especifica el método para dar formato al texto.</span><span class="sxs-lookup"><span data-stu-id="458b1-129">Specifies the method of formatting the text.</span></span> <span data-ttu-id="458b1-130">Puede ser cualquier combinación de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="458b1-130">It can be any combination of the following values:</span></span>



| <span data-ttu-id="458b1-131">Value</span><span class="sxs-lookup"><span data-stu-id="458b1-131">Value</span></span>                                                                                                                                                         | <span data-ttu-id="458b1-132">Significado</span><span class="sxs-lookup"><span data-stu-id="458b1-132">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <span data-ttu-id="458b1-133"><dt>**\_inferior DT**</dt></span><span class="sxs-lookup"><span data-stu-id="458b1-133"><dt>**DT\_BOTTOM**</dt></span></span> </dl>             | <span data-ttu-id="458b1-134">Justifica el texto en la parte inferior del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="458b1-134">Justifies the text to the bottom of the rectangle.</span></span> <span data-ttu-id="458b1-135">Este valor se debe combinar con DT \_ SINGLELINE.</span><span class="sxs-lookup"><span data-stu-id="458b1-135">This value must be combined with DT\_SINGLELINE.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <span data-ttu-id="458b1-136"><dt>**DT \_ CALCRECT**</dt></span><span class="sxs-lookup"><span data-stu-id="458b1-136"><dt>**DT\_CALCRECT**</dt></span></span> </dl>       | <span data-ttu-id="458b1-137">Determina el ancho y el alto del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="458b1-137">Determines the width and height of the rectangle.</span></span> <span data-ttu-id="458b1-138">Si hay varias líneas de texto, **DrawText** usa el ancho del rectángulo señalado por el parámetro pRect y extiende la base del rectángulo para enlazar la última línea de texto.</span><span class="sxs-lookup"><span data-stu-id="458b1-138">If there are multiple lines of text, **DrawText** uses the width of the rectangle pointed to by the pRect parameter and extends the base of the rectangle to bound the last line of text.</span></span> <span data-ttu-id="458b1-139">Si solo hay una línea de texto, **DrawText** modifica el lado derecho del rectángulo de modo que delimita el último carácter de la línea.</span><span class="sxs-lookup"><span data-stu-id="458b1-139">If there is only one line of text, **DrawText** modifies the right side of the rectangle so that it bounds the last character in the line.</span></span> <span data-ttu-id="458b1-140">En cualquier caso, **DrawText** devuelve el alto del texto con formato, pero no dibuja el texto.</span><span class="sxs-lookup"><span data-stu-id="458b1-140">In either case, **DrawText** returns the height of the formatted text but does not draw the text.</span></span><br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <span data-ttu-id="458b1-141"><dt>**\_Centro DT**</dt></span><span class="sxs-lookup"><span data-stu-id="458b1-141"><dt>**DT\_CENTER**</dt></span></span> </dl>             | <span data-ttu-id="458b1-142">Centra el texto horizontalmente en el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="458b1-142">Centers text horizontally in the rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <span data-ttu-id="458b1-143"><dt>**DT \_ EXPANDTABS**</dt></span><span class="sxs-lookup"><span data-stu-id="458b1-143"><dt>**DT\_EXPANDTABS**</dt></span></span> </dl> | <span data-ttu-id="458b1-144">Expande los caracteres de tabulación.</span><span class="sxs-lookup"><span data-stu-id="458b1-144">Expands tab characters.</span></span> <span data-ttu-id="458b1-145">El número de caracteres predeterminado por tabulación es ocho.</span><span class="sxs-lookup"><span data-stu-id="458b1-145">The default number of characters per tab is eight.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <span data-ttu-id="458b1-146"><dt>**DT a la \_ izquierda**</dt></span><span class="sxs-lookup"><span data-stu-id="458b1-146"><dt>**DT\_LEFT**</dt></span></span> </dl>                   | <span data-ttu-id="458b1-147">Alinea el texto a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="458b1-147">Aligns text to the left.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <span data-ttu-id="458b1-148"><dt>**DT \_ NOclip**</dt></span><span class="sxs-lookup"><span data-stu-id="458b1-148"><dt>**DT\_NOCLIP**</dt></span></span> </dl>             | <span data-ttu-id="458b1-149">Dibuja sin recortes.</span><span class="sxs-lookup"><span data-stu-id="458b1-149">Draws without clipping.</span></span> <span data-ttu-id="458b1-150">**DrawText** es algo más rápido cuando \_ se usa DT noclip.</span><span class="sxs-lookup"><span data-stu-id="458b1-150">**DrawText** is somewhat faster when DT\_NOCLIP is used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <span data-ttu-id="458b1-151"><dt>**\_derecho DT**</dt></span><span class="sxs-lookup"><span data-stu-id="458b1-151"><dt>**DT\_RIGHT**</dt></span></span> </dl>                | <span data-ttu-id="458b1-152">Alinea el texto a la derecha.</span><span class="sxs-lookup"><span data-stu-id="458b1-152">Aligns text to the right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <span data-ttu-id="458b1-153"><dt>**DT \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="458b1-153"><dt>**DT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="458b1-154">Muestra texto en orden de lectura de derecha a izquierda para el texto bidireccional cuando se selecciona una fuente hebreo o árabe.</span><span class="sxs-lookup"><span data-stu-id="458b1-154">Displays text in right-to-left reading order for bidirectional text when a Hebrew or Arabic font is selected.</span></span> <span data-ttu-id="458b1-155">El orden de lectura predeterminado para todo el texto es de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="458b1-155">The default reading order for all text is left-to-right.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <span data-ttu-id="458b1-156"><dt>**DT \_ SINGLELINE**</dt></span><span class="sxs-lookup"><span data-stu-id="458b1-156"><dt>**DT\_SINGLELINE**</dt></span></span> </dl> | <span data-ttu-id="458b1-157">Muestra texto solo en una sola línea.</span><span class="sxs-lookup"><span data-stu-id="458b1-157">Displays text on a single line only.</span></span> <span data-ttu-id="458b1-158">Los retornos de carro y los saltos de línea no interrumpen la línea.</span><span class="sxs-lookup"><span data-stu-id="458b1-158">Carriage returns and line feeds do not break the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <span data-ttu-id="458b1-159"><dt>**\_superior DT**</dt></span><span class="sxs-lookup"><span data-stu-id="458b1-159"><dt>**DT\_TOP**</dt></span></span> </dl>                      | <span data-ttu-id="458b1-160">Texto que justifica la parte superior.</span><span class="sxs-lookup"><span data-stu-id="458b1-160">Top-justifies text.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <span data-ttu-id="458b1-161"><dt>**\_vCenter DT**</dt></span><span class="sxs-lookup"><span data-stu-id="458b1-161"><dt>**DT\_VCENTER**</dt></span></span> </dl>          | <span data-ttu-id="458b1-162">Centra el texto verticalmente (solo una línea).</span><span class="sxs-lookup"><span data-stu-id="458b1-162">Centers text vertically (single line only).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <span data-ttu-id="458b1-163"><dt>**DT \_ WORDBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="458b1-163"><dt>**DT\_WORDBREAK**</dt></span></span> </dl>    | <span data-ttu-id="458b1-164">Rompe las palabras.</span><span class="sxs-lookup"><span data-stu-id="458b1-164">Breaks words.</span></span> <span data-ttu-id="458b1-165">Las líneas se dividen automáticamente entre palabras si una palabra se extiende más allá del borde del rectángulo especificado por el parámetro pRect.</span><span class="sxs-lookup"><span data-stu-id="458b1-165">Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the pRect parameter.</span></span> <span data-ttu-id="458b1-166">Una secuencia de retorno de carro/avance de línea también rompe la línea.</span><span class="sxs-lookup"><span data-stu-id="458b1-166">A carriage return/line feed sequence also breaks the line.</span></span><br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="458b1-167">*Color* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="458b1-167">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="458b1-168">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="458b1-168">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="458b1-169">Color del texto.</span><span class="sxs-lookup"><span data-stu-id="458b1-169">Color of the text.</span></span> <span data-ttu-id="458b1-170">Para obtener más información, vea [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="458b1-170">For more information, see [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="458b1-171">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="458b1-171">Return value</span></span>

<span data-ttu-id="458b1-172">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="458b1-172">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="458b1-173">Si la función se ejecuta correctamente, el valor devuelto es el alto del texto en unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="458b1-173">If the function succeeds, the return value is the height of the text in logical units.</span></span> <span data-ttu-id="458b1-174">Si \_ se especifica dt vCenter o DT \_ Bottom, el valor devuelto es el desplazamiento de pRect (superior a la parte inferior) del texto dibujado.</span><span class="sxs-lookup"><span data-stu-id="458b1-174">If DT\_VCENTER or DT\_BOTTOM is specified, the return value is the offset from pRect (top to the bottom) of the drawn text.</span></span> <span data-ttu-id="458b1-175">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="458b1-175">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="458b1-176">Observaciones</span><span class="sxs-lookup"><span data-stu-id="458b1-176">Remarks</span></span>

<span data-ttu-id="458b1-177">Los parámetros de este método son muy similares a los de la función [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) de GDI.</span><span class="sxs-lookup"><span data-stu-id="458b1-177">The parameters of this method are very similar to those of the GDI [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) function.</span></span>

<span data-ttu-id="458b1-178">Este método admite cadenas ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="458b1-178">This method supports both ANSI and Unicode strings.</span></span>

<span data-ttu-id="458b1-179">Se debe llamar a este método dentro de un [**BeginScene**](/windows/desktop/api) ... Bloque [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .</span><span class="sxs-lookup"><span data-stu-id="458b1-179">This method must be called inside a [**BeginScene**](/windows/desktop/api) ... [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) block.</span></span> <span data-ttu-id="458b1-180">La única excepción es cuando una aplicación llama a **DrawText** con DT \_ CALCRECT para calcular el tamaño de un bloque de texto determinado.</span><span class="sxs-lookup"><span data-stu-id="458b1-180">The only exception is when an application calls **DrawText** with DT\_CALCRECT to calculate the size of a given block of text.</span></span>

<span data-ttu-id="458b1-181">A menos \_ que se use el formato DT noclip, este método recorta el texto para que no aparezca fuera del rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="458b1-181">Unless the DT\_NOCLIP format is used, this method clips the text so that it does not appear outside the specified rectangle.</span></span> <span data-ttu-id="458b1-182">Se supone que todo el formato tiene varias líneas a menos que \_ se especifique el formato DT SINGLELINE.</span><span class="sxs-lookup"><span data-stu-id="458b1-182">All formatting is assumed to have multiple lines unless the DT\_SINGLELINE format is specified.</span></span>

<span data-ttu-id="458b1-183">Si la fuente seleccionada es demasiado grande para el rectángulo, este método no intenta sustituir una fuente menor.</span><span class="sxs-lookup"><span data-stu-id="458b1-183">If the selected font is too large for the rectangle, this method does not attempt to substitute a smaller font.</span></span>

<span data-ttu-id="458b1-184">Este método solo admite fuentes cuyo escape y orientación son cero.</span><span class="sxs-lookup"><span data-stu-id="458b1-184">This method supports only fonts whose escapement and orientation are both zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="458b1-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="458b1-185">Requirements</span></span>



| <span data-ttu-id="458b1-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="458b1-186">Requirement</span></span> | <span data-ttu-id="458b1-187">Value</span><span class="sxs-lookup"><span data-stu-id="458b1-187">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="458b1-188">Encabezado</span><span class="sxs-lookup"><span data-stu-id="458b1-188">Header</span></span><br/>  | <dl> <span data-ttu-id="458b1-189"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="458b1-189"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="458b1-190">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="458b1-190">Library</span></span><br/> | <dl> <span data-ttu-id="458b1-191"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="458b1-191"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="458b1-192">Vea también</span><span class="sxs-lookup"><span data-stu-id="458b1-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="458b1-193">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="458b1-193">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
