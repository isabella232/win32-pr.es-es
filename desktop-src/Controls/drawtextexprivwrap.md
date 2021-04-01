---
title: DrawTextExPrivWrap función)
description: Dibuja texto con formato en el rectángulo especificado. Esta función contiene una llamada a DrawTextEx.
ms.assetid: 3212282c-1adb-4f7e-b4d7-7d833b26ac60
keywords:
- DrawTextExPrivWrap (función) controles de Windows
topic_type:
- apiref
api_name:
- DrawTextExPrivWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba496a121af3ba88ed24ab6c9c7834c90153ec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997113"
---
# <a name="drawtextexprivwrap-function"></a><span data-ttu-id="0561d-105">DrawTextExPrivWrap función)</span><span class="sxs-lookup"><span data-stu-id="0561d-105">DrawTextExPrivWrap function</span></span>

<span data-ttu-id="0561d-106">\[**DrawTextExPrivWrap** está disponible a través de Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="0561d-106">\[**DrawTextExPrivWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="0561d-107">Podría modificarse o no estar disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0561d-107">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0561d-108">Se recomienda usar [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) directamente en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="0561d-108">It is recommended to use [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) directly instead.\]</span></span>

<span data-ttu-id="0561d-109">Dibuja texto con formato en el rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="0561d-109">Draws formatted text in the specified rectangle.</span></span> <span data-ttu-id="0561d-110">Esta función contiene una llamada a [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span><span class="sxs-lookup"><span data-stu-id="0561d-110">This function wraps a call to [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="0561d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0561d-111">Syntax</span></span>


```C++
int WINAPI DrawTextExPrivWrap(
  _In_    HDC              hdc,
  _Inout_ LPTSTR           lpchText,
  _In_    int              cchText,
  _Inout_ LPRECT           lprc,
  _In_    UINT             dwDTFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a><span data-ttu-id="0561d-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0561d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0561d-113">*HDC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0561d-113">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0561d-114">Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0561d-114">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0561d-115">Identificador del contexto de dispositivo en el que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="0561d-115">A handle to the device context in which to draw.</span></span>

</dd> <dt>

<span data-ttu-id="0561d-116">*lpchText* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0561d-116">*lpchText* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0561d-117">Tipo: **[ **LPTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0561d-117">Type: **[**LPTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0561d-118">Un puntero a un búfer que contiene el texto que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="0561d-118">A pointer to a buffer that contains the text to draw.</span></span> <span data-ttu-id="0561d-119">Si el parámetro *cchText* es-1, la cadena debe terminar en NULL.</span><span class="sxs-lookup"><span data-stu-id="0561d-119">If the *cchText* parameter is -1, the string must be null-terminated.</span></span>

<span data-ttu-id="0561d-120">Si *dwDTFormat* incluye DT \_ MODIFYSTRING, la función podría agregar hasta cuatro caracteres adicionales a esta cadena.</span><span class="sxs-lookup"><span data-stu-id="0561d-120">If *dwDTFormat* includes DT\_MODIFYSTRING, the function might add up to four additional characters to this string.</span></span> <span data-ttu-id="0561d-121">El búfer que contiene la cadena debe ser lo suficientemente grande como para dar cabida a estos caracteres adicionales.</span><span class="sxs-lookup"><span data-stu-id="0561d-121">The buffer that contains the string should be large enough to accommodate these extra characters.</span></span>

</dd> <dt>

<span data-ttu-id="0561d-122">*cchText* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0561d-122">*cchText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0561d-123">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="0561d-123">Type: **int**</span></span>

<span data-ttu-id="0561d-124">La longitud de la cadena a la que apunta *lpchText*.</span><span class="sxs-lookup"><span data-stu-id="0561d-124">The length of the string pointed to by *lpchText*.</span></span> <span data-ttu-id="0561d-125">Si *cchText* es-1, se supone que el parámetro *lpchText* es un puntero a una cadena terminada en NULL y [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) calcula el recuento de caracteres automáticamente.</span><span class="sxs-lookup"><span data-stu-id="0561d-125">If *cchText* is -1, then the *lpchText* parameter is assumed to be a pointer to a null-terminated string and [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="0561d-126">*LPRC* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0561d-126">*lprc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0561d-127">Tipo: **LPRECT**</span><span class="sxs-lookup"><span data-stu-id="0561d-127">Type: **LPRECT**</span></span>

<span data-ttu-id="0561d-128">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene el rectángulo, en coordenadas lógicas, en la que se va a dar formato al texto.</span><span class="sxs-lookup"><span data-stu-id="0561d-128">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span>

</dd> <dt>

<span data-ttu-id="0561d-129">*dwDTFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0561d-129">*dwDTFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0561d-130">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0561d-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0561d-131">Opciones de formato.</span><span class="sxs-lookup"><span data-stu-id="0561d-131">The formatting options.</span></span> <span data-ttu-id="0561d-132">Consulte la documentación de [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) para obtener una lista completa de opciones.</span><span class="sxs-lookup"><span data-stu-id="0561d-132">See the documentation for [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="0561d-133">*lpDTParams* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0561d-133">*lpDTParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0561d-134">Tipo: **LPDRAWTEXTPARAMS**</span><span class="sxs-lookup"><span data-stu-id="0561d-134">Type: **LPDRAWTEXTPARAMS**</span></span>

<span data-ttu-id="0561d-135">Puntero a una estructura [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) que especifica opciones de formato adicionales.</span><span class="sxs-lookup"><span data-stu-id="0561d-135">A pointer to a [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) structure that specifies additional formatting options.</span></span> <span data-ttu-id="0561d-136">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0561d-136">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0561d-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0561d-137">Return value</span></span>

<span data-ttu-id="0561d-138">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="0561d-138">Type: **int**</span></span>

<span data-ttu-id="0561d-139">Si la función se ejecuta correctamente, el valor devuelto es el alto de texto en unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="0561d-139">If the function succeeds, the return value is the text height in logical units.</span></span> <span data-ttu-id="0561d-140">Si se especifica **DT \_ vCenter** o **DT \_ Bottom** , el valor devuelto es el desplazamiento desde el miembro **superior** de *LPRC* hasta la parte inferior del texto dibujado.</span><span class="sxs-lookup"><span data-stu-id="0561d-140">If **DT\_VCENTER** or **DT\_BOTTOM** is specified, the return value is the offset from the **top** member of *lprc* to the bottom of the drawn text.</span></span>

<span data-ttu-id="0561d-141">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="0561d-141">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="0561d-142">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="0561d-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="0561d-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0561d-143">Remarks</span></span>

<span data-ttu-id="0561d-144">**DrawTextExPrivWrap** no se exporta por nombre o se declara en un archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="0561d-144">**DrawTextExPrivWrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="0561d-145">Para usarlo, debe utilizar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y el ordinal de solicitud 416 de ComCtl32.dll para obtener un puntero de función.</span><span class="sxs-lookup"><span data-stu-id="0561d-145">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 416 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="0561d-146">Para obtener más comentarios, vea [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span><span class="sxs-lookup"><span data-stu-id="0561d-146">For additional remarks, please see [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="0561d-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0561d-147">Requirements</span></span>



| <span data-ttu-id="0561d-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="0561d-148">Requirement</span></span> | <span data-ttu-id="0561d-149">Value</span><span class="sxs-lookup"><span data-stu-id="0561d-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0561d-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0561d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="0561d-151">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0561d-151">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="0561d-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0561d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="0561d-153">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0561d-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0561d-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0561d-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0561d-155"><dt>Comctl32.dll (versión 6,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="0561d-155"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

