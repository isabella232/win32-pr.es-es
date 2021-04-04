---
description: Desusado. Identifica si el año especificado es un año bisiesto dentro de la era especificada para el calendario específico.
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: IsCalendarLeapYear función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCalendarLeapYear
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 484531f8107bacb70f9e24ba2537090317825e26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910109"
---
# <a name="iscalendarleapyear-function"></a><span data-ttu-id="f0438-104">IsCalendarLeapYear función)</span><span class="sxs-lookup"><span data-stu-id="f0438-104">IsCalendarLeapYear function</span></span>

<span data-ttu-id="f0438-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="f0438-105">Deprecated.</span></span> <span data-ttu-id="f0438-106">Identifica si el año especificado es un año bisiesto dentro de la era especificada para el calendario específico.</span><span class="sxs-lookup"><span data-stu-id="f0438-106">Identifies whether the specified year is a leap year within the given era for the specific calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0438-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0438-107">Syntax</span></span>


```C++
BOOL IsCalendarLeapYear(
  _In_ CALID calId,
  _In_ UINT  year,
  _In_ UINT  era
);
```



## <a name="parameters"></a><span data-ttu-id="f0438-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0438-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0438-109">*calId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0438-109">*calId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0438-110">[Identificador del calendario](calendar-identifiers.md) que se va a usar para comprobar el año bisiesto.</span><span class="sxs-lookup"><span data-stu-id="f0438-110">The [calendar identifier](calendar-identifiers.md) to use for checking leap year.</span></span>

</dd> <dt>

<span data-ttu-id="f0438-111">*año* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0438-111">*year* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0438-112">Año que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="f0438-112">The year to check.</span></span>

</dd> <dt>

<span data-ttu-id="f0438-113">*era* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0438-113">*era* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0438-114">La era que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="f0438-114">The era to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0438-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0438-115">Return value</span></span>

<span data-ttu-id="f0438-116">Devuelve **true** si el año especificado es un año bisiesto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f0438-116">Returns **TRUE** if the specified year is a leap year, or **FALSE** otherwise.</span></span> <span data-ttu-id="f0438-117">Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="f0438-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="f0438-118">ERROR \_ de \_ parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="f0438-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="f0438-119">Cualquiera de los valores de parámetro no era válido.</span><span class="sxs-lookup"><span data-stu-id="f0438-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0438-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0438-120">Remarks</span></span>

<span data-ttu-id="f0438-121">Esta función no tiene asociado un archivo de encabezado o archivo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f0438-121">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="f0438-122">La aplicación puede llamar a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre de DLL (Kernel32.dll) para obtener un identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="f0438-122">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="f0438-123">Después, puede llamar a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el nombre de esta función para obtener la dirección de la función.</span><span class="sxs-lookup"><span data-stu-id="f0438-123">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0438-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0438-124">Requirements</span></span>



| <span data-ttu-id="f0438-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0438-125">Requirement</span></span> | <span data-ttu-id="f0438-126">Value</span><span class="sxs-lookup"><span data-stu-id="f0438-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0438-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0438-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f0438-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f0438-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f0438-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0438-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f0438-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0438-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0438-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0438-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0438-132"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0438-132"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0438-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0438-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0438-134">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="f0438-134">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="f0438-135">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="f0438-135">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> </dl>

 

 
