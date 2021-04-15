---
description: Compara dos cadenas de caracteres Unicode con una configuración regional especificada.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: CompareStringWrapW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 0731182f5c01ad56db722972628d2cbe39373835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984351"
---
# <a name="comparestringwrapw-function"></a><span data-ttu-id="3a740-103">CompareStringWrapW función)</span><span class="sxs-lookup"><span data-stu-id="3a740-103">CompareStringWrapW function</span></span>

<span data-ttu-id="3a740-104">\[**CompareStringWrapW** está disponible para su uso en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3a740-104">\[**CompareStringWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="3a740-105">No estará disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3a740-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="3a740-106">Debe usar [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="3a740-106">You should use [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in its place.\]</span></span>

<span data-ttu-id="3a740-107">Compara dos cadenas de caracteres Unicode con una configuración regional especificada.</span><span class="sxs-lookup"><span data-stu-id="3a740-107">Compares two Unicode character strings, using a specified locale.</span></span>

> [!Note]  
> <span data-ttu-id="3a740-108">**CompareStringWrapW** es un contenedor para la función **CompareStringW** .</span><span class="sxs-lookup"><span data-stu-id="3a740-108">**CompareStringWrapW** is a wrapper for the **CompareStringW** function.</span></span> <span data-ttu-id="3a740-109">Vea la página [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) para obtener más notas de uso.</span><span class="sxs-lookup"><span data-stu-id="3a740-109">See the [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3a740-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a740-110">Syntax</span></span>


```C++
int CompareStringWrapW(
  _In_ LCID    Locale,
  _In_ DWORD   dwCmpFlags,
  _In_ LPCWSTR lpString1,
  _In_ int     cchCount1,
  _In_ LPCWSTR lpString2,
  _In_ int     cchCount2
);
```



## <a name="parameters"></a><span data-ttu-id="3a740-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a740-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a740-112">*Configuración regional* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a740-112">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a740-113">Tipo: **LCID**</span><span class="sxs-lookup"><span data-stu-id="3a740-113">Type: **LCID**</span></span>

<span data-ttu-id="3a740-114">Identificador de configuración regional que se usa para la comparación.</span><span class="sxs-lookup"><span data-stu-id="3a740-114">A locale identifier used for the comparison.</span></span> <span data-ttu-id="3a740-115">Este parámetro puede ser uno de los siguientes identificadores de configuración regional predefinidos o un identificador de configuración regional creado por la macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) .</span><span class="sxs-lookup"><span data-stu-id="3a740-115">This parameter can be one of the following predefined locale identifiers or a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="3a740-116"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**configuración \_ predeterminada del sistema local \_**</span><span class="sxs-lookup"><span data-stu-id="3a740-116"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="3a740-117">La configuración regional predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="3a740-117">The system's default locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="3a740-118"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_valor predeterminado del usuario de configuración regional \_**</span><span class="sxs-lookup"><span data-stu-id="3a740-118"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="3a740-119">Configuración regional predeterminada del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="3a740-119">The current user's default locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3a740-120">*dwCmpFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a740-120">*dwCmpFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a740-121">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3a740-121">Type: **DWORD**</span></span>

<span data-ttu-id="3a740-122">Marcas que indican cómo la función compara las dos cadenas.</span><span class="sxs-lookup"><span data-stu-id="3a740-122">The flags that indicate how the function compares the two strings.</span></span> <span data-ttu-id="3a740-123">De forma predeterminada, no se establecen estas marcas.</span><span class="sxs-lookup"><span data-stu-id="3a740-123">By default, these flags are not set.</span></span> <span data-ttu-id="3a740-124">Establezca en cero para obtener el comportamiento predeterminado o en cualquier combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3a740-124">Set to zero to get the default behavior or to any combination of the following values.</span></span>

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span data-ttu-id="3a740-125"><span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**NORMA \_ IGNORECASE**</span><span class="sxs-lookup"><span data-stu-id="3a740-125"><span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**NORM\_IGNORECASE**</span></span>


</dt> <dd>

<span data-ttu-id="3a740-126">Omitir mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a740-126">Ignore case.</span></span>

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span data-ttu-id="3a740-127"><span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**NORMA \_ IGNOREKANATYPE**</span><span class="sxs-lookup"><span data-stu-id="3a740-127"><span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**NORM\_IGNOREKANATYPE**</span></span>


</dt> <dd>

<span data-ttu-id="3a740-128">No diferencie entre caracteres hiragana y katakana.</span><span class="sxs-lookup"><span data-stu-id="3a740-128">Do not differentiate between Hiragana and Katakana characters.</span></span> <span data-ttu-id="3a740-129">Los caracteres hiragana y katakana correspondientes se comparan como iguales.</span><span class="sxs-lookup"><span data-stu-id="3a740-129">Corresponding Hiragana and Katakana characters compare as equal.</span></span>

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span data-ttu-id="3a740-130"><span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**NORMA \_ IGNORENONSPACE**</span><span class="sxs-lookup"><span data-stu-id="3a740-130"><span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**NORM\_IGNORENONSPACE**</span></span>


</dt> <dd>

<span data-ttu-id="3a740-131">Omitir caracteres que no sean de espacio.</span><span class="sxs-lookup"><span data-stu-id="3a740-131">Ignore nonspacing characters.</span></span>

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span data-ttu-id="3a740-132"><span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**NORMA \_ IGNORESYMBOLS**</span><span class="sxs-lookup"><span data-stu-id="3a740-132"><span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**NORM\_IGNORESYMBOLS**</span></span>


</dt> <dd>

<span data-ttu-id="3a740-133">Omitir símbolos.</span><span class="sxs-lookup"><span data-stu-id="3a740-133">Ignore symbols.</span></span>

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span data-ttu-id="3a740-134"><span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**NORMA \_ IGNOREWIDTH**</span><span class="sxs-lookup"><span data-stu-id="3a740-134"><span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**NORM\_IGNOREWIDTH**</span></span>


</dt> <dd>

<span data-ttu-id="3a740-135">No diferencie entre un carácter de un solo byte y el mismo carácter que un carácter de doble byte.</span><span class="sxs-lookup"><span data-stu-id="3a740-135">Do not differentiate between a single-byte character and the same character as a double-byte character.</span></span>

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span data-ttu-id="3a740-136"><span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**ORDENAR \_ STRINGSORT**</span><span class="sxs-lookup"><span data-stu-id="3a740-136"><span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**SORT\_STRINGSORT**</span></span>


</dt> <dd>

<span data-ttu-id="3a740-137">Trate los signos de puntuación iguales que los símbolos.</span><span class="sxs-lookup"><span data-stu-id="3a740-137">Treat punctuation the same as symbols.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3a740-138">*lpString1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a740-138">*lpString1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a740-139">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="3a740-139">Type: **LPCWSTR**</span></span>

<span data-ttu-id="3a740-140">Puntero a la primera cadena Unicode que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="3a740-140">A pointer to the first Unicode string to be compared.</span></span>

</dd> <dt>

<span data-ttu-id="3a740-141">*cchCount1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a740-141">*cchCount1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a740-142">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3a740-142">Type: **int**</span></span>

<span data-ttu-id="3a740-143">Número de caracteres de la cadena a la que apunta el parámetro *lpString1* .</span><span class="sxs-lookup"><span data-stu-id="3a740-143">The number of characters in the string pointed to by the *lpString1* parameter.</span></span> <span data-ttu-id="3a740-144">El recuento no incluye el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="3a740-144">The count does not include the terminating null character.</span></span> <span data-ttu-id="3a740-145">Si este parámetro es un valor negativo, se supone que la cadena termina en NULL y la longitud se calcula automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3a740-145">If this parameter is a negative value, the string is assumed to be null-terminated and the length is calculated automatically.</span></span>

</dd> <dt>

<span data-ttu-id="3a740-146">*lpString2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a740-146">*lpString2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a740-147">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="3a740-147">Type: **LPCWSTR**</span></span>

<span data-ttu-id="3a740-148">Puntero a la segunda cadena Unicode que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="3a740-148">A pointer to the second Unicode string to be compared.</span></span>

</dd> <dt>

<span data-ttu-id="3a740-149">*cchCount2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a740-149">*cchCount2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a740-150">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3a740-150">Type: **int**</span></span>

<span data-ttu-id="3a740-151">Número de caracteres de la cadena a la que apunta el parámetro *lpString2* .</span><span class="sxs-lookup"><span data-stu-id="3a740-151">The number of characters in the string pointed to by the *lpString2* parameter.</span></span> <span data-ttu-id="3a740-152">El recuento no incluye el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="3a740-152">The count does not include the terminating null character.</span></span> <span data-ttu-id="3a740-153">Si este parámetro es un valor negativo, se supone que la cadena termina en NULL y la longitud se calcula automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3a740-153">If this parameter is a negative value, the string is assumed to be null-terminated and the length is calculated automatically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a740-154">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a740-154">Return value</span></span>

<span data-ttu-id="3a740-155">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3a740-155">Type: **int**</span></span>

<span data-ttu-id="3a740-156">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="3a740-156">If the function fails, the return value is zero.</span></span> <span data-ttu-id="3a740-157">Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="3a740-157">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="3a740-158">**GetLastError** puede devolver uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="3a740-158">**GetLastError** may return one of the following error codes.</span></span>

-   <span data-ttu-id="3a740-159">ERROR de \_ marcas no válidas \_</span><span class="sxs-lookup"><span data-stu-id="3a740-159">ERROR\_INVALID\_FLAGS</span></span>
-   <span data-ttu-id="3a740-160">ERROR \_ de \_ parámetro no válido</span><span class="sxs-lookup"><span data-stu-id="3a740-160">ERROR\_INVALID\_PARAMETER</span></span>

<span data-ttu-id="3a740-161">Si la función se ejecuta correctamente, el valor devuelto es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3a740-161">If the function succeeds, the return value is one of the following values.</span></span> 

| <span data-ttu-id="3a740-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a740-162">Requirement</span></span> | <span data-ttu-id="3a740-163">Value</span><span class="sxs-lookup"><span data-stu-id="3a740-163">Value</span></span> |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a740-164">CSTR \_ menor \_ que</span><span class="sxs-lookup"><span data-stu-id="3a740-164">CSTR\_LESS\_THAN</span></span>    | <span data-ttu-id="3a740-165">La cadena a la que apunta el parámetro *lpString1* es menos en el valor léxico que la cadena a la que apunta el parámetro *lpString2* .</span><span class="sxs-lookup"><span data-stu-id="3a740-165">The string pointed to by the *lpString1* parameter is less in lexical value than the string pointed to by the *lpString2* parameter.</span></span> |
| <span data-ttu-id="3a740-166">CSTR \_ igual</span><span class="sxs-lookup"><span data-stu-id="3a740-166">CSTR\_EQUAL</span></span>         | <span data-ttu-id="3a740-167">La cadena a la que apunta *lpString1* tiene el mismo valor léxico que la cadena a la que apunta *lpString2*.</span><span class="sxs-lookup"><span data-stu-id="3a740-167">The string pointed to by *lpString1* is equal in lexical value to the string pointed to by *lpString2*.</span></span>                              |
| <span data-ttu-id="3a740-168">CSTR \_ mayor \_ que</span><span class="sxs-lookup"><span data-stu-id="3a740-168">CSTR\_GREATER\_THAN</span></span> | <span data-ttu-id="3a740-169">La cadena a la que apunta *lpString1* es mayor en el valor léxico que la cadena a la que apunta *lpString2*</span><span class="sxs-lookup"><span data-stu-id="3a740-169">The string pointed to by *lpString1* is greater in lexical value than the string pointed to by *lpString2*</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="3a740-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a740-170">Remarks</span></span>

<span data-ttu-id="3a740-171">**Advertencia de seguridad:** El uso incorrecto de esta función puede poner en peligro la seguridad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3a740-171">**Security Warning:** Using this function incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="3a740-172">Las cadenas que no se comparan correctamente pueden generar entradas no válidas.</span><span class="sxs-lookup"><span data-stu-id="3a740-172">Strings that are not compared correctly can produce invalid input.</span></span> <span data-ttu-id="3a740-173">Pruebe las cadenas para asegurarse de que son válidas antes de utilizarlas y proporcionar controladores de errores.</span><span class="sxs-lookup"><span data-stu-id="3a740-173">Test strings to make sure they are valid before using them and provide error handlers.</span></span> <span data-ttu-id="3a740-174">Para obtener más información, vea [consideraciones de seguridad: características internacionales](../intl/security-considerations--international-features.md)</span><span class="sxs-lookup"><span data-stu-id="3a740-174">For more information, see [Security Considerations: International Features](../intl/security-considerations--international-features.md)</span></span>

<span data-ttu-id="3a740-175">El método preferido es usar [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) junto con la capa de Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="3a740-175">The preferred method is to use [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="3a740-176">Se debe llamar a **CompareStringWrapW** directamente desde Shlwapi.dll, mediante el ordinal 45.</span><span class="sxs-lookup"><span data-stu-id="3a740-176">**CompareStringWrapW** must be called directly from Shlwapi.dll, using ordinal 45.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a740-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a740-177">Requirements</span></span>



| <span data-ttu-id="3a740-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a740-178">Requirement</span></span> | <span data-ttu-id="3a740-179">Value</span><span class="sxs-lookup"><span data-stu-id="3a740-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a740-180">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a740-180">Minimum supported client</span></span><br/> | <span data-ttu-id="3a740-181">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3a740-181">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a740-182">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a740-182">Minimum supported server</span></span><br/> | <span data-ttu-id="3a740-183">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a740-183">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3a740-184">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a740-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a740-185"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="3a740-185"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="3a740-186">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3a740-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a740-187"><dt>Shlwapi.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3a740-187"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a740-188">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a740-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a740-189">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="3a740-189">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
