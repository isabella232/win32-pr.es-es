---
description: Desusado. Ajusta una fecha en un número especificado de años, meses, semanas o días.
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: AdjustCalendarDate función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdjustCalendarDate
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: ce2f61fd7d7d6354130873b5b2b2376c856e3958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686729"
---
# <a name="adjustcalendardate-function"></a><span data-ttu-id="799cd-104">AdjustCalendarDate función)</span><span class="sxs-lookup"><span data-stu-id="799cd-104">AdjustCalendarDate function</span></span>

<span data-ttu-id="799cd-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="799cd-105">Deprecated.</span></span> <span data-ttu-id="799cd-106">Ajusta una fecha en un número especificado de años, meses, semanas o días.</span><span class="sxs-lookup"><span data-stu-id="799cd-106">Adjusts a date by a specified number of years, months, weeks, or days.</span></span>

## <a name="syntax"></a><span data-ttu-id="799cd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="799cd-107">Syntax</span></span>


```C++
BOOL AdjustCalendarDate(
  _Inout_ LPCALDATETIME        lpCalDateTime,
  _In_    CALDATETIME_DATEUNIT calUnit,
  _Out_   INT                  amount
);
```



## <a name="parameters"></a><span data-ttu-id="799cd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="799cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="799cd-109">*lpCalDateTime* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="799cd-109">*lpCalDateTime* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="799cd-110">Puntero a una estructura [**CALDATETIME**](caldatetime.md) que contiene la información de fecha y calendario que se va a ajustar.</span><span class="sxs-lookup"><span data-stu-id="799cd-110">Pointer to a [**CALDATETIME**](caldatetime.md) structure that contains the date and calendar information to adjust.</span></span>

</dd> <dt>

<span data-ttu-id="799cd-111">*calUnit* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="799cd-111">*calUnit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="799cd-112">El valor de enumeración de [**CALDATETIME \_ DATEUNIT**](caldatetime-dateunit.md) que indica la unidad de fecha, por ejemplo, DayUnit.</span><span class="sxs-lookup"><span data-stu-id="799cd-112">The [**CALDATETIME\_DATEUNIT**](caldatetime-dateunit.md) enumeration value indicating the date unit, for example, DayUnit.</span></span>

</dd> <dt>

<span data-ttu-id="799cd-113">*cantidad* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="799cd-113">*amount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="799cd-114">Cantidad por la que se va a ajustar la fecha especificada.</span><span class="sxs-lookup"><span data-stu-id="799cd-114">The amount by which to adjust the specified date.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="799cd-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="799cd-115">Return value</span></span>

<span data-ttu-id="799cd-116">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="799cd-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="799cd-117">Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="799cd-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="799cd-118">\_fecha \_ de error fuera \_ del \_ intervalo.</span><span class="sxs-lookup"><span data-stu-id="799cd-118">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="799cd-119">La fecha especificada estaba fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="799cd-119">The specified date was out of range.</span></span>
-   <span data-ttu-id="799cd-120">ERROR \_ de \_ parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="799cd-120">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="799cd-121">Cualquiera de los valores de parámetro no era válido.</span><span class="sxs-lookup"><span data-stu-id="799cd-121">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="799cd-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="799cd-122">Remarks</span></span>

<span data-ttu-id="799cd-123">Esta función no tiene asociado un archivo de encabezado o archivo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="799cd-123">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="799cd-124">La aplicación puede llamar a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre de DLL (Kernel32.dll) para obtener un identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="799cd-124">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="799cd-125">Después, puede llamar a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con el identificador de módulo y el nombre de esta función para obtener la dirección de la función.</span><span class="sxs-lookup"><span data-stu-id="799cd-125">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="799cd-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="799cd-126">Requirements</span></span>



| <span data-ttu-id="799cd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="799cd-127">Requirement</span></span> | <span data-ttu-id="799cd-128">Value</span><span class="sxs-lookup"><span data-stu-id="799cd-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="799cd-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="799cd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="799cd-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="799cd-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="799cd-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="799cd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="799cd-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="799cd-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="799cd-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="799cd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="799cd-134"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="799cd-134"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="799cd-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="799cd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="799cd-136">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="799cd-136">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="799cd-137">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="799cd-137">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="799cd-138">NLS: ejemplo de API basadas en nombre</span><span class="sxs-lookup"><span data-stu-id="799cd-138">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
