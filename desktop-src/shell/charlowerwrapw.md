---
description: Convierte una cadena de caracteres Unicode o un carácter individual en minúsculas.
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: CharLowerWrapW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharLowerWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 3911e0366d30f3eb9420391f9d06867ded73530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540558"
---
# <a name="charlowerwrapw-function"></a><span data-ttu-id="39571-103">CharLowerWrapW función)</span><span class="sxs-lookup"><span data-stu-id="39571-103">CharLowerWrapW function</span></span>

<span data-ttu-id="39571-104">\[**CharLowerWrapW** está disponible para su uso en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="39571-104">\[**CharLowerWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="39571-105">Puede que no esté disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="39571-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="39571-106">Debe usar [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="39571-106">You should use [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in its place.\]</span></span>

<span data-ttu-id="39571-107">Convierte una cadena de caracteres Unicode o un carácter individual en minúsculas.</span><span class="sxs-lookup"><span data-stu-id="39571-107">Converts a Unicode character string or a single character to lowercase.</span></span> <span data-ttu-id="39571-108">Si el operando es una cadena de caracteres, la función convierte los caracteres en su lugar.</span><span class="sxs-lookup"><span data-stu-id="39571-108">If the operand is a character string, the function converts the characters in place.</span></span>

> [!Note]  
> <span data-ttu-id="39571-109">**CharLowerWrapW** es un contenedor para la función **CharLowerW** .</span><span class="sxs-lookup"><span data-stu-id="39571-109">**CharLowerWrapW** is a wrapper for the **CharLowerW** function.</span></span> <span data-ttu-id="39571-110">Vea la página [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) para obtener más notas de uso.</span><span class="sxs-lookup"><span data-stu-id="39571-110">See the [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="39571-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39571-111">Syntax</span></span>


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a><span data-ttu-id="39571-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39571-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39571-113">*PCH* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="39571-113">*pch* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="39571-114">Tipo: **LPWStr**</span><span class="sxs-lookup"><span data-stu-id="39571-114">Type: **LPWSTR**</span></span>

<span data-ttu-id="39571-115">Puntero a una cadena Unicode terminada en null o a un solo carácter.</span><span class="sxs-lookup"><span data-stu-id="39571-115">A pointer to a null-terminated Unicode string or a single character.</span></span> <span data-ttu-id="39571-116">Si la palabra de orden superior de este parámetro es cero, la palabra de orden inferior debe contener solo un carácter que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="39571-116">If the high-order word of this parameter is zero, the low-order word must contain only a single character to be converted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39571-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39571-117">Return value</span></span>

<span data-ttu-id="39571-118">Tipo: **LPWStr**</span><span class="sxs-lookup"><span data-stu-id="39571-118">Type: **LPWSTR**</span></span>

<span data-ttu-id="39571-119">Si *PCH* es una cadena de caracteres, la función devuelve un puntero a la cadena convertida.</span><span class="sxs-lookup"><span data-stu-id="39571-119">If *pch* is a character string, the function returns a pointer to the converted string.</span></span> <span data-ttu-id="39571-120">Dado que la cadena se convierte en contexto, el valor devuelto es igual a *PCH*.</span><span class="sxs-lookup"><span data-stu-id="39571-120">Since the string is converted in place, the return value is equal to *pch*.</span></span>

<span data-ttu-id="39571-121">Si *PCH* es un carácter único, el valor devuelto es un valor de 32 bits cuya palabra de orden superior es cero y la palabra de orden inferior contiene el carácter convertido.</span><span class="sxs-lookup"><span data-stu-id="39571-121">If *pch* is a single character, the return value is a 32-bit value whose high-order word is zero, and low-order word contains the converted character.</span></span>

<span data-ttu-id="39571-122">No hay ninguna indicación de si se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="39571-122">There is no indication of success or failure.</span></span> <span data-ttu-id="39571-123">El error es poco frecuente.</span><span class="sxs-lookup"><span data-stu-id="39571-123">Failure is rare.</span></span> <span data-ttu-id="39571-124">No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="39571-124">There is no extended error information for this function; do not call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="39571-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39571-125">Remarks</span></span>

<span data-ttu-id="39571-126">El método preferido es usar [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) junto con la capa de Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="39571-126">The preferred method is to use [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="39571-127">Se debe llamar a **CharLowerWrapW** directamente desde Shlwapi.dll, mediante el ordinal 38.</span><span class="sxs-lookup"><span data-stu-id="39571-127">**CharLowerWrapW** must be called directly from Shlwapi.dll, using ordinal 38.</span></span>

## <a name="requirements"></a><span data-ttu-id="39571-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39571-128">Requirements</span></span>



| <span data-ttu-id="39571-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="39571-129">Requirement</span></span> | <span data-ttu-id="39571-130">Value</span><span class="sxs-lookup"><span data-stu-id="39571-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39571-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39571-131">Minimum supported client</span></span><br/> | <span data-ttu-id="39571-132">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="39571-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39571-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39571-133">Minimum supported server</span></span><br/> | <span data-ttu-id="39571-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="39571-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="39571-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="39571-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39571-136"><dt>Shlwapi.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="39571-136"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39571-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="39571-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39571-138">**CharLower**</span><span class="sxs-lookup"><span data-stu-id="39571-138">**CharLower**</span></span>](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
