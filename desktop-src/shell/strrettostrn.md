---
description: 'Toma una estructura STRRET devuelta por IShellFolder:: GetDisplayNameOf, la convierte en una cadena y coloca el resultado en un búfer.'
title: StrRetToStrN función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrRetToStrN
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: a816fb5f-8320-4b63-a85d-dd4c59596ead
ms.openlocfilehash: 89a8d991e22e8615456bd8d4690c046ec0d325d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997953"
---
# <a name="strrettostrn-function"></a><span data-ttu-id="35ef6-103">StrRetToStrN función)</span><span class="sxs-lookup"><span data-stu-id="35ef6-103">StrRetToStrN function</span></span>

<span data-ttu-id="35ef6-104">Toma una estructura [**Strret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) devuelta por [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), la convierte en una cadena y coloca el resultado en un búfer.</span><span class="sxs-lookup"><span data-stu-id="35ef6-104">Takes an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure returned by [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), converts it to a string, and places the result in a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ef6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35ef6-105">Syntax</span></span>


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a><span data-ttu-id="35ef6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35ef6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ef6-107">*pszOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="35ef6-107">*pszOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35ef6-108">Tipo: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="35ef6-108">Type: **LPTSTR**</span></span>

<span data-ttu-id="35ef6-109">Búfer que va a contener el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="35ef6-109">Buffer to hold the display name.</span></span> <span data-ttu-id="35ef6-110">Se devolverá como una cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="35ef6-110">It will be returned as a null-terminated string.</span></span> <span data-ttu-id="35ef6-111">Si *cchOut* es demasiado pequeño, el nombre se truncará para ajustarse.</span><span class="sxs-lookup"><span data-stu-id="35ef6-111">If *cchOut* is too small, the name will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="35ef6-112">*cchOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35ef6-112">*cchOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ef6-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="35ef6-113">Type: **UINT**</span></span>

<span data-ttu-id="35ef6-114">Tamaño de *pszOut*, en caracteres.</span><span class="sxs-lookup"><span data-stu-id="35ef6-114">Size of *pszOut*, in characters.</span></span> <span data-ttu-id="35ef6-115">Si *cchOut* es demasiado pequeño, la cadena se truncará para ajustarse.</span><span class="sxs-lookup"><span data-stu-id="35ef6-115">If *cchOut* is too small, the string will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="35ef6-116">*pStrRet* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="35ef6-116">*pStrRet* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="35ef6-117">Tipo: **LPSTRRET**</span><span class="sxs-lookup"><span data-stu-id="35ef6-117">Type: **LPSTRRET**</span></span>

<span data-ttu-id="35ef6-118">Puntero a una estructura [**Strret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) .</span><span class="sxs-lookup"><span data-stu-id="35ef6-118">Pointer to an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure.</span></span> <span data-ttu-id="35ef6-119">Cuando la función devuelve, este puntero ya no será válido.</span><span class="sxs-lookup"><span data-stu-id="35ef6-119">When the function returns, this pointer will no longer be valid.</span></span>

</dd> <dt>

<span data-ttu-id="35ef6-120">*PIDL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35ef6-120">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ef6-121">Tipo: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="35ef6-121">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="35ef6-122">Puntero a la estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) del elemento.</span><span class="sxs-lookup"><span data-stu-id="35ef6-122">Pointer to the item's [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35ef6-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35ef6-123">Return value</span></span>

<span data-ttu-id="35ef6-124">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="35ef6-124">Type: **BOOL**</span></span>

<span data-ttu-id="35ef6-125">**True si es** correcto, **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="35ef6-125">**TRUE** for success, **FALSE** for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="35ef6-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35ef6-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="35ef6-127">A partir de Shell32.dll versión 5,0, llamar a esta función es equivalente a llamar a [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span><span class="sxs-lookup"><span data-stu-id="35ef6-127">As of Shell32.dll version 5.0, calling this function is equivalent to calling [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span></span>

 

<span data-ttu-id="35ef6-128">**StrRetToStrN** no se exporta por nombre.</span><span class="sxs-lookup"><span data-stu-id="35ef6-128">**StrRetToStrN** is not exported by name.</span></span> <span data-ttu-id="35ef6-129">Para usarlo, debe utilizar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) y el ordinal de solicitud 96 de Shell32.dll para obtener un puntero de función.</span><span class="sxs-lookup"><span data-stu-id="35ef6-129">To use it, you must use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 96 from Shell32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="35ef6-130">Si el miembro **uType** de la estructura a la que apunta *pStrRet* se establece en **Strret \_ WSTR**, el miembro **pOleStr** de esa estructura se liberará en la devolución.</span><span class="sxs-lookup"><span data-stu-id="35ef6-130">If the **uType** member of the structure pointed to by *pStrRet* is set to **STRRET\_WSTR**, the **pOleStr** member of that structure will be freed on return.</span></span>

<span data-ttu-id="35ef6-131">Tenga en cuenta que esta función se exporta desde Shell32.dll en lugar de Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="35ef6-131">Note that this function is exported from Shell32.dll rather than Shlwapi.dll.</span></span> <span data-ttu-id="35ef6-132">También se incluye en ShlObj. h en lugar de en shlwapi. h.</span><span class="sxs-lookup"><span data-stu-id="35ef6-132">It is also included in Shlobj.h rather than Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ef6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35ef6-133">Requirements</span></span>



| <span data-ttu-id="35ef6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="35ef6-134">Requirement</span></span> | <span data-ttu-id="35ef6-135">Value</span><span class="sxs-lookup"><span data-stu-id="35ef6-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ef6-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35ef6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="35ef6-137">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="35ef6-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="35ef6-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35ef6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="35ef6-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="35ef6-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="35ef6-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35ef6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35ef6-141"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="35ef6-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ef6-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="35ef6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ef6-143">**StrRetToStr**</span><span class="sxs-lookup"><span data-stu-id="35ef6-143">**StrRetToStr**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[<span data-ttu-id="35ef6-144">**StrRetToBuf**</span><span class="sxs-lookup"><span data-stu-id="35ef6-144">**StrRetToBuf**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
