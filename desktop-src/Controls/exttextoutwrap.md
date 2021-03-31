---
title: ExtTextOutWrap función)
description: Dibuja texto con la fuente, el color de fondo y el color de texto seleccionados actualmente. Opcionalmente, puede proporcionar dimensiones que se usarán para el recorte, la opacidad o ambos. Esta función contiene una llamada a ExtTextOut.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- ExtTextOutWrap (función) controles de Windows
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a173fedb7d8534dbd926a8a147e833435a7710b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149942"
---
# <a name="exttextoutwrap-function"></a><span data-ttu-id="481d5-106">ExtTextOutWrap función)</span><span class="sxs-lookup"><span data-stu-id="481d5-106">ExtTextOutWrap function</span></span>

<span data-ttu-id="481d5-107">\[**ExtTextOutWrap** está disponible a través de Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="481d5-107">\[**ExtTextOutWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="481d5-108">Podría modificarse o no estar disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="481d5-108">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="481d5-109">Se recomienda usar [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) directamente en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="481d5-109">It is recommended to use [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) directly instead.\]</span></span>

<span data-ttu-id="481d5-110">Dibuja texto con la fuente, el color de fondo y el color de texto seleccionados actualmente.</span><span class="sxs-lookup"><span data-stu-id="481d5-110">Draws text using the currently selected font, background color, and text color.</span></span> <span data-ttu-id="481d5-111">Opcionalmente, puede proporcionar dimensiones que se usarán para el recorte, la opacidad o ambos.</span><span class="sxs-lookup"><span data-stu-id="481d5-111">You can optionally provide dimensions to be used for clipping, opacity, or both.</span></span> <span data-ttu-id="481d5-112">Esta función contiene una llamada a [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span><span class="sxs-lookup"><span data-stu-id="481d5-112">This function wraps a call to [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span></span>

## <a name="syntax"></a><span data-ttu-id="481d5-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="481d5-113">Syntax</span></span>


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a><span data-ttu-id="481d5-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="481d5-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="481d5-115">*HDC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="481d5-115">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="481d5-116">Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="481d5-116">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="481d5-117">Identificador del contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="481d5-117">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="481d5-118">*X* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="481d5-118">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="481d5-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="481d5-119">Type: **int**</span></span>

<span data-ttu-id="481d5-120">La coordenada x, en coordenadas lógicas, del punto de referencia utilizado para colocar la cadena.</span><span class="sxs-lookup"><span data-stu-id="481d5-120">The x-coordinate, in logical coordinates, of the reference point used to position the string.</span></span>

</dd> <dt>

<span data-ttu-id="481d5-121">*Y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="481d5-121">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="481d5-122">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="481d5-122">Type: **int**</span></span>

<span data-ttu-id="481d5-123">La coordenada y, en coordenadas lógicas, del punto de referencia utilizado para colocar la cadena.</span><span class="sxs-lookup"><span data-stu-id="481d5-123">The y-coordinate, in logical coordinates, of the reference point used to position the string.</span></span>

</dd> <dt>

<span data-ttu-id="481d5-124">*uOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="481d5-124">*uOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="481d5-125">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="481d5-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="481d5-126">Valores que especifican cómo usar el rectángulo definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="481d5-126">Values that specify how to use the application-defined rectangle.</span></span> <span data-ttu-id="481d5-127">Consulte [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) para obtener una lista completa de opciones.</span><span class="sxs-lookup"><span data-stu-id="481d5-127">See [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="481d5-128">*LPRC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="481d5-128">*lprc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="481d5-129">Tipo: \**const [**Rect**](/previous-versions//dd162897(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="481d5-129">Type: \**const [**RECT**](/previous-versions//dd162897(v=vs.85))\** _</span></span>

<span data-ttu-id="481d5-130">Puntero a una estructura [_ *Rect* \*](/previous-versions//dd162897(v=vs.85)) opcional que especifica las dimensiones, en coordenadas lógicas, de un rectángulo que se usa para el recorte, la opacidad o ambos.</span><span class="sxs-lookup"><span data-stu-id="481d5-130">A pointer to an optional [_ *RECT*\*](/previous-versions//dd162897(v=vs.85)) structure that specifies the dimensions, in logical coordinates, of a rectangle that is used for clipping, opacity, or both.</span></span>

</dd> <dt>

<span data-ttu-id="481d5-131">*lpString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="481d5-131">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="481d5-132">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="481d5-132">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="481d5-133">Puntero a un búfer que contiene el texto que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="481d5-133">A pointer to a buffer that contains the text to be drawn.</span></span> <span data-ttu-id="481d5-134">No es necesario que la cadena termine en cero, ya que *cbCount* especifica la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="481d5-134">The string does not need to be zero-terminated, since *cbCount* specifies the length of the string.</span></span>

</dd> <dt>

<span data-ttu-id="481d5-135">*cbCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="481d5-135">*cbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="481d5-136">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="481d5-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="481d5-137">Longitud de la cadena, en bytes, a la que apunta *lpString*.</span><span class="sxs-lookup"><span data-stu-id="481d5-137">The length of the string, in bytes, pointed to by *lpString*.</span></span>

</dd> <dt>

<span data-ttu-id="481d5-138">*lpDx* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="481d5-138">*lpDx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="481d5-139">Tipo: \**const [**int**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="481d5-139">Type: \**const [**INT**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="481d5-140">Puntero a una matriz opcional de valores que indican la distancia entre los orígenes de las celdas de caracteres adyacentes.</span><span class="sxs-lookup"><span data-stu-id="481d5-140">A pointer to an optional array of values that indicate the distance between origins of adjacent character cells.</span></span> <span data-ttu-id="481d5-141">Por ejemplo, _lpDx \[ unidades lógicas \* x separan \] los orígenes de la celda de carácter x y la celda de carácter (x + 1).</span><span class="sxs-lookup"><span data-stu-id="481d5-141">For example, _lpDx\*\[x\] logical units separate the origins of character cell x and character cell (x + 1).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="481d5-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="481d5-142">Return value</span></span>

<span data-ttu-id="481d5-143">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="481d5-143">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="481d5-144">Devuelve un valor distinto de cero si la cadena se dibuja correctamente.</span><span class="sxs-lookup"><span data-stu-id="481d5-144">Returns a nonzero value if the string is drawn successfully.</span></span> <span data-ttu-id="481d5-145">Sin embargo, si se llama a la versión ANSI de [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) con el índice del GLIFO de ETO \_ \_ , la función devuelve **true** aunque la función no hace nada.</span><span class="sxs-lookup"><span data-stu-id="481d5-145">However, if the ANSI version of [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) is called with ETO\_GLYPH\_INDEX, the function returns **TRUE** even though the function does nothing.</span></span>

<span data-ttu-id="481d5-146">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="481d5-146">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="481d5-147">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="481d5-147">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="481d5-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="481d5-148">Remarks</span></span>

<span data-ttu-id="481d5-149">**ExtTextOutWrap** no se exporta por nombre o se declara en un archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="481d5-149">**ExtTextOutWrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="481d5-150">Para usarlo, debe utilizar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y el ordinal de solicitud 417 de ComCtl32.dll para obtener un puntero de función.</span><span class="sxs-lookup"><span data-stu-id="481d5-150">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 417 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="481d5-151">Para obtener más comentarios, vea [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span><span class="sxs-lookup"><span data-stu-id="481d5-151">For additional remarks, please see [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span></span>

## <a name="requirements"></a><span data-ttu-id="481d5-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="481d5-152">Requirements</span></span>



| <span data-ttu-id="481d5-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="481d5-153">Requirement</span></span> | <span data-ttu-id="481d5-154">Value</span><span class="sxs-lookup"><span data-stu-id="481d5-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="481d5-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="481d5-155">Minimum supported client</span></span><br/> | <span data-ttu-id="481d5-156">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="481d5-156">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="481d5-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="481d5-157">Minimum supported server</span></span><br/> | <span data-ttu-id="481d5-158">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="481d5-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="481d5-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="481d5-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="481d5-160"><dt>Comctl32.dll (versión 6,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="481d5-160"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

