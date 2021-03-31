---
title: Str_GetPtr función)
description: Copia una cadena de un búfer a otro.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Str_GetPtr controles de función de Windows
topic_type:
- apiref
api_name:
- Str_GetPtr
- Str_GetPtrA
- Str_GetPtrW
api_location:
- ComCtl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec99bb4d91bde86d901c0e7ed4761bafd15f3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801532"
---
# <a name="str_getptr-function"></a><span data-ttu-id="d7703-104">Str \_ GetPtr función)</span><span class="sxs-lookup"><span data-stu-id="d7703-104">Str\_GetPtr function</span></span>

<span data-ttu-id="d7703-105">\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d7703-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="d7703-106">Podría modificarse o no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d7703-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="d7703-107">Copia una cadena de un búfer a otro.</span><span class="sxs-lookup"><span data-stu-id="d7703-107">Copies a string from one buffer to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7703-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7703-108">Syntax</span></span>


```C++
int WINAPI Str_GetPtr(
  _In_    LPCTSTR pszSource,
  _Inout_ LPCSTR  pszDest,
  _In_    int     cchDest
);
```



## <a name="parameters"></a><span data-ttu-id="d7703-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7703-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7703-110">*pszSource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7703-110">*pszSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7703-111">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d7703-111">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d7703-112">Puntero a una cadena de origen.</span><span class="sxs-lookup"><span data-stu-id="d7703-112">A pointer to a source string.</span></span>

</dd> <dt>

<span data-ttu-id="d7703-113">*pszDest* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d7703-113">*pszDest* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7703-114">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d7703-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d7703-115">Puntero al búfer de destino.</span><span class="sxs-lookup"><span data-stu-id="d7703-115">A pointer to the destination buffer.</span></span> <span data-ttu-id="d7703-116">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="d7703-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d7703-117">*cchDest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7703-117">*cchDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7703-118">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="d7703-118">Type: **int**</span></span>

<span data-ttu-id="d7703-119">Tamaño de *pszDest*, en caracteres.</span><span class="sxs-lookup"><span data-stu-id="d7703-119">The size of *pszDest*, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7703-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7703-120">Return value</span></span>

<span data-ttu-id="d7703-121">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="d7703-121">Type: **int**</span></span>

<span data-ttu-id="d7703-122">Si *pszDest* es **null** o *cchDest* es cero, devuelve el tamaño del búfer, en caracteres, necesario para contener una copia terminada en NULL de la cadena a la que apunta *pszSource*.</span><span class="sxs-lookup"><span data-stu-id="d7703-122">If *pszDest* is **NULL** or *cchDest* is zero, returns the size of the buffer, in characters, needed to contain a null-terminated copy of the string pointed to by *pszSource*.</span></span>

<span data-ttu-id="d7703-123">Si *pszDest* no es **null**, devuelve el número de caracteres copiados correctamente, incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="d7703-123">If *pszDest* is non-**NULL**, returns the number of characters successfully copied, including the terminating null character.</span></span>

<span data-ttu-id="d7703-124">Si *pszDest* no puede contener la cadena completa a la que apunta *pszSource*, se copian los caracteres (*cchDest*-1), la cadena termina en NULL y se devuelve *cchDest* .</span><span class="sxs-lookup"><span data-stu-id="d7703-124">If *pszDest* cannot hold the entire string pointed to by *pszSource*, then (*cchDest*-1) characters are copied, the string null-terminated, and *cchDest* returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7703-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7703-125">Remarks</span></span>

<span data-ttu-id="d7703-126">**Str \_ GetPtr** está disponible como versiones ANSI (**Str \_ GetPtrA**) y Unicode (**Str \_ GetPtrW**).</span><span class="sxs-lookup"><span data-stu-id="d7703-126">**Str\_GetPtr** is available as ANSI (**Str\_GetPtrA**) and Unicode (**Str\_GetPtrW**) versions.</span></span> <span data-ttu-id="d7703-127">Estas funciones no se exportan por nombre o se declaran en un archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="d7703-127">These functions are not exported by name or declared in a public header file.</span></span> <span data-ttu-id="d7703-128">Para usarlos, debe utilizar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y el ordinal de solicitud 233 (**Str \_ GetPtrA**) o 235 (**Str \_ GetPtrW**) de ComCtl32.dll para obtener un puntero de función.</span><span class="sxs-lookup"><span data-stu-id="d7703-128">To use them, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 233 (**Str\_GetPtrA**) or 235 (**Str\_GetPtrW**) from ComCtl32.dll to obtain a function pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7703-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7703-129">Requirements</span></span>



| <span data-ttu-id="d7703-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7703-130">Requirement</span></span> | <span data-ttu-id="d7703-131">Value</span><span class="sxs-lookup"><span data-stu-id="d7703-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7703-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7703-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d7703-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d7703-133">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d7703-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7703-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d7703-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7703-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7703-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7703-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7703-137"><dt>ComCtl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7703-137"><dt>ComCtl32.dll</dt></span></span> </dl> |
| <span data-ttu-id="d7703-138">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="d7703-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d7703-139">**Str \_ GetPtrW** (Unicode) y **Str \_ GetPtrA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d7703-139">**Str\_GetPtrW** (Unicode) and **Str\_GetPtrA** (ANSI)</span></span><br/>                       |



 

