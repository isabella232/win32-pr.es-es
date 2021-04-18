---
description: Proporciona una lista de los scripts usados en la cadena Unicode especificada.
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: Función DownlevelGetStringScripts (Idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetStringScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: bc5a9fdaf3beb9e1c401943f923fa48bd9d4b44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688346"
---
# <a name="downlevelgetstringscripts-function"></a><span data-ttu-id="18cd9-103">DownlevelGetStringScripts función)</span><span class="sxs-lookup"><span data-stu-id="18cd9-103">DownlevelGetStringScripts function</span></span>

<span data-ttu-id="18cd9-104">Proporciona una lista de los scripts usados en la cadena Unicode especificada.</span><span class="sxs-lookup"><span data-stu-id="18cd9-104">Provides a list of scripts used in the specified Unicode string.</span></span>

> [!Note]  
> <span data-ttu-id="18cd9-105">Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="18cd9-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="18cd9-106">Su uso requiere el paquete de descarga.</span><span class="sxs-lookup"><span data-stu-id="18cd9-106">Its use requires the download package.</span></span> <span data-ttu-id="18cd9-107">Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores deben llamar a [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).</span><span class="sxs-lookup"><span data-stu-id="18cd9-107">Applications that only run on Windows Vista and later should call [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="18cd9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18cd9-108">Syntax</span></span>


```C++
int DownlevelGetStringScripts(
  _In_  DWORD   dwFlags,
  _In_  LPCWSTR lpString,
  _In_  int     cchString,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a><span data-ttu-id="18cd9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18cd9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18cd9-110">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18cd9-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18cd9-111">Marcas que especifican las opciones para la recuperación del script.</span><span class="sxs-lookup"><span data-stu-id="18cd9-111">Flags specifying options for script retrieval.</span></span>



| <span data-ttu-id="18cd9-112">Value</span><span class="sxs-lookup"><span data-stu-id="18cd9-112">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="18cd9-113">Significado</span><span class="sxs-lookup"><span data-stu-id="18cd9-113">Meaning</span></span>                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <span data-ttu-id="18cd9-114"><dt>**GSS \_ permitir \_ herencia \_ común**</dt></span><span class="sxs-lookup"><span data-stu-id="18cd9-114"><dt>**GSS\_ALLOW\_INHERITED\_COMMON**</dt></span></span> </dl> | <span data-ttu-id="18cd9-115">Recupere la información de script "Qaii" (HEREDAda) y "Zyyy" (común).</span><span class="sxs-lookup"><span data-stu-id="18cd9-115">Retrieve "Qaii" (INHERITED) and "Zyyy" (COMMON) script information.</span></span> <span data-ttu-id="18cd9-116">Este valor no afecta al procesamiento de caracteres sin asignar.</span><span class="sxs-lookup"><span data-stu-id="18cd9-116">This value does not affect the processing of unassigned characters.</span></span> <span data-ttu-id="18cd9-117">Estos caracteres de la cadena de entrada siempre provocan que aparezca un "ZZZZ" (script sin asignar) en la cadena de script.</span><span class="sxs-lookup"><span data-stu-id="18cd9-117">These characters in the input string always cause a "Zzzz" (UNASSIGNED script) to appear in the script string.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="18cd9-118">De forma predeterminada, esta función omite cualquier carácter común o heredado en la cadena de entrada Unicode.</span><span class="sxs-lookup"><span data-stu-id="18cd9-118">By default, this function ignores any inherited or common characters in the input Unicode string.</span></span> <span data-ttu-id="18cd9-119">Si \_ \_ no se establece GSS allow perherited \_ Common, no se mostrarán "Qaii" ni "Zyyy" en la cadena de script, aunque la cadena de entrada contenga dichos caracteres.</span><span class="sxs-lookup"><span data-stu-id="18cd9-119">If GSS\_ALLOW\_INHERITED\_COMMON is not set, neither "Qaii" nor "Zyyy" will appear in the script string, even if the input string contains such characters.</span></span> <span data-ttu-id="18cd9-120">Si \_ \_ se establece GSS allow perherited \_ Common, y si la cadena de entrada contiene caracteres heredados o comunes, "Qaii" y/o "Zyyy" aparecen en la cadena de script.</span><span class="sxs-lookup"><span data-stu-id="18cd9-120">If GSS\_ALLOW\_INHERITED\_COMMON is set, and if the input string contains inherited and/or common characters, "Qaii" and/or "Zyyy" appear in the script string.</span></span> <span data-ttu-id="18cd9-121">Consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="18cd9-121">See the Remarks section.</span></span>

 

</dd> <dt>

<span data-ttu-id="18cd9-122">*lpString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18cd9-122">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18cd9-123">Puntero a la cadena Unicode que se va a analizar.</span><span class="sxs-lookup"><span data-stu-id="18cd9-123">Pointer to the Unicode string to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="18cd9-124">*cchString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18cd9-124">*cchString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18cd9-125">Tamaño, en caracteres, de la cadena Unicode indicada por *lpString*.</span><span class="sxs-lookup"><span data-stu-id="18cd9-125">Size, in characters, of the Unicode string indicated by *lpString*.</span></span> <span data-ttu-id="18cd9-126">La aplicación establece este parámetro en-1 si la cadena termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="18cd9-126">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="18cd9-127">Si la aplicación establece este parámetro en 0, la función recupera una cadena Unicode nula (L " \\ 0") en *lpScripts* y devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="18cd9-127">If the application sets this parameter to 0, the function retrieves a null Unicode string (L"\\0") in *lpScripts* and returns 1.</span></span>

</dd> <dt>

<span data-ttu-id="18cd9-128">*lpScripts* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="18cd9-128">*lpScripts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18cd9-129">Puntero a un búfer en el que esta función recupera una cadena terminada en null que representa una lista de scripts, utilizando la notación de 4 caracteres utilizada en [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="18cd9-129">Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="18cd9-130">Cada nombre de script consta de cuatro caracteres latinos y los nombres se recuperan en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="18cd9-130">Each script name consists of four Latin characters, and the names are retrieved in alphabetical order.</span></span> <span data-ttu-id="18cd9-131">Cada nombre, incluido el último, va seguido de un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="18cd9-131">Each name, including the last, is followed by a semicolon.</span></span>

<span data-ttu-id="18cd9-132">Como alternativa, este parámetro puede contener un **valor null** si *cchScripts* se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="18cd9-132">Alternatively, this parameter can contain **NULL** if *cchScripts* set to 0.</span></span> <span data-ttu-id="18cd9-133">En este caso, la función devuelve el tamaño necesario para el búfer de script.</span><span class="sxs-lookup"><span data-stu-id="18cd9-133">In this case, the function returns the required size for the script buffer.</span></span>

</dd> <dt>

<span data-ttu-id="18cd9-134">*cchScripts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18cd9-134">*cchScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18cd9-135">Tamaño, en caracteres, para el búfer de script indicado por *lpScripts*.</span><span class="sxs-lookup"><span data-stu-id="18cd9-135">Size, in characters, for the script buffer indicated by *lpScripts*.</span></span>

<span data-ttu-id="18cd9-136">Como alternativa, la aplicación puede establecer este parámetro en 0.</span><span class="sxs-lookup"><span data-stu-id="18cd9-136">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="18cd9-137">En este caso, la función recupera **null** en *lpScripts* y devuelve el tamaño requerido para el búfer de script.</span><span class="sxs-lookup"><span data-stu-id="18cd9-137">In this case, the function retrieves **NULL** in *lpScripts* and returns the required size for the script buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18cd9-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18cd9-138">Return value</span></span>

<span data-ttu-id="18cd9-139">Devuelve el número de caracteres recuperados en el búfer de salida, incluido un carácter nulo de terminación, si es correcto y *cchScripts* está establecido en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="18cd9-139">Returns the number of characters retrieved in the output buffer, including a terminating null character, if successful and *cchScripts* is set to a nonzero value.</span></span> <span data-ttu-id="18cd9-140">La función devuelve 1 para indicar que no se ha encontrado ningún script, por ejemplo, cuando la cadena de entrada solo contiene caracteres comunes o HEREDAdos y \_ \_ no se ha establecido GSS allow perherited \_ Common.</span><span class="sxs-lookup"><span data-stu-id="18cd9-140">The function returns 1 to indicate that no script has been found, for example, when the input string only contains COMMON or INHERITED characters and GSS\_ALLOW\_INHERITED\_COMMON is not set.</span></span> <span data-ttu-id="18cd9-141">Dado que cada script encontrado agrega cinco caracteres (cuatro caracteres + delimitador), una operación matemática simple proporciona el número de scripts como (código devuelto \_ -1)/5.</span><span class="sxs-lookup"><span data-stu-id="18cd9-141">Given that each found script adds five characters (four characters + delimiter), a simple mathematical operation provides the script count as (return\_code - 1) / 5.</span></span>

<span data-ttu-id="18cd9-142">Si la función se ejecuta correctamente y el valor de *cchScripts* es 0, el valor devuelto es el tamaño necesario, en caracteres que incluye un carácter nulo de terminación, para el búfer de script.</span><span class="sxs-lookup"><span data-stu-id="18cd9-142">If the function succeeds and the value of *cchScripts* is 0, the return value is the required size, in characters including a terminating null character, for the script buffer.</span></span> <span data-ttu-id="18cd9-143">El número de scripts es como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="18cd9-143">The script count is as described above.</span></span>

<span data-ttu-id="18cd9-144">La función devuelve 0 si no se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="18cd9-144">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="18cd9-145">Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="18cd9-145">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="18cd9-146">ERROR \_ BADDB.</span><span class="sxs-lookup"><span data-stu-id="18cd9-146">ERROR\_BADDB.</span></span> <span data-ttu-id="18cd9-147">La función no pudo obtener acceso a los datos.</span><span class="sxs-lookup"><span data-stu-id="18cd9-147">The function could not access the data.</span></span> <span data-ttu-id="18cd9-148">Esta situación no debería producirse normalmente y normalmente indica una instalación incorrecta, un problema de disco o un tipo similar.</span><span class="sxs-lookup"><span data-stu-id="18cd9-148">This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</span></span>
-   <span data-ttu-id="18cd9-149">ERROR \_ de \_ búfer insuficiente.</span><span class="sxs-lookup"><span data-stu-id="18cd9-149">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="18cd9-150">Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **null**.</span><span class="sxs-lookup"><span data-stu-id="18cd9-150">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="18cd9-151">ERROR en \_ marcas no válidas \_ .</span><span class="sxs-lookup"><span data-stu-id="18cd9-151">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="18cd9-152">Los valores proporcionados para marcas no eran válidos.</span><span class="sxs-lookup"><span data-stu-id="18cd9-152">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="18cd9-153">ERROR \_ de \_ parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="18cd9-153">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="18cd9-154">Cualquiera de los valores de parámetro no era válido.</span><span class="sxs-lookup"><span data-stu-id="18cd9-154">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="18cd9-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18cd9-155">Remarks</span></span>

<span data-ttu-id="18cd9-156">Esta función es útil como parte de una estrategia para mitigar los problemas de seguridad relacionados con [los nombres de dominio internacionalizados (IDN)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="18cd9-156">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="18cd9-157">La determinación del script se basa en los valores de script publicados por Unicode Consortium en <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> , excepto en que los caracteres sin asignar tienen el valor "ZZZZ" (sin asignar) en lugar de "Zyyy" (común).</span><span class="sxs-lookup"><span data-stu-id="18cd9-157">The script determination is based on the script values published by the Unicode Consortium in <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt>, except that the unassigned characters have the value "Zzzz" (UNASSIGNED) instead of "Zyyy" (COMMON).</span></span>

<span data-ttu-id="18cd9-158">Estos son algunos ejemplos del comportamiento de esta función:</span><span class="sxs-lookup"><span data-stu-id="18cd9-158">Here are some examples of the behavior of this function:</span></span>



<span data-ttu-id="18cd9-159">Cadena de entrada</span><span class="sxs-lookup"><span data-stu-id="18cd9-159">Input string</span></span>

<span data-ttu-id="18cd9-160">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="18cd9-160">*dwFlags*</span></span>

<span data-ttu-id="18cd9-161">*lpScripts*</span><span class="sxs-lookup"><span data-stu-id="18cd9-161">*lpScripts*</span></span>

<span data-ttu-id="18cd9-162">Scripts</span><span class="sxs-lookup"><span data-stu-id="18cd9-162">Scripts</span></span>

<span data-ttu-id="18cd9-163">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="18cd9-163">Microsoft.com</span></span>

<span data-ttu-id="18cd9-164">0</span><span class="sxs-lookup"><span data-stu-id="18cd9-164">0</span></span>

<span data-ttu-id="18cd9-165">LATN</span><span class="sxs-lookup"><span data-stu-id="18cd9-165">Latn;</span></span>

<span data-ttu-id="18cd9-166">Latín</span><span class="sxs-lookup"><span data-stu-id="18cd9-166">Latin</span></span>

<span data-ttu-id="18cd9-167">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="18cd9-167">Microsoft.com</span></span>

<span data-ttu-id="18cd9-168">GSS \_ permitir \_ herencia \_ común</span><span class="sxs-lookup"><span data-stu-id="18cd9-168">GSS\_ALLOW\_INHERITED\_COMMON</span></span>

<span data-ttu-id="18cd9-169">LATN Zyyy;</span><span class="sxs-lookup"><span data-stu-id="18cd9-169">Latn;Zyyy;</span></span>

<span data-ttu-id="18cd9-170">Latín + común</span><span class="sxs-lookup"><span data-stu-id="18cd9-170">Latin + Common</span></span>

<span data-ttu-id="18cd9-171">$ {ROWSPAN2} $Ni ño $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="18cd9-171">${ROWSPAN2}$Niño${REMOVE}$</span></span>  

<span data-ttu-id="18cd9-172">004E 0069 0241 006F</span><span class="sxs-lookup"><span data-stu-id="18cd9-172">004E 0069 0241 006F</span></span>

<span data-ttu-id="18cd9-173">$ {ROWSPAN2} $GSS \_ permitir \_ \_ Common $ {Remove} $ heredado</span><span class="sxs-lookup"><span data-stu-id="18cd9-173">${ROWSPAN2}$GSS\_ALLOW\_INHERITED\_COMMON${REMOVE}$</span></span>  

<span data-ttu-id="18cd9-174">$ {ROWSPAN2} $Latn; $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="18cd9-174">${ROWSPAN2}$Latn;${REMOVE}$</span></span>  

<span data-ttu-id="18cd9-175">$ {ROWSPAN2} $Latin $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="18cd9-175">${ROWSPAN2}$Latin${REMOVE}$</span></span>  

<span data-ttu-id="18cd9-176">Usa letra latina minúscula N con TILDE</span><span class="sxs-lookup"><span data-stu-id="18cd9-176">Uses LATIN SMALL LETTER N WITH TILDE</span></span>

<span data-ttu-id="18cd9-177">$ {ROWSPAN2} $Ni ño $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="18cd9-177">${ROWSPAN2}$Niño${REMOVE}$</span></span>  

<span data-ttu-id="18cd9-178">004E 0069 006E 0303 006F</span><span class="sxs-lookup"><span data-stu-id="18cd9-178">004E 0069 006E 0303 006F</span></span>

<span data-ttu-id="18cd9-179">$ {ROWSPAN2} $GSS \_ permitir \_ \_ Common $ {Remove} $ heredado</span><span class="sxs-lookup"><span data-stu-id="18cd9-179">${ROWSPAN2}$GSS\_ALLOW\_INHERITED\_COMMON${REMOVE}$</span></span>  

<span data-ttu-id="18cd9-180">$ {ROWSPAN2} $Latn; Qaii; $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="18cd9-180">${ROWSPAN2}$Latn;Qaii;${REMOVE}$</span></span>  

<span data-ttu-id="18cd9-181">$ {ROWSPAN2} $Latin + heredado $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="18cd9-181">${ROWSPAN2}$Latin + Inherited${REMOVE}$</span></span>  

<span data-ttu-id="18cd9-182">Usa TILDE de combinación</span><span class="sxs-lookup"><span data-stu-id="18cd9-182">Uses COMBINING TILDE</span></span>

<span data-ttu-id="18cd9-183">$ {ROWSPAN2} $Sp ооf $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="18cd9-183">${ROWSPAN2}$Spооf${REMOVE}$</span></span>  

<span data-ttu-id="18cd9-184">0053 0070 043e 043e 0066</span><span class="sxs-lookup"><span data-stu-id="18cd9-184">0053 0070 043e 043e 0066</span></span>

<span data-ttu-id="18cd9-185">$ {ROWSPAN2} $0 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="18cd9-185">${ROWSPAN2}$0${REMOVE}$</span></span>  

<span data-ttu-id="18cd9-186">$ {ROWSPAN2} $Latn; Cyrl; $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="18cd9-186">${ROWSPAN2}$Latn;Cyrl;${REMOVE}$</span></span>  

<span data-ttu-id="18cd9-187">$ {ROWSPAN2} $Latin + cirílico $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="18cd9-187">${ROWSPAN2}$Latin + Cyrillic${REMOVE}$</span></span>  

<span data-ttu-id="18cd9-188">Usa letra minúscula cirílica O</span><span class="sxs-lookup"><span data-stu-id="18cd9-188">Uses CYRILLIC SMALL LETTER O</span></span>

<span data-ttu-id="18cd9-189"></span><span class="sxs-lookup"><span data-stu-id="18cd9-189"></span></span>

<span data-ttu-id="18cd9-190">U + F000</span><span class="sxs-lookup"><span data-stu-id="18cd9-190">U+f000</span></span>

<span data-ttu-id="18cd9-191">0</span><span class="sxs-lookup"><span data-stu-id="18cd9-191">0</span></span>

<span data-ttu-id="18cd9-192">ZZZZ</span><span class="sxs-lookup"><span data-stu-id="18cd9-192">Zzzz;</span></span>

<span data-ttu-id="18cd9-193">Sin asignar</span><span class="sxs-lookup"><span data-stu-id="18cd9-193">Unassigned</span></span>

<span data-ttu-id="18cd9-194"></span><span class="sxs-lookup"><span data-stu-id="18cd9-194"></span></span>

<span data-ttu-id="18cd9-195">U + F000</span><span class="sxs-lookup"><span data-stu-id="18cd9-195">U+f000</span></span>

<span data-ttu-id="18cd9-196">GSS \_ permitir \_ herencia \_ común</span><span class="sxs-lookup"><span data-stu-id="18cd9-196">GSS\_ALLOW\_INHERITED\_COMMON</span></span>

<span data-ttu-id="18cd9-197">ZZZZ</span><span class="sxs-lookup"><span data-stu-id="18cd9-197">Zzzz;</span></span>

<span data-ttu-id="18cd9-198">Sin asignar</span><span class="sxs-lookup"><span data-stu-id="18cd9-198">Unassigned</span></span>



 

<span data-ttu-id="18cd9-199">El archivo de encabezado y DLL necesarios forman parte de la descarga ["API de mitigación de nombres de dominio internacionalizados (IDN) de Microsoft"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) , disponible en el [centro de descarga de MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="18cd9-199">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="18cd9-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18cd9-200">Requirements</span></span>



| <span data-ttu-id="18cd9-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="18cd9-201">Requirement</span></span> | <span data-ttu-id="18cd9-202">Value</span><span class="sxs-lookup"><span data-stu-id="18cd9-202">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18cd9-203">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18cd9-203">Minimum supported client</span></span><br/> | <span data-ttu-id="18cd9-204">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="18cd9-204">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                 |
| <span data-ttu-id="18cd9-205">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18cd9-205">Minimum supported server</span></span><br/> | <span data-ttu-id="18cd9-206">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="18cd9-206">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                        |
| <span data-ttu-id="18cd9-207">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="18cd9-207">Redistributable</span></span><br/>          | <span data-ttu-id="18cd9-208">API de mitigación de nombres de dominio internacionalizados (IDN) de Microsoft en Windows XP (SP2 o posterior), Windows Server 2003 (SP1 o posterior) o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18cd9-208">Microsoft Internationalized Domain Name (IDN) Mitigation APIs on Windows XP (SP2 or later), Windows Server 2003 (SP1 or later), or Windows Vista</span></span><br/> |
| <span data-ttu-id="18cd9-209">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18cd9-209">Header</span></span><br/>                   | <dl> <span data-ttu-id="18cd9-210"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="18cd9-210"><dt>Idndl.h</dt></span></span> </dl>                                                                          |
| <span data-ttu-id="18cd9-211">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="18cd9-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18cd9-212"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18cd9-212"><dt>Idndl.dll</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="18cd9-213">Vea también</span><span class="sxs-lookup"><span data-stu-id="18cd9-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18cd9-214">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="18cd9-214">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="18cd9-215">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="18cd9-215">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="18cd9-216">Administrar nombres de dominio internacionalizados (IDN)</span><span class="sxs-lookup"><span data-stu-id="18cd9-216">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="18cd9-217">**DownlevelGetLocaleScripts**</span><span class="sxs-lookup"><span data-stu-id="18cd9-217">**DownlevelGetLocaleScripts**</span></span>](downlevelgetlocalescripts.md)
</dt> <dt>

[<span data-ttu-id="18cd9-218">**DownlevelVerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="18cd9-218">**DownlevelVerifyScripts**</span></span>](downlevelverifyscripts.md)
</dt> <dt>

[<span data-ttu-id="18cd9-219">**GetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="18cd9-219">**GetStringScripts**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 
