---
description: Desusado. Convierte una estructura SYSTEMTIME especificada en una estructura CALDATETIME.
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: ConvertSystemTimeToCalDateTime función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertSystemTimeToCalDateTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 738899c7307797f0edeade93f7e4e706919be900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652709"
---
# <a name="convertsystemtimetocaldatetime-function"></a><span data-ttu-id="f4ead-104">ConvertSystemTimeToCalDateTime función)</span><span class="sxs-lookup"><span data-stu-id="f4ead-104">ConvertSystemTimeToCalDateTime function</span></span>

<span data-ttu-id="f4ead-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="f4ead-105">Deprecated.</span></span> <span data-ttu-id="f4ead-106">Convierte una estructura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) especificada en una estructura [**CALDATETIME**](caldatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="f4ead-106">Converts a specified [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure to a [**CALDATETIME**](caldatetime.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ead-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4ead-107">Syntax</span></span>


```C++
BOOL ConvertSystemTimeToCalDateTime(
  _In_  const SYSTEMTIME   *lpSysTime,
  _In_        CALID         calId,
  _Out_       LPCALDATETIME lpCalDateTime

);
```



## <a name="parameters"></a><span data-ttu-id="f4ead-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4ead-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4ead-109">*lpSysTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f4ead-109">*lpSysTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ead-110">Puntero a la estructura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="f4ead-110">Pointer to the [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure to convert.</span></span>

</dd> <dt>

<span data-ttu-id="f4ead-111">*calId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f4ead-111">*calId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ead-112">Identificador del [calendario](calendar-identifiers.md) del sistema que se va a utilizar en la conversión.</span><span class="sxs-lookup"><span data-stu-id="f4ead-112">The system [calendar identifier](calendar-identifiers.md) to use in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="f4ead-113">*lpCalDateTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f4ead-113">*lpCalDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ead-114">Puntero a la estructura [**CALDATETIME**](caldatetime.md) equivalente.</span><span class="sxs-lookup"><span data-stu-id="f4ead-114">Pointer to the equivalent [**CALDATETIME**](caldatetime.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4ead-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4ead-115">Return value</span></span>

<span data-ttu-id="f4ead-116">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f4ead-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="f4ead-117">Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="f4ead-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="f4ead-118">ERROR \_ de \_ parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="f4ead-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="f4ead-119">Cualquiera de los valores de parámetro no era válido.</span><span class="sxs-lookup"><span data-stu-id="f4ead-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4ead-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4ead-120">Remarks</span></span>

<span data-ttu-id="f4ead-121">La primera fecha admitida por esta función es el 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="f4ead-121">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="f4ead-122">Esta función no tiene asociado un archivo de encabezado o archivo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f4ead-122">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="f4ead-123">La aplicación puede llamar a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre de DLL (Kernel32.dll) para obtener un identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="f4ead-123">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="f4ead-124">Después, puede llamar a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con el identificador de módulo y el nombre de esta función para obtener la dirección de la función.</span><span class="sxs-lookup"><span data-stu-id="f4ead-124">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4ead-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4ead-125">Requirements</span></span>



| <span data-ttu-id="f4ead-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4ead-126">Requirement</span></span> | <span data-ttu-id="f4ead-127">Value</span><span class="sxs-lookup"><span data-stu-id="f4ead-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ead-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4ead-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f4ead-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f4ead-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f4ead-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4ead-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f4ead-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4ead-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f4ead-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f4ead-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4ead-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4ead-133"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4ead-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4ead-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ead-135">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="f4ead-135">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="f4ead-136">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="f4ead-136">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="f4ead-137">Recuperar información de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="f4ead-137">Retrieving Time and Date Information</span></span>](time-and-date.md)
</dt> </dl>

 

 
