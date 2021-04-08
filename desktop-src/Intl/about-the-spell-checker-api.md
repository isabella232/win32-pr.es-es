---
description: Para los usuarios de todo el mundo, la entrada de texto es parte de una experiencia informática moderna, para blogs, comentarios, tweets, mensajería instantánea o cualquier otro tipo de escritura de texto. En Windows 8, la revisión ortográfica está integrada en los controles de edición.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: Acerca de la API de revisión ortográfica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d356823e665781052e2a2d5ea98b358155038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910993"
---
# <a name="about-the-spell-checking-api"></a><span data-ttu-id="55333-104">Acerca de la API de revisión ortográfica</span><span class="sxs-lookup"><span data-stu-id="55333-104">About the Spell Checking API</span></span>

<span data-ttu-id="55333-105">Para los usuarios de todo el mundo, la entrada de texto es parte de una experiencia informática moderna, para blogs, comentarios, tweets, mensajería instantánea o cualquier otro tipo de escritura de texto.</span><span class="sxs-lookup"><span data-stu-id="55333-105">For users worldwide, textual input is part of a modern computing experience, for blogging, commenting, tweeting, instant messaging, or any other kind of text typing.</span></span> <span data-ttu-id="55333-106">En Windows 8, la revisión ortográfica está integrada en los controles de edición.</span><span class="sxs-lookup"><span data-stu-id="55333-106">In Windows 8, spell checking is built-in to edit controls.</span></span>

<span data-ttu-id="55333-107">Los desarrolladores pueden usar la API de revisión ortográfica en sus aplicaciones para consumir los servicios de revisión ortográfica disponibles.</span><span class="sxs-lookup"><span data-stu-id="55333-107">Developers can use the spell checking API in their apps to consume available spell checking services.</span></span> <span data-ttu-id="55333-108">Los desarrolladores también pueden crear comprobadores ortográficos que se convierten en proveedores y se integran en el marco de revisión ortográfica de Windows.</span><span class="sxs-lookup"><span data-stu-id="55333-108">Developers can also create spell checkers that become providers and are integrated into the Windows spell checking framework.</span></span>

<span data-ttu-id="55333-109">La API de revisión ortográfica está diseñada para que la usen los desarrolladores profesionales de C/C++ de las aplicaciones de modelo de objetos componentes (COM) de Windows.</span><span class="sxs-lookup"><span data-stu-id="55333-109">The Spell Checking API is designed for use by professional C/C++ developers of Windows Component Object Model (COM) apps.</span></span> <span data-ttu-id="55333-110">No se admite el uso de la API de revisión ortográfica en un servicio de Windows o ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="55333-110">The Spell Checking API is not supported for use in a Windows or ASP.NET service.</span></span>

## <a name="versioning"></a><span data-ttu-id="55333-111">Control de versiones</span><span class="sxs-lookup"><span data-stu-id="55333-111">Versioning</span></span>

<span data-ttu-id="55333-112">La API de revisión ortográfica está disponible a partir de Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="55333-112">The Spell Checking API is available beginning with the Windows 8 or Windows Server 2012.</span></span> <span data-ttu-id="55333-113">Las futuras adiciones a la API se controlarán mediante la creación de nuevas interfaces que se pueden determinar mediante [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en las existentes.</span><span class="sxs-lookup"><span data-stu-id="55333-113">Future additions to the API will be handled by creating new interfaces that can be determined using [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the existing ones.</span></span>

## <a name="interfaces"></a><span data-ttu-id="55333-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="55333-114">Interfaces</span></span>

<span data-ttu-id="55333-115">Todas las interfaces deben liberarse cuando ya no se usen.</span><span class="sxs-lookup"><span data-stu-id="55333-115">All interfaces must be released when they are no longer used.</span></span> <span data-ttu-id="55333-116">Todas **las cadenas (** y los elementos **LPOLESTR** de [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) devueltas (parámetro out) deben liberarse con [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) cuando ya no se usen.</span><span class="sxs-lookup"><span data-stu-id="55333-116">All returned (out parameter) **LPWSTR** strings (and **LPOLESTR** items from [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) must be released with [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) when no longer used.</span></span>

## <a name="error-handling"></a><span data-ttu-id="55333-117">Control de errores</span><span class="sxs-lookup"><span data-stu-id="55333-117">Error handling</span></span>

<span data-ttu-id="55333-118">Los errores se devuelven como **HRESULT** s.</span><span class="sxs-lookup"><span data-stu-id="55333-118">Errors are returned as **HRESULT** s.</span></span> <span data-ttu-id="55333-119">[**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) y [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) no se admiten en esta API.</span><span class="sxs-lookup"><span data-stu-id="55333-119">[**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) and [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) are not supported in this API.</span></span> <span data-ttu-id="55333-120">Los errores no son especialmente accionables salvo los argumentos incorrectos.</span><span class="sxs-lookup"><span data-stu-id="55333-120">Errors are not particularly actionable except for incorrect arguments.</span></span>

<span data-ttu-id="55333-121">Los códigos de error RPC estándar pueden ser devueltos por cualquiera de las llamadas a la API porque son fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="55333-121">Standard RPC error codes may be returned by any of the API calls because they are out-of-proc.</span></span> <span data-ttu-id="55333-122">Se aplican los tiempos de espera de RPC estándar.</span><span class="sxs-lookup"><span data-stu-id="55333-122">Standard RPC timeouts apply.</span></span>

## <a name="security"></a><span data-ttu-id="55333-123">Seguridad</span><span class="sxs-lookup"><span data-stu-id="55333-123">Security</span></span>

<span data-ttu-id="55333-124">La API de revisión ortográfica puede cargar código externo (proveedores de corrector ortográfico).</span><span class="sxs-lookup"><span data-stu-id="55333-124">The Spell Checking API may load external code (spell check providers).</span></span> <span data-ttu-id="55333-125">Este código se ejecutará fuera de proceso y en un contexto de seguridad restringido.</span><span class="sxs-lookup"><span data-stu-id="55333-125">It will run this code out-of-proc and under a restricted security context.</span></span>

## <a name="dictionary-files"></a><span data-ttu-id="55333-126">Archivos de Diccionario</span><span class="sxs-lookup"><span data-stu-id="55333-126">Dictionary files</span></span>

<span data-ttu-id="55333-127">Los diccionarios específicos del usuario para un idioma, que contienen el contenido de las listas de palabras agregadas, excluidas y de Autocorrección, se encuentran en% AppData% \\ Microsoft \\ Spelling \\ *<language tag>* .</span><span class="sxs-lookup"><span data-stu-id="55333-127">The user-specific dictionaries for a language, which hold the content for the Added, Excluded, and AutoCorrect word lists, are located under %AppData%\\Microsoft\\Spelling\\*<language tag>*.</span></span> <span data-ttu-id="55333-128">Los nombres de archivo son default. dic (agregado), default. exc (Excluded) y default. ACL (Autocorrección).</span><span class="sxs-lookup"><span data-stu-id="55333-128">The filenames are default.dic (Added), default.exc (Excluded) and default.acl (AutoCorrect).</span></span> <span data-ttu-id="55333-129">Los archivos son texto sin formato UTF-16 LE que debe comenzar con la marca de orden de bytes (BOM) adecuada.</span><span class="sxs-lookup"><span data-stu-id="55333-129">The files are UTF-16 LE plaintext that must start with the appropriate Byte Order Mark (BOM).</span></span> <span data-ttu-id="55333-130">Cada línea contiene una palabra (en las listas de palabras agregadas y excluidas) o un par de Autocorrección con las palabras separadas por una barra vertical (" \| ") (en la lista de palabras de Autocorrección).</span><span class="sxs-lookup"><span data-stu-id="55333-130">Each line contains a word (in the Added and Excluded word lists), or an autocorrect pair with the words separated by a vertical bar ("\|") (in the AutoCorrect word list).</span></span> <span data-ttu-id="55333-131">Otros archivos. dic,. exc y. ACL presentes en el directorio serán detectados por el servicio de revisión ortográfica y agregados a las listas de palabras de usuario.</span><span class="sxs-lookup"><span data-stu-id="55333-131">Other .dic, .exc, and .acl files present in the directory will be detected by the spell checking service and added to the user word lists.</span></span> <span data-ttu-id="55333-132">Estos archivos se consideran de solo lectura y no se modifican mediante la API de revisión ortográfica.</span><span class="sxs-lookup"><span data-stu-id="55333-132">These files are considered to be read-only and are not modified by the spell checking API.</span></span>

## <a name="installing-a-spell-checking-provider"></a><span data-ttu-id="55333-133">Instalación de un proveedor de revisión ortográfica</span><span class="sxs-lookup"><span data-stu-id="55333-133">Installing a spell checking provider</span></span>

<span data-ttu-id="55333-134">La instalación de un proveedor de revisión ortográfica debe colocar todos los archivos que utiliza en una ubicación que permita el acceso de lectura desde el SID ([identificador de seguridad](../secauthz/security-identifiers.md)) "todos los paquetes de aplicación".</span><span class="sxs-lookup"><span data-stu-id="55333-134">The installation of a spell checking provider must place all the files it uses in a location that allows read access from the SID ([security identifier](../secauthz/security-identifiers.md)) "ALL APPLICATION PACKAGES".</span></span> <span data-ttu-id="55333-135">Instalarlo en una carpeta en "archivos de programa" funciona bien.</span><span class="sxs-lookup"><span data-stu-id="55333-135">Installing it in a folder under "Program Files" works well.</span></span> <span data-ttu-id="55333-136">Además, el proveedor debe establecer algunas claves en el registro para que aparezcan en la API de revisión ortográfica.</span><span class="sxs-lookup"><span data-stu-id="55333-136">Also, the provider must set some keys in the registry for it to appear to the spell checking API.</span></span> <span data-ttu-id="55333-137">Puede estar en el subárbol del \_ usuario actual HKEY \_ o en el \_ \_ subárbol del equipo local HKEY, en función de si debe instalarse solo para el usuario actual o para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="55333-137">It can be in either the HKEY\_CURRENT\_USER hive or the HKEY\_LOCAL\_MACHINE hive depending on whether it should install only for the current user or all users.</span></span>


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



<span data-ttu-id="55333-138">El [ejemplo de proveedor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) de revisión ortográfica proporciona un ejemplo del registro necesario para instalar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="55333-138">The [spell checking provider sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) provides an example of the registration needed to install a provider.</span></span>

<span data-ttu-id="55333-139">Si va a crear nuevas opciones de revisión ortográfica para un proveedor de revisión ortográfica, consulte [**IOptionDescription:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) para obtener instrucciones sobre la nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="55333-139">If you are creating new spell checking options for a spell checking provider, see [**IOptionDescription::Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) for guidance on naming.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55333-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55333-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55333-141">Referencia de la API de revisión ortográfica</span><span class="sxs-lookup"><span data-stu-id="55333-141">Spell Checking API Reference</span></span>](spell-checker-api-reference.md)
</dt> <dt>

[<span data-ttu-id="55333-142">Ejemplo de cliente de revisión ortográfica</span><span class="sxs-lookup"><span data-stu-id="55333-142">Spell checking client sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[<span data-ttu-id="55333-143">Ejemplo de proveedor de revisión ortográfica</span><span class="sxs-lookup"><span data-stu-id="55333-143">Spell checking provider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[<span data-ttu-id="55333-144">**IOptionDescription:: ID**</span><span class="sxs-lookup"><span data-stu-id="55333-144">**IOptionDescription::Id**</span></span>](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[<span data-ttu-id="55333-145">**IEnumString**</span><span class="sxs-lookup"><span data-stu-id="55333-145">**IEnumString**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

<span data-ttu-id="55333-146">[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="55333-146">[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
</dt> </dl>

 

 
