---
description: Recupera el nombre de configuración regional para el elemento primario de la configuración regional proporcionada.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: Función DownlevelGetParentLocaleName (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: d3a556d68c33249d2e6b49c48035cc58d8bac8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002782"
---
# <a name="downlevelgetparentlocalename-function"></a><span data-ttu-id="e3cd4-103">DownlevelGetParentLocaleName función)</span><span class="sxs-lookup"><span data-stu-id="e3cd4-103">DownlevelGetParentLocaleName function</span></span>

<span data-ttu-id="e3cd4-104">Recupera el [nombre de configuración regional](locale-names.md) para el elemento primario de la configuración regional proporcionada.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-104">Retrieves the [locale name](locale-names.md) for the parent of the supplied locale.</span></span>

> [!Note]  
> <span data-ttu-id="e3cd4-105">Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="e3cd4-106">Su uso requiere el paquete de descarga.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-106">Its use requires the download package.</span></span> <span data-ttu-id="e3cd4-107">Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores deben llamar a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* establecido en [ \_ SPARENT de configuración regional](locale-sparent.md).</span><span class="sxs-lookup"><span data-stu-id="e3cd4-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SPARENT](locale-sparent.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e3cd4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3cd4-108">Syntax</span></span>


```C++
int DownlevelGetParentLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName
);
```



## <a name="parameters"></a><span data-ttu-id="e3cd4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3cd4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3cd4-110">*Configuración regional* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3cd4-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cd4-111">[Identificador de configuración regional](locale-identifiers.md) de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-111">[Locale identifier](locale-identifiers.md) of the locale.</span></span> <span data-ttu-id="e3cd4-112">Puede usar la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para crear un identificador de configuración regional o usar uno de los siguientes valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier or use one of the following predefined values.</span></span>

-   [<span data-ttu-id="e3cd4-113">configuración regional \_ INvariable</span><span class="sxs-lookup"><span data-stu-id="e3cd4-113">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="e3cd4-114">configuración \_ predeterminada del sistema local \_</span><span class="sxs-lookup"><span data-stu-id="e3cd4-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="e3cd4-115">\_valor predeterminado del usuario de configuración regional \_</span><span class="sxs-lookup"><span data-stu-id="e3cd4-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

<span data-ttu-id="e3cd4-116">**Windows Vista y versiones posteriores:** También se admiten los siguientes identificadores de configuración regional personalizados.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-116">**Windows Vista and later:** The following custom locale identifiers are also supported.</span></span>

-   [<span data-ttu-id="e3cd4-117">CONFIGURACIÓN \_ predeterminada personalizada \_</span><span class="sxs-lookup"><span data-stu-id="e3cd4-117">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="e3cd4-118">CONFIGURACIÓN predeterminada de la \_ \_ interfaz de usuario personalizada \_</span><span class="sxs-lookup"><span data-stu-id="e3cd4-118">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="e3cd4-119">configuración regional \_ personalizada no \_ especificada</span><span class="sxs-lookup"><span data-stu-id="e3cd4-119">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> <dt>

<span data-ttu-id="e3cd4-120">*lpName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e3cd4-120">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cd4-121">Puntero a un búfer en el que la función recupera el nombre de la configuración regional primaria, o uno de los siguientes valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-121">Pointer to a buffer in which the function retrieves the parent locale name, or one of the following predefined values.</span></span> <span data-ttu-id="e3cd4-122">Este parámetro se establece en **null** si *cchName* está establecido en 0.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-122">This parameter is set to **NULL** if *cchName* is set to 0.</span></span>

-   [<span data-ttu-id="e3cd4-123">nombre de configuración regional \_ \_ invariable</span><span class="sxs-lookup"><span data-stu-id="e3cd4-123">LOCALE\_NAME\_INVARIANT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="e3cd4-124">nombre de configuración regional \_ \_ predeterminado del sistema \_</span><span class="sxs-lookup"><span data-stu-id="e3cd4-124">LOCALE\_NAME\_SYSTEM\_DEFAULT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="e3cd4-125">nombre de configuración regional \_ \_ predeterminado del usuario \_</span><span class="sxs-lookup"><span data-stu-id="e3cd4-125">LOCALE\_NAME\_USER\_DEFAULT</span></span>](locale-name-constants.md)

</dd> <dt>

<span data-ttu-id="e3cd4-126">*cchName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3cd4-126">*cchName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cd4-127">Tamaño del búfer indicado por *lpName*, en puntos de código UTF-16.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-127">Size of the buffer indicated by *lpName*, in UTF-16 code points.</span></span> <span data-ttu-id="e3cd4-128">Un valor de 0 para este parámetro hace que la función omita el búfer *lpName* y devuelva el tamaño del búfer, en caracteres (caracteres null incluidos), necesario para contener el nombre de la configuración regional primaria.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-128">A value of 0 for this parameter causes the function to ignore the *lpName* buffer and return the size of the buffer, in characters (null characters included), required to contain the parent locale name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3cd4-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3cd4-129">Return value</span></span>

<span data-ttu-id="e3cd4-130">Devuelve el recuento de puntos de código UTF-16 en el nombre de la configuración regional, incluido el carácter nulo de terminación, si es correcto.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-130">Returns the count of UTF-16 code points in the locale name, including the terminating null character, if successful.</span></span>

<span data-ttu-id="e3cd4-131">Esta función devuelve 0 si no se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-131">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="e3cd4-132">Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="e3cd4-132">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="e3cd4-133">ERROR \_ de \_ búfer insuficiente.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-133">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="e3cd4-134">Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **null**.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-134">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="e3cd4-135">ERROR \_ de \_ parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-135">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="e3cd4-136">Cualquiera de los valores de parámetro no era válido.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-136">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3cd4-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3cd4-137">Remarks</span></span>

<span data-ttu-id="e3cd4-138">El archivo de encabezado y DLL necesarios forman parte de la descarga de la "API de asignación de datos de Microsoft NLS Downlevel", disponible en el [centro de descarga de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="e3cd4-138">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3cd4-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3cd4-139">Requirements</span></span>



| <span data-ttu-id="e3cd4-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3cd4-140">Requirement</span></span> | <span data-ttu-id="e3cd4-141">Value</span><span class="sxs-lookup"><span data-stu-id="e3cd4-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3cd4-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3cd4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e3cd4-143">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e3cd4-143">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e3cd4-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3cd4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e3cd4-145">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3cd4-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3cd4-146">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="e3cd4-146">Redistributable</span></span><br/>          | <span data-ttu-id="e3cd4-147">API de asignación de datos de Microsoft NLS Downlevel Windows XP con SP2 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="e3cd4-147">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and later</span></span><br/>  |
| <span data-ttu-id="e3cd4-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3cd4-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3cd4-149"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3cd4-149"><dt>Nlsdl.h</dt></span></span> </dl>    |
| <span data-ttu-id="e3cd4-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e3cd4-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3cd4-151"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3cd4-151"><dt>NlsMap.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3cd4-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3cd4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3cd4-153">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="e3cd4-153">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="e3cd4-154">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="e3cd4-154">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="e3cd4-155">Asignar datos de configuración regional</span><span class="sxs-lookup"><span data-stu-id="e3cd4-155">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="e3cd4-156">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-156">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
