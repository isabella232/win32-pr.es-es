---
description: 'La búsqueda: el protocolo de aplicación es una Convención extensible para llamar a la aplicación de búsqueda en el escritorio en Windows Vista con Service Pack 1 (SP1) y versiones posteriores.'
title: Usar el protocolo de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 91a1ec25-f6ab-4377-8478-20bc51a1d5df
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a9223a2a30cab85f8e1b0dac0d0df2dc4fe8f80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997881"
---
# <a name="using-the-search-protocol"></a><span data-ttu-id="9f471-103">Usar el protocolo de búsqueda</span><span class="sxs-lookup"><span data-stu-id="9f471-103">Using the search Protocol</span></span>

<span data-ttu-id="9f471-104">La **búsqueda:** el [Protocolo de aplicación](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) es una Convención extensible para llamar a la aplicación de búsqueda en el escritorio en Windows Vista con Service Pack 1 (SP1) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9f471-104">The **search:** [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is an extensible convention for calling the desktop search application on Windows Vista with Service Pack 1 (SP1) and later versions.</span></span> <span data-ttu-id="9f471-105">El protocolo se creó en Windows Vista con SP1 (para obtener información, consulte el artículo [de Knowledge Base información general sobre los cambios de Windows Vista Desktop Search en Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) para proporcionar a Windows una forma de determinar y llamar a la aplicación de búsqueda de escritorio predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9f471-105">The protocol was created in Windows Vista with SP1 (for information see the Knowledge Base article [Overview of Windows Vista desktop search Changes in Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) to give Windows a way to determine and call the default desktop search application.</span></span>

<span data-ttu-id="9f471-106">La sintaxis del protocolo proporciona una serie de parámetros útiles para realizar búsquedas de escritorio comunes, como los términos de búsqueda especificados por el usuario o la ubicación en la que se inició la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9f471-106">The protocol syntax provides a number of parameters useful for performing common desktop searches, such as user-entered search terms or the location on which the search was begun.</span></span> <span data-ttu-id="9f471-107">Cuando los usuarios buscan desde uno de los dos puntos de entrada de búsqueda disponibles (el menú **Inicio** o el explorador de Windows), el sistema operativo usa el protocolo de búsqueda para iniciar la aplicación de búsqueda en el escritorio predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9f471-107">When users search from one of the two available search entry points (either the **Start** menu or Windows Explorer), the operating system uses the search protocol to launch the default desktop search application.</span></span> <span data-ttu-id="9f471-108">Para ello, se agregan los términos de búsqueda especificados por el usuario a la sintaxis del Protocolo de búsqueda estándar y se pasa esa información a la aplicación registrada como aplicación de búsqueda predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9f471-108">It does this by adding the user-entered search terms to the standard search protocol syntax and passing that information to the application registered as the default search application.</span></span>

<span data-ttu-id="9f471-109">Si no se instala ninguna otra aplicación de búsqueda en el escritorio, una búsqueda introducida en estos puntos de entrada inicia el explorador de Windows Search.</span><span class="sxs-lookup"><span data-stu-id="9f471-109">If no other desktop search applications are installed, a search entered into these entry points launches the Windows Search Explorer.</span></span> <span data-ttu-id="9f471-110">Sin embargo, los desarrolladores de terceros pueden crear, instalar y registrar sus aplicaciones para administrar el protocolo de búsqueda y ser la aplicación de búsqueda predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9f471-110">However, third-party developers can create, install, and register their applications to handle the search protocol and to be the default search application.</span></span> <span data-ttu-id="9f471-111">Dichas aplicaciones deben admitir la sintaxis del Protocolo de búsqueda y registrarse con la característica [programas predeterminados](default-programs.md) para garantizar una experiencia sin problemas con Windows.</span><span class="sxs-lookup"><span data-stu-id="9f471-111">Such applications need to support the search protocol syntax and register with the [Default Programs](default-programs.md) feature to ensure a seamless experience with Windows.</span></span>

<span data-ttu-id="9f471-112">Si desarrolla una aplicación pensada para usarse o basarse en una aplicación de búsqueda de escritorio específica, no debe depender exclusivamente de la **búsqueda:** el protocolo.</span><span class="sxs-lookup"><span data-stu-id="9f471-112">If you develop an application that is intended to use or build upon a specific desktop search application, you should not depend exclusively on the **search:** protocol.</span></span> <span data-ttu-id="9f471-113">Dado que muchas aplicaciones podrían poseer el protocolo **Search:** , no hay ninguna garantía de que la aplicación de búsqueda de escritorio de destino la posea en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="9f471-113">Because many applications could own the **search:** protocol, there is no guarantee that your targeted desktop search application will own it at any given time.</span></span> <span data-ttu-id="9f471-114">En su lugar, debe usar un protocolo de búsqueda privado definido por esa aplicación de búsqueda de escritorio de destino.</span><span class="sxs-lookup"><span data-stu-id="9f471-114">Instead, you should use a private search protocol defined by that targeted desktop search application.</span></span> <span data-ttu-id="9f471-115">Esto significa que las aplicaciones de búsqueda en el escritorio destinadas a ser una plataforma para aplicaciones de terceros deben admitir el protocolo **Search:** y su propio protocolo de búsqueda de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9f471-115">This means that desktop search applications intended to be a platform for third-party applications should support both the **search:** protocol and their own proprietary search protocol.</span></span>

> [!Note]  
> <span data-ttu-id="9f471-116">El protocolo **Search:** no reemplaza el propietario [Search-MS:](../search/-search-3x-wds-qryidx-searchms.md) Protocol.</span><span class="sxs-lookup"><span data-stu-id="9f471-116">The **search:** protocol does not replace the proprietary [search-ms:](../search/-search-3x-wds-qryidx-searchms.md) protocol.</span></span> <span data-ttu-id="9f471-117">Las aplicaciones pueden seguir usando la **búsqueda-MS:** protocolo para iniciar el explorador de búsqueda de ventanas o para consultar el indizador de Windows Search de forma silenciosa.</span><span class="sxs-lookup"><span data-stu-id="9f471-117">Applications can still use the **search-ms:** protocol to launch Window Search Explorer or to silently query the Windows Search indexer.</span></span>

 

<span data-ttu-id="9f471-118">En este tema se trata lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9f471-118">This topic covers the following:</span></span>

-   [<span data-ttu-id="9f471-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f471-119">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="9f471-120">Windows Vista con SP1 uso de la búsqueda: Protocolo</span><span class="sxs-lookup"><span data-stu-id="9f471-120">Windows Vista with SP1 use of the search: protocol</span></span>](#windows-vista-with-sp1-use-of-the-search-protocol)
-   [<span data-ttu-id="9f471-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9f471-121">Examples</span></span>](#examples)
-   [<span data-ttu-id="9f471-122">Registro de la aplicación que controla el protocolo</span><span class="sxs-lookup"><span data-stu-id="9f471-122">Registering the Application that Handles the Protocol</span></span>](#registering-the-application-that-handles-the-protocol)
    -   [<span data-ttu-id="9f471-123">Entradas del registro</span><span class="sxs-lookup"><span data-stu-id="9f471-123">Registry Entries</span></span>](#registry-entries)
-   [<span data-ttu-id="9f471-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f471-124">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="9f471-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f471-125">Syntax</span></span>

<span data-ttu-id="9f471-126">El protocolo de búsqueda usa la siguiente sintaxis codificada como dirección URL estándar:</span><span class="sxs-lookup"><span data-stu-id="9f471-126">The search protocol uses the following standard URL-encoded syntax:</span></span>


```C++
search:parameter=value[&parameter=value]&
```



<span data-ttu-id="9f471-127">La sintaxis comienza por identificar el protocolo en sí (**Buscar:**).</span><span class="sxs-lookup"><span data-stu-id="9f471-127">The syntax begins by identifying the protocol itself (**search:**).</span></span> <span data-ttu-id="9f471-128">Los pares de parámetro/valor son argumentos pasados al motor de búsqueda, como se describe en la tabla siguiente, que muestra todos los parámetros posibles para la sintaxis del Protocolo de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9f471-128">The parameter/value pairs are arguments passed to the Search engine, as described in the following table, which shows all of the possible parameters for the search protocol syntax.</span></span>



| <span data-ttu-id="9f471-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9f471-129">Parameter</span></span>                                              | <span data-ttu-id="9f471-130">Value</span><span class="sxs-lookup"><span data-stu-id="9f471-130">Value</span></span>                                                         | <span data-ttu-id="9f471-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f471-131">Description</span></span>                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f471-132">Query</span><span class="sxs-lookup"><span data-stu-id="9f471-132">query</span></span>                                                  | <span data-ttu-id="9f471-133">Texto con codificación URL</span><span class="sxs-lookup"><span data-stu-id="9f471-133">URL-encoded text</span></span>                                              | <span data-ttu-id="9f471-134">Texto de la consulta escrito por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9f471-134">The query text entered by the user.</span></span>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="9f471-135">inputlocale</span><span class="sxs-lookup"><span data-stu-id="9f471-135">inputlocale</span></span>](search-protocol-localeidentifiers.md)   | <span data-ttu-id="9f471-136">Cualquier identificador de código de idioma (LCID) válido</span><span class="sxs-lookup"><span data-stu-id="9f471-136">Any valid language code identifier (LCID)</span></span>                     | <span data-ttu-id="9f471-137">LCID que identifica el idioma de entrada de la consulta.</span><span class="sxs-lookup"><span data-stu-id="9f471-137">The LCID that identifies the input language for the query.</span></span>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="9f471-138">keywordlocale</span><span class="sxs-lookup"><span data-stu-id="9f471-138">keywordlocale</span></span>](search-protocol-localeidentifiers.md) | <span data-ttu-id="9f471-139">Cualquier LCID válido</span><span class="sxs-lookup"><span data-stu-id="9f471-139">Any valid LCID</span></span>                                                | <span data-ttu-id="9f471-140">LCID que identifica el idioma de la versión internacional del indexador.</span><span class="sxs-lookup"><span data-stu-id="9f471-140">The LCID that identifies the language of the international version of the Indexer.</span></span> <span data-ttu-id="9f471-141">El valor predeterminado es 1033 (en-US).</span><span class="sxs-lookup"><span data-stu-id="9f471-141">The default is 1033 (en-us).</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="9f471-142">rutas</span><span class="sxs-lookup"><span data-stu-id="9f471-142">crumb</span></span>](search-protocol-crumb.md)                     | <span data-ttu-id="9f471-143">AQS (instrucción)</span><span class="sxs-lookup"><span data-stu-id="9f471-143">AQS statement</span></span>                                                 | <span data-ttu-id="9f471-144">Este argumento restringe el ámbito en el que se busca.</span><span class="sxs-lookup"><span data-stu-id="9f471-144">This argument restricts the scope being searched.</span></span> <span data-ttu-id="9f471-145">En Windows Vista, el protocolo de búsqueda admite AQS completo, así como una implementación especial para un `location` argumento.</span><span class="sxs-lookup"><span data-stu-id="9f471-145">In Windows Vista, the search protocol supports full AQS as well as a special implementation for a `location` argument.</span></span> <span data-ttu-id="9f471-146">En Windows XP, el protocolo de búsqueda también admite AQS completo, salvo una implementación especial de `kind` y `store` .</span><span class="sxs-lookup"><span data-stu-id="9f471-146">In Windows XP, the search protocol also supports full AQS, except for a special implementation of `kind` and `store`.</span></span> |
| [<span data-ttu-id="9f471-147">sintáctica</span><span class="sxs-lookup"><span data-stu-id="9f471-147">syntax</span></span>](search-protocol-syntaxargument.md)           | <span data-ttu-id="9f471-148">NQS, AQS (no distingue mayúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="9f471-148">NQS, AQS (not case sensitive)</span></span>                                 | <span data-ttu-id="9f471-149">Sintaxis de consulta que se va a usar para buscar en el índice: sintaxis de consulta natural o sintaxis de consulta avanzada (AQS).</span><span class="sxs-lookup"><span data-stu-id="9f471-149">The query syntax to use to search the index: either Natural Query Syntax or Advanced Query Syntax (AQS).</span></span> <span data-ttu-id="9f471-150">AQS es el valor predeterminado y siempre se asume que se analiza y se admite.</span><span class="sxs-lookup"><span data-stu-id="9f471-150">AQS is the default and is always assumed parsed and supported.</span></span>                                                                                                                        |
| [<span data-ttu-id="9f471-151">stackedby</span><span class="sxs-lookup"><span data-stu-id="9f471-151">stackedby</span></span>](search-protocol-stackedby.md)             | <span data-ttu-id="9f471-152">Cualquier propiedad válida del sistema de propiedades</span><span class="sxs-lookup"><span data-stu-id="9f471-152">Any valid property from the property system</span></span>                   | <span data-ttu-id="9f471-153">Propiedad que especifica la columna por la que se van a apilar los resultados.</span><span class="sxs-lookup"><span data-stu-id="9f471-153">A property that specifies the column to stack results by.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="9f471-154">subquery</span><span class="sxs-lookup"><span data-stu-id="9f471-154">subquery</span></span>](search-protocol-subquery.md)               | <span data-ttu-id="9f471-155">Una ruta de acceso completa para un archivo de búsqueda guardado ( \* . Search-MS)</span><span class="sxs-lookup"><span data-stu-id="9f471-155">A fully specified path for a Saved Search file (\*.search-ms)</span></span> | <span data-ttu-id="9f471-156">Los resultados de la subconsulta se utilizan como el origen de la consulta.</span><span class="sxs-lookup"><span data-stu-id="9f471-156">The results of the subquery are used as the source for the query.</span></span> <span data-ttu-id="9f471-157">Es decir, se busca en los términos de la consulta con los resultados de la subconsulta.</span><span class="sxs-lookup"><span data-stu-id="9f471-157">That is, the query terms are searched for against the results of the subquery.</span></span>                                                                                                                                               |
| <span data-ttu-id="9f471-158">displayname</span><span class="sxs-lookup"><span data-stu-id="9f471-158">displayname</span></span>                                            | <span data-ttu-id="9f471-159">Cadena con codificación URL</span><span class="sxs-lookup"><span data-stu-id="9f471-159">URL-encoded string</span></span>                                            | <span data-ttu-id="9f471-160">Nombre de la búsqueda actual.</span><span class="sxs-lookup"><span data-stu-id="9f471-160">The name of the current search.</span></span>                                                                                                                                                                                                                                                                |



 

## <a name="windows-vista-with-sp1-use-of-the-search-protocol"></a><span data-ttu-id="9f471-161">Windows Vista con SP1 uso de la búsqueda: Protocolo</span><span class="sxs-lookup"><span data-stu-id="9f471-161">Windows Vista with SP1 use of the search: protocol</span></span>

<span data-ttu-id="9f471-162">Windows Vista con SP1 tiene varios puntos de entrada desde los que llama a **Search:** Protocol.</span><span class="sxs-lookup"><span data-stu-id="9f471-162">Windows Vista with SP1 has several entry points from which it calls the **search:** protocol.</span></span> <span data-ttu-id="9f471-163">Estos puntos de entrada se describen a continuación, así como la sintaxis común asociada a cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="9f471-163">These entry points are outlined below as well as the common syntax associated with each.</span></span>



| <span data-ttu-id="9f471-164">Punto de entrada del Protocolo de búsqueda</span><span class="sxs-lookup"><span data-stu-id="9f471-164">Search protocol entry point</span></span> | <span data-ttu-id="9f471-165">Ubicación</span><span class="sxs-lookup"><span data-stu-id="9f471-165">Location</span></span>         | <span data-ttu-id="9f471-166">Consulta llamada</span><span class="sxs-lookup"><span data-stu-id="9f471-166">Query called</span></span>                                                         |
|-----------------------------|------------------|----------------------------------------------------------------------|
| <span data-ttu-id="9f471-167">**Buscar en todas partes**</span><span class="sxs-lookup"><span data-stu-id="9f471-167">**Search Everywhere**</span></span>       | <span data-ttu-id="9f471-168">Menú **Inicio**</span><span class="sxs-lookup"><span data-stu-id="9f471-168">**Start** menu</span></span>   | <span data-ttu-id="9f471-169">buscar: consulta = *término de búsqueda*<></span><span class="sxs-lookup"><span data-stu-id="9f471-169">search:query=<*Search Term*></span></span>                                   |
| <span data-ttu-id="9f471-170">**Buscar en todas partes**</span><span class="sxs-lookup"><span data-stu-id="9f471-170">**Search Everywhere**</span></span>       | <span data-ttu-id="9f471-171">Explorador de Windows</span><span class="sxs-lookup"><span data-stu-id="9f471-171">Windows Explorer</span></span> | <span data-ttu-id="9f471-172">buscar: consulta =<*término de búsqueda*>&en la ubicación: <*Ubicación*></span><span class="sxs-lookup"><span data-stu-id="9f471-172">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |
| <span data-ttu-id="9f471-173">Tecla del logotipo de Windows+F</span><span class="sxs-lookup"><span data-stu-id="9f471-173">Windows logo key+F</span></span>          | <span data-ttu-id="9f471-174">En cualquier lugar</span><span class="sxs-lookup"><span data-stu-id="9f471-174">Anywhere</span></span>         | <span data-ttu-id="9f471-175">buscan</span><span class="sxs-lookup"><span data-stu-id="9f471-175">search:</span></span>                                                              |
| <span data-ttu-id="9f471-176">CTRL+F</span><span class="sxs-lookup"><span data-stu-id="9f471-176">CTRL+F</span></span>                      | <span data-ttu-id="9f471-177">Explorador de Windows</span><span class="sxs-lookup"><span data-stu-id="9f471-177">Windows Explorer</span></span> | <span data-ttu-id="9f471-178">buscar: consulta =<*término de búsqueda*>&en la ubicación: <*Ubicación*></span><span class="sxs-lookup"><span data-stu-id="9f471-178">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |
| <span data-ttu-id="9f471-179">F3</span><span class="sxs-lookup"><span data-stu-id="9f471-179">F3</span></span>                          | <span data-ttu-id="9f471-180">Menú **Inicio**</span><span class="sxs-lookup"><span data-stu-id="9f471-180">**Start** menu</span></span>   | <span data-ttu-id="9f471-181">buscan</span><span class="sxs-lookup"><span data-stu-id="9f471-181">search:</span></span>                                                              |
| <span data-ttu-id="9f471-182">F3</span><span class="sxs-lookup"><span data-stu-id="9f471-182">F3</span></span>                          | <span data-ttu-id="9f471-183">Explorador de Windows</span><span class="sxs-lookup"><span data-stu-id="9f471-183">Windows Explorer</span></span> | <span data-ttu-id="9f471-184">buscar: consulta =<*término de búsqueda*>&en la ubicación: <*Ubicación*></span><span class="sxs-lookup"><span data-stu-id="9f471-184">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |



 

<span data-ttu-id="9f471-185">Los puntos de entrada del Protocolo de búsqueda de Windows Vista con SP1 no aprovechan todos los parámetros posibles del Protocolo de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9f471-185">The Windows Vista with SP1 search protocol entry points do not take advantage of all the possible parameters in the search protocol.</span></span> <span data-ttu-id="9f471-186">Las aplicaciones que solo se preocupan por la administración de llamadas del Protocolo de búsqueda desde Windows Vista con SP1 pueden utilizar la tabla siguiente como guía del mínimo necesario para implementar.</span><span class="sxs-lookup"><span data-stu-id="9f471-186">Applications that are only concerned with handling search protocol calls from Windows Vista with SP1 can use the following table as a guide to the minimum they need to implement.</span></span>



| <span data-ttu-id="9f471-187">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9f471-187">Parameter</span></span>                                              | <span data-ttu-id="9f471-188">¿Lo usa Windows?</span><span class="sxs-lookup"><span data-stu-id="9f471-188">Used by Windows?</span></span> | <span data-ttu-id="9f471-189">Cómo Windows Vista con SP1 lo utiliza al llamar a Search:</span><span class="sxs-lookup"><span data-stu-id="9f471-189">How Windows Vista with SP1 uses it when calling search:</span></span>                                                                                                                                                                                                                     |
|--------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f471-190">Query</span><span class="sxs-lookup"><span data-stu-id="9f471-190">query</span></span>                                                  | <span data-ttu-id="9f471-191">Sí</span><span class="sxs-lookup"><span data-stu-id="9f471-191">Yes</span></span>              | <span data-ttu-id="9f471-192">Texto de la consulta escrito por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9f471-192">The query text entered by the user.</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="9f471-193">rutas</span><span class="sxs-lookup"><span data-stu-id="9f471-193">crumb</span></span>](search-protocol-crumb.md)                     | <span data-ttu-id="9f471-194">Sí</span><span class="sxs-lookup"><span data-stu-id="9f471-194">Yes</span></span>              | <span data-ttu-id="9f471-195">[migas](search-protocol-crumb.md) de uso del `location` argumento para especificar el origen de la consulta.</span><span class="sxs-lookup"><span data-stu-id="9f471-195">[crumb](search-protocol-crumb.md) uses the `location` argument to specify where the query came from.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="9f471-196">subquery</span><span class="sxs-lookup"><span data-stu-id="9f471-196">subquery</span></span>](search-protocol-subquery.md)               | <span data-ttu-id="9f471-197">Sí</span><span class="sxs-lookup"><span data-stu-id="9f471-197">Yes</span></span>              | <span data-ttu-id="9f471-198">Los resultados del argumento de la [subconsulta](search-protocol-subquery.md) se utilizan como el ámbito de los elementos que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="9f471-198">The results of the [Subquery](search-protocol-subquery.md) argument are used as the scope of items to search.</span></span> <span data-ttu-id="9f471-199">Esto se suele usar si un usuario usaba un archivo. Search-ms para buscar y, a continuación, se llama a la aplicación de búsqueda de escritorio predeterminada desde dentro de esa búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9f471-199">This would typically be used if a user was using a .search-ms file to search and then called the default desktop search application from within that search.</span></span> |
| [<span data-ttu-id="9f471-200">inputlocale</span><span class="sxs-lookup"><span data-stu-id="9f471-200">inputlocale</span></span>](search-protocol-localeidentifiers.md)   | <span data-ttu-id="9f471-201">No</span><span class="sxs-lookup"><span data-stu-id="9f471-201">No</span></span>               | <span data-ttu-id="9f471-202">No se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="9f471-202">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="9f471-203">keywordlocale</span><span class="sxs-lookup"><span data-stu-id="9f471-203">keywordlocale</span></span>](search-protocol-localeidentifiers.md) | <span data-ttu-id="9f471-204">No</span><span class="sxs-lookup"><span data-stu-id="9f471-204">No</span></span>               | <span data-ttu-id="9f471-205">No se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="9f471-205">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="9f471-206">sintáctica</span><span class="sxs-lookup"><span data-stu-id="9f471-206">syntax</span></span>](search-protocol-syntaxargument.md)           | <span data-ttu-id="9f471-207">No</span><span class="sxs-lookup"><span data-stu-id="9f471-207">No</span></span>               | <span data-ttu-id="9f471-208">No se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="9f471-208">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="9f471-209">stackedby</span><span class="sxs-lookup"><span data-stu-id="9f471-209">stackedby</span></span>](search-protocol-stackedby.md)             | <span data-ttu-id="9f471-210">No</span><span class="sxs-lookup"><span data-stu-id="9f471-210">No</span></span>               | <span data-ttu-id="9f471-211">No se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="9f471-211">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="9f471-212">displayname</span><span class="sxs-lookup"><span data-stu-id="9f471-212">displayname</span></span>                                            | <span data-ttu-id="9f471-213">No</span><span class="sxs-lookup"><span data-stu-id="9f471-213">No</span></span>               | <span data-ttu-id="9f471-214">No se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="9f471-214">Not currently used.</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="examples"></a><span data-ttu-id="9f471-215">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9f471-215">Examples</span></span>

<span data-ttu-id="9f471-216">Si un usuario escribe "Microsoft" en el menú **Inicio** y hace clic en **Buscar en todas partes**, se realiza la llamada del Protocolo de búsqueda resultante:</span><span class="sxs-lookup"><span data-stu-id="9f471-216">If a user enters "Microsoft" in the **Start** menu and clicks **Search Everywhere**, the resulting search protocol call is made:</span></span>


```C++
search:query=microsoft&
```



<span data-ttu-id="9f471-217">Si un usuario escribe "Seattle" en el explorador de Windows en C: \\ carpeta y, a continuación, hace clic en **Buscar en todas partes**, se realiza la siguiente llamada, usando caracteres de escape para ': ' y ' \\ ':</span><span class="sxs-lookup"><span data-stu-id="9f471-217">If a user enters "Seattle" in Windows Explorer within C:\\MyFolder and then clicks **Search Everywhere**, the following call is made, using escape characters for ':' and '\\':</span></span>


```C++
search:query=seattle&crumb=location:C%3A%5CMyFolder
```



## <a name="registering-the-application-that-handles-the-protocol"></a><span data-ttu-id="9f471-218">Registro de la aplicación que controla el protocolo</span><span class="sxs-lookup"><span data-stu-id="9f471-218">Registering the Application that Handles the Protocol</span></span>

<span data-ttu-id="9f471-219">Dado que varias aplicaciones pueden competir por el protocolo de búsqueda, debe registrar la aplicación con la característica [programas predeterminados](default-programs.md) durante la instalación para permitir que el usuario configure el valor predeterminado más fácilmente.</span><span class="sxs-lookup"><span data-stu-id="9f471-219">Because multiple applications can contend for the search protocol, you should register your application with the [Default Programs](default-programs.md) feature during installation to enable the user to configure the default more easily.</span></span> <span data-ttu-id="9f471-220">Además de los procedimientos de instalación que se suelen realizar en Windows XP, una aplicación basada en Windows Vista debe registrarse con la característica programas predeterminados para que la aplicación y los usuarios puedan configurar los valores predeterminados sin problemas.</span><span class="sxs-lookup"><span data-stu-id="9f471-220">In addition to the installation procedures normally practiced under Windows XP, a Windows Vista-based application must register with the Default Programs feature so that the application and users can seamlessly configure defaults.</span></span>

<span data-ttu-id="9f471-221">Después de instalar los archivos binarios necesarios en el equipo del usuario, la rutina de instalación debe completar estas tareas generales:</span><span class="sxs-lookup"><span data-stu-id="9f471-221">After installing the necessary binary files on the user's computer, your installation routine should complete these general tasks:</span></span>

1.  <span data-ttu-id="9f471-222">Escriba los ProgID en **el \_ \_ equipo local HKEY**, tal como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="9f471-222">Write ProgIDs to **HKEY\_LOCAL\_MACHINE**, as described below.</span></span> <span data-ttu-id="9f471-223">Tenga en cuenta que las aplicaciones deben crear ProgID específicos de la aplicación para el protocolo de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9f471-223">Note that applications must create application-specific ProgIDs for the search protocol.</span></span>
2.  <span data-ttu-id="9f471-224">Notificar Asociación del Protocolo de búsqueda en el nivel de equipo.</span><span class="sxs-lookup"><span data-stu-id="9f471-224">Claim machine-level search protocol association.</span></span>
3.  <span data-ttu-id="9f471-225">Registre la aplicación con los [programas predeterminados](default-programs.md), como se explica en [registrar una aplicación para su uso con programas predeterminados](default-programs.md), como un complemento para el protocolo de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9f471-225">Register the application with [Default Programs](default-programs.md), as explained in [Registering an Application for Use with Default Programs](default-programs.md), as a contender for the search protocol.</span></span>

### <a name="registry-entries"></a><span data-ttu-id="9f471-226">Entradas del Registro</span><span class="sxs-lookup"><span data-stu-id="9f471-226">Registry Entries</span></span>

<span data-ttu-id="9f471-227">A continuación se muestran ejemplos de las entradas del registro necesarias para una aplicación de búsqueda de escritorio ficticia, contoso Search.</span><span class="sxs-lookup"><span data-stu-id="9f471-227">The following are examples of the required registry entries for a fictional desktop search application, Contoso Search.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            URL Protocol = ""
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            DefaultIcon
               (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe,-7
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe %1
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Contoso Search = "Software\\Contoso\\Search\\Capabilities"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               ApplicationName = "Contoso Search Test App"
               ApplicationDescription = "Contoso search is a great new desktop search application"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               UrlAssociations
                  search = "contoso-search"
```

## <a name="related-topics"></a><span data-ttu-id="9f471-228">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f471-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f471-229">Sintaxis de consulta avanzada</span><span class="sxs-lookup"><span data-stu-id="9f471-229">Advanced Query Syntax</span></span>](../search/-search-3x-advancedquerysyntax.md)
</dt> <dt>

[<span data-ttu-id="9f471-230">Programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="9f471-230">Default Programs</span></span>](default-programs.md)
</dt> </dl>

 

 
