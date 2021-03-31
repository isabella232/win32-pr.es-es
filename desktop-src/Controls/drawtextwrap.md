---
title: DrawTextWrap función)
description: Dibuja texto con formato en el rectángulo especificado. Da formato al texto según el método especificado (expandir pestañas, justificar caracteres, líneas de división, etc.). Esta función contiene una llamada a DrawText.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- DrawTextWrap (función) controles de Windows
topic_type:
- apiref
api_name:
- DrawTextWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfc5eb707b4016a592ad339223e0f32ab21d4a29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995983"
---
# <a name="drawtextwrap-function"></a><span data-ttu-id="efcb3-106">DrawTextWrap función)</span><span class="sxs-lookup"><span data-stu-id="efcb3-106">DrawTextWrap function</span></span>

<span data-ttu-id="efcb3-107">\[**DrawTextWrap** está disponible a través de Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="efcb3-107">\[**DrawTextWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="efcb3-108">Podría modificarse o no estar disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="efcb3-108">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="efcb3-109">En su lugar, se recomienda usar [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) directamente.\]</span><span class="sxs-lookup"><span data-stu-id="efcb3-109">It is recommended to use [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) directly instead.\]</span></span>

<span data-ttu-id="efcb3-110">Dibuja texto con formato en el rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="efcb3-110">Draws formatted text in the specified rectangle.</span></span> <span data-ttu-id="efcb3-111">Da formato al texto según el método especificado (expandir pestañas, justificar caracteres, líneas de división, etc.).</span><span class="sxs-lookup"><span data-stu-id="efcb3-111">It formats the text according to the specified method (expanding tabs, justifying characters, breaking lines, and so on).</span></span> <span data-ttu-id="efcb3-112">Esta función contiene una llamada a [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="efcb3-112">This function wraps a call to [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span></span>

## <a name="syntax"></a><span data-ttu-id="efcb3-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efcb3-113">Syntax</span></span>


```C++
int WINAPI DrawTextWrap(
  _In_    HDC              hdc,
  _Inout_ LPCTSTR          lpString,
  _In_    int              nCount,
  _Inout_ LPRECT           lpRect,
  _In_    UINT             uFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a><span data-ttu-id="efcb3-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efcb3-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efcb3-115">*HDC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="efcb3-115">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efcb3-116">Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="efcb3-116">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="efcb3-117">Identificador del contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efcb3-117">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="efcb3-118">*lpString* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="efcb3-118">*lpString* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="efcb3-119">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="efcb3-119">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="efcb3-120">Un puntero a un búfer que contiene el texto que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="efcb3-120">A pointer to a buffer that contains the text to draw.</span></span> <span data-ttu-id="efcb3-121">Si el parámetro *nCount* es-1, la cadena debe terminar en NULL.</span><span class="sxs-lookup"><span data-stu-id="efcb3-121">If the *nCount* parameter is -1, the string must be null-terminated.</span></span>

<span data-ttu-id="efcb3-122">Si *uFormat* incluye DT \_ MODIFYSTRING, la función podría agregar hasta cuatro caracteres adicionales a esta cadena.</span><span class="sxs-lookup"><span data-stu-id="efcb3-122">If *uFormat* includes DT\_MODIFYSTRING, the function might add up to four additional characters to this string.</span></span> <span data-ttu-id="efcb3-123">El búfer que contiene la cadena debe ser lo suficientemente grande como para dar cabida a estos caracteres adicionales.</span><span class="sxs-lookup"><span data-stu-id="efcb3-123">The buffer that contains the string should be large enough to accommodate these extra characters.</span></span>

</dd> <dt>

<span data-ttu-id="efcb3-124">*nCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="efcb3-124">*nCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efcb3-125">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="efcb3-125">Type: **int**</span></span>

<span data-ttu-id="efcb3-126">La longitud de la cadena a la que apunta *lpString*.</span><span class="sxs-lookup"><span data-stu-id="efcb3-126">The length of the string pointed to by *lpString*.</span></span> <span data-ttu-id="efcb3-127">Si *nCount* es-1, se supone que el parámetro *lpString* es un puntero a una cadena terminada en NULL y [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) calcula el recuento de caracteres automáticamente.</span><span class="sxs-lookup"><span data-stu-id="efcb3-127">If *nCount* is -1, then the *lpString* parameter is assumed to be a pointer to a null-terminated string and [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="efcb3-128">*lpRect* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="efcb3-128">*lpRect* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="efcb3-129">Tipo: **LPRECT**</span><span class="sxs-lookup"><span data-stu-id="efcb3-129">Type: **LPRECT**</span></span>

<span data-ttu-id="efcb3-130">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene el rectángulo, en coordenadas lógicas, en la que se va a dar formato al texto.</span><span class="sxs-lookup"><span data-stu-id="efcb3-130">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span>

</dd> <dt>

<span data-ttu-id="efcb3-131">*uFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="efcb3-131">*uFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efcb3-132">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="efcb3-132">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="efcb3-133">Opciones de formato.</span><span class="sxs-lookup"><span data-stu-id="efcb3-133">The formatting options.</span></span> <span data-ttu-id="efcb3-134">Consulte la documentación de [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) para obtener una lista completa de opciones.</span><span class="sxs-lookup"><span data-stu-id="efcb3-134">See the documentation for [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="efcb3-135">*lpDTParams* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="efcb3-135">*lpDTParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efcb3-136">Tipo: **LPDRAWTEXTPARAMS**</span><span class="sxs-lookup"><span data-stu-id="efcb3-136">Type: **LPDRAWTEXTPARAMS**</span></span>

<span data-ttu-id="efcb3-137">Puntero a una estructura [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) que especifica opciones de formato adicionales.</span><span class="sxs-lookup"><span data-stu-id="efcb3-137">A pointer to a [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) structure that specifies additional formatting options.</span></span> <span data-ttu-id="efcb3-138">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="efcb3-138">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efcb3-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efcb3-139">Return value</span></span>

<span data-ttu-id="efcb3-140">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="efcb3-140">Type: **int**</span></span>

<span data-ttu-id="efcb3-141">Si la función se ejecuta correctamente, el valor devuelto es el alto de texto en unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="efcb3-141">If the function succeeds, the return value is the text height in logical units.</span></span> <span data-ttu-id="efcb3-142">Si se especifica **DT \_ vCenter** o **DT \_ Bottom** , el valor devuelto es el desplazamiento desde el miembro **superior** de *LPRC* hasta la parte inferior del texto dibujado si se produce un error en la función, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="efcb3-142">If **DT\_VCENTER** or **DT\_BOTTOM** is specified, the return value is the offset from the **top** member of *lprc* to the bottom of the drawn text If the function fails, the return value is zero.</span></span>

<span data-ttu-id="efcb3-143">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="efcb3-143">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="efcb3-144">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="efcb3-144">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="efcb3-145">Comentarios</span><span class="sxs-lookup"><span data-stu-id="efcb3-145">Remarks</span></span>

<span data-ttu-id="efcb3-146">**DrawTextWrap** no se exporta por nombre o se declara en un encabezado público.</span><span class="sxs-lookup"><span data-stu-id="efcb3-146">**DrawTextWrap** is not exported by name or declared in a public header.</span></span> <span data-ttu-id="efcb3-147">Para usarlo, debe utilizar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y el ordinal de solicitud 415 de ComCtl32.dll para obtener un puntero de función.</span><span class="sxs-lookup"><span data-stu-id="efcb3-147">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 415 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="efcb3-148">Para obtener más comentarios, consulte [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="efcb3-148">For additional remarks, please see [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span></span>

## <a name="requirements"></a><span data-ttu-id="efcb3-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efcb3-149">Requirements</span></span>



| <span data-ttu-id="efcb3-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="efcb3-150">Requirement</span></span> | <span data-ttu-id="efcb3-151">Value</span><span class="sxs-lookup"><span data-stu-id="efcb3-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efcb3-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efcb3-152">Minimum supported client</span></span><br/> | <span data-ttu-id="efcb3-153">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="efcb3-153">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="efcb3-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efcb3-154">Minimum supported server</span></span><br/> | <span data-ttu-id="efcb3-155">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="efcb3-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="efcb3-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="efcb3-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efcb3-157"><dt>Comctl32.dll (versión 6,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="efcb3-157"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

