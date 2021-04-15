---
description: Desusado. Obtiene el día de la semana que corresponde a un día especificado y rellena el miembro DayOfWeek de la estructura CALDATETIME especificada con ese valor.
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: UpdateCalendarDayOfWeek función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateCalendarDayOfWeek
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 316af539e6ca0476f0f8d575a160fcd7c3219e90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688703"
---
# <a name="updatecalendardayofweek-function"></a><span data-ttu-id="7f2dc-104">UpdateCalendarDayOfWeek función)</span><span class="sxs-lookup"><span data-stu-id="7f2dc-104">UpdateCalendarDayOfWeek function</span></span>

<span data-ttu-id="7f2dc-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="7f2dc-105">Deprecated.</span></span> <span data-ttu-id="7f2dc-106">Obtiene el día de la semana que corresponde a un día especificado y rellena el miembro **DayOfWeek** de la estructura [**CALDATETIME**](caldatetime.md) especificada con ese valor.</span><span class="sxs-lookup"><span data-stu-id="7f2dc-106">Gets the day of the week that corresponds to a specified day and populates the **DayOfWeek** member in the specified [**CALDATETIME**](caldatetime.md) structure with that value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f2dc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f2dc-107">Syntax</span></span>


```C++
BOOL UpdateCalendarDayOfWeek(
  _Inout_ LPCALDATETIME lpCalDateTime
);
```



## <a name="parameters"></a><span data-ttu-id="7f2dc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f2dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f2dc-109">*lpCalDateTime* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7f2dc-109">*lpCalDateTime* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2dc-110">Puntero a la estructura [**CALDATETIME**](caldatetime.md) que contiene la fecha para la que se va a establecer el día de la semana.</span><span class="sxs-lookup"><span data-stu-id="7f2dc-110">Pointer to the [**CALDATETIME**](caldatetime.md) structure containing the date for which to set the day of the week.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f2dc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f2dc-111">Return value</span></span>

<span data-ttu-id="7f2dc-112">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7f2dc-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="7f2dc-113">Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="7f2dc-113">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="7f2dc-114">\_fecha \_ de error fuera \_ del \_ intervalo.</span><span class="sxs-lookup"><span data-stu-id="7f2dc-114">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="7f2dc-115">La fecha especificada estaba fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="7f2dc-115">The specified date was out of range.</span></span>
-   <span data-ttu-id="7f2dc-116">ERROR \_ de \_ parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="7f2dc-116">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="7f2dc-117">Cualquiera de los valores de parámetro no era válido.</span><span class="sxs-lookup"><span data-stu-id="7f2dc-117">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f2dc-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f2dc-118">Remarks</span></span>

<span data-ttu-id="7f2dc-119">Esta función no tiene asociado un archivo de encabezado o archivo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7f2dc-119">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="7f2dc-120">La aplicación puede llamar a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre de DLL (Kernel32.dll) para obtener un identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="7f2dc-120">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="7f2dc-121">Después, puede llamar a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el nombre de esta función para obtener la dirección de la función.</span><span class="sxs-lookup"><span data-stu-id="7f2dc-121">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f2dc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f2dc-122">Requirements</span></span>



| <span data-ttu-id="7f2dc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f2dc-123">Requirement</span></span> | <span data-ttu-id="7f2dc-124">Value</span><span class="sxs-lookup"><span data-stu-id="7f2dc-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f2dc-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f2dc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7f2dc-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7f2dc-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7f2dc-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f2dc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7f2dc-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f2dc-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7f2dc-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7f2dc-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f2dc-130"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f2dc-130"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f2dc-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f2dc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f2dc-132">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="7f2dc-132">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="7f2dc-133">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="7f2dc-133">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="7f2dc-134">**CALDATETIME**</span><span class="sxs-lookup"><span data-stu-id="7f2dc-134">**CALDATETIME**</span></span>](caldatetime.md)
</dt> </dl>

 

 
