---
description: Da formato a la hora como una cadena de hora para una configuración regional especificada.
ms.assetid: 048b209c-f757-4b65-9ce7-282a5c21021f
title: GetTimeFormatWrapW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTimeFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 53f1bb88c2b3a79b58f3025daec31a7b1340b642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985483"
---
# <a name="gettimeformatwrapw-function"></a><span data-ttu-id="ff485-103">GetTimeFormatWrapW función)</span><span class="sxs-lookup"><span data-stu-id="ff485-103">GetTimeFormatWrapW function</span></span>

<span data-ttu-id="ff485-104">\[**GetTimeFormatWrapW** está disponible para su uso en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ff485-104">\[**GetTimeFormatWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="ff485-105">Puede que no esté disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ff485-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="ff485-106">Debe usar [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="ff485-106">You should use [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in its place.\]</span></span>

<span data-ttu-id="ff485-107">Da formato a la hora como una cadena de hora para una configuración regional especificada.</span><span class="sxs-lookup"><span data-stu-id="ff485-107">Formats time as a time string for a specified locale.</span></span> <span data-ttu-id="ff485-108">La función da formato a una hora especificada o a la hora del sistema local.</span><span class="sxs-lookup"><span data-stu-id="ff485-108">The function formats either a specified time or the local system time.</span></span>

> [!Note]  
> <span data-ttu-id="ff485-109">**GetTimeFormatWrapW** es un contenedor para la función **GetTimeFormatW** .</span><span class="sxs-lookup"><span data-stu-id="ff485-109">**GetTimeFormatWrapW** is a wrapper for the **GetTimeFormatW** function.</span></span> <span data-ttu-id="ff485-110">Vea la página [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) para obtener más notas de uso.</span><span class="sxs-lookup"><span data-stu-id="ff485-110">See the [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ff485-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff485-111">Syntax</span></span>


```C++
int GetTimeFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpTime,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzTimeStr,
  _In_        int        cchTime
);
```



## <a name="parameters"></a><span data-ttu-id="ff485-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff485-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff485-113">*Configuración regional* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ff485-113">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff485-114">Tipo: **LCID**</span><span class="sxs-lookup"><span data-stu-id="ff485-114">Type: **LCID**</span></span>

<span data-ttu-id="ff485-115">Especifica la configuración regional para la que se va a dar formato a la cadena de hora.</span><span class="sxs-lookup"><span data-stu-id="ff485-115">Specifies the locale for which the time string is to be formatted.</span></span> <span data-ttu-id="ff485-116">Si *pwzFormat* es **null**, la función da formato a la cadena según el formato de hora de esta configuración regional.</span><span class="sxs-lookup"><span data-stu-id="ff485-116">If *pwzFormat* is **NULL**, the function formats the string according to the time format for this locale.</span></span> <span data-ttu-id="ff485-117">Si *pwzFormat* no es **null**, la función usa la configuración regional solo para la información que no se especifica en la cadena de formato de imagen (por ejemplo, los marcadores de hora de la configuración regional).</span><span class="sxs-lookup"><span data-stu-id="ff485-117">If *pwzFormat* is not **NULL**, the function uses the locale only for information not specified in the format picture string (for example, the locale's time markers).</span></span>

<span data-ttu-id="ff485-118">Este parámetro puede ser un identificador de configuración regional creado por la macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) , o uno de los siguientes valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="ff485-118">This parameter can be a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro, or one of the following predefined values.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="ff485-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**configuración \_ predeterminada del sistema local \_**</span><span class="sxs-lookup"><span data-stu-id="ff485-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="ff485-120">Configuración regional predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="ff485-120">Default system locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="ff485-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_valor predeterminado del usuario de configuración regional \_**</span><span class="sxs-lookup"><span data-stu-id="ff485-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="ff485-122">Configuración regional predeterminada del usuario.</span><span class="sxs-lookup"><span data-stu-id="ff485-122">Default user locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ff485-123">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ff485-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff485-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ff485-124">Type: **DWORD**</span></span>

<span data-ttu-id="ff485-125">Especifica varias opciones de función.</span><span class="sxs-lookup"><span data-stu-id="ff485-125">Specifies various function options.</span></span> <span data-ttu-id="ff485-126">Puede especificar una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ff485-126">You can specify a combination of the following values.</span></span>

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span data-ttu-id="ff485-127"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**configuración regional \_ NOUSEROVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="ff485-127"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE\_NOUSEROVERRIDE**</span></span>


</dt> <dd>

<span data-ttu-id="ff485-128">Si se establece, la función da formato a la cadena con el formato de hora predeterminado del sistema para la configuración regional especificada.</span><span class="sxs-lookup"><span data-stu-id="ff485-128">If set, the function formats the string using the system default time format for the specified locale.</span></span> <span data-ttu-id="ff485-129">Si no se establece, la función da formato a la cadena mediante cualquier reemplazo de usuario al formato de hora predeterminado de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="ff485-129">If not set, the function formats the string using any user overrides to the locale's default time format.</span></span> <span data-ttu-id="ff485-130">Esta marca solo se puede establecer si *pwzFormat* es **null**.</span><span class="sxs-lookup"><span data-stu-id="ff485-130">This flag can only be set if *pwzFormat* is **NULL**.</span></span>

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span data-ttu-id="ff485-131"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**configuración regional \_ use \_ CP \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="ff485-131"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALE\_USE\_CP\_ACP**</span></span>


</dt> <dd>

<span data-ttu-id="ff485-132">Usa la página de códigos ANSI del sistema para la traducción de cadenas en lugar de la página de códigos de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="ff485-132">Uses the system ANSI code page for string translation instead of the locale code page.</span></span>

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span data-ttu-id="ff485-133"><span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**HORA \_ NOMINUTESORSECONDS**</span><span class="sxs-lookup"><span data-stu-id="ff485-133"><span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**TIME\_NOMINUTESORSECONDS**</span></span>


</dt> <dd>

<span data-ttu-id="ff485-134">No usa minutos ni segundos.</span><span class="sxs-lookup"><span data-stu-id="ff485-134">Does not use minutes or seconds.</span></span>

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span data-ttu-id="ff485-135"><span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**TIEMPO \_ NOsegundos**</span><span class="sxs-lookup"><span data-stu-id="ff485-135"><span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**TIME\_NOSECONDS**</span></span>


</dt> <dd>

<span data-ttu-id="ff485-136">No utiliza segundos.</span><span class="sxs-lookup"><span data-stu-id="ff485-136">Does not use seconds.</span></span>

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span data-ttu-id="ff485-137"><span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**HORA \_ NOTIMEMARKER**</span><span class="sxs-lookup"><span data-stu-id="ff485-137"><span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**TIME\_NOTIMEMARKER**</span></span>


</dt> <dd>

<span data-ttu-id="ff485-138">No utiliza un marcador de hora.</span><span class="sxs-lookup"><span data-stu-id="ff485-138">Does not use a time marker.</span></span>

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span data-ttu-id="ff485-139"><span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**HORA \_ FORCE24HOURFORMAT**</span><span class="sxs-lookup"><span data-stu-id="ff485-139"><span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**TIME\_FORCE24HOURFORMAT**</span></span>


</dt> <dd>

<span data-ttu-id="ff485-140">Siempre usa un formato de hora de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="ff485-140">Always uses a 24-hour time format.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ff485-141">*lpTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ff485-141">*lpTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff485-142">Tipo: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _</span><span class="sxs-lookup"><span data-stu-id="ff485-142">Type: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)\** _</span></span>

<span data-ttu-id="ff485-143">Puntero a una estructura [_ *SYSTEMTIME* \*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que contiene la información de hora a la que se va a dar formato.</span><span class="sxs-lookup"><span data-stu-id="ff485-143">A pointer to a [_ *SYSTEMTIME*\*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains the time information to be formatted.</span></span> <span data-ttu-id="ff485-144">Si este puntero es **null**, la función utiliza la hora actual del sistema local.</span><span class="sxs-lookup"><span data-stu-id="ff485-144">If this pointer is **NULL**, the function uses the current local system time.</span></span>

</dd> <dt>

<span data-ttu-id="ff485-145">*pwzFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ff485-145">*pwzFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff485-146">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ff485-146">Type: **LPCWSTR**</span></span>

<span data-ttu-id="ff485-147">Puntero a un formato que se va a usar para formar la cadena de hora.</span><span class="sxs-lookup"><span data-stu-id="ff485-147">A pointer to a format to use to form the time string.</span></span> <span data-ttu-id="ff485-148">Si *pwzFormat* es **null**, la función usa el formato de hora de la configuración regional especificada.</span><span class="sxs-lookup"><span data-stu-id="ff485-148">If *pwzFormat* is **NULL**, the function uses the time format of the specified locale.</span></span> <span data-ttu-id="ff485-149">Consulte [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="ff485-149">See [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) for more details.</span></span>

</dd> <dt>

<span data-ttu-id="ff485-150">*pwzTimeStr* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ff485-150">*pwzTimeStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff485-151">Tipo: **LPWStr**</span><span class="sxs-lookup"><span data-stu-id="ff485-151">Type: **LPWSTR**</span></span>

<span data-ttu-id="ff485-152">Puntero a un búfer que recibe la cadena de hora con formato.</span><span class="sxs-lookup"><span data-stu-id="ff485-152">A pointer to a buffer that receives the formatted time string.</span></span>

</dd> <dt>

<span data-ttu-id="ff485-153">*cchTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ff485-153">*cchTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff485-154">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ff485-154">Type: **int**</span></span>

<span data-ttu-id="ff485-155">Tamaño, en caracteres, del búfer *pwzTimeStr* .</span><span class="sxs-lookup"><span data-stu-id="ff485-155">The size, in characters, of the *pwzTimeStr* buffer.</span></span> <span data-ttu-id="ff485-156">Si *cchTime* es cero, la función devuelve el número de caracteres necesarios para contener la cadena de tiempo con formato y no se utiliza el búfer al que apunta *pwzTimeStr* .</span><span class="sxs-lookup"><span data-stu-id="ff485-156">If *cchTime* is zero, the function returns the number of characters required to hold the formatted time string, and the buffer pointed to by *pwzTimeStr* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff485-157">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff485-157">Return value</span></span>

<span data-ttu-id="ff485-158">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ff485-158">Type: **int**</span></span>

<span data-ttu-id="ff485-159">Si la función se ejecuta correctamente, el valor devuelto es el número de caracteres que se escriben en el búfer al que apunta *pwzTimeStr*.</span><span class="sxs-lookup"><span data-stu-id="ff485-159">If the function succeeds, the return value is the number of characters written to the buffer pointed to by *pwzTimeStr*.</span></span> <span data-ttu-id="ff485-160">Si el parámetro *cchTime* es cero, el valor devuelto es el número de caracteres necesarios para contener la cadena de hora con formato.</span><span class="sxs-lookup"><span data-stu-id="ff485-160">If the *cchTime* parameter is zero, the return value is the number of characters required to hold the formatted time string.</span></span> <span data-ttu-id="ff485-161">El recuento incluye el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="ff485-161">The count includes the terminating null character.</span></span>

<span data-ttu-id="ff485-162">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="ff485-162">If the function fails, the return value is zero.</span></span> <span data-ttu-id="ff485-163">Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="ff485-163">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="ff485-164">**GetLastError** puede devolver uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="ff485-164">**GetLastError** may return one of the following error codes.</span></span>

<dl> <dt>

<span data-ttu-id="ff485-165">**ERROR \_ de \_ búfer insuficiente**</span><span class="sxs-lookup"><span data-stu-id="ff485-165">**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dt>

<span data-ttu-id="ff485-166">**ERROR de \_ marcas no válidas \_**</span><span class="sxs-lookup"><span data-stu-id="ff485-166">**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dt>

<span data-ttu-id="ff485-167">**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="ff485-167">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ff485-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff485-168">Remarks</span></span>

<span data-ttu-id="ff485-169">**GetTimeFormatWrapW** ofrece la posibilidad de usar cadenas Unicode en sistemas operativos anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ff485-169">**GetTimeFormatWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="ff485-170">El método preferido es usar [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) junto con la capa de Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="ff485-170">The preferred method is to use [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="ff485-171">Se debe llamar a **GetTimeFormatWrapW** directamente desde Shlwapi.dll, mediante el ordinal 310.</span><span class="sxs-lookup"><span data-stu-id="ff485-171">**GetTimeFormatWrapW** must be called directly from Shlwapi.dll, using ordinal 310.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff485-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff485-172">Requirements</span></span>



| <span data-ttu-id="ff485-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff485-173">Requirement</span></span> | <span data-ttu-id="ff485-174">Value</span><span class="sxs-lookup"><span data-stu-id="ff485-174">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff485-175">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff485-175">Minimum supported client</span></span><br/> | <span data-ttu-id="ff485-176">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ff485-176">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ff485-177">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff485-177">Minimum supported server</span></span><br/> | <span data-ttu-id="ff485-178">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff485-178">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ff485-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ff485-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff485-180"><dt>Shlwapi.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ff485-180"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff485-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff485-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff485-182">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="ff485-182">**GetTimeFormat**</span></span>](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 
