---
description: Desusado.
ms.assetid: eb2622bc-a98d-42bd-ab59-7a849000d79d
title: GetCalendarDateFormatEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarDateFormatEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: b0130bf62c742d0565b1c98c138ac8c71ddf7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687619"
---
# <a name="getcalendardateformatex-function"></a><span data-ttu-id="260dc-103">GetCalendarDateFormatEx función)</span><span class="sxs-lookup"><span data-stu-id="260dc-103">GetCalendarDateFormatEx function</span></span>

<span data-ttu-id="260dc-104">En desuso.</span><span class="sxs-lookup"><span data-stu-id="260dc-104">Deprecated.</span></span> <span data-ttu-id="260dc-105">Recupera una cadena de fecha con el formato correcto para la configuración regional especificada utilizando la fecha y el calendario especificados.</span><span class="sxs-lookup"><span data-stu-id="260dc-105">Retrieves a properly formatted date string for the specified locale using the specified date and calendar.</span></span> <span data-ttu-id="260dc-106">El usuario puede especificar el formato de fecha corta, el formato de fecha larga, el formato de mes o un modelo de formato personalizado.</span><span class="sxs-lookup"><span data-stu-id="260dc-106">The user can specify the short date format, the long date format, the year month format, or a custom format pattern.</span></span>

> [!Note]  
> <span data-ttu-id="260dc-107">Esta función puede recuperar datos que cambian entre versiones, por ejemplo, debido a una configuración regional personalizada.</span><span class="sxs-lookup"><span data-stu-id="260dc-107">This function can retrieve data that changes between releases, for example, due to a custom locale.</span></span> <span data-ttu-id="260dc-108">Si la aplicación debe conservar o transmitir datos, consulte [uso de datos de configuración regional persistentes](using-persistent-locale-data.md).</span><span class="sxs-lookup"><span data-stu-id="260dc-108">If your application must persist or transmit data, see [Using Persistent Locale Data](using-persistent-locale-data.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="260dc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="260dc-109">Syntax</span></span>


```C++
BOOL GetCalendarDateFormatEx(
  _In_        LPCWSTR       lpszLocale,
  _In_        DWORD         dwFlags,
  _In_  const LPCALDATETIME lpCalDateTime,
  _In_        LPCWSTR       lpFormat,
  _Out_       LPWSTR        lpDateStr,
  _In_        int           cchDate
);
```



## <a name="parameters"></a><span data-ttu-id="260dc-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="260dc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="260dc-111">*lpszLocale* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="260dc-111">*lpszLocale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="260dc-112">Puntero a un nombre de configuración regional o a uno de los siguientes valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="260dc-112">Pointer to a locale name, or one of the following predefined values.</span></span>

-   [<span data-ttu-id="260dc-113">nombre de configuración regional \_ \_ invariable</span><span class="sxs-lookup"><span data-stu-id="260dc-113">LOCALE\_NAME\_INVARIANT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="260dc-114">nombre de configuración regional \_ \_ predeterminado del sistema \_</span><span class="sxs-lookup"><span data-stu-id="260dc-114">LOCALE\_NAME\_SYSTEM\_DEFAULT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="260dc-115">nombre de configuración regional \_ \_ predeterminado del usuario \_</span><span class="sxs-lookup"><span data-stu-id="260dc-115">LOCALE\_NAME\_USER\_DEFAULT</span></span>](locale-name-constants.md)

</dd> <dt>

<span data-ttu-id="260dc-116">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="260dc-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="260dc-117">Marcas que especifican las opciones de formato de fecha.</span><span class="sxs-lookup"><span data-stu-id="260dc-117">Flags specifying date format options.</span></span> <span data-ttu-id="260dc-118">Si *lpFormat* no está establecido en **null**, este parámetro debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="260dc-118">If *lpFormat* is not set to **NULL**, this parameter must be set to 0.</span></span> <span data-ttu-id="260dc-119">Si *lpFormat* se establece en **null**, la aplicación puede especificar una combinación de los siguientes valores y [ \_ NOUSEROVERRIDE de configuración regional](locale-nouseroverride.md).</span><span class="sxs-lookup"><span data-stu-id="260dc-119">If *lpFormat* is set to **NULL**, the application can specify a combination of the following values and [LOCALE\_NOUSEROVERRIDE](locale-nouseroverride.md).</span></span>



| <span data-ttu-id="260dc-120">Value</span><span class="sxs-lookup"><span data-stu-id="260dc-120">Value</span></span>                                                                                                                                                               | <span data-ttu-id="260dc-121">Significado</span><span class="sxs-lookup"><span data-stu-id="260dc-121">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <span data-ttu-id="260dc-122"><dt>**FECHA \_ fechacorta**</dt></span><span class="sxs-lookup"><span data-stu-id="260dc-122"><dt>**DATE\_SHORTDATE**</dt></span></span> </dl>    | <span data-ttu-id="260dc-123">Use el formato de fecha corta.</span><span class="sxs-lookup"><span data-stu-id="260dc-123">Use the short date format.</span></span> <span data-ttu-id="260dc-124">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="260dc-124">This is the default.</span></span> <span data-ttu-id="260dc-125">Este valor no se puede usar con la fecha \_ LONGDATE o \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="260dc-125">This value cannot be used with DATE\_LONGDATE or DATE\_YEARMONTH.</span></span> <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <span data-ttu-id="260dc-126"><dt>**FECHA \_ LONGDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="260dc-126"><dt>**DATE\_LONGDATE**</dt></span></span> </dl>       | <span data-ttu-id="260dc-127">Use el formato de fecha larga.</span><span class="sxs-lookup"><span data-stu-id="260dc-127">Use the long date format.</span></span> <span data-ttu-id="260dc-128">Este valor no se puede usar con la fecha \_ fechacorta o \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="260dc-128">This value cannot be used with DATE\_SHORTDATE or DATE\_YEARMONTH.</span></span> <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <span data-ttu-id="260dc-129"><dt>**FECHA \_ YEARMONTH**</dt></span><span class="sxs-lookup"><span data-stu-id="260dc-129"><dt>**DATE\_YEARMONTH**</dt></span></span> </dl>    | <span data-ttu-id="260dc-130">Use el formato de año/mes.</span><span class="sxs-lookup"><span data-stu-id="260dc-130">Use the year/month format.</span></span> <span data-ttu-id="260dc-131">Este valor no se puede usar con la fecha \_ fechacorta o \_ LONGDATE.</span><span class="sxs-lookup"><span data-stu-id="260dc-131">This value cannot be used with DATE\_SHORTDATE or DATE\_LONGDATE.</span></span><br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <span data-ttu-id="260dc-132"><dt>**FECHA \_ LTRREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="260dc-132"><dt>**DATE\_LTRREADING**</dt></span></span> </dl> | <span data-ttu-id="260dc-133">Agregue marcas para el diseño de lectura de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="260dc-133">Add marks for left-to-right reading layout.</span></span> <span data-ttu-id="260dc-134">Este valor no se puede usar con la fecha \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="260dc-134">This value cannot be used with DATE\_RTLREADING.</span></span><br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <span data-ttu-id="260dc-135"><dt>**FECHA \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="260dc-135"><dt>**DATE\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="260dc-136">Agregue marcas para el diseño de lectura de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="260dc-136">Add marks for right-to-left reading layout.</span></span> <span data-ttu-id="260dc-137">Este valor no se puede usar con la fecha \_ LTRREADING</span><span class="sxs-lookup"><span data-stu-id="260dc-137">This value cannot be used with DATE\_LTRREADING</span></span><br/>                        |



 

</dd> <dt>

<span data-ttu-id="260dc-138">*lpCalDateTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="260dc-138">*lpCalDateTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="260dc-139">Puntero a una estructura [**CALDATETIME**](caldatetime.md) que contiene la información de fecha y de calendario a la que se va a dar formato.</span><span class="sxs-lookup"><span data-stu-id="260dc-139">Pointer to a [**CALDATETIME**](caldatetime.md) structure that contains the date and calendar information to format.</span></span>

</dd> <dt>

<span data-ttu-id="260dc-140">*lpFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="260dc-140">*lpFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="260dc-141">Puntero a una cadena de imagen de formato que se usa para formar la cadena de fecha.</span><span class="sxs-lookup"><span data-stu-id="260dc-141">Pointer to a format picture string that is used to form the date string.</span></span> <span data-ttu-id="260dc-142">Los valores posibles de la cadena de formato de imagen se definen en [imágenes con formato de día, mes, año y era](day--month--year--and-era-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="260dc-142">Possible values for the format picture string are defined in [Day, Month, Year, and Era Format Pictures](day--month--year--and-era-format-pictures.md).</span></span>

<span data-ttu-id="260dc-143">La cadena de formato de imagen debe terminar en NULL.</span><span class="sxs-lookup"><span data-stu-id="260dc-143">The format picture string must be null-terminated.</span></span> <span data-ttu-id="260dc-144">La función usa la configuración regional solo para la información que no se especifica en la cadena de formato de imagen, por ejemplo, los nombres de día y mes de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="260dc-144">The function uses the locale only for information not specified in the format picture string, for example, the day and month names for the locale.</span></span> <span data-ttu-id="260dc-145">La aplicación establece este parámetro en **null** si la función va a usar el formato de fecha de la configuración regional especificada.</span><span class="sxs-lookup"><span data-stu-id="260dc-145">The application sets this parameter to **NULL** if the function is to use the date format of the specified locale.</span></span>

</dd> <dt>

<span data-ttu-id="260dc-146">*lpDateStr* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="260dc-146">*lpDateStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="260dc-147">Puntero a un búfer en el que esta función recibe la cadena de fecha con formato.</span><span class="sxs-lookup"><span data-stu-id="260dc-147">Pointer to a buffer in which this function receives the formatted date string.</span></span>

</dd> <dt>

<span data-ttu-id="260dc-148">*cchDate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="260dc-148">*cchDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="260dc-149">Tamaño, en caracteres, del búfer *lpDateStr* .</span><span class="sxs-lookup"><span data-stu-id="260dc-149">Size, in characters, of the *lpDateStr* buffer.</span></span> <span data-ttu-id="260dc-150">Como alternativa, la aplicación puede establecer este parámetro en 0.</span><span class="sxs-lookup"><span data-stu-id="260dc-150">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="260dc-151">En este caso, la función devuelve el número de caracteres necesarios para contener la cadena de fecha con formato y no se usa el parámetro *lpDateStr* .</span><span class="sxs-lookup"><span data-stu-id="260dc-151">In this case, the function returns the number of characters required to hold the formatted date string, and the *lpDateStr* parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="260dc-152">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="260dc-152">Return value</span></span>

<span data-ttu-id="260dc-153">Devuelve el número de caracteres que se escriben en el búfer de *lpDateStr* si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="260dc-153">Returns the number of characters written to the *lpDateStr* buffer if successful.</span></span> <span data-ttu-id="260dc-154">Si el parámetro *cchDate* se establece en 0, la función devuelve el número de caracteres necesarios para contener la cadena de fecha con formato, incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="260dc-154">If the *cchDate* parameter is set to 0, the function returns the number of characters required to hold the formatted date string, including the terminating null character.</span></span>

<span data-ttu-id="260dc-155">Esta función devuelve 0 si no se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="260dc-155">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="260dc-156">Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="260dc-156">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="260dc-157">\_fecha \_ de error fuera \_ del \_ intervalo.</span><span class="sxs-lookup"><span data-stu-id="260dc-157">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="260dc-158">La fecha especificada estaba fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="260dc-158">The specified date was out of range.</span></span>
-   <span data-ttu-id="260dc-159">ERROR \_ de \_ búfer insuficiente.</span><span class="sxs-lookup"><span data-stu-id="260dc-159">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="260dc-160">Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **null**.</span><span class="sxs-lookup"><span data-stu-id="260dc-160">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="260dc-161">ERROR en \_ marcas no válidas \_ .</span><span class="sxs-lookup"><span data-stu-id="260dc-161">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="260dc-162">Los valores proporcionados para marcas no eran válidos.</span><span class="sxs-lookup"><span data-stu-id="260dc-162">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="260dc-163">ERROR \_ de \_ parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="260dc-163">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="260dc-164">Cualquiera de los valores de parámetro no era válido.</span><span class="sxs-lookup"><span data-stu-id="260dc-164">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="260dc-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="260dc-165">Remarks</span></span>

<span data-ttu-id="260dc-166">La primera fecha admitida por esta función es el 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="260dc-166">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="260dc-167">Esta función no tiene asociado un archivo de encabezado o archivo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="260dc-167">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="260dc-168">La aplicación puede llamar a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre de DLL (Kernel32.dll) para obtener un identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="260dc-168">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="260dc-169">Después, puede llamar a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el nombre de esta función para obtener la dirección de la función.</span><span class="sxs-lookup"><span data-stu-id="260dc-169">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="260dc-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="260dc-170">Requirements</span></span>



| <span data-ttu-id="260dc-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="260dc-171">Requirement</span></span> | <span data-ttu-id="260dc-172">Value</span><span class="sxs-lookup"><span data-stu-id="260dc-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="260dc-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="260dc-173">Minimum supported client</span></span><br/> | <span data-ttu-id="260dc-174">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="260dc-174">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="260dc-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="260dc-175">Minimum supported server</span></span><br/> | <span data-ttu-id="260dc-176">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="260dc-176">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="260dc-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="260dc-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="260dc-178"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="260dc-178"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="260dc-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="260dc-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="260dc-180">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="260dc-180">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="260dc-181">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="260dc-181">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="260dc-182">Imágenes con formato de día, mes, año y era</span><span class="sxs-lookup"><span data-stu-id="260dc-182">Day, Month, Year, and Era Format Pictures</span></span>](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[<span data-ttu-id="260dc-183">NLS: ejemplo de API basadas en nombre</span><span class="sxs-lookup"><span data-stu-id="260dc-183">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> <dt>

[<span data-ttu-id="260dc-184">**EnumDateFormatsExEx**</span><span class="sxs-lookup"><span data-stu-id="260dc-184">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[<span data-ttu-id="260dc-185">**GetDateFormat**</span><span class="sxs-lookup"><span data-stu-id="260dc-185">**GetDateFormat**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[<span data-ttu-id="260dc-186">**GetDateFormatEx**</span><span class="sxs-lookup"><span data-stu-id="260dc-186">**GetDateFormatEx**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[<span data-ttu-id="260dc-187">**CALDATETIME**</span><span class="sxs-lookup"><span data-stu-id="260dc-187">**CALDATETIME**</span></span>](caldatetime.md)
</dt> </dl>

 

 
