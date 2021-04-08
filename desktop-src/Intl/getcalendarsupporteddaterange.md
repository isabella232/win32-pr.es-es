---
description: Desusado. Obtiene el intervalo de fechas admitido para un calendario especificado.
ms.assetid: fe036ac5-77c0-4e83-8d70-db3fa0f7c803
title: GetCalendarSupportedDateRange función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarSupportedDateRange
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 57b1175ef7bcf5b6b5d91af63682ca565bc0f1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002379"
---
# <a name="getcalendarsupporteddaterange-function"></a><span data-ttu-id="9f9e9-104">GetCalendarSupportedDateRange función)</span><span class="sxs-lookup"><span data-stu-id="9f9e9-104">GetCalendarSupportedDateRange function</span></span>

<span data-ttu-id="9f9e9-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="9f9e9-105">Deprecated.</span></span> <span data-ttu-id="9f9e9-106">Obtiene el intervalo de fechas admitido para un calendario especificado.</span><span class="sxs-lookup"><span data-stu-id="9f9e9-106">Gets the supported date range for a specified calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f9e9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f9e9-107">Syntax</span></span>


```C++
BOOL GetCalendarSupportedDateRange(
  _In_  CALID         Calendar,
  _Out_ LPCALDATETIME lpCalMinDateTime,
  _Out_ LPCALDATETIME lpCalMaxDateTime
);
```



## <a name="parameters"></a><span data-ttu-id="9f9e9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f9e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f9e9-109">*Calendario* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9f9e9-109">*Calendar* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f9e9-110">[Identificador de calendario](calendar-identifiers.md) para el que se va a obtener el intervalo de fechas admitido.</span><span class="sxs-lookup"><span data-stu-id="9f9e9-110">[Calendar identifier](calendar-identifiers.md) for which to get the supported date range.</span></span>

</dd> <dt>

<span data-ttu-id="9f9e9-111">*lpCalMinDateTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9f9e9-111">*lpCalMinDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f9e9-112">Puntero a una estructura [**CALDATETIME**](caldatetime.md) que define la fecha mínima admitida.</span><span class="sxs-lookup"><span data-stu-id="9f9e9-112">Pointer to a [**CALDATETIME**](caldatetime.md) structure defining the minimum supported date.</span></span>

</dd> <dt>

<span data-ttu-id="9f9e9-113">*lpCalMaxDateTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9f9e9-113">*lpCalMaxDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f9e9-114">Puntero a una estructura [**CALDATETIME**](caldatetime.md) que define la fecha máxima admitida.</span><span class="sxs-lookup"><span data-stu-id="9f9e9-114">Pointer to a [**CALDATETIME**](caldatetime.md) structure defining the maximum supported date.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f9e9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f9e9-115">Return value</span></span>

<span data-ttu-id="9f9e9-116">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9f9e9-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="9f9e9-117">Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="9f9e9-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="9f9e9-118">ERROR \_ de \_ parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="9f9e9-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="9f9e9-119">Cualquiera de los valores de parámetro no era válido.</span><span class="sxs-lookup"><span data-stu-id="9f9e9-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f9e9-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f9e9-120">Remarks</span></span>

<span data-ttu-id="9f9e9-121">La primera fecha admitida por esta función es el 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="9f9e9-121">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="9f9e9-122">Esta función no tiene asociado un archivo de encabezado o archivo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9f9e9-122">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="9f9e9-123">La aplicación puede llamar a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre de DLL (Kernel32.dll) para obtener un identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="9f9e9-123">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="9f9e9-124">Después, puede llamar a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con el identificador de módulo y el nombre de esta función para obtener la dirección de la función.</span><span class="sxs-lookup"><span data-stu-id="9f9e9-124">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f9e9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f9e9-125">Requirements</span></span>



| <span data-ttu-id="9f9e9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f9e9-126">Requirement</span></span> | <span data-ttu-id="9f9e9-127">Value</span><span class="sxs-lookup"><span data-stu-id="9f9e9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f9e9-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f9e9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9f9e9-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9f9e9-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9f9e9-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f9e9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9f9e9-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f9e9-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9f9e9-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9f9e9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f9e9-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f9e9-133"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f9e9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f9e9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f9e9-135">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="9f9e9-135">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="9f9e9-136">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="9f9e9-136">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="9f9e9-137">NLS: ejemplo de API basadas en nombre</span><span class="sxs-lookup"><span data-stu-id="9f9e9-137">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
