---
description: Determina si un carácter es un carácter alfabético o numérico.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: IsCharAlphaNumericWrapW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCharAlphaNumericWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bf7f1b4db54cc5374214ff45b51579556dc22062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984722"
---
# <a name="ischaralphanumericwrapw-function"></a><span data-ttu-id="7e745-103">IsCharAlphaNumericWrapW función)</span><span class="sxs-lookup"><span data-stu-id="7e745-103">IsCharAlphaNumericWrapW function</span></span>

<span data-ttu-id="7e745-104">\[**IsCharAlphaNumericWrapW** está disponible para su uso en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7e745-104">\[**IsCharAlphaNumericWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="7e745-105">No estará disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="7e745-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="7e745-106">Debe usar [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="7e745-106">You should use [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in its place.\]</span></span>

<span data-ttu-id="7e745-107">Determina si un carácter es un carácter alfabético o numérico.</span><span class="sxs-lookup"><span data-stu-id="7e745-107">Determines whether a character is either an alphabetical or a numeric character.</span></span> <span data-ttu-id="7e745-108">Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través del panel de control.</span><span class="sxs-lookup"><span data-stu-id="7e745-108">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span>

> [!Note]  
> <span data-ttu-id="7e745-109">**IsCharAlphaNumericWrapW** es un contenedor para la función **IsCharAlphaNumericW** .</span><span class="sxs-lookup"><span data-stu-id="7e745-109">**IsCharAlphaNumericWrapW** is a wrapper for the **IsCharAlphaNumericW** function.</span></span> <span data-ttu-id="7e745-110">Vea la página [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) para obtener más notas de uso.</span><span class="sxs-lookup"><span data-stu-id="7e745-110">See the [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7e745-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e745-111">Syntax</span></span>


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a><span data-ttu-id="7e745-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e745-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e745-113">*CH* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7e745-113">*ch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e745-114">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="7e745-114">Type: **WCHAR**</span></span>

<span data-ttu-id="7e745-115">Carácter Unicode que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="7e745-115">The Unicode character to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e745-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e745-116">Return value</span></span>

<span data-ttu-id="7e745-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="7e745-117">Type: **BOOL**</span></span>

<span data-ttu-id="7e745-118">Si el carácter es alfanumérico, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="7e745-118">If the character is alphanumeric, the return value is nonzero.</span></span>

<span data-ttu-id="7e745-119">Si el carácter no es alfanumérico, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="7e745-119">If the character is not alphanumeric, the return value is zero.</span></span> <span data-ttu-id="7e745-120">Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="7e745-120">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="7e745-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e745-121">Remarks</span></span>

<span data-ttu-id="7e745-122">**IsCharAlphaNumericWrapW** ofrece la posibilidad de usar cadenas Unicode en sistemas operativos anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7e745-122">**IsCharAlphaNumericWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="7e745-123">El método preferido es usar [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) junto con la capa de Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="7e745-123">The preferred method is to use [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="7e745-124">Se debe llamar a **IsCharAlphaNumericWrapW** directamente desde Shlwapi.dll, mediante el ordinal 28.</span><span class="sxs-lookup"><span data-stu-id="7e745-124">**IsCharAlphaNumericWrapW** must be called directly from Shlwapi.dll, using ordinal 28.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e745-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e745-125">Requirements</span></span>



| <span data-ttu-id="7e745-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e745-126">Requirement</span></span> | <span data-ttu-id="7e745-127">Value</span><span class="sxs-lookup"><span data-stu-id="7e745-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e745-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e745-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7e745-129">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7e745-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e745-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e745-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7e745-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e745-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7e745-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e745-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e745-133"><dt>Shlwapi.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="7e745-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e745-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e745-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e745-135">**IsCharAlphaNumeric**</span><span class="sxs-lookup"><span data-stu-id="7e745-135">**IsCharAlphaNumeric**</span></span>](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
