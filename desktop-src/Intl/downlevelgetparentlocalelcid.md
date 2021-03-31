---
description: Recupera el identificador de configuración regional para el elemento primario de la configuración regional proporcionada.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: Función DownlevelGetParentLocaleLCID (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b34f30425147057efe8039cc36514d699199c9a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361228"
---
# <a name="downlevelgetparentlocalelcid-function"></a><span data-ttu-id="72638-103">DownlevelGetParentLocaleLCID función)</span><span class="sxs-lookup"><span data-stu-id="72638-103">DownlevelGetParentLocaleLCID function</span></span>

<span data-ttu-id="72638-104">Recupera el [identificador de configuración regional](locale-identifiers.md) para el elemento primario de la configuración regional proporcionada.</span><span class="sxs-lookup"><span data-stu-id="72638-104">Retrieves the [locale identifier](locale-identifiers.md) for the parent of the supplied locale.</span></span>

> [!Note]  
> <span data-ttu-id="72638-105">Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="72638-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="72638-106">Su uso requiere el paquete de descarga.</span><span class="sxs-lookup"><span data-stu-id="72638-106">Its use requires the download package.</span></span> <span data-ttu-id="72638-107">Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores deben llamar a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* establecido en [ \_ SPARENT de configuración regional](locale-sparent.md).</span><span class="sxs-lookup"><span data-stu-id="72638-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SPARENT](locale-sparent.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="72638-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72638-108">Syntax</span></span>


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a><span data-ttu-id="72638-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72638-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72638-110">*Configuración regional* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72638-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72638-111">Identificador de configuración regional de la configuración regional para la que se va a recuperar el identificador de configuración regional primaria.</span><span class="sxs-lookup"><span data-stu-id="72638-111">Locale identifier of the locale for which to retrieve the parent locale identifier.</span></span> <span data-ttu-id="72638-112">Puede usar la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para crear un identificador de configuración regional o usar uno de los siguientes valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="72638-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier or use one of the following predefined values.</span></span>

-   [<span data-ttu-id="72638-113">configuración regional \_ INvariable</span><span class="sxs-lookup"><span data-stu-id="72638-113">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="72638-114">configuración \_ predeterminada del sistema local \_</span><span class="sxs-lookup"><span data-stu-id="72638-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="72638-115">\_valor predeterminado del usuario de configuración regional \_</span><span class="sxs-lookup"><span data-stu-id="72638-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

<span data-ttu-id="72638-116">**Windows Vista y versiones posteriores:** También se admiten los siguientes identificadores de configuración regional personalizados.</span><span class="sxs-lookup"><span data-stu-id="72638-116">**Windows Vista and later:** The following custom locale identifiers are also supported.</span></span>

-   [<span data-ttu-id="72638-117">CONFIGURACIÓN \_ predeterminada personalizada \_</span><span class="sxs-lookup"><span data-stu-id="72638-117">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="72638-118">CONFIGURACIÓN predeterminada de la \_ \_ interfaz de usuario personalizada \_</span><span class="sxs-lookup"><span data-stu-id="72638-118">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="72638-119">configuración regional \_ personalizada no \_ especificada</span><span class="sxs-lookup"><span data-stu-id="72638-119">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72638-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72638-120">Return value</span></span>

<span data-ttu-id="72638-121">Devuelve el identificador de configuración regional principal si se realiza correctamente o 0 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="72638-121">Returns the parent locale identifier if successful, or 0 otherwise.</span></span> <span data-ttu-id="72638-122">Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="72638-122">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="72638-123">ERROR \_ de \_ parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="72638-123">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="72638-124">Cualquiera de los valores de parámetro no era válido.</span><span class="sxs-lookup"><span data-stu-id="72638-124">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="72638-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72638-125">Remarks</span></span>

<span data-ttu-id="72638-126">El archivo de encabezado y DLL necesarios forman parte de la descarga de la "API de asignación de datos de Microsoft NLS Downlevel", disponible en el [centro de descarga de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="72638-126">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="72638-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72638-127">Requirements</span></span>



| <span data-ttu-id="72638-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="72638-128">Requirement</span></span> | <span data-ttu-id="72638-129">Value</span><span class="sxs-lookup"><span data-stu-id="72638-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72638-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72638-130">Minimum supported client</span></span><br/> | <span data-ttu-id="72638-131">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="72638-131">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="72638-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72638-132">Minimum supported server</span></span><br/> | <span data-ttu-id="72638-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="72638-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72638-134">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="72638-134">Redistributable</span></span><br/>          | <span data-ttu-id="72638-135">API de asignación de datos de Microsoft NLS Downlevel Windows XPor vista</span><span class="sxs-lookup"><span data-stu-id="72638-135">Microsoft NLS Downlevel Data Mapping APIs onWindows XPor Windows Vista</span></span><br/>     |
| <span data-ttu-id="72638-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72638-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="72638-137"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="72638-137"><dt>Nlsdl.h</dt></span></span> </dl>    |
| <span data-ttu-id="72638-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="72638-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72638-139"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72638-139"><dt>NlsMap.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72638-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="72638-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72638-141">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="72638-141">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="72638-142">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="72638-142">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="72638-143">Asignar datos de configuración regional</span><span class="sxs-lookup"><span data-stu-id="72638-143">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="72638-144">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="72638-144">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
