---
description: Da formato a una fecha como una cadena de fecha para una configuración regional especificada.
ms.assetid: e45f6d1c-2890-44f6-8406-022c99c59e02
title: GetDateFormatWrapW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDateFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: c9c369584fd15a27d5e684452b2277104b5b1da4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276754"
---
# <a name="getdateformatwrapw-function"></a><span data-ttu-id="ed199-103">GetDateFormatWrapW función)</span><span class="sxs-lookup"><span data-stu-id="ed199-103">GetDateFormatWrapW function</span></span>

<span data-ttu-id="ed199-104">\[**GetDateFormatWrapW** está disponible para su uso en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ed199-104">\[**GetDateFormatWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="ed199-105">No estará disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ed199-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="ed199-106">Debe usar [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="ed199-106">You should use [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in its place.\]</span></span>

<span data-ttu-id="ed199-107">Da formato a una fecha como una cadena de fecha para una configuración regional especificada.</span><span class="sxs-lookup"><span data-stu-id="ed199-107">Formats a date as a date string for a specified locale.</span></span> <span data-ttu-id="ed199-108">La función da formato a una fecha especificada o a la fecha del sistema local.</span><span class="sxs-lookup"><span data-stu-id="ed199-108">The function formats either a specified date or the local system date.</span></span>

> [!Note]  
> <span data-ttu-id="ed199-109">**GetDateFormatWrapW** es un contenedor para la función **GetDateFormatW** .</span><span class="sxs-lookup"><span data-stu-id="ed199-109">**GetDateFormatWrapW** is a wrapper for the **GetDateFormatW** function.</span></span> <span data-ttu-id="ed199-110">Vea la página [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) para obtener más notas de uso.</span><span class="sxs-lookup"><span data-stu-id="ed199-110">See the [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ed199-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed199-111">Syntax</span></span>


```C++
int GetDateFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpDate,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzDateStr,
  _In_        int        cchDate
);
```



## <a name="parameters"></a><span data-ttu-id="ed199-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed199-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed199-113">*Configuración regional* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed199-113">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed199-114">Tipo: **LCID**</span><span class="sxs-lookup"><span data-stu-id="ed199-114">Type: **LCID**</span></span>

<span data-ttu-id="ed199-115">La configuración regional para la que se va a dar formato a la cadena de fecha.</span><span class="sxs-lookup"><span data-stu-id="ed199-115">The locale for which the date string is to be formatted.</span></span> <span data-ttu-id="ed199-116">Si *pwzFormat* es **null**, la función da formato a la cadena de acuerdo con el formato de fecha de esta configuración regional.</span><span class="sxs-lookup"><span data-stu-id="ed199-116">If *pwzFormat* is **NULL**, the function formats the string according to the date format for this locale.</span></span> <span data-ttu-id="ed199-117">Si *pwzFormat* no es **null**, la función usa la configuración regional solo para la información que no se especifica en la cadena de formato de imagen (por ejemplo, los nombres de día y mes de la configuración regional).</span><span class="sxs-lookup"><span data-stu-id="ed199-117">If *pwzFormat* is not **NULL**, the function uses the locale only for information not specified in the format picture string (for example, the locale's day and month names).</span></span>

<span data-ttu-id="ed199-118">Este parámetro puede ser un identificador de configuración regional creado por la macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) , o uno de los siguientes valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="ed199-118">This parameter can be a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro, or one of the following predefined values.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="ed199-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**configuración \_ predeterminada del sistema local \_**</span><span class="sxs-lookup"><span data-stu-id="ed199-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="ed199-120">Configuración regional predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="ed199-120">Default system locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="ed199-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_valor predeterminado del usuario de configuración regional \_**</span><span class="sxs-lookup"><span data-stu-id="ed199-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="ed199-122">Configuración regional predeterminada del usuario.</span><span class="sxs-lookup"><span data-stu-id="ed199-122">Default user locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ed199-123">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed199-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed199-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ed199-124">Type: **DWORD**</span></span>

<span data-ttu-id="ed199-125">Especifica varias opciones de función.</span><span class="sxs-lookup"><span data-stu-id="ed199-125">Specifies various function options.</span></span> <span data-ttu-id="ed199-126">Si *pwzFormat* no es **null**, este parámetro debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ed199-126">If *pwzFormat* is not **NULL**, this parameter must be zero.</span></span> <span data-ttu-id="ed199-127">Si *pwzFormat* es **null**, puede especificar una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ed199-127">If *pwzFormat* is **NULL**, you can specify a combination of the following values.</span></span> <span data-ttu-id="ed199-128">Si no especifica la fecha \_ YEARMONTH, la fecha \_ fechacorta o la fecha \_ LONGDATE, y *pwzFormat* es **null**, se \_ usará la fecha fechacorta como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ed199-128">If you do not specify either DATE\_YEARMONTH, DATE\_SHORTDATE, or DATE\_LONGDATE, and *pwzFormat* is **NULL**, then DATE\_SHORTDATE is used as the default.</span></span>

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span data-ttu-id="ed199-129"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**configuración regional \_ NOUSEROVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="ed199-129"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE\_NOUSEROVERRIDE**</span></span>


</dt> <dd>

<span data-ttu-id="ed199-130">Si se establece, la función da formato a la cadena con el formato de fecha predeterminado del sistema para la configuración regional especificada.</span><span class="sxs-lookup"><span data-stu-id="ed199-130">If set, the function formats the string using the system default date format for the specified locale.</span></span> <span data-ttu-id="ed199-131">Si no se establece, la función da formato a la cadena mediante cualquier invalidación de usuario en el formato de fecha predeterminado de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="ed199-131">If not set, the function formats the string using any user overrides to the locale's default date format.</span></span>

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span data-ttu-id="ed199-132"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**configuración regional \_ use \_ CP \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="ed199-132"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALE\_USE\_CP\_ACP**</span></span>


</dt> <dd>

<span data-ttu-id="ed199-133">Usa la página de códigos ANSI del sistema para la traducción de cadenas en lugar de la página de códigos de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="ed199-133">Uses the system ANSI code page for string translation instead of the locale's code page.</span></span>

</dd> <dt>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>

<span data-ttu-id="ed199-134"><span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**FECHA \_ fechacorta**</span><span class="sxs-lookup"><span data-stu-id="ed199-134"><span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**DATE\_SHORTDATE**</span></span>


</dt> <dd>

<span data-ttu-id="ed199-135">Utiliza el formato de fecha corta.</span><span class="sxs-lookup"><span data-stu-id="ed199-135">Uses the short date format.</span></span> <span data-ttu-id="ed199-136">Este valor no se puede usar con la fecha \_ LONGDATE o \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="ed199-136">This value cannot be used with DATE\_LONGDATE or DATE\_YEARMONTH.</span></span>

</dd> <dt>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>

<span data-ttu-id="ed199-137"><span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**FECHA \_ LONGDATE**</span><span class="sxs-lookup"><span data-stu-id="ed199-137"><span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**DATE\_LONGDATE**</span></span>


</dt> <dd>

<span data-ttu-id="ed199-138">Utiliza el formato de fecha larga.</span><span class="sxs-lookup"><span data-stu-id="ed199-138">Uses the long date format.</span></span> <span data-ttu-id="ed199-139">Este valor no se puede usar con la fecha \_ fechacorta o \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="ed199-139">This value cannot be used with DATE\_SHORTDATE or DATE\_YEARMONTH.</span></span>

</dd> <dt>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>

<span data-ttu-id="ed199-140"><span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**FECHA \_ YEARMONTH**</span><span class="sxs-lookup"><span data-stu-id="ed199-140"><span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**DATE\_YEARMONTH**</span></span>


</dt> <dd>

<span data-ttu-id="ed199-141">Usa el formato de año/mes.</span><span class="sxs-lookup"><span data-stu-id="ed199-141">Uses the year/month format.</span></span> <span data-ttu-id="ed199-142">Este valor no se puede usar con la fecha \_ fechacorta o \_ LONGDATE.</span><span class="sxs-lookup"><span data-stu-id="ed199-142">This value cannot be used with DATE\_SHORTDATE or DATE\_LONGDATE.</span></span>

</dd> <dt>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>

<span data-ttu-id="ed199-143"><span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**FECHA \_ usar \_ \_ calendario Alt**</span><span class="sxs-lookup"><span data-stu-id="ed199-143"><span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**DATE\_USE\_ALT\_CALENDAR**</span></span>


</dt> <dd>

<span data-ttu-id="ed199-144">Utiliza el calendario alternativo, si existe, para dar formato a la cadena de fecha.</span><span class="sxs-lookup"><span data-stu-id="ed199-144">Uses the alternate calendar, if one exists, to format the date string.</span></span> <span data-ttu-id="ed199-145">Si se establece esta marca, la función usa el formato predeterminado para ese calendario alternativo, en lugar de utilizar las invalidaciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="ed199-145">If this flag is set, the function uses the default format for that alternate calendar, rather than using any user overrides.</span></span> <span data-ttu-id="ed199-146">Las invalidaciones de usuario solo se utilizarán en caso de que no haya ningún formato predeterminado para el calendario alternativo especificado.</span><span class="sxs-lookup"><span data-stu-id="ed199-146">The user overrides will be used only in the event that there is no default format for the specified alternate calendar.</span></span>

</dd> <dt>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>

<span data-ttu-id="ed199-147"><span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**FECHA \_ LTRREADING**</span><span class="sxs-lookup"><span data-stu-id="ed199-147"><span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**DATE\_LTRREADING**</span></span>


</dt> <dd>

<span data-ttu-id="ed199-148">Agrega marcas para el diseño de lectura de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="ed199-148">Adds marks for left-to-right reading layout.</span></span> <span data-ttu-id="ed199-149">Este valor no se puede usar con la fecha \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="ed199-149">This value cannot be used with DATE\_RTLREADING.</span></span>

</dd> <dt>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>

<span data-ttu-id="ed199-150"><span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**FECHA \_ RTLREADING**</span><span class="sxs-lookup"><span data-stu-id="ed199-150"><span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**DATE\_RTLREADING**</span></span>


</dt> <dd>

<span data-ttu-id="ed199-151">Agrega marcas para el diseño de lectura de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="ed199-151">Adds marks for right-to-left reading layout.</span></span> <span data-ttu-id="ed199-152">Este valor no se puede usar con la fecha \_ LTRREADING.</span><span class="sxs-lookup"><span data-stu-id="ed199-152">This value cannot be used with DATE\_LTRREADING.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ed199-153">*lpDate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed199-153">*lpDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed199-154">Tipo: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _</span><span class="sxs-lookup"><span data-stu-id="ed199-154">Type: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)\** _</span></span>

<span data-ttu-id="ed199-155">Puntero a una estructura [_ *SYSTEMTIME* \*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que contiene la información de fecha a la que se va a dar formato.</span><span class="sxs-lookup"><span data-stu-id="ed199-155">A pointer to a [_ *SYSTEMTIME*\*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date information to be formatted.</span></span> <span data-ttu-id="ed199-156">Si este puntero es **null**, la función usa la fecha actual del sistema local.</span><span class="sxs-lookup"><span data-stu-id="ed199-156">If this pointer is **NULL**, the function uses the current local system date.</span></span>

</dd> <dt>

<span data-ttu-id="ed199-157">*pwzFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed199-157">*pwzFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed199-158">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ed199-158">Type: **LPCWSTR**</span></span>

<span data-ttu-id="ed199-159">Puntero a una imagen de formato que se va a usar para formar la cadena de fecha.</span><span class="sxs-lookup"><span data-stu-id="ed199-159">A pointer to a format picture to use to form the date string.</span></span> <span data-ttu-id="ed199-160">Si *pwzFormat* es **null**, la función usa el formato de fecha de la configuración regional especificada.</span><span class="sxs-lookup"><span data-stu-id="ed199-160">If *pwzFormat* is **NULL**, the function uses the date format of the specified locale.</span></span> <span data-ttu-id="ed199-161">Consulte [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="ed199-161">See [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) for more details.</span></span>

</dd> <dt>

<span data-ttu-id="ed199-162">*pwzDateStr* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ed199-162">*pwzDateStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed199-163">Tipo: **LPWStr**</span><span class="sxs-lookup"><span data-stu-id="ed199-163">Type: **LPWSTR**</span></span>

<span data-ttu-id="ed199-164">Un puntero a un búfer que recibe la cadena de fecha con formato.</span><span class="sxs-lookup"><span data-stu-id="ed199-164">A pointer to a buffer that receives the formatted date string.</span></span>

</dd> <dt>

<span data-ttu-id="ed199-165">*cchDate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed199-165">*cchDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed199-166">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ed199-166">Type: **int**</span></span>

<span data-ttu-id="ed199-167">Especifica el tamaño, en caracteres, del búfer de *pwzDateStr* .</span><span class="sxs-lookup"><span data-stu-id="ed199-167">Specifies the size, in characters, of the *pwzDateStr* buffer.</span></span> <span data-ttu-id="ed199-168">Si *cchDate* es cero, la función devuelve el número de caracteres necesarios para contener la cadena de fecha con formato y no se utiliza el búfer al que apunta *pwzDateStr* .</span><span class="sxs-lookup"><span data-stu-id="ed199-168">If *cchDate* is zero, the function returns the number of characters required to hold the formatted date string, and the buffer pointed to by *pwzDateStr* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed199-169">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed199-169">Return value</span></span>

<span data-ttu-id="ed199-170">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ed199-170">Type: **int**</span></span>

<span data-ttu-id="ed199-171">Si la función se ejecuta correctamente, el valor devuelto es el número de caracteres que se escriben en el búfer al que apunta *pwzDateStr*.</span><span class="sxs-lookup"><span data-stu-id="ed199-171">If the function succeeds, the return value is the number of characters written to the buffer pointed to by *pwzDateStr*.</span></span> <span data-ttu-id="ed199-172">Si el parámetro *cchDate* es cero, el valor devuelto es el número de caracteres necesarios para contener la cadena de fecha con formato.</span><span class="sxs-lookup"><span data-stu-id="ed199-172">If the *cchDate* parameter is zero, the return value is the number of characters required to hold the formatted date string.</span></span> <span data-ttu-id="ed199-173">El recuento incluye el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="ed199-173">The count includes the terminating null character.</span></span>

<span data-ttu-id="ed199-174">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="ed199-174">If the function fails, the return value is zero.</span></span> <span data-ttu-id="ed199-175">Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="ed199-175">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="ed199-176">**GetLastError** puede devolver uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="ed199-176">**GetLastError** may return one of the following error codes.</span></span>

<dl> <dt>

<span data-ttu-id="ed199-177">**ERROR \_ de \_ búfer insuficiente**</span><span class="sxs-lookup"><span data-stu-id="ed199-177">**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dt>

<span data-ttu-id="ed199-178">**ERROR de \_ marcas no válidas \_**</span><span class="sxs-lookup"><span data-stu-id="ed199-178">**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dt>

<span data-ttu-id="ed199-179">**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="ed199-179">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ed199-180">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed199-180">Remarks</span></span>

<span data-ttu-id="ed199-181">**GetDateFormatWrapW** ofrece la posibilidad de usar cadenas Unicode en sistemas operativos anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ed199-181">**GetDateFormatWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="ed199-182">El método preferido es usar [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) junto con la capa de Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="ed199-182">The preferred method is to use [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="ed199-183">Se debe llamar a **GetDateFormatWrapW** directamente desde Shlwapi.dll, mediante el ordinal 311.</span><span class="sxs-lookup"><span data-stu-id="ed199-183">**GetDateFormatWrapW** must be called directly from Shlwapi.dll, using ordinal 311.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed199-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed199-184">Requirements</span></span>



| <span data-ttu-id="ed199-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed199-185">Requirement</span></span> | <span data-ttu-id="ed199-186">Value</span><span class="sxs-lookup"><span data-stu-id="ed199-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed199-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed199-187">Minimum supported client</span></span><br/> | <span data-ttu-id="ed199-188">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ed199-188">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed199-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed199-189">Minimum supported server</span></span><br/> | <span data-ttu-id="ed199-190">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed199-190">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ed199-191">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed199-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed199-192"><dt>Shlwapi.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ed199-192"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed199-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed199-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed199-194">**GetDateFormat**</span><span class="sxs-lookup"><span data-stu-id="ed199-194">**GetDateFormat**</span></span>](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> </dl>

 

 
