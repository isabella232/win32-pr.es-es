---
description: Envía una cadena Unicode al depurador para su presentación.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: Función OutputDebugStringWrapW (Shlwapip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OutputDebugStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: e8213aee48a90a816e2968aac115159472ed7b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997777"
---
# <a name="outputdebugstringwrapw-function"></a><span data-ttu-id="bb32a-103">OutputDebugStringWrapW función)</span><span class="sxs-lookup"><span data-stu-id="bb32a-103">OutputDebugStringWrapW function</span></span>

<span data-ttu-id="bb32a-104">\[Esta función está disponible para su uso en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb32a-104">\[This function is available for use in Windows XP.</span></span> <span data-ttu-id="bb32a-105">Puede que no esté disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bb32a-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="bb32a-106">Use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="bb32a-106">Use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in its place.\]</span></span>

<span data-ttu-id="bb32a-107">Envía una cadena Unicode al depurador para su presentación.</span><span class="sxs-lookup"><span data-stu-id="bb32a-107">Sends a Unicode string to the debugger for display.</span></span>

> [!Note]  
> <span data-ttu-id="bb32a-108">**OutputDebugStringWrapW** es un contenedor para la función **OutputDebugStringW** .</span><span class="sxs-lookup"><span data-stu-id="bb32a-108">**OutputDebugStringWrapW** is a wrapper for the **OutputDebugStringW** function.</span></span> <span data-ttu-id="bb32a-109">Vea la página [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) para obtener más notas de uso.</span><span class="sxs-lookup"><span data-stu-id="bb32a-109">See the [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bb32a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb32a-110">Syntax</span></span>


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a><span data-ttu-id="bb32a-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb32a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb32a-112">*lpOutputString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb32a-112">*lpOutputString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb32a-113">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="bb32a-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="bb32a-114">Puntero a la cadena Unicode terminada en null que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="bb32a-114">A pointer to the null-terminated Unicode string to be displayed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb32a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb32a-115">Return value</span></span>

<span data-ttu-id="bb32a-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bb32a-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb32a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb32a-117">Remarks</span></span>

<span data-ttu-id="bb32a-118">**OutputDebugStringWrapW** ofrece la posibilidad de usar cadenas Unicode en sistemas operativos anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb32a-118">**OutputDebugStringWrapW** provides the ability to use Unicode strings in operating systems prior to Windows XP.</span></span> <span data-ttu-id="bb32a-119">El método preferido es usar [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) junto con la capa de Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="bb32a-119">The preferred method is to use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="bb32a-120">Se debe llamar a **OutputDebugStringWrapW** directamente desde Shlwapi.dll, mediante el ordinal 115.</span><span class="sxs-lookup"><span data-stu-id="bb32a-120">**OutputDebugStringWrapW** must be called directly from Shlwapi.dll, using ordinal 115.</span></span>

<span data-ttu-id="bb32a-121">Si la aplicación no tiene ningún depurador, el depurador del sistema muestra la cadena.</span><span class="sxs-lookup"><span data-stu-id="bb32a-121">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="bb32a-122">Si la aplicación no tiene ningún depurador y el depurador del sistema no está activo, **OutputDebugStringWrapW** no hace nada.</span><span class="sxs-lookup"><span data-stu-id="bb32a-122">If the application has no debugger and the system debugger is not active, **OutputDebugStringWrapW** does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb32a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb32a-123">Requirements</span></span>



| <span data-ttu-id="bb32a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb32a-124">Requirement</span></span> | <span data-ttu-id="bb32a-125">Value</span><span class="sxs-lookup"><span data-stu-id="bb32a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb32a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb32a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bb32a-127">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bb32a-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb32a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb32a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bb32a-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb32a-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bb32a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb32a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb32a-131"><dt>Shlwapip. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb32a-131"><dt>Shlwapip.h</dt></span></span> </dl>                         |
| <span data-ttu-id="bb32a-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bb32a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb32a-133"><dt>Shlwapi.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="bb32a-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb32a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb32a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb32a-135">**OutputDebugString**</span><span class="sxs-lookup"><span data-stu-id="bb32a-135">**OutputDebugString**</span></span>](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
