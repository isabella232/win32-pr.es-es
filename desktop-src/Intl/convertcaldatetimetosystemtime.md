---
description: Desusado. Convierte una estructura CALDATETIME especificada en una estructura SYSTEMTIME.
ms.assetid: 0c3f602d-62de-4c27-95d9-d35738f3279d
title: ConvertCalDateTimeToSystemTime función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertCalDateTimeToSystemTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 9c317a31904e2d1b0b2110f6b2dc367ac3e2e0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687620"
---
# <a name="convertcaldatetimetosystemtime-function"></a><span data-ttu-id="e940b-104">ConvertCalDateTimeToSystemTime función)</span><span class="sxs-lookup"><span data-stu-id="e940b-104">ConvertCalDateTimeToSystemTime function</span></span>

<span data-ttu-id="e940b-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="e940b-105">Deprecated.</span></span> <span data-ttu-id="e940b-106">Convierte una estructura [**CALDATETIME**](caldatetime.md) especificada en una estructura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="e940b-106">Converts a specified [**CALDATETIME**](caldatetime.md) structure to a [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e940b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e940b-107">Syntax</span></span>


```C++
BOOL ConvertCalDateTimeToSystemTime(
  _In_  const LPCALDATETIME lpCalDateTime,
  _Out_       SYSTEMTIME    *lpSysTime
);
```



## <a name="parameters"></a><span data-ttu-id="e940b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e940b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e940b-109">*lpCalDateTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e940b-109">*lpCalDateTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e940b-110">Puntero a la estructura [**CALDATETIME**](caldatetime.md) que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="e940b-110">Pointer to the [**CALDATETIME**](caldatetime.md) structure to convert.</span></span>

</dd> <dt>

<span data-ttu-id="e940b-111">*lpSysTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e940b-111">*lpSysTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e940b-112">Puntero a la estructura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) equivalente.</span><span class="sxs-lookup"><span data-stu-id="e940b-112">Pointer to the equivalent [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e940b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e940b-113">Return value</span></span>

<span data-ttu-id="e940b-114">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e940b-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="e940b-115">Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="e940b-115">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="e940b-116">\_fecha \_ de error fuera \_ del \_ intervalo.</span><span class="sxs-lookup"><span data-stu-id="e940b-116">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="e940b-117">La fecha especificada estaba fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="e940b-117">The specified date was out of range.</span></span>
-   <span data-ttu-id="e940b-118">ERROR \_ de \_ parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="e940b-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="e940b-119">Cualquiera de los valores de parámetro no era válido.</span><span class="sxs-lookup"><span data-stu-id="e940b-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="e940b-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e940b-120">Remarks</span></span>

<span data-ttu-id="e940b-121">Esta función no tiene asociado un archivo de encabezado o archivo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e940b-121">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="e940b-122">La aplicación puede llamar a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre de DLL (Kernel32.dll) para obtener un identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="e940b-122">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="e940b-123">Después, puede llamar a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con el identificador de módulo y el nombre de esta función para obtener la dirección de la función.</span><span class="sxs-lookup"><span data-stu-id="e940b-123">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="e940b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e940b-124">Requirements</span></span>



| <span data-ttu-id="e940b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e940b-125">Requirement</span></span> | <span data-ttu-id="e940b-126">Value</span><span class="sxs-lookup"><span data-stu-id="e940b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e940b-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e940b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e940b-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e940b-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e940b-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e940b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e940b-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e940b-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e940b-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e940b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e940b-132"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e940b-132"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e940b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e940b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e940b-134">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="e940b-134">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="e940b-135">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="e940b-135">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="e940b-136">Recuperar información de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="e940b-136">Retrieving Time and Date Information</span></span>](time-and-date.md)
</dt> </dl>

 

 
