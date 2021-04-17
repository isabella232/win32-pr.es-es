---
description: Compara dos listas de scripts enumeradas.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: Función DownlevelVerifyScripts (Idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelVerifyScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 62e029576d53109e3c57faf4ec913472f8aea65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668413"
---
# <a name="downlevelverifyscripts-function"></a><span data-ttu-id="7354c-103">DownlevelVerifyScripts función)</span><span class="sxs-lookup"><span data-stu-id="7354c-103">DownlevelVerifyScripts function</span></span>

<span data-ttu-id="7354c-104">Compara dos listas de scripts enumeradas.</span><span class="sxs-lookup"><span data-stu-id="7354c-104">Compares two enumerated lists of scripts.</span></span>

> [!Note]  
> <span data-ttu-id="7354c-105">Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7354c-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="7354c-106">Su uso requiere el paquete de descarga.</span><span class="sxs-lookup"><span data-stu-id="7354c-106">Its use requires the download package.</span></span> <span data-ttu-id="7354c-107">Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores deben llamar a [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).</span><span class="sxs-lookup"><span data-stu-id="7354c-107">Applications that only run on Windows Vista and later should call [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7354c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7354c-108">Syntax</span></span>


```C++
BOOL DownlevelVerifyScripts(
  _In_ DWORD   dwFlags,
  _In_ LPCWSTR lpLocaleScripts,
  _In_ int     cchLocaleScripts,
  _In_ LPCWSTR lpTestScripts,
  _In_ int     cchTestScripts
);
```



## <a name="parameters"></a><span data-ttu-id="7354c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7354c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7354c-110">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7354c-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7354c-111">Marcas que especifican las opciones de comprobación de script.</span><span class="sxs-lookup"><span data-stu-id="7354c-111">Flags specifying script verification options.</span></span>



| <span data-ttu-id="7354c-112">Value</span><span class="sxs-lookup"><span data-stu-id="7354c-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="7354c-113">Significado</span><span class="sxs-lookup"><span data-stu-id="7354c-113">Meaning</span></span>                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <span data-ttu-id="7354c-114"><dt>**VS \_ permitir \_ latín**</dt></span><span class="sxs-lookup"><span data-stu-id="7354c-114"><dt>**VS\_ALLOW\_LATIN**</dt></span></span> </dl> | <span data-ttu-id="7354c-115">Permitir "latn" (alfabeto latino) en la lista de pruebas, aunque no esté en la lista de configuraciones regionales.</span><span class="sxs-lookup"><span data-stu-id="7354c-115">Allow "Latn" (Latin script) in the test list, even if it is not in the locale list.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7354c-116">*lpLocaleScripts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7354c-116">*lpLocaleScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7354c-117">Puntero a la lista de configuraciones regionales, la lista enumerada de scripts para una configuración regional determinada.</span><span class="sxs-lookup"><span data-stu-id="7354c-117">Pointer to the locale list, the enumerated list of scripts for a given locale.</span></span> <span data-ttu-id="7354c-118">Esta lista se rellena normalmente mediante una llamada a [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).</span><span class="sxs-lookup"><span data-stu-id="7354c-118">This list is typically populated by calling [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).</span></span>

</dd> <dt>

<span data-ttu-id="7354c-119">*cchLocaleScripts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7354c-119">*cchLocaleScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7354c-120">Tamaño, en caracteres, de la cadena indicada por *lpLocaleScripts*.</span><span class="sxs-lookup"><span data-stu-id="7354c-120">Size, in characters, of the string indicated by *lpLocaleScripts*.</span></span> <span data-ttu-id="7354c-121">La aplicación establece este parámetro en-1 si la cadena termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="7354c-121">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="7354c-122">Si este parámetro se establece en 0, se produce un error en la función.</span><span class="sxs-lookup"><span data-stu-id="7354c-122">If this parameter is set to 0, the function fails.</span></span>

</dd> <dt>

<span data-ttu-id="7354c-123">*lpTestScripts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7354c-123">*lpTestScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7354c-124">Puntero a la lista de pruebas, una segunda lista enumerada de scripts.</span><span class="sxs-lookup"><span data-stu-id="7354c-124">Pointer to the test list, a second enumerated list of scripts.</span></span> <span data-ttu-id="7354c-125">Esta lista se rellena normalmente mediante una llamada a [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).</span><span class="sxs-lookup"><span data-stu-id="7354c-125">This list is typically populated by calling [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).</span></span>

</dd> <dt>

<span data-ttu-id="7354c-126">*cchTestScripts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7354c-126">*cchTestScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7354c-127">Tamaño, en caracteres, de la cadena indicada por *lpTestScripts*.</span><span class="sxs-lookup"><span data-stu-id="7354c-127">Size, in characters, of the string indicated by *lpTestScripts*.</span></span> <span data-ttu-id="7354c-128">La aplicación establece este parámetro en-1 si la cadena termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="7354c-128">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="7354c-129">Si este parámetro se establece en 0, se produce un error en la función.</span><span class="sxs-lookup"><span data-stu-id="7354c-129">If this parameter is set to 0, the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7354c-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7354c-130">Return value</span></span>

<span data-ttu-id="7354c-131">Devuelve **true** si la lista de pruebas no está vacía y todos los elementos de la lista también se incluyen en la lista de configuraciones regionales.</span><span class="sxs-lookup"><span data-stu-id="7354c-131">Returns **TRUE** if the test list is non-empty and all items in the list are also included in the locale list.</span></span> <span data-ttu-id="7354c-132">De lo contrario, la función devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="7354c-132">Otherwise, the function returns **FALSE**.</span></span>

<span data-ttu-id="7354c-133">Un valor devuelto de **false** puede indicar que la lista de pruebas contiene un elemento que no está en la lista de configuraciones regionales o puede indicar un error.</span><span class="sxs-lookup"><span data-stu-id="7354c-133">A return value of **FALSE** can indicate that the test list contains an item that is not in the locale list, or it can indicate an error.</span></span> <span data-ttu-id="7354c-134">Para distinguir entre estos dos casos, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="7354c-134">To distinguish between these two cases, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="7354c-135">Si **DownlevelVerifyScripts** ha determinado correctamente que hay un elemento en la lista de pruebas que no está en la lista de configuraciones regionales, **GETLASTERROR** devuelve el error \_ Success.</span><span class="sxs-lookup"><span data-stu-id="7354c-135">If **DownlevelVerifyScripts** has successfully determined that there is an item in the test list that is not in the locale list, **GetLastError** returns ERROR\_SUCCESS.</span></span> <span data-ttu-id="7354c-136">De lo contrario, **GetLastError** puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="7354c-136">Otherwise, **GetLastError** can return one of the following error codes:</span></span>

-   <span data-ttu-id="7354c-137">ERROR en \_ marcas no válidas \_ .</span><span class="sxs-lookup"><span data-stu-id="7354c-137">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="7354c-138">Los valores proporcionados para marcas no eran válidos.</span><span class="sxs-lookup"><span data-stu-id="7354c-138">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="7354c-139">ERROR \_ de \_ parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="7354c-139">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="7354c-140">Cualquiera de los valores de parámetro no era válido.</span><span class="sxs-lookup"><span data-stu-id="7354c-140">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="7354c-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7354c-141">Remarks</span></span>

<span data-ttu-id="7354c-142">Esta función compara cadenas, como "LATN; Cyrl; ", que consta de una serie de nombres de script de 4 caracteres, con cada nombre de script seguido de un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="7354c-142">This function compares strings, such as "Latn;Cyrl;", that consist of a series of 4-character script names, with each script name followed by a semicolon.</span></span> <span data-ttu-id="7354c-143">También tiene un caso especial en el que se debe tener en cuenta el hecho de que el script Latino se usa a menudo en idiomas y configuraciones regionales para los que no es nativo.</span><span class="sxs-lookup"><span data-stu-id="7354c-143">It also has a special case to account for the fact that the Latin script is often used in languages and locales for which it is not native.</span></span>

<span data-ttu-id="7354c-144">Esta función es útil como parte de una estrategia para mitigar los problemas de seguridad relacionados con [los nombres de dominio internacionalizados (IDN)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="7354c-144">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="7354c-145">A continuación se muestran ejemplos de la devolución de esta función y una llamada subsiguiente a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) en varios escenarios.</span><span class="sxs-lookup"><span data-stu-id="7354c-145">The following are examples of the return of this function and a subsequent call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) in various scenarios.</span></span> <span data-ttu-id="7354c-146">Los dos últimos ejemplos ilustran, respectivamente, un caso en el que la lista de pruebas carece de un punto y coma de terminación (cadena incorrecta) y un caso en el que la lista de pruebas está vacía.</span><span class="sxs-lookup"><span data-stu-id="7354c-146">The last two examples illustrate, respectively, a case in which the test list lacks a terminating semicolon (malformed string) and a case in which the test list is empty.</span></span>



| <span data-ttu-id="7354c-147">Cadena "locale"</span><span class="sxs-lookup"><span data-stu-id="7354c-147">"Locale" string</span></span> | <span data-ttu-id="7354c-148">Cadena "Test"</span><span class="sxs-lookup"><span data-stu-id="7354c-148">"Test" string</span></span> | <span data-ttu-id="7354c-149">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="7354c-149">*dwFlags*</span></span>        | <span data-ttu-id="7354c-150">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7354c-150">Return value</span></span> | <span data-ttu-id="7354c-151">Devolución de GetLastError</span><span class="sxs-lookup"><span data-stu-id="7354c-151">GetLastError return</span></span>       |
|-----------------|---------------|------------------|--------------|---------------------------|
| <span data-ttu-id="7354c-152">Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="7354c-152">Hani;Hira;Kana;</span></span> | <span data-ttu-id="7354c-153">Hani;</span><span class="sxs-lookup"><span data-stu-id="7354c-153">Hani;</span></span>         | <span data-ttu-id="7354c-154">N/D</span><span class="sxs-lookup"><span data-stu-id="7354c-154">N/A</span></span>              | <span data-ttu-id="7354c-155">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="7354c-155">**TRUE**</span></span>     | <span data-ttu-id="7354c-156">N/D</span><span class="sxs-lookup"><span data-stu-id="7354c-156">N/A</span></span>                       |
| <span data-ttu-id="7354c-157">Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="7354c-157">Hani;Hira;Kana;</span></span> | <span data-ttu-id="7354c-158">Hani; LATN</span><span class="sxs-lookup"><span data-stu-id="7354c-158">Hani;Latn;</span></span>    | <span data-ttu-id="7354c-159">0</span><span class="sxs-lookup"><span data-stu-id="7354c-159">0</span></span>                | <span data-ttu-id="7354c-160">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="7354c-160">**FALSE**</span></span>    | <span data-ttu-id="7354c-161">ERROR \_ correcto</span><span class="sxs-lookup"><span data-stu-id="7354c-161">ERROR\_SUCCESS</span></span>            |
| <span data-ttu-id="7354c-162">Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="7354c-162">Hani;Hira;Kana;</span></span> | <span data-ttu-id="7354c-163">Hani; LATN</span><span class="sxs-lookup"><span data-stu-id="7354c-163">Hani;Latn;</span></span>    | <span data-ttu-id="7354c-164">VS \_ permitir \_ latín</span><span class="sxs-lookup"><span data-stu-id="7354c-164">VS\_ALLOW\_LATIN</span></span> | <span data-ttu-id="7354c-165">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="7354c-165">**TRUE**</span></span>     | <span data-ttu-id="7354c-166">N/D</span><span class="sxs-lookup"><span data-stu-id="7354c-166">N/A</span></span>                       |
| <span data-ttu-id="7354c-167">Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="7354c-167">Hani;Hira;Kana;</span></span> | <span data-ttu-id="7354c-168">Cyrl</span><span class="sxs-lookup"><span data-stu-id="7354c-168">Cyrl;</span></span>         | <span data-ttu-id="7354c-169">N/D</span><span class="sxs-lookup"><span data-stu-id="7354c-169">N/A</span></span>              | <span data-ttu-id="7354c-170">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="7354c-170">**FALSE**</span></span>    | <span data-ttu-id="7354c-171">ERROR \_ correcto</span><span class="sxs-lookup"><span data-stu-id="7354c-171">ERROR\_SUCCESS</span></span>            |
| <span data-ttu-id="7354c-172">Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="7354c-172">Hani;Hira;Kana;</span></span> | <span data-ttu-id="7354c-173">Cyrl</span><span class="sxs-lookup"><span data-stu-id="7354c-173">Cyrl;</span></span>         | <span data-ttu-id="7354c-174">N/D</span><span class="sxs-lookup"><span data-stu-id="7354c-174">N/A</span></span>              | <span data-ttu-id="7354c-175">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="7354c-175">**FALSE**</span></span>    | <span data-ttu-id="7354c-176">ERROR \_ de \_ parámetro no válido</span><span class="sxs-lookup"><span data-stu-id="7354c-176">ERROR\_INVALID\_PARAMETER</span></span> |
| <span data-ttu-id="7354c-177">Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="7354c-177">Hani;Hira;Kana;</span></span> |               | <span data-ttu-id="7354c-178">N/D</span><span class="sxs-lookup"><span data-stu-id="7354c-178">N/A</span></span>              | <span data-ttu-id="7354c-179">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="7354c-179">**FALSE**</span></span>    | <span data-ttu-id="7354c-180">ERROR \_ correcto</span><span class="sxs-lookup"><span data-stu-id="7354c-180">ERROR\_SUCCESS</span></span>            |



 

<span data-ttu-id="7354c-181">El archivo de encabezado y DLL necesarios forman parte de la descarga ["API de mitigación de nombres de dominio internacionalizados (IDN) de Microsoft"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponible en el [centro de descarga de MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="7354c-181">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="7354c-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7354c-182">Requirements</span></span>



| <span data-ttu-id="7354c-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="7354c-183">Requirement</span></span> | <span data-ttu-id="7354c-184">Value</span><span class="sxs-lookup"><span data-stu-id="7354c-184">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7354c-185">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7354c-185">Minimum supported client</span></span><br/> | <span data-ttu-id="7354c-186">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7354c-186">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                  |
| <span data-ttu-id="7354c-187">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7354c-187">Minimum supported server</span></span><br/> | <span data-ttu-id="7354c-188">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7354c-188">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                         |
| <span data-ttu-id="7354c-189">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7354c-189">Redistributable</span></span><br/>          | <span data-ttu-id="7354c-190">API de mitigación de nombres de dominio internacionalizados (IDN) de Microsoft Windows XP con SP2, Windows Server 2003 con SP1, orWindows vista</span><span class="sxs-lookup"><span data-stu-id="7354c-190">Microsoft Internationalized Domain Name (IDN) Mitigation APIs onWindows XP with SP2,Windows Server 2003 with SP1, orWindows Vista</span></span><br/> |
| <span data-ttu-id="7354c-191">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7354c-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="7354c-192"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7354c-192"><dt>Idndl.h</dt></span></span> </dl>                                                           |
| <span data-ttu-id="7354c-193">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7354c-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7354c-194"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7354c-194"><dt>Idndl.dll</dt></span></span> </dl>                                                         |



## <a name="see-also"></a><span data-ttu-id="7354c-195">Vea también</span><span class="sxs-lookup"><span data-stu-id="7354c-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7354c-196">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="7354c-196">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="7354c-197">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="7354c-197">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="7354c-198">Administrar nombres de dominio internacionalizados (IDN)</span><span class="sxs-lookup"><span data-stu-id="7354c-198">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="7354c-199">**DownlevelGetLocaleScripts**</span><span class="sxs-lookup"><span data-stu-id="7354c-199">**DownlevelGetLocaleScripts**</span></span>](downlevelgetlocalescripts.md)
</dt> <dt>

[<span data-ttu-id="7354c-200">**DownlevelGetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="7354c-200">**DownlevelGetStringScripts**</span></span>](downlevelgetstringscripts.md)
</dt> <dt>

[<span data-ttu-id="7354c-201">**VerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="7354c-201">**VerifyScripts**</span></span>](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 
