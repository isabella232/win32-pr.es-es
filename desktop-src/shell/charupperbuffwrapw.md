---
description: Convierte los caracteres en minúsculas de un búfer en caracteres en mayúsculas.
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: CharUpperBuffWrapW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharUpperBuffWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: dacc5e7609ca7f91bf7c66651d7ba9bdd11ab688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540555"
---
# <a name="charupperbuffwrapw-function"></a><span data-ttu-id="1df26-103">CharUpperBuffWrapW función)</span><span class="sxs-lookup"><span data-stu-id="1df26-103">CharUpperBuffWrapW function</span></span>

<span data-ttu-id="1df26-104">\[**CharUpperBuffWrapW** está disponible para su uso en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1df26-104">\[**CharUpperBuffWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="1df26-105">Puede que no esté disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1df26-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="1df26-106">Debe usar [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="1df26-106">You should use [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in its place.\]</span></span>

<span data-ttu-id="1df26-107">Convierte los caracteres en minúsculas de un búfer en caracteres en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="1df26-107">Converts lowercase characters in a buffer to uppercase characters.</span></span> <span data-ttu-id="1df26-108">La función convierte los caracteres en su lugar.</span><span class="sxs-lookup"><span data-stu-id="1df26-108">The function converts the characters in place.</span></span>

> [!Note]  
> <span data-ttu-id="1df26-109">**CharUpperBuffWrapW** es un contenedor para la función **CharUpperBuffW** .</span><span class="sxs-lookup"><span data-stu-id="1df26-109">**CharUpperBuffWrapW** is a wrapper for the **CharUpperBuffW** function.</span></span> <span data-ttu-id="1df26-110">Vea la página [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) para obtener más notas de uso.</span><span class="sxs-lookup"><span data-stu-id="1df26-110">See the [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1df26-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1df26-111">Syntax</span></span>


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a><span data-ttu-id="1df26-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1df26-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1df26-113">*PCH* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1df26-113">*pch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df26-114">Tipo: **LPWStr**</span><span class="sxs-lookup"><span data-stu-id="1df26-114">Type: **LPWSTR**</span></span>

<span data-ttu-id="1df26-115">Puntero a un búfer que contiene uno o más caracteres Unicode que se van a procesar.</span><span class="sxs-lookup"><span data-stu-id="1df26-115">A pointer to a buffer that contains one or more Unicode characters to process.</span></span>

</dd> <dt>

<span data-ttu-id="1df26-116">*cchLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1df26-116">*cchLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df26-117">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1df26-117">Type: **DWORD**</span></span>

<span data-ttu-id="1df26-118">Especifica el tamaño, en caracteres, del búfer al que apunta *PCH*.</span><span class="sxs-lookup"><span data-stu-id="1df26-118">Specifies the size, in characters, of the buffer pointed to by *pch*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1df26-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1df26-119">Return value</span></span>

<span data-ttu-id="1df26-120">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1df26-120">Type: **DWORD**</span></span>

<span data-ttu-id="1df26-121">Número de caracteres procesados.</span><span class="sxs-lookup"><span data-stu-id="1df26-121">The number of characters processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="1df26-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1df26-122">Remarks</span></span>

<span data-ttu-id="1df26-123">El método preferido es usar [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) junto con la capa de Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="1df26-123">The preferred method is to use [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="1df26-124">Se debe llamar a **CharUpperBuffWrapW** directamente desde Shlwapi.dll, mediante el ordinal 44.</span><span class="sxs-lookup"><span data-stu-id="1df26-124">**CharUpperBuffWrapW** must be called directly from Shlwapi.dll, using ordinal 44.</span></span>

## <a name="requirements"></a><span data-ttu-id="1df26-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1df26-125">Requirements</span></span>



| <span data-ttu-id="1df26-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1df26-126">Requirement</span></span> | <span data-ttu-id="1df26-127">Value</span><span class="sxs-lookup"><span data-stu-id="1df26-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1df26-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1df26-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1df26-129">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1df26-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1df26-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1df26-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1df26-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1df26-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1df26-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1df26-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1df26-133"><dt>Shlwapi.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="1df26-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1df26-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="1df26-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df26-135">**CharUpperBuff**</span><span class="sxs-lookup"><span data-stu-id="1df26-135">**CharUpperBuff**</span></span>](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
