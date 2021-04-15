---
description: Define los atributos de fuente.
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: D3DX10_FONT_DESC estructura (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FONT_DESC
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 0b358c57e6410827177e76e3da30b2f5f9896ee2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649401"
---
# <a name="d3dx10_font_desc-structure"></a><span data-ttu-id="6cc45-103">D3DX10 de la \_ \_ estructura DESC de la fuente</span><span class="sxs-lookup"><span data-stu-id="6cc45-103">D3DX10\_FONT\_DESC structure</span></span>

<span data-ttu-id="6cc45-104">Define los atributos de fuente.</span><span class="sxs-lookup"><span data-stu-id="6cc45-104">Defines font attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc45-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6cc45-105">Syntax</span></span>


```C++
typedef struct D3DX10_FONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName[LF_FACESIZE];
} D3DX10_FONT_DESC, *LPD3DX10_FONT_DESC;
```



## <a name="members"></a><span data-ttu-id="6cc45-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="6cc45-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6cc45-107">**Height**</span><span class="sxs-lookup"><span data-stu-id="6cc45-107">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="6cc45-108">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6cc45-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6cc45-109">Alto, en unidades lógicas, de la celda de caracteres o carácter de la fuente.</span><span class="sxs-lookup"><span data-stu-id="6cc45-109">Height, in logical units, of the font's character cell or character.</span></span>

</dd> <dt>

<span data-ttu-id="6cc45-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="6cc45-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="6cc45-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6cc45-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6cc45-112">Ancho, en unidades lógicas, de caracteres de la fuente.</span><span class="sxs-lookup"><span data-stu-id="6cc45-112">Width, in logical units, of characters in the font.</span></span>

</dd> <dt>

<span data-ttu-id="6cc45-113">**Peso**</span><span class="sxs-lookup"><span data-stu-id="6cc45-113">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="6cc45-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6cc45-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6cc45-115">Peso de la fuente en el intervalo comprendido entre 0 y 1000.</span><span class="sxs-lookup"><span data-stu-id="6cc45-115">Weight of the font in the range from 0 through 1000.</span></span>

</dd> <dt>

<span data-ttu-id="6cc45-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="6cc45-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="6cc45-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6cc45-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6cc45-118">Número de niveles de mipmap solicitados.</span><span class="sxs-lookup"><span data-stu-id="6cc45-118">Number of mipmap levels requested.</span></span> <span data-ttu-id="6cc45-119">Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="6cc45-119">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="6cc45-120">Si el valor es 1, el espacio de textura se asigna de forma idéntica al espacio de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="6cc45-120">If the value is 1, the texture space is mapped identically to the screen space.</span></span>

</dd> <dt>

<span data-ttu-id="6cc45-121">**Cursiva**</span><span class="sxs-lookup"><span data-stu-id="6cc45-121">**Italic**</span></span>
</dt> <dd>

<span data-ttu-id="6cc45-122">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6cc45-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6cc45-123">Establézcalo en **true** para una fuente en cursiva.</span><span class="sxs-lookup"><span data-stu-id="6cc45-123">Set to **TRUE** for an Italic font.</span></span>

</dd> <dt>

<span data-ttu-id="6cc45-124">**CharSet**</span><span class="sxs-lookup"><span data-stu-id="6cc45-124">**CharSet**</span></span>
</dt> <dd>

<span data-ttu-id="6cc45-125">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6cc45-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6cc45-126">Juego de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6cc45-126">Character set.</span></span>

</dd> <dt>

<span data-ttu-id="6cc45-127">**OutputPrecision**</span><span class="sxs-lookup"><span data-stu-id="6cc45-127">**OutputPrecision**</span></span>
</dt> <dd>

<span data-ttu-id="6cc45-128">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6cc45-128">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6cc45-129">Precisión de salida.</span><span class="sxs-lookup"><span data-stu-id="6cc45-129">Output precision.</span></span> <span data-ttu-id="6cc45-130">La precisión de salida define el grado en que la salida debe coincidir con el alto de fuente, el ancho, la orientación de carácter, el escape, el paso y el tipo de fuente solicitados.</span><span class="sxs-lookup"><span data-stu-id="6cc45-130">The output precision defines how closely the output must match the requested font height, width, character orientation, escapement, pitch, and font type.</span></span>

</dd> <dt>

<span data-ttu-id="6cc45-131">**Quality**</span><span class="sxs-lookup"><span data-stu-id="6cc45-131">**Quality**</span></span>
</dt> <dd>

<span data-ttu-id="6cc45-132">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6cc45-132">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6cc45-133">Calidad de salida.</span><span class="sxs-lookup"><span data-stu-id="6cc45-133">Output quality.</span></span>

</dd> <dt>

<span data-ttu-id="6cc45-134">**PitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="6cc45-134">**PitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="6cc45-135">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6cc45-135">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6cc45-136">El paso y la familia de la fuente.</span><span class="sxs-lookup"><span data-stu-id="6cc45-136">Pitch and family of the font.</span></span>

</dd> <dt>

<span data-ttu-id="6cc45-137">**FaceName \[ LF \_\]**</span><span class="sxs-lookup"><span data-stu-id="6cc45-137">**FaceName\[LF\_FACESIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="6cc45-138">Tipo: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="6cc45-138">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="6cc45-139">Una cadena terminada en NULL que especifica el nombre del tipo de letra de la fuente.</span><span class="sxs-lookup"><span data-stu-id="6cc45-139">A NULL-terminated string that specifies the typeface name of the font.</span></span> <span data-ttu-id="6cc45-140">La longitud de la cadena no debe superar los 32 caracteres, incluido el carácter **nulo** de terminación.</span><span class="sxs-lookup"><span data-stu-id="6cc45-140">The length of the string must not exceed 32 characters, including the terminating **NULL** character.</span></span> <span data-ttu-id="6cc45-141">Si FaceName es una cadena vacía, se utilizará la primera fuente que coincida con los demás atributos especificados.</span><span class="sxs-lookup"><span data-stu-id="6cc45-141">If FaceName is an empty string, the first font that matches the other specified attributes will be used.</span></span> <span data-ttu-id="6cc45-142">Si la configuración del compilador requiere Unicode, el tipo de datos TCHAR se resuelve como WCHAR; de lo contrario, el tipo de datos se resuelve como CHAR.</span><span class="sxs-lookup"><span data-stu-id="6cc45-142">If the compiler settings require Unicode, the data type TCHAR resolves to WCHAR; otherwise, the data type resolves to CHAR.</span></span> <span data-ttu-id="6cc45-143">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="6cc45-143">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6cc45-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6cc45-144">Remarks</span></span>

<span data-ttu-id="6cc45-145">La configuración del compilador también determina el tipo de estructura.</span><span class="sxs-lookup"><span data-stu-id="6cc45-145">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="6cc45-146">Si se define Unicode, el \_ tipo de estructura D3DX10 Font desc se \_ resuelve como una \_ fuente D3DX10 \_ DESCW; de lo contrario, el tipo de estructura se resuelve como una \_ fuente D3DX10 \_ Desca.</span><span class="sxs-lookup"><span data-stu-id="6cc45-146">If Unicode is defined, the D3DX10\_FONT\_DESC structure type resolves to a D3DX10\_FONT\_DESCW; otherwise the structure type resolves to a D3DX10\_FONT\_DESCA.</span></span>

<span data-ttu-id="6cc45-147">Los valores posibles de los miembros anteriores se proporcionan en la estructura de [LOGFONT](/previous-versions//ms533931(v=vs.85)) de GDI.</span><span class="sxs-lookup"><span data-stu-id="6cc45-147">Possible values of the above members are given in the GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cc45-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cc45-148">Requirements</span></span>



| <span data-ttu-id="6cc45-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cc45-149">Requirement</span></span> | <span data-ttu-id="6cc45-150">Value</span><span class="sxs-lookup"><span data-stu-id="6cc45-150">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc45-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6cc45-151">Header</span></span><br/> | <dl> <span data-ttu-id="6cc45-152"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cc45-152"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cc45-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="6cc45-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc45-154">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="6cc45-154">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
