---
description: Convierte un identificador de configuración regional en un nombre de configuración regional.
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: Función DownlevelLCIDToLocaleName (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLCIDToLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: 2f8e4ce9763348cf765522ebbd624a6e82f1071a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668414"
---
# <a name="downlevellcidtolocalename-function"></a><span data-ttu-id="2c4c3-103">DownlevelLCIDToLocaleName función)</span><span class="sxs-lookup"><span data-stu-id="2c4c3-103">DownlevelLCIDToLocaleName function</span></span>

<span data-ttu-id="2c4c3-104">Convierte un [identificador de configuración](locale-identifiers.md) regional en un [nombre de configuración regional](locale-names.md).</span><span class="sxs-lookup"><span data-stu-id="2c4c3-104">Converts a [locale identifier](locale-identifiers.md) to a [locale name](locale-names.md).</span></span>

> [!Note]  
> <span data-ttu-id="2c4c3-105">Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="2c4c3-106">Su uso requiere un paquete de descarga.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-106">Its use requires a download package.</span></span> <span data-ttu-id="2c4c3-107">Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores deben llamar a [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) para recuperar un nombre de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-107">Applications that run only on Windows Vista and later should call [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) to retrieve a locale name.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2c4c3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c4c3-108">Syntax</span></span>


```C++
int DownlevelLCIDToLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName,
  _In_  DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2c4c3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c4c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c4c3-110">*Configuración regional* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2c4c3-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4c3-111">Identificador de configuración regional que se va a traducir.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-111">The locale identifier to translate.</span></span> <span data-ttu-id="2c4c3-112">Puede usar la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para crear un identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier.</span></span> <span data-ttu-id="2c4c3-113">Esta función no admite configuraciones regionales neutras ni los siguientes valores de identificador de configuración regional específicos.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-113">This function does not support neutral locales or the following specific locale identifier values.</span></span>

-   [<span data-ttu-id="2c4c3-114">configuración \_ predeterminada del sistema local \_</span><span class="sxs-lookup"><span data-stu-id="2c4c3-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="2c4c3-115">\_valor predeterminado del usuario de configuración regional \_</span><span class="sxs-lookup"><span data-stu-id="2c4c3-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)
-   [<span data-ttu-id="2c4c3-116">CONFIGURACIÓN \_ predeterminada personalizada \_</span><span class="sxs-lookup"><span data-stu-id="2c4c3-116">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="2c4c3-117">CONFIGURACIÓN predeterminada de la \_ \_ interfaz de usuario personalizada \_</span><span class="sxs-lookup"><span data-stu-id="2c4c3-117">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="2c4c3-118">configuración regional \_ personalizada no \_ especificada</span><span class="sxs-lookup"><span data-stu-id="2c4c3-118">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> <dt>

<span data-ttu-id="2c4c3-119">*lpName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2c4c3-119">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4c3-120">Puntero a un búfer en el que esta función recupera el nombre de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-120">Pointer to a buffer in which this function retrieves the locale name.</span></span> <span data-ttu-id="2c4c3-121">La función recupera **null** si *cchName* está establecido en 0.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-121">The function retrieves **NULL** if *cchName* is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="2c4c3-122">*cchName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2c4c3-122">*cchName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4c3-123">Tamaño, en puntos de código UTF-16, del búfer de nombres de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-123">Size, in UTF-16 code points, of the locale name buffer.</span></span> <span data-ttu-id="2c4c3-124">La aplicación establece este parámetro en 0 para devolver el tamaño necesario del búfer del nombre de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-124">The application sets this parameter to 0 to return the required size of the locale name buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2c4c3-125">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2c4c3-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4c3-126">Marcas que especifican el tipo de nombre que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-126">Flags specifying the type of name to retrieve.</span></span> <span data-ttu-id="2c4c3-127">El valor predeterminado es el nombre de la configuración regional de nivel inferior \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2c4c3-127">The default value is DOWNLEVEL\_LOCALE\_NAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c4c3-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c4c3-128">Return value</span></span>

<span data-ttu-id="2c4c3-129">Devuelve el recuento de puntos de código UTF-16 en el nombre de la configuración regional, incluido el carácter nulo de terminación, si es correcto.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-129">Returns the count of UTF-16 code points in the locale name, including the terminating null character, if successful.</span></span> <span data-ttu-id="2c4c3-130">Si la función se ejecuta correctamente y el valor de *cchName* es 0, el valor devuelto es el tamaño necesario, en caracteres (incluidos los caracteres null), para el búfer de nombre de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-130">If the function succeeds and the value of *cchName* is 0, the return value is the required size, in characters (including null characters), for the locale name buffer.</span></span>

<span data-ttu-id="2c4c3-131">La función devuelve 0 si no se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-131">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="2c4c3-132">Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="2c4c3-132">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="2c4c3-133">ERROR \_ de \_ búfer insuficiente.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-133">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="2c4c3-134">Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **null**.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-134">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="2c4c3-135">ERROR en \_ marcas no válidas \_ .</span><span class="sxs-lookup"><span data-stu-id="2c4c3-135">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="2c4c3-136">El valor de *dwFlags* no es válido.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-136">The value of *dwFlags* is not valid.</span></span>
-   <span data-ttu-id="2c4c3-137">ERROR \_ de \_ parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-137">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="2c4c3-138">Cualquiera de los valores de parámetro no era válido.</span><span class="sxs-lookup"><span data-stu-id="2c4c3-138">Any of the parameter values were invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c4c3-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c4c3-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2c4c3-140">Esta función no admite [configuraciones regionales personalizadas](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="2c4c3-140">This function does not support [custom locales](custom-locales.md).</span></span>

 

<span data-ttu-id="2c4c3-141">El archivo de encabezado y DLL necesarios forman parte de la descarga de la "API de asignación de datos de Microsoft NLS Downlevel", disponible en el [centro de descarga de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="2c4c3-141">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c4c3-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c4c3-142">Requirements</span></span>



| <span data-ttu-id="2c4c3-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c4c3-143">Requirement</span></span> | <span data-ttu-id="2c4c3-144">Value</span><span class="sxs-lookup"><span data-stu-id="2c4c3-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4c3-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c4c3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2c4c3-146">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2c4c3-146">Windows XP \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="2c4c3-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c4c3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2c4c3-148">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c4c3-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2c4c3-149">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="2c4c3-149">Redistributable</span></span><br/>          | <span data-ttu-id="2c4c3-150">API de asignación de datos de Microsoft NLS Downlevel Windows XP con SP2 y laterorWindows vista</span><span class="sxs-lookup"><span data-stu-id="2c4c3-150">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista</span></span><br/> |
| <span data-ttu-id="2c4c3-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c4c3-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c4c3-152"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c4c3-152"><dt>Nlsdl.h</dt></span></span> </dl>                  |
| <span data-ttu-id="2c4c3-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c4c3-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c4c3-154"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c4c3-154"><dt>NlsMap.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="2c4c3-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c4c3-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c4c3-156">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="2c4c3-156">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="2c4c3-157">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="2c4c3-157">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="2c4c3-158">Asignar datos de configuración regional</span><span class="sxs-lookup"><span data-stu-id="2c4c3-158">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="2c4c3-159">**LCIDToLocaleName**</span><span class="sxs-lookup"><span data-stu-id="2c4c3-159">**LCIDToLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 
