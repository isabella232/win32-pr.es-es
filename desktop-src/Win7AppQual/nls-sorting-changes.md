---
description: .
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: Cambios de ordenación de NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa4935a6874e28270e73904eb352cd6332e650b7
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314958"
---
# <a name="nls-sorting-changes"></a><span data-ttu-id="974e9-103">Cambios de ordenación de NLS</span><span class="sxs-lookup"><span data-stu-id="974e9-103">NLS Sorting Changes</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="974e9-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="974e9-104">Affected Platforms</span></span>

 <span data-ttu-id="974e9-105">**Clientes** : Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="974e9-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="974e9-106">**Servidores** : windows Server 2003, windows Server 2008, windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="974e9-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="974e9-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="974e9-107">Feature Impact</span></span>

 <span data-ttu-id="974e9-108">**Gravedad** alta</span><span class="sxs-lookup"><span data-stu-id="974e9-108">**Severity** - High</span></span>  
<span data-ttu-id="974e9-109">**Frecuencia** baja (pocas aplicaciones afectadas, pero si se ven afectadas, siempre interrumpidas)</span><span class="sxs-lookup"><span data-stu-id="974e9-109">**Frequency** - Low (few apps impacted, but if impacted, always broken)</span></span>  


## <a name="description"></a><span data-ttu-id="974e9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="974e9-110">Description</span></span>

<span data-ttu-id="974e9-111">Las funciones de National Language support (NLS) ayudan a las aplicaciones a satisfacer las distintas necesidades de idioma y de la configuración regional de los usuarios de todo el mundo.</span><span class="sxs-lookup"><span data-stu-id="974e9-111">The National Language Support (NLS) functions help applications support the different language- and locale-specific needs of users around the world.</span></span> <span data-ttu-id="974e9-112">Las nuevas versiones de Windows casi invariables incluyen cambios de NLS.</span><span class="sxs-lookup"><span data-stu-id="974e9-112">New Windows versions almost invariably include NLS changes.</span></span> <span data-ttu-id="974e9-113">Este cambio afecta a la intercalación y la ordenación, y, por lo tanto, a las aplicaciones que tienen índices persistentes.</span><span class="sxs-lookup"><span data-stu-id="974e9-113">This change affects collation and sorting, and therefore applications that have persistent indexes.</span></span>

<span data-ttu-id="974e9-114">Una tabla de intercalación tiene dos números que identifican su versión (revisión): la versión definida y la versión NLS.</span><span class="sxs-lookup"><span data-stu-id="974e9-114">A collation table has two numbers that identify its version (revision): the defined version and the NLS version.</span></span> <span data-ttu-id="974e9-115">Ambas versiones son valores DWORD, compuesto por una versión principal y una versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="974e9-115">Both versions are DWORD values, composed of a major version and a minor version.</span></span> <span data-ttu-id="974e9-116">El primer byte de un valor está reservado, los dos bytes siguientes representan la versión principal y el último byte representa la versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="974e9-116">The first byte of a value is reserved, the next two bytes represent the major version, and the last byte represents the minor version.</span></span> <span data-ttu-id="974e9-117">En términos hexadecimales, el patrón es 0xRRMMMMmm, donde R es igual a Reserved, M es igual a Major y m es igual a Minor.</span><span class="sxs-lookup"><span data-stu-id="974e9-117">In hexadecimal terms, the pattern is 0xRRMMMMmm, where R equals Reserved, M equals major, and m equals minor.</span></span> <span data-ttu-id="974e9-118">Por ejemplo, una versión principal de 3 con una versión secundaria de 4 se representa como 0x304.</span><span class="sxs-lookup"><span data-stu-id="974e9-118">For example, a major version of 3 with a minor version of 4 is represented as 0x304.</span></span>

<span data-ttu-id="974e9-119">En el caso de una versión principal, uno o más puntos de código cambian para que la aplicación deba volver a indizar todos los datos para que las comparaciones sean válidas.</span><span class="sxs-lookup"><span data-stu-id="974e9-119">For a major version, one or more code points change so that the application must re-index all data for comparisons to be valid.</span></span> <span data-ttu-id="974e9-120">En el caso de una versión secundaria, no se mueve nada, pero se agregan puntos de código.</span><span class="sxs-lookup"><span data-stu-id="974e9-120">For a minor version, nothing moves, but code points are added.</span></span> <span data-ttu-id="974e9-121">Para este tipo de versión, la aplicación solo tiene que volver a indexar las cadenas con valores que no se pudieron ordenar previamente.</span><span class="sxs-lookup"><span data-stu-id="974e9-121">For this type of version, the application only has to re-index strings with previously unsortable values.</span></span> <span data-ttu-id="974e9-122">En Resumen, este es el significado de los números de versión en relación con los cambios de datos en las tablas de excepciones específicas de la configuración regional y las tablas predeterminadas:</span><span class="sxs-lookup"><span data-stu-id="974e9-122">In summary, here is what the version numbers mean in relation to the data changes in the locale-specific exception tables and default tables:</span></span>

<span data-ttu-id="974e9-123">**NLSVersion principal** : se han modificado los puntos de código de las tablas "excepción" o de configuración regional específicas</span><span class="sxs-lookup"><span data-stu-id="974e9-123">**NLSVersion Major** – Changed code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="974e9-124">**NLSVersion Minor** : se han agregado nuevos puntos de código en las tablas "Exception" (excepciones) o específicas de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="974e9-124">**NLSVersion Minor** – Added new code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="974e9-125">**DefinedVersion principal** : cambios de los puntos de código en la tabla predeterminada</span><span class="sxs-lookup"><span data-stu-id="974e9-125">**DefinedVersion Major** – Changed code points in the default table</span></span>  
<span data-ttu-id="974e9-126">**DefinedVersion Minor** : se han agregado nuevos puntos de código en la tabla predeterminada</span><span class="sxs-lookup"><span data-stu-id="974e9-126">**DefinedVersion Minor** – Added new code points in the default table</span></span>  


<span data-ttu-id="974e9-127">**Ordenar los números de versión de las versiones de lanzamiento:**</span><span class="sxs-lookup"><span data-stu-id="974e9-127">**Sorting version numbers for released versions:**</span></span>



| <span data-ttu-id="974e9-128">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="974e9-128">Operating System</span></span>    | <span data-ttu-id="974e9-129">Release</span><span class="sxs-lookup"><span data-stu-id="974e9-129">Release</span></span>           | <span data-ttu-id="974e9-130">Versión (0xRRMMMMmm)</span><span class="sxs-lookup"><span data-stu-id="974e9-130">Version (0xRRMMMMmm)</span></span>         |
|---------------------|-------------------|------------------------------|
| <span data-ttu-id="974e9-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="974e9-131">Windows XP</span></span>          | <span data-ttu-id="974e9-132">RTM/SP1/SP2/SP3/...</span><span class="sxs-lookup"><span data-stu-id="974e9-132">RTM/SP1/SP2/SP3/…</span></span> | <span data-ttu-id="974e9-133">N/A: no GetNLSVersion () API</span><span class="sxs-lookup"><span data-stu-id="974e9-133">N/A - no GetNLSVersion() API</span></span> |
| <span data-ttu-id="974e9-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="974e9-134">Windows Server 2003</span></span> | <span data-ttu-id="974e9-135">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="974e9-135">RTM/SP1</span></span>           | <span data-ttu-id="974e9-136">0x00 0000 01</span><span class="sxs-lookup"><span data-stu-id="974e9-136">0x00 0000 01</span></span>                 |
| <span data-ttu-id="974e9-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="974e9-137">Windows Vista</span></span>       | <span data-ttu-id="974e9-138">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="974e9-138">RTM/SP1</span></span>           | <span data-ttu-id="974e9-139">0x00 0405 00</span><span class="sxs-lookup"><span data-stu-id="974e9-139">0x00 0405 00</span></span>                 |
| <span data-ttu-id="974e9-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="974e9-140">Windows Server 2008</span></span> | <span data-ttu-id="974e9-141">RTM</span><span class="sxs-lookup"><span data-stu-id="974e9-141">RTM</span></span>               | <span data-ttu-id="974e9-142">0x00 0501 00/0x00 5001 00</span><span class="sxs-lookup"><span data-stu-id="974e9-142">0x00 0501 00 / 0x00 5001 00</span></span>  |
| <span data-ttu-id="974e9-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="974e9-143">Windows 7</span></span>           | <span data-ttu-id="974e9-144">RTM</span><span class="sxs-lookup"><span data-stu-id="974e9-144">RTM</span></span>               | <span data-ttu-id="974e9-145">0x00060100</span><span class="sxs-lookup"><span data-stu-id="974e9-145">0x00060100</span></span>                   |



 

## <a name="manifestation"></a><span data-ttu-id="974e9-146">Manifestación</span><span class="sxs-lookup"><span data-stu-id="974e9-146">Manifestation</span></span>

<span data-ttu-id="974e9-147">Las aplicaciones (como bases de datos) con índices persistentes que no comprueben la versión de NLS y vuelvan a indexarse tras el cambio de versión no se podrán ordenar correctamente o puede que no proporcionen los resultados solicitados.</span><span class="sxs-lookup"><span data-stu-id="974e9-147">Applications (such as databases) with persistent indexes that do not check the NLS version and re-index upon version change will fail to sort correctly or may fail to provide requested results.</span></span>

<span data-ttu-id="974e9-148">En el caso de las interfaces de usuario, las listas (por ejemplo, alfabético, numérico, alfanumérico, símbolos, etc.) se pueden ordenar de forma incorrecta.</span><span class="sxs-lookup"><span data-stu-id="974e9-148">In the case of user interfaces, lists (for example, alphabetical, numeric, alphanumeric, symbols, and so on) may sort incorrectly.</span></span>

## <a name="solution"></a><span data-ttu-id="974e9-149">Solución</span><span class="sxs-lookup"><span data-stu-id="974e9-149">Solution</span></span>

<span data-ttu-id="974e9-150">La aplicación puede llamar a **GetNLSVersionEx** (Windows Vista o posterior) o **GetNLSVersion** (anterior a Windows Vista) para recuperar la versión definida y la versión de NLS para una tabla de intercalación.</span><span class="sxs-lookup"><span data-stu-id="974e9-150">Your application can call either **GetNLSVersionEx** (Windows Vista or later) or **GetNLSVersion** (prior to Windows Vista) to retrieve both the defined version and the NLS version for a collation table.</span></span>

-   <span data-ttu-id="974e9-151">GetNLSVersionEx:</span><span class="sxs-lookup"><span data-stu-id="974e9-151">GetNLSVersionEx:</span></span>

<span data-ttu-id="974e9-152">*Recupera información sobre la versión actual de una función NLS especificada para una configuración regional especificada por nombre.*</span><span class="sxs-lookup"><span data-stu-id="974e9-152">*Retrieves information about the current version of a specified NLS capability for a locale specified by name*</span></span>  
<span data-ttu-id="974e9-153">Esta función permite a una aplicación como Active Directory determinar si un cambio de NLS afecta a la configuración regional utilizada para una tabla de índice determinada.</span><span class="sxs-lookup"><span data-stu-id="974e9-153">This function allows an application such as Active Directory to determine whether an NLS change affects the locale used for a particular index table.</span></span> <span data-ttu-id="974e9-154">Si no es así, no es necesario volver a indizar la tabla.</span><span class="sxs-lookup"><span data-stu-id="974e9-154">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="974e9-155">Para obtener más información, vea controlar la información regional y de idioma.</span><span class="sxs-lookup"><span data-stu-id="974e9-155">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="974e9-156">Esta función admite configuraciones regionales personalizadas.</span><span class="sxs-lookup"><span data-stu-id="974e9-156">This function supports custom locales.</span></span> <span data-ttu-id="974e9-157">Si *lpLocaleName* especifica una configuración regional complementaria, los datos recuperados son los datos correctos para el orden de intercalación asociado a esa configuración regional complementaria.</span><span class="sxs-lookup"><span data-stu-id="974e9-157">If *lpLocaleName* specifies a supplemental locale, the data retrieved is the correct data for the collation order associated with that supplemental locale.</span></span>  

<span data-ttu-id="974e9-158">**Nota:** Las versiones de Windows anteriores a Windows Vista no admiten **GetNLSVersionEx**.</span><span class="sxs-lookup"><span data-stu-id="974e9-158">**Note:** Versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  


-   <span data-ttu-id="974e9-159">GetNLSVersion (se usa para aplicaciones que se ejecutan en versiones de Windows anteriores a Windows Vista):</span><span class="sxs-lookup"><span data-stu-id="974e9-159">GetNLSVersion (use for applications running on versions of Windows prior to Windows Vista):</span></span>

<span data-ttu-id="974e9-160">*Recupera información sobre la versión actual de una función NLS especificada para una configuración regional especificada por el identificador*</span><span class="sxs-lookup"><span data-stu-id="974e9-160">*Retrieves information about the current version of a specified NLS capability for a locale specified by identifier*</span></span>  
<span data-ttu-id="974e9-161">Esta función permite a una aplicación como Active Directory determinar si un cambio de NLS afecta al identificador de configuración regional que se usa para una tabla de índice determinada.</span><span class="sxs-lookup"><span data-stu-id="974e9-161">This function allows an application such as Active Directory to determine if an NLS change affects the locale identifier used for a particular index table.</span></span> <span data-ttu-id="974e9-162">Si no es así, no es necesario volver a indizar la tabla.</span><span class="sxs-lookup"><span data-stu-id="974e9-162">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="974e9-163">Para obtener más información, vea controlar la información regional y de idioma.</span><span class="sxs-lookup"><span data-stu-id="974e9-163">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="974e9-164">**Nota:** Esta función recupera información solo sobre una configuración regional especificada por el identificador.</span><span class="sxs-lookup"><span data-stu-id="974e9-164">**Note:** This function retrieves information only about a locale specified by identifier.</span></span> <span data-ttu-id="974e9-165">La función **GetNLSVersionEx** admite configuraciones regionales, características y nombres RFC 4646 adicionales.</span><span class="sxs-lookup"><span data-stu-id="974e9-165">The **GetNLSVersionEx** function supports additional locales, features, and RFC 4646 names.</span></span> <span data-ttu-id="974e9-166">Sin embargo, las versiones de Windows anteriores a Windows Vista no admiten **GetNLSVersionEx**.</span><span class="sxs-lookup"><span data-stu-id="974e9-166">However, versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  
<span data-ttu-id="974e9-167">Las aplicaciones diseñadas para ejecutarse solo en Windows Vista y versiones posteriores deben usar **GetNLSVersionEx** en preferencia a esta función.</span><span class="sxs-lookup"><span data-stu-id="974e9-167">Applications meant to run only on Windows Vista and later should use **GetNLSVersionEx** in preference to this function.</span></span> <span data-ttu-id="974e9-168">**GetNLSVersionEx** proporciona una buena compatibilidad para las configuraciones regionales complementarias.</span><span class="sxs-lookup"><span data-stu-id="974e9-168">**GetNLSVersionEx** provides good support for supplemental locales.</span></span>  


## <a name="compatibility-test"></a><span data-ttu-id="974e9-169">Prueba de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="974e9-169">Compatibility Test</span></span>

<span data-ttu-id="974e9-170">**Pasos para saber si una versión de intercalación ha cambiado (es decir, es necesario volver a indizar):**</span><span class="sxs-lookup"><span data-stu-id="974e9-170">**Steps to tell if a collation version changed (that is, you need to re-index):**</span></span>

-   <span data-ttu-id="974e9-171">**Use GetNLSVersionEx ()** para recuperar una estructura **NLSVERSIONINFOEX** al realizar la indexación original de los datos.</span><span class="sxs-lookup"><span data-stu-id="974e9-171">**Use GetNLSVersionEx()** to retrieve an **NLSVERSIONINFOEX** structure when doing the original indexing of your data.</span></span>
-   <span data-ttu-id="974e9-172">Almacene las siguientes propiedades con el índice para identificar la versión:  **NLSVERSIONINFOEX. dwNLSVersion** y **NLSVERSIONINFOEX. dwDefinedVersion** : estas dos propiedades juntas especifican la versión de la tabla de ordenación que está usando.</span><span class="sxs-lookup"><span data-stu-id="974e9-172">Store the following properties with your index to identify the version:  **NLSVERSIONINFOEX.dwNLSVersion** and **NLSVERSIONINFOEX.dwDefinedVersion** – These two properties together specify the version of the sorting table you are using.</span></span>  
    <span data-ttu-id="974e9-173">**NLSVERSIONINFOEX. dwEffectiveId** : especifica la configuración regional efectiva de la ordenación.</span><span class="sxs-lookup"><span data-stu-id="974e9-173">**NLSVERSIONINFOEX.dwEffectiveId** - This specifies the effective locale of your sort.</span></span> <span data-ttu-id="974e9-174">Una configuración regional personalizada apuntará a la ordenación de una configuración regional integrada.</span><span class="sxs-lookup"><span data-stu-id="974e9-174">A custom locale will point to an in-box locale's sort.</span></span>  
    
-   <span data-ttu-id="974e9-175">Al usar el índice **, use GetNlsVersionEx ()** para detectar la versión de los datos.</span><span class="sxs-lookup"><span data-stu-id="974e9-175">When using the index use **GetNlsVersionEx()** to discover the version of your data.</span></span>
-   <span data-ttu-id="974e9-176">Si alguna de las tres propiedades ha cambiado, los datos de ordenación que está utilizando podrían devolver resultados diferentes y cualquier indexación que tenga podría no encontrar registros.</span><span class="sxs-lookup"><span data-stu-id="974e9-176">If any of the three properties has changed, the sorting data you are using could return different results and any indexing you have may fail to find records.</span></span>
-   <span data-ttu-id="974e9-177">Si sabe que los datos no contienen puntos de código Unicode no válidos (es decir, todas las cadenas devuelven **true** desde una llamada a **IsNLSDefinedString ()**), puede considerarlas iguales si solo cambió el byte bajo de **dwNLSVersion** y **dwDefinedVersion** (las versiones secundarias descritas anteriormente).</span><span class="sxs-lookup"><span data-stu-id="974e9-177">If you KNOW that your data does not contain invalid Unicode code points (that is, all of your strings returned **TRUE** from a call to **IsNLSDefinedString()**), then you may consider them the same if ONLY the low byte of **dwNLSVersion** and **dwDefinedVersion** changed (the minor versions described above).</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="974e9-178">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="974e9-178">Links to Other Resources</span></span>

-   [<span data-ttu-id="974e9-179">Internacionalización para aplicaciones para Windows</span><span class="sxs-lookup"><span data-stu-id="974e9-179">Internationalization for Windows Applications</span></span>](../intl/international-support.md)
-   [<span data-ttu-id="974e9-180">GetNLSVersionEx función)</span><span class="sxs-lookup"><span data-stu-id="974e9-180">GetNLSVersionEx Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [<span data-ttu-id="974e9-181">GetNLSVersion función)</span><span class="sxs-lookup"><span data-stu-id="974e9-181">GetNLSVersion Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [<span data-ttu-id="974e9-182">Cómo saber si la versión de intercalación ha cambiado</span><span class="sxs-lookup"><span data-stu-id="974e9-182">How to tell if the collation version changed</span></span>](/archive/blogs/shawnste/)

 

 
