---
description: Proporciona una lista de scripts para la configuración regional especificada.
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: Función DownlevelGetLocaleScripts (Idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetLocaleScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: f636ab426cd4d50878df93e3e30d69de54d60ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278612"
---
# <a name="downlevelgetlocalescripts-function"></a><span data-ttu-id="45f5c-103">DownlevelGetLocaleScripts función)</span><span class="sxs-lookup"><span data-stu-id="45f5c-103">DownlevelGetLocaleScripts function</span></span>

<span data-ttu-id="45f5c-104">Proporciona una lista de scripts para la configuración regional especificada.</span><span class="sxs-lookup"><span data-stu-id="45f5c-104">Provides a list of scripts for the specified locale.</span></span>

> [!Note]  
> <span data-ttu-id="45f5c-105">Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="45f5c-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="45f5c-106">Su uso requiere el paquete de descarga.</span><span class="sxs-lookup"><span data-stu-id="45f5c-106">Its use requires the download package.</span></span> <span data-ttu-id="45f5c-107">Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores deben llamar a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* establecido en [ \_ SSCRIPTS de configuración regional](locale-sscripts.md).</span><span class="sxs-lookup"><span data-stu-id="45f5c-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SSCRIPTS](locale-sscripts.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="45f5c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45f5c-108">Syntax</span></span>


```C++
int DownlevelGetLocaleScripts(
  _In_  LPCWSTR lpLocaleName,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a><span data-ttu-id="45f5c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45f5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45f5c-110">*lpLocaleName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45f5c-110">*lpLocaleName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45f5c-111">Puntero a un [nombre de configuración regional](locale-names.md)terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="45f5c-111">Pointer to a null-terminated [locale name](locale-names.md).</span></span>

</dd> <dt>

<span data-ttu-id="45f5c-112">*lpScripts* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="45f5c-112">*lpScripts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45f5c-113">Puntero a un búfer en el que esta función recupera una cadena terminada en null que representa una lista de scripts, utilizando la notación de 4 caracteres utilizada en [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="45f5c-113">Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="45f5c-114">Cada nombre de script consta de cuatro caracteres latinos y los nombres se recuperan en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="45f5c-114">Each script name consists of four Latin characters, and the names are retrieved in alphabetical order.</span></span> <span data-ttu-id="45f5c-115">Cada una de ellas, incluida la última, va seguida de un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="45f5c-115">Each of them, including the last, is followed by a semicolon.</span></span>

<span data-ttu-id="45f5c-116">Como alternativa, este parámetro puede contener un **valor null** si *cchScripts* está establecido en 0.</span><span class="sxs-lookup"><span data-stu-id="45f5c-116">Alternatively, this parameter can contain **NULL** if *cchScripts* is set to 0.</span></span> <span data-ttu-id="45f5c-117">En este caso, la función devuelve el tamaño necesario para el búfer de script.</span><span class="sxs-lookup"><span data-stu-id="45f5c-117">In this case, the function returns the required size for the script buffer.</span></span>

</dd> <dt>

<span data-ttu-id="45f5c-118">*cchScripts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45f5c-118">*cchScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45f5c-119">Tamaño, en caracteres, para el búfer de script indicado por *lpScripts*.</span><span class="sxs-lookup"><span data-stu-id="45f5c-119">Size, in characters, for the script buffer indicated by *lpScripts*.</span></span>

<span data-ttu-id="45f5c-120">Como alternativa, la aplicación puede establecer este parámetro en 0.</span><span class="sxs-lookup"><span data-stu-id="45f5c-120">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="45f5c-121">En este caso, la función recupera **null** en *lpScripts* y devuelve el tamaño requerido para el búfer de script.</span><span class="sxs-lookup"><span data-stu-id="45f5c-121">In this case, the function retrieves **NULL** in *lpScripts* and returns the required size for the script buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45f5c-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45f5c-122">Return value</span></span>

<span data-ttu-id="45f5c-123">Devuelve el número de caracteres recuperados en el búfer de script, incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="45f5c-123">Returns the number of characters retrieved in the script buffer, including the terminating null character.</span></span> <span data-ttu-id="45f5c-124">Si la función se ejecuta correctamente y el valor de *cchScripts* es 0, el valor devuelto es el tamaño necesario, en caracteres que incluye un carácter nulo de terminación, para el búfer de script.</span><span class="sxs-lookup"><span data-stu-id="45f5c-124">If the function succeeds and the value of *cchScripts* is 0, the return value is the required size, in characters including a terminating null character, for the script buffer.</span></span>

<span data-ttu-id="45f5c-125">Esta función devuelve 0 si no se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="45f5c-125">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="45f5c-126">Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="45f5c-126">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="45f5c-127">ERROR \_ BADDB.</span><span class="sxs-lookup"><span data-stu-id="45f5c-127">ERROR\_BADDB.</span></span> <span data-ttu-id="45f5c-128">La función no pudo obtener acceso a los datos.</span><span class="sxs-lookup"><span data-stu-id="45f5c-128">The function could not access the data.</span></span> <span data-ttu-id="45f5c-129">Esta situación no debería producirse normalmente y normalmente indica una instalación incorrecta, un problema de disco o un tipo similar.</span><span class="sxs-lookup"><span data-stu-id="45f5c-129">This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</span></span>
-   <span data-ttu-id="45f5c-130">ERROR \_ de \_ búfer insuficiente.</span><span class="sxs-lookup"><span data-stu-id="45f5c-130">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="45f5c-131">Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **null**.</span><span class="sxs-lookup"><span data-stu-id="45f5c-131">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="45f5c-132">ERROR \_ de \_ parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="45f5c-132">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="45f5c-133">Cualquiera de los valores de parámetro no era válido.</span><span class="sxs-lookup"><span data-stu-id="45f5c-133">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="45f5c-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45f5c-134">Remarks</span></span>

<span data-ttu-id="45f5c-135">Esta función es útil como parte de una estrategia para mitigar los problemas de seguridad relacionados con [los nombres de dominio internacionalizados (IDN)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="45f5c-135">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="45f5c-136">Estos son algunos ejemplos de entradas y salidas para esta función, suponiendo un tamaño de búfer suficiente:</span><span class="sxs-lookup"><span data-stu-id="45f5c-136">Here are some examples of inputs and outputs for this function, assuming a sufficient buffer size:</span></span>



| <span data-ttu-id="45f5c-137">Configuración regional</span><span class="sxs-lookup"><span data-stu-id="45f5c-137">Locale</span></span>                  | <span data-ttu-id="45f5c-138">*lpLocaleName*</span><span class="sxs-lookup"><span data-stu-id="45f5c-138">*lpLocaleName*</span></span> | <span data-ttu-id="45f5c-139">*lpScripts*</span><span class="sxs-lookup"><span data-stu-id="45f5c-139">*lpScripts*</span></span>     |
|-------------------------|----------------|-----------------|
| <span data-ttu-id="45f5c-140">Spanish (Traditional Sort) - Spain</span><span class="sxs-lookup"><span data-stu-id="45f5c-140">English (United States)</span></span> | <span data-ttu-id="45f5c-141">es-ES</span><span class="sxs-lookup"><span data-stu-id="45f5c-141">en-US</span></span>          | <span data-ttu-id="45f5c-142">LATN</span><span class="sxs-lookup"><span data-stu-id="45f5c-142">Latn;</span></span>           |
| <span data-ttu-id="45f5c-143">Hindi (India)</span><span class="sxs-lookup"><span data-stu-id="45f5c-143">Hindi (India)</span></span>           | <span data-ttu-id="45f5c-144">hi-IN</span><span class="sxs-lookup"><span data-stu-id="45f5c-144">hi-IN</span></span>          | <span data-ttu-id="45f5c-145">Deva</span><span class="sxs-lookup"><span data-stu-id="45f5c-145">Deva;</span></span>           |
| <span data-ttu-id="45f5c-146">Japonés (Japón)</span><span class="sxs-lookup"><span data-stu-id="45f5c-146">Japanese (Japan)</span></span>        | <span data-ttu-id="45f5c-147">ja-JP</span><span class="sxs-lookup"><span data-stu-id="45f5c-147">ja-JP</span></span>          | <span data-ttu-id="45f5c-148">Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="45f5c-148">Hani;Hira;Kana;</span></span> |



 

<span data-ttu-id="45f5c-149">La lista no contiene el script Latino a menos que sea una parte esencial del sistema de escritura usado para una configuración regional.</span><span class="sxs-lookup"><span data-stu-id="45f5c-149">The list does not contain the Latin script unless it is an essential part of the writing system used for a locale.</span></span> <span data-ttu-id="45f5c-150">Sin embargo, los caracteres latinos se suelen usar en el contexto de configuraciones regionales para las que no son nativos, como en el caso de un nombre empresarial extranjero.</span><span class="sxs-lookup"><span data-stu-id="45f5c-150">However, Latin characters are often used in the context of locales for which they are not native, as for a foreign business name.</span></span> <span data-ttu-id="45f5c-151">En el ejemplo anterior de Hindi en India, el único script recuperado es "Deva" (para devanagari), aunque los caracteres latinos también pueden aparecer en texto Hindi.</span><span class="sxs-lookup"><span data-stu-id="45f5c-151">In the example above for Hindi in India, the only script retrieved is "Deva" (for Devanagari), although Latin characters can also appear in Hindi text.</span></span> <span data-ttu-id="45f5c-152">La función [**DownlevelVerifyScripts**](downlevelverifyscripts.md) tiene una marca especial para abordar ese caso.</span><span class="sxs-lookup"><span data-stu-id="45f5c-152">The [**DownlevelVerifyScripts**](downlevelverifyscripts.md) function has a special flag to address that case.</span></span>

<span data-ttu-id="45f5c-153">El archivo de encabezado y DLL necesarios forman parte de la descarga ["API de mitigación de nombres de dominio internacionalizados (IDN) de Microsoft"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponible en el [centro de descarga de MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="45f5c-153">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="45f5c-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45f5c-154">Requirements</span></span>



| <span data-ttu-id="45f5c-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="45f5c-155">Requirement</span></span> | <span data-ttu-id="45f5c-156">Value</span><span class="sxs-lookup"><span data-stu-id="45f5c-156">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45f5c-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45f5c-157">Minimum supported client</span></span><br/> | <span data-ttu-id="45f5c-158">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="45f5c-158">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                 |
| <span data-ttu-id="45f5c-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45f5c-159">Minimum supported server</span></span><br/> | <span data-ttu-id="45f5c-160">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="45f5c-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                        |
| <span data-ttu-id="45f5c-161">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="45f5c-161">Redistributable</span></span><br/>          | <span data-ttu-id="45f5c-162">API de mitigación de nombres de dominio internacionalizados (IDN) de Microsoft en Windows XP (SP2 o posterior), Windows Server 2003 (SP1 o posterior) o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45f5c-162">Microsoft Internationalized Domain Name (IDN) Mitigation APIs on Windows XP (SP2 or later), Windows Server 2003 (SP1 or later), or Windows Vista</span></span><br/> |
| <span data-ttu-id="45f5c-163">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45f5c-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="45f5c-164"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="45f5c-164"><dt>Idndl.h</dt></span></span> </dl>                                                                          |
| <span data-ttu-id="45f5c-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="45f5c-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45f5c-166"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45f5c-166"><dt>Idndl.dll</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="45f5c-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="45f5c-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45f5c-168">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="45f5c-168">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="45f5c-169">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="45f5c-169">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="45f5c-170">Administrar nombres de dominio internacionalizados (IDN)</span><span class="sxs-lookup"><span data-stu-id="45f5c-170">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="45f5c-171">**DownlevelGetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="45f5c-171">**DownlevelGetStringScripts**</span></span>](downlevelgetstringscripts.md)
</dt> <dt>

[<span data-ttu-id="45f5c-172">**DownlevelVerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="45f5c-172">**DownlevelVerifyScripts**</span></span>](downlevelverifyscripts.md)
</dt> <dt>

[<span data-ttu-id="45f5c-173">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="45f5c-173">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
