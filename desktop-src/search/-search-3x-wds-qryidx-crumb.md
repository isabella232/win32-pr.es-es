---
description: Comprenda cómo usar el argumento CRUMB en Windows Search para controlar el ámbito de una búsqueda.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Argumento CRUMB (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f56287c7182c0cf370250d53075a1c951ddf28b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403738"
---
# <a name="crumb-argument-windows-search"></a><span data-ttu-id="2f782-103">Argumento CRUMB (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="2f782-103">CRUMB Argument (Windows Search)</span></span>

<span data-ttu-id="2f782-104">El argumento admite instrucciones de sintaxis de consulta avanzada (AQS) completa y es especialmente útil como medio de controlar el `crumb` ámbito de una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2f782-104">The `crumb` argument supports full Advanced Query Syntax (AQS) statements and is especially useful as a means of controlling the scope of a search.</span></span> <span data-ttu-id="2f782-105">Además de los argumentos de AQS, el argumento puede tomar un parámetro especial en Windows Vista y los parámetros y en XP, como se describe más `crumb` `location` adelante en este `kind` `store` tema.</span><span class="sxs-lookup"><span data-stu-id="2f782-105">In addition to AQS ements, the `crumb` argument can take a special `location` parameter on Windows Vista and `kind` and `store` parameters on XP, as described later in this topic.</span></span>

<span data-ttu-id="2f782-106">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="2f782-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="2f782-107">Sintaxis de crumb</span><span class="sxs-lookup"><span data-stu-id="2f782-107">Crumb Syntax</span></span>](#crumb-syntax)
    -   [<span data-ttu-id="2f782-108">Ejemplos generales</span><span class="sxs-lookup"><span data-stu-id="2f782-108">General Examples</span></span>](#general-examples)
-   [<span data-ttu-id="2f782-109">Uso de crumb con Vista (ubicación)</span><span class="sxs-lookup"><span data-stu-id="2f782-109">Using crumb with Vista (location)</span></span>](#using-crumb-with-vista-location)
    -   [<span data-ttu-id="2f782-110">Ejemplos de Vista</span><span class="sxs-lookup"><span data-stu-id="2f782-110">Vista Examples</span></span>](#vista-examples)
    -   [<span data-ttu-id="2f782-111">Constantes para carpetas comunes</span><span class="sxs-lookup"><span data-stu-id="2f782-111">Constants for Common Folders</span></span>](#constants-for-common-folders)
-   [<span data-ttu-id="2f782-112">Uso de crumb con Windows XP (tipo y tienda)</span><span class="sxs-lookup"><span data-stu-id="2f782-112">Using crumb with Windows XP (kind and store)</span></span>](#using-crumb-with-windows-xp-kind-and-store)
    -   [<span data-ttu-id="2f782-113">Ejemplos de XP</span><span class="sxs-lookup"><span data-stu-id="2f782-113">XP Examples</span></span>](#xp-examples)
-   [<span data-ttu-id="2f782-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f782-114">Related topics</span></span>](#related-topics)

 

## <a name="crumb-syntax"></a><span data-ttu-id="2f782-115">Sintaxis de crumb</span><span class="sxs-lookup"><span data-stu-id="2f782-115">Crumb Syntax</span></span>

<span data-ttu-id="2f782-116">La sintaxis crumb es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="2f782-116">The crumb syntax is as follows:</span></span>


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



<span data-ttu-id="2f782-117">La <column> parte es cualquier propiedad del sistema de propiedades y</span><span class="sxs-lookup"><span data-stu-id="2f782-117">The <column> portion is any property in the property system, and the</span></span> <value> <span data-ttu-id="2f782-118">portion es un valor válido para esa propiedad.</span><span class="sxs-lookup"><span data-stu-id="2f782-118">portion is a valid value for that property.</span></span> <span data-ttu-id="2f782-119">La <label> parte es un alias opcional para la propiedad que se muestra como una sugerencia de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="2f782-119">The <label> portion is an optional alias for the property that displays as a user interface hint.</span></span>

### <a name="general-examples"></a><span data-ttu-id="2f782-120">Ejemplos generales</span><span class="sxs-lookup"><span data-stu-id="2f782-120">General Examples</span></span>


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a><span data-ttu-id="2f782-121">Uso de crumb con Vista (ubicación)</span><span class="sxs-lookup"><span data-stu-id="2f782-121">Using crumb with Vista (location)</span></span>

<span data-ttu-id="2f782-122">En el parámetro crumb, Windows Vista admite AQS completo y también la propiedad , que tiene una implementación especial `location` disponible solo en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2f782-122">In the crumb parameter, Windows Vista supports full AQS and also the `location` property, which has a special implementation available only on Windows Vista.</span></span> <span data-ttu-id="2f782-123">Puede usar una cadena de AQS o la propiedad dentro `location` de un único parámetro crumb, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="2f782-123">You can use either an AQS string or the `location` property within a single crumb parameter, but not both.</span></span> <span data-ttu-id="2f782-124">Si el parámetro crumb incluye AQS, se omite todo lo demás en ese parámetro crumb.</span><span class="sxs-lookup"><span data-stu-id="2f782-124">If the crumb parameter includes AQS, everything else in that crumb parameter is ignored.</span></span>

<span data-ttu-id="2f782-125">La `location` propiedad permite especificar una ruta de acceso para buscar.</span><span class="sxs-lookup"><span data-stu-id="2f782-125">The `location` property enables you to specify a path to search.</span></span> <span data-ttu-id="2f782-126">Windows Vista puede omitir el indexador y recorrer el directorio directamente si la ubicación está fuera del ámbito de rastreo del indexador.</span><span class="sxs-lookup"><span data-stu-id="2f782-126">Windows Vista can bypass the Indexer and traverse the directory directly if the location is outside the Indexer's crawl scope.</span></span> <span data-ttu-id="2f782-127">Por lo tanto, estas búsquedas pueden ser más lentas que las búsquedas que usan el indexador.</span><span class="sxs-lookup"><span data-stu-id="2f782-127">Consequently, these searches may be slower than searches that use the Indexer.</span></span>

<span data-ttu-id="2f782-128">Al especificar una `location` propiedad, se admiten dos parámetros adicionales y opcionales:</span><span class="sxs-lookup"><span data-stu-id="2f782-128">When you specify a `location` property, two additional parameters are supported and optional:</span></span>



| <span data-ttu-id="2f782-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2f782-129">Parameter</span></span> | <span data-ttu-id="2f782-130">Valores</span><span class="sxs-lookup"><span data-stu-id="2f782-130">Values</span></span>                  | <span data-ttu-id="2f782-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f782-131">Description</span></span>                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f782-132">Inserción</span><span class="sxs-lookup"><span data-stu-id="2f782-132">inclusion</span></span> | <span data-ttu-id="2f782-133">include, exclude</span><span class="sxs-lookup"><span data-stu-id="2f782-133">include, exclude</span></span>        | <span data-ttu-id="2f782-134">Especifica si la consulta debe incluir o excluir elementos de esa ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="2f782-134">Specifies whether the query should include or exclude items from that path.</span></span> <span data-ttu-id="2f782-135">"Include" es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2f782-135">"Include" is the default.</span></span> <span data-ttu-id="2f782-136">Windows Vista no admite exclusiones sin inclusiones.</span><span class="sxs-lookup"><span data-stu-id="2f782-136">Windows Vista does not support exclusions without inclusions.</span></span> <span data-ttu-id="2f782-137">(Vea el ejemplo)</span><span class="sxs-lookup"><span data-stu-id="2f782-137">(See example)</span></span> |
| <span data-ttu-id="2f782-138">recursión</span><span class="sxs-lookup"><span data-stu-id="2f782-138">recursion</span></span> | <span data-ttu-id="2f782-139">recursiva, no recursiva</span><span class="sxs-lookup"><span data-stu-id="2f782-139">recursive, nonrecursive</span></span> | <span data-ttu-id="2f782-140">Especifica si la búsqueda debe repetir todas las subcarpetas a partir del valor definido en la ubicación:</span><span class="sxs-lookup"><span data-stu-id="2f782-140">Specifies whether the search should recurse all subfolders starting from the value defined in the location:</span></span><value><span data-ttu-id="2f782-141">.</span><span class="sxs-lookup"><span data-stu-id="2f782-141">.</span></span> <span data-ttu-id="2f782-142">"Recursive" es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2f782-142">"Recursive" is the default.</span></span>                             |



 

<span data-ttu-id="2f782-143">Para el ámbito de una búsqueda mediante el protocolo search-ms:, tiene diferentes opciones en función del destino del ámbito.</span><span class="sxs-lookup"><span data-stu-id="2f782-143">To scope a search using the search-ms: protocol, you have different options depending on the target of the scope.</span></span>

<span data-ttu-id="2f782-144">Carpeta en una máquina local:</span><span class="sxs-lookup"><span data-stu-id="2f782-144">Folder on a local machine:</span></span>

-   <span data-ttu-id="2f782-145">Usar AQS (crumb=folder:<ruta de acceso con codificación URL>)</span><span class="sxs-lookup"><span data-stu-id="2f782-145">Use AQS (crumb=folder:<URL-encoded path>)</span></span>
-   <span data-ttu-id="2f782-146">Uso del argumento location (crumb=location:<ruta de acceso codificada con dirección URL>)</span><span class="sxs-lookup"><span data-stu-id="2f782-146">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="2f782-147">Carpeta en una máquina o red remota:</span><span class="sxs-lookup"><span data-stu-id="2f782-147">Folder on a remote machine/network:</span></span>

-   <span data-ttu-id="2f782-148">Uso del argumento location (crumb=location:<ruta de acceso codificada con dirección URL>)</span><span class="sxs-lookup"><span data-stu-id="2f782-148">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="2f782-149">Carpeta a la que se accede a través de un controlador de protocolo UNC conocido:</span><span class="sxs-lookup"><span data-stu-id="2f782-149">Folder accessed via a known UNC protocol handler:</span></span>

-   <span data-ttu-id="2f782-150">Use AQS (crumb=store: <UNC protocol handler name> )</span><span class="sxs-lookup"><span data-stu-id="2f782-150">Use AQS (crumb=store:<UNC protocol handler name>)</span></span>
-   <span data-ttu-id="2f782-151">Uso del argumento location (crumb=location:<ruta de acceso codificada con dirección URL>)</span><span class="sxs-lookup"><span data-stu-id="2f782-151">Use location argument (crumb=location:<URL-encoded path>)</span></span>

### <a name="vista-examples"></a><span data-ttu-id="2f782-152">Ejemplos de Vista</span><span class="sxs-lookup"><span data-stu-id="2f782-152">Vista Examples</span></span>


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



<span data-ttu-id="2f782-153">En el primer ejemplo se ejecuta una búsqueda de "vacaciones" a partir de la ubicación shell://Personal (un acceso directo especial a la carpeta Mis documentos del usuario), incluida esa carpeta y todas las subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="2f782-153">The first example executes a search for "vacation" starting at the shell://Personal location (a special shortcut to the user's My Documents folder), including that folder and all subfolders.</span></span> <span data-ttu-id="2f782-154">Consulte la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2f782-154">See table below.</span></span>

<span data-ttu-id="2f782-155">En el segundo ejemplo se ejecuta una búsqueda en C: \\ Imágenes, pero no en C: \\ Imágenes \\ duplicadas.</span><span class="sxs-lookup"><span data-stu-id="2f782-155">The second example executes a search within C:\\Pictures, but not in C:\\Pictures\\Duplicates.</span></span>

<span data-ttu-id="2f782-156">En el tercer ejemplo se ejecuta una búsqueda en C: Documentos, limitado a archivos con la propiedad \\ kind establecida en imágenes.</span><span class="sxs-lookup"><span data-stu-id="2f782-156">The third example executes a search within C:\\Documents, limited to files with the kind property set to pics.</span></span>

### <a name="constants-for-common-folders"></a><span data-ttu-id="2f782-157">Constantes para carpetas comunes</span><span class="sxs-lookup"><span data-stu-id="2f782-157">Constants for Common Folders</span></span>

<span data-ttu-id="2f782-158">Windows Vista permite el uso de valores [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) que proporcionan una manera única independiente del sistema de identificar las carpetas especiales usadas con frecuencia por las aplicaciones, pero que pueden no tener el mismo nombre o ubicación en un sistema determinado.</span><span class="sxs-lookup"><span data-stu-id="2f782-158">Windows Vista enables the use of [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) values that provide a unique system-independent way to identify special folders used frequently by applications, but which may not have the same name or location on any given system.</span></span> <span data-ttu-id="2f782-159">Por ejemplo, la carpeta del sistema puede ser "C: Windows" en \\ un sistema y "C: \\ Winnt" en otro.</span><span class="sxs-lookup"><span data-stu-id="2f782-159">For example, the system folder may be "C:\\Windows" on one system and "C:\\Winnt" on another.</span></span> <span data-ttu-id="2f782-160">Antes de Windows Vista, [se usaban los CSID.](/windows/desktop/shell/csidl)</span><span class="sxs-lookup"><span data-stu-id="2f782-160">Prior to Windows Vista, [CSIDLs](/windows/desktop/shell/csidl) were used.</span></span>

<span data-ttu-id="2f782-161">Use estas ubicaciones con esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="2f782-161">Use these locations with this syntax:</span></span>


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a><span data-ttu-id="2f782-162">Uso de crumb con Windows XP (tipo y tienda)</span><span class="sxs-lookup"><span data-stu-id="2f782-162">Using crumb with Windows XP (kind and store)</span></span>

<span data-ttu-id="2f782-163">Por Windows Search en Windows XP (WDS 3.x), los términos "kind" y "store" de AQS tienen una implementación especial.</span><span class="sxs-lookup"><span data-stu-id="2f782-163">For Windows Search on Windows XP (WDS 3.x), the AQS terms "kind" and "store" have a special implementation.</span></span> <span data-ttu-id="2f782-164">Los valores "kind" son los mismos [que se usan en WDS 2.x.](../lwef/-search-2x-wds-perceivedtype.md)</span><span class="sxs-lookup"><span data-stu-id="2f782-164">The "kind" values are the same [values used in WDS 2.x](../lwef/-search-2x-wds-perceivedtype.md).</span></span> <span data-ttu-id="2f782-165">Entre los valores de "store" se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2f782-165">The "store" values include the following:</span></span>

-   <span data-ttu-id="2f782-166">Mapi</span><span class="sxs-lookup"><span data-stu-id="2f782-166">mapi</span></span>
-   <span data-ttu-id="2f782-167">archivo</span><span class="sxs-lookup"><span data-stu-id="2f782-167">file</span></span>
-   <span data-ttu-id="2f782-168">outlookexpress</span><span class="sxs-lookup"><span data-stu-id="2f782-168">outlookexpress</span></span>
-   <span data-ttu-id="2f782-169">cualquiera</span><span class="sxs-lookup"><span data-stu-id="2f782-169">any</span></span>

### <a name="xp-examples"></a><span data-ttu-id="2f782-170">Ejemplos de XP</span><span class="sxs-lookup"><span data-stu-id="2f782-170">XP Examples</span></span>


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



<span data-ttu-id="2f782-171">En el primer ejemplo se devuelven correos electrónicos de Microsoft Outlook Express de John con la etiqueta personalizada "Correo electrónico de E/S".</span><span class="sxs-lookup"><span data-stu-id="2f782-171">The first example returns Microsoft Outlook Express emails from John with the custom label, "OE Mail".</span></span> <span data-ttu-id="2f782-172">En el segundo ejemplo se ejecuta una búsqueda de cualquier comunicación de John.</span><span class="sxs-lookup"><span data-stu-id="2f782-172">The second example executes a search for any communication from John.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f782-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f782-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f782-174">Tareas iniciales con Parameter-Value argumentos</span><span class="sxs-lookup"><span data-stu-id="2f782-174">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="2f782-175">Argumentos del identificador de configuración regional</span><span class="sxs-lookup"><span data-stu-id="2f782-175">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="2f782-176">Argumento SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f782-176">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="2f782-177">Argumento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="2f782-177">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="2f782-178">Argumento SUBQUERY</span><span class="sxs-lookup"><span data-stu-id="2f782-178">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
