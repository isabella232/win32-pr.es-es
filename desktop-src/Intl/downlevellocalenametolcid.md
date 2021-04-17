---
description: Convierte un nombre de configuración regional en un identificador de configuración regional que se puede utilizar para obtener información del sistema operativo.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: Función DownlevelLocaleNameToLCID (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: c41b82c59b63a5b324e15f89c1f77118d454e428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653005"
---
# <a name="downlevellocalenametolcid-function"></a><span data-ttu-id="c508b-103">DownlevelLocaleNameToLCID función)</span><span class="sxs-lookup"><span data-stu-id="c508b-103">DownlevelLocaleNameToLCID function</span></span>

<span data-ttu-id="c508b-104">Convierte un [nombre de configuración regional](locale-names.md) en un [identificador de configuración regional](locale-identifiers.md) que se puede utilizar para obtener información del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c508b-104">Converts a [locale name](locale-names.md) to a [locale identifier](locale-identifiers.md) that can be used to get information from the operating system.</span></span>

> [!Note]  
> <span data-ttu-id="c508b-105">Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c508b-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="c508b-106">Su uso requiere un paquete de descarga.</span><span class="sxs-lookup"><span data-stu-id="c508b-106">Its use requires a download package.</span></span> <span data-ttu-id="c508b-107">Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores deben llamar a [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) para recuperar un identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="c508b-107">Applications that only run on Windows Vista and later should call [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) to retrieve a locale identifier.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c508b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c508b-108">Syntax</span></span>


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c508b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c508b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c508b-110">*lpName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c508b-110">*lpName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c508b-111">Puntero a una cadena terminada en null que representa un [nombre de configuración regional](locale-names.md).</span><span class="sxs-lookup"><span data-stu-id="c508b-111">Pointer to a null-terminated string representing a [locale name](locale-names.md).</span></span>

</dd> <dt>

<span data-ttu-id="c508b-112">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c508b-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c508b-113">Marcas que especifican el tipo de nombre.</span><span class="sxs-lookup"><span data-stu-id="c508b-113">Flags specifying the type of name.</span></span> <span data-ttu-id="c508b-114">El valor predeterminado es el nombre de la configuración regional de nivel inferior \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c508b-114">The default is DOWNLEVEL\_LOCALE\_NAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c508b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c508b-115">Return value</span></span>

<span data-ttu-id="c508b-116">Devuelve el identificador de configuración regional que corresponde al nombre de la configuración regional si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="c508b-116">Returns the locale identifier that corresponds to the locale name if successful.</span></span>

<span data-ttu-id="c508b-117">La función devuelve 0 si no se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="c508b-117">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="c508b-118">Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="c508b-118">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="c508b-119">ERROR en \_ marcas no válidas \_ .</span><span class="sxs-lookup"><span data-stu-id="c508b-119">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="c508b-120">Los valores proporcionados para marcas no eran válidos.</span><span class="sxs-lookup"><span data-stu-id="c508b-120">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="c508b-121">ERROR \_ de \_ parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="c508b-121">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="c508b-122">Cualquiera de los valores de parámetro no era válido.</span><span class="sxs-lookup"><span data-stu-id="c508b-122">Any of the parameter values were invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="c508b-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c508b-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c508b-124">Esta función no admite configuraciones regionales neutras.</span><span class="sxs-lookup"><span data-stu-id="c508b-124">This function does not support neutral locales.</span></span> <span data-ttu-id="c508b-125">La función [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) equivalente admite [configuraciones regionales personalizadas](custom-locales.md), pero solo para Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c508b-125">The equivalent [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) function supports [custom locales](custom-locales.md), but only for Windows Vista and later.</span></span>

 

<span data-ttu-id="c508b-126">El archivo de encabezado y DLL necesarios forman parte de la descarga de la "API de asignación de datos de Microsoft NLS Downlevel", disponible en el [centro de descarga de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="c508b-126">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="c508b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c508b-127">Requirements</span></span>



| <span data-ttu-id="c508b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c508b-128">Requirement</span></span> | <span data-ttu-id="c508b-129">Value</span><span class="sxs-lookup"><span data-stu-id="c508b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c508b-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c508b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c508b-131">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c508b-131">Windows XP \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="c508b-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c508b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c508b-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c508b-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c508b-134">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="c508b-134">Redistributable</span></span><br/>          | <span data-ttu-id="c508b-135">API de asignación de datos de Microsoft NLS Downlevel Windows XP con SP2 y laterorWindows vista</span><span class="sxs-lookup"><span data-stu-id="c508b-135">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista</span></span><br/> |
| <span data-ttu-id="c508b-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c508b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c508b-137"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c508b-137"><dt>Nlsdl.h</dt></span></span> </dl>                  |
| <span data-ttu-id="c508b-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c508b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c508b-139"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c508b-139"><dt>NlsMap.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="c508b-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c508b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c508b-141">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="c508b-141">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="c508b-142">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="c508b-142">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="c508b-143">Asignar datos de configuración regional</span><span class="sxs-lookup"><span data-stu-id="c508b-143">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="c508b-144">**LocaleNameToLCID**</span><span class="sxs-lookup"><span data-stu-id="c508b-144">**LocaleNameToLCID**</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 
