---
title: Establecer y recuperar opciones de Internet
description: En este tema se describe cómo establecer y recuperar opciones de Internet mediante las funciones InternetSetOption y InternetQueryOption.
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- Establecer y recuperar opciones de Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418bf21620cf7b7c4426844c95a39ef1fde04e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904759"
---
# <a name="setting-and-retrieving-internet-options"></a><span data-ttu-id="e503d-104">Establecer y recuperar opciones de Internet</span><span class="sxs-lookup"><span data-stu-id="e503d-104">Setting and Retrieving Internet Options</span></span>

<span data-ttu-id="e503d-105">En este tema se describe cómo establecer y recuperar opciones de Internet mediante las funciones [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) y [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .</span><span class="sxs-lookup"><span data-stu-id="e503d-105">This topic describes how to set and retrieve Internet options using the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) functions.</span></span>

<span data-ttu-id="e503d-106">Las opciones de Internet se pueden establecer en o recuperar desde un identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) especificado o la configuración actual en Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e503d-106">Internet options can be set on, or retrieved from, a specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle or the current settings in Microsoft Internet Explorer.</span></span>

-   [<span data-ttu-id="e503d-107">Pasos de implementación</span><span class="sxs-lookup"><span data-stu-id="e503d-107">Implementation Steps</span></span>](#implementation-steps)
    -   [<span data-ttu-id="e503d-108">Elegir opciones de Internet</span><span class="sxs-lookup"><span data-stu-id="e503d-108">Choosing Internet Options</span></span>](#choosing-internet-options)
    -   [<span data-ttu-id="e503d-109">Elección del controlador HINTERNET</span><span class="sxs-lookup"><span data-stu-id="e503d-109">Choosing the HINTERNET Handle</span></span>](#choosing-the-hinternet-handle)
    -   [<span data-ttu-id="e503d-110">Establecimiento o recuperación de las opciones</span><span class="sxs-lookup"><span data-stu-id="e503d-110">Setting or Retrieving the Options</span></span>](#setting-or-retrieving-the-options)
-   [<span data-ttu-id="e503d-111">Ámbito del identificador de HINTERNET</span><span class="sxs-lookup"><span data-stu-id="e503d-111">Scope of HINTERNET Handle</span></span>](#scope-of-hinternet-handle)
-   [<span data-ttu-id="e503d-112">Establecer opciones individuales</span><span class="sxs-lookup"><span data-stu-id="e503d-112">Setting Individual Options</span></span>](#setting-individual-options)
-   [<span data-ttu-id="e503d-113">Recuperación de opciones individuales</span><span class="sxs-lookup"><span data-stu-id="e503d-113">Retrieving Individual Options</span></span>](#retrieving-individual-options)
    -   [<span data-ttu-id="e503d-114">Ejemplo completo</span><span class="sxs-lookup"><span data-stu-id="e503d-114">Complete Sample</span></span>](#complete-sample)
-   [<span data-ttu-id="e503d-115">Establecer opciones de conexión</span><span class="sxs-lookup"><span data-stu-id="e503d-115">Setting Connection Options</span></span>](#setting-connection-options)
-   [<span data-ttu-id="e503d-116">Recuperación de opciones de conexión</span><span class="sxs-lookup"><span data-stu-id="e503d-116">Retrieving Connection Options</span></span>](#retrieving-connection-options)
-   [<span data-ttu-id="e503d-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e503d-117">Related topics</span></span>](#related-topics)

## <a name="implementation-steps"></a><span data-ttu-id="e503d-118">Pasos de implementación</span><span class="sxs-lookup"><span data-stu-id="e503d-118">Implementation Steps</span></span>

<span data-ttu-id="e503d-119">Para establecer o recuperar las opciones de Internet, realice lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e503d-119">To set or retrieve Internet options complete the following:</span></span>

-   [<span data-ttu-id="e503d-120">Elegir opciones de Internet</span><span class="sxs-lookup"><span data-stu-id="e503d-120">Choosing Internet Options</span></span>](#choosing-internet-options)
-   [<span data-ttu-id="e503d-121">Elección del controlador HINTERNET</span><span class="sxs-lookup"><span data-stu-id="e503d-121">Choosing the HINTERNET Handle</span></span>](#choosing-the-hinternet-handle)
-   [<span data-ttu-id="e503d-122">Establecimiento o recuperación de las opciones</span><span class="sxs-lookup"><span data-stu-id="e503d-122">Setting or Retrieving the Options</span></span>](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a><span data-ttu-id="e503d-123">Elegir opciones de Internet</span><span class="sxs-lookup"><span data-stu-id="e503d-123">Choosing Internet Options</span></span>

<span data-ttu-id="e503d-124">Dado que hay tantas opciones de Internet, es importante elegir las opciones adecuadas.</span><span class="sxs-lookup"><span data-stu-id="e503d-124">Because there are so many Internet options, choosing the right options is important.</span></span> <span data-ttu-id="e503d-125">Muchas opciones de Internet afectan al comportamiento de las funciones WinINet e Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="e503d-125">Many Internet options affect the behavior of the WinINet functions and Internet Explorer:</span></span>

<span data-ttu-id="e503d-126">Por ejemplo, puede:</span><span class="sxs-lookup"><span data-stu-id="e503d-126">For example, you can:</span></span>

-   <span data-ttu-id="e503d-127">Controlar la autenticación básica de servidor y proxy mediante la configuración de nombres de usuario y contraseñas.</span><span class="sxs-lookup"><span data-stu-id="e503d-127">Handle basic server and proxy authentication by setting user names and passwords.</span></span>
-   <span data-ttu-id="e503d-128">Establezca o recupere la cadena de agente de usuario utilizada por los servidores para identificar las características de la aplicación cliente o el explorador.</span><span class="sxs-lookup"><span data-stu-id="e503d-128">Set or retrieve the user agent string used by servers to identify the features of the client application or browser.</span></span>
-   <span data-ttu-id="e503d-129">Recupera el tipo de identificador del identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="e503d-129">Retrieve the handle type of the specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="e503d-130">Para obtener más información y una lista de las opciones de Internet, vea [**marcas de opciones**](option-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e503d-130">For more information and a list of the Internet options, see [**Option Flags**](option-flags.md).</span></span>

<span data-ttu-id="e503d-131">En Internet Explorer 5 y versiones posteriores, algunas opciones se pueden establecer o recuperar desde una conexión a Internet específica mediante la lista de opciones de [**Internet \_ por \_ \_ \_ cada**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) una de las estructuras de opciones de Internet y [**\_ por \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) conexión.</span><span class="sxs-lookup"><span data-stu-id="e503d-131">In Internet Explorer 5 and later, some options can be set or retrieved from a specific Internet connection using the [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) and [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span> <span data-ttu-id="e503d-132">Para obtener más información y una lista de opciones que se pueden establecer o recuperar de una conexión a Internet específica, vea el miembro **dwOptions** de la estructura de la [**\_ opción Internet por \_ Conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="e503d-132">For more information and a list of options that can be set or retrieved from a specific Internet connection, see the **dwOptions** member of the [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structure.</span></span>

### <a name="choosing-the-hinternet-handle"></a><span data-ttu-id="e503d-133">Elección del controlador HINTERNET</span><span class="sxs-lookup"><span data-stu-id="e503d-133">Choosing the HINTERNET Handle</span></span>

<span data-ttu-id="e503d-134">El identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) que se usa para establecer o recuperar opciones de Internet determina el ámbito de la operación.</span><span class="sxs-lookup"><span data-stu-id="e503d-134">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle used to set or retrieve Internet options determines the scope of the operation.</span></span> <span data-ttu-id="e503d-135">Todos los identificadores creados a través de este identificador heredarán las opciones establecidas en este controlador.</span><span class="sxs-lookup"><span data-stu-id="e503d-135">All the handles created through this handle will inherit the options set on this handle.</span></span>

<span data-ttu-id="e503d-136">Por ejemplo, las aplicaciones cliente que requieren un proxy con autenticación, probablemente no requieren el establecimiento del nombre de usuario y la contraseña de proxy cada vez que la aplicación intenta obtener acceso a un recurso de Internet.</span><span class="sxs-lookup"><span data-stu-id="e503d-136">For example, client applications that require a proxy with authentication, probably do not require setting the proxy user name and password every time the application attempts to access an Internet resource.</span></span> <span data-ttu-id="e503d-137">Si el mismo proxy controla todas las solicitudes de una conexión determinada, el establecimiento del nombre de usuario y la contraseña de proxy en un tipo de conexión [**HINTERNET**](appendix-a-hinternet-handles.md) identificador, es decir, un identificador creado por una llamada a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), permitiría que cualquier llamada procedente de este controlador **HINTERNET** usara el mismo nombre de usuario y contraseña de proxy.</span><span class="sxs-lookup"><span data-stu-id="e503d-137">If all requests on a given connection are handled by the same proxy, setting the proxy user name and password on a connection type [**HINTERNET**](appendix-a-hinternet-handles.md) handle, that is, a handle created by a call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), would allow any calls derived from this **HINTERNET** handle to use the same proxy user name and password.</span></span> <span data-ttu-id="e503d-138">Establecer el nombre de usuario y la contraseña de proxy cada vez que [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) crea un identificador de **HINTERNET** requiere una sobrecarga adicional e innecesaria.</span><span class="sxs-lookup"><span data-stu-id="e503d-138">Setting the proxy user name and password every time an **HINTERNET** handle is created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) would require extra and unnecessary overhead.</span></span> <span data-ttu-id="e503d-139">Tenga en cuenta que si la aplicación usa un proxy que requiere autenticación, debe establecer las credenciales de proxy en cada nueva conexión.</span><span class="sxs-lookup"><span data-stu-id="e503d-139">Be aware that if the application uses a proxy that requires authentication, it should set the proxy credentials on every new connection.</span></span>

### <a name="setting-or-retrieving-the-options"></a><span data-ttu-id="e503d-140">Establecimiento o recuperación de las opciones</span><span class="sxs-lookup"><span data-stu-id="e503d-140">Setting or Retrieving the Options</span></span>

<span data-ttu-id="e503d-141">Cuando haya determinado qué opciones de Internet y identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) usar, recupere esas opciones de Internet.</span><span class="sxs-lookup"><span data-stu-id="e503d-141">When you have determined what Internet options and [**HINTERNET**](appendix-a-hinternet-handles.md) handle to use, retrieve those Internet options.</span></span> <span data-ttu-id="e503d-142">Para establecer o recuperar opciones, llame a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="e503d-142">To set or retrieve options, call either [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

## <a name="scope-of-hinternet-handle"></a><span data-ttu-id="e503d-143">Ámbito del identificador de HINTERNET</span><span class="sxs-lookup"><span data-stu-id="e503d-143">Scope of HINTERNET Handle</span></span>

<span data-ttu-id="e503d-144">El identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) que se usa para establecer o recuperar opciones de Internet determina las acciones para las que las opciones son válidas.</span><span class="sxs-lookup"><span data-stu-id="e503d-144">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle used to set or retrieve Internet options determines the actions for which the options are valid.</span></span>

<span data-ttu-id="e503d-145">Estos identificadores tienen tres niveles:</span><span class="sxs-lookup"><span data-stu-id="e503d-145">These handles have three levels:</span></span>

-   <span data-ttu-id="e503d-146">El identificador [**HINTERNET**](appendix-a-hinternet-handles.md) raíz (creado por una llamada a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) incluiría todas las opciones de Internet que afectan a esta instancia de Wininet.</span><span class="sxs-lookup"><span data-stu-id="e503d-146">The root [**HINTERNET**](appendix-a-hinternet-handles.md) handle (created by a call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) would contain all the Internet options that affect this instance of WinINet.</span></span>
-   <span data-ttu-id="e503d-147">[**HINTERNET**](appendix-a-hinternet-handles.md) controla que se conecta a un servidor (creado por una llamada a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))</span><span class="sxs-lookup"><span data-stu-id="e503d-147">[**HINTERNET**](appendix-a-hinternet-handles.md) handles that connect to a server (created by a call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))</span></span>
-   <span data-ttu-id="e503d-148">[**HINTERNET**](appendix-a-hinternet-handles.md) controla los identificadores asociados a un recurso o una enumeración de los recursos de un servidor determinado.</span><span class="sxs-lookup"><span data-stu-id="e503d-148">[**HINTERNET**](appendix-a-hinternet-handles.md) handles associated with a resource or enumeration of resources on a particular server.</span></span>

<span data-ttu-id="e503d-149">Además de los distintos identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) , una aplicación también puede usar **null** para establecer o recuperar los valores predeterminados de las opciones de Internet usadas por Internet Explorer y las funciones de Wininet.</span><span class="sxs-lookup"><span data-stu-id="e503d-149">In addition to the various [**HINTERNET**](appendix-a-hinternet-handles.md) handles, an application can also use **NULL** to set or retrieve the default values of the Internet options used by Internet Explorer and the WinINet functions.</span></span> <span data-ttu-id="e503d-150">Al establecer las opciones de Internet cuando se usa **null** como identificador, se cambian los valores predeterminados de las opciones, que se almacenan actualmente en el registro.</span><span class="sxs-lookup"><span data-stu-id="e503d-150">Setting Internet options when using **NULL** as the handle changes the default values of the options, which are currently stored in the registry.</span></span> <span data-ttu-id="e503d-151">Las aplicaciones cliente no deben usar funciones del registro para cambiar los valores predeterminados de las opciones de Internet, ya que la implementación de cómo se almacenan las opciones se puede modificar en el futuro.</span><span class="sxs-lookup"><span data-stu-id="e503d-151">Client applications should not use registry functions to change the default values of the Internet options, because the implementation of how the options are stored can be altered in the future.</span></span>

<span data-ttu-id="e503d-152">En la tabla siguiente se enumeran los tipos de identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) y el ámbito de las opciones de Internet asociadas a ellos.</span><span class="sxs-lookup"><span data-stu-id="e503d-152">The following table lists the type of [**HINTERNET**](appendix-a-hinternet-handles.md) handles and the scope of the Internet options associated with them.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e503d-153">Tipo de identificador</span><span class="sxs-lookup"><span data-stu-id="e503d-153">Handle Type</span></span></th>
<th><span data-ttu-id="e503d-154">Ámbito</span><span class="sxs-lookup"><span data-stu-id="e503d-154">Scope</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e503d-155"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="e503d-155"><strong>NULL</strong></span></span></td>
<td><span data-ttu-id="e503d-156">La configuración de opciones predeterminada de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e503d-156">The default option settings for Internet Explorer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e503d-157">INTERNET_HANDLE_TYPE_CONNECT_FTP</span><span class="sxs-lookup"><span data-stu-id="e503d-157">INTERNET_HANDLE_TYPE_CONNECT_FTP</span></span></td>
<td><span data-ttu-id="e503d-158">La configuración de la opción para esta conexión a un servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="e503d-158">The option settings for this connection to an FTP server.</span></span> <span data-ttu-id="e503d-159">Estas opciones afectan a las operaciones iniciadas desde este identificador de <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , como descargas de archivos.</span><span class="sxs-lookup"><span data-stu-id="e503d-159">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e503d-160">INTERNET_HANDLE_TYPE_CONNECT_GOPHER</span><span class="sxs-lookup"><span data-stu-id="e503d-160">INTERNET_HANDLE_TYPE_CONNECT_GOPHER</span></span></td>
<td><span data-ttu-id="e503d-161">La configuración de la opción para esta conexión a un servidor gopher.</span><span class="sxs-lookup"><span data-stu-id="e503d-161">The option settings for this connection to a Gopher server.</span></span> <span data-ttu-id="e503d-162">Estas opciones afectan a las operaciones iniciadas desde este identificador de <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , como descargas de archivos.</span><span class="sxs-lookup"><span data-stu-id="e503d-162">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e503d-163">Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="e503d-163">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e503d-164">INTERNET_HANDLE_TYPE_CONNECT_HTTP</span><span class="sxs-lookup"><span data-stu-id="e503d-164">INTERNET_HANDLE_TYPE_CONNECT_HTTP</span></span></td>
<td><span data-ttu-id="e503d-165">La configuración de la opción para esta conexión a un servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="e503d-165">The option settings for this connection to an HTTP server.</span></span> <span data-ttu-id="e503d-166">Estas opciones afectan a las operaciones iniciadas desde este identificador de <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , como descargas de archivos.</span><span class="sxs-lookup"><span data-stu-id="e503d-166">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e503d-167">INTERNET_HANDLE_TYPE_FILE_REQUEST</span><span class="sxs-lookup"><span data-stu-id="e503d-167">INTERNET_HANDLE_TYPE_FILE_REQUEST</span></span></td>
<td><span data-ttu-id="e503d-168">La configuración de opciones asociada a esta solicitud de archivo.</span><span class="sxs-lookup"><span data-stu-id="e503d-168">The option settings associated with this file request.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e503d-169">INTERNET_HANDLE_TYPE_FTP_FILE</span><span class="sxs-lookup"><span data-stu-id="e503d-169">INTERNET_HANDLE_TYPE_FTP_FILE</span></span></td>
<td><span data-ttu-id="e503d-170">La configuración de opciones asociada a esta descarga de recursos FTP.</span><span class="sxs-lookup"><span data-stu-id="e503d-170">The option settings associated with this FTP resource download.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e503d-171">INTERNET_HANDLE_TYPE_FTP_FILE_HTML</span><span class="sxs-lookup"><span data-stu-id="e503d-171">INTERNET_HANDLE_TYPE_FTP_FILE_HTML</span></span></td>
<td><span data-ttu-id="e503d-172">La configuración de opciones asociada a esta descarga de recursos FTP tiene el formato HTML.</span><span class="sxs-lookup"><span data-stu-id="e503d-172">The option settings associated with this FTP resource download formatted in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e503d-173">INTERNET_HANDLE_TYPE_FTP_FIND</span><span class="sxs-lookup"><span data-stu-id="e503d-173">INTERNET_HANDLE_TYPE_FTP_FIND</span></span></td>
<td><span data-ttu-id="e503d-174">La configuración de opciones asociada a esta búsqueda de archivos en un servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="e503d-174">The option settings associated with this search of files on an FTP server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e503d-175">INTERNET_HANDLE_TYPE_FTP_FIND_HTML</span><span class="sxs-lookup"><span data-stu-id="e503d-175">INTERNET_HANDLE_TYPE_FTP_FIND_HTML</span></span></td>
<td><span data-ttu-id="e503d-176">La configuración de opciones asociada a esta búsqueda de archivos en un servidor FTP con formato HTML.</span><span class="sxs-lookup"><span data-stu-id="e503d-176">The option settings associated with this search of files on an FTP server formatted in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e503d-177">INTERNET_HANDLE_TYPE_GOPHER_FILE</span><span class="sxs-lookup"><span data-stu-id="e503d-177">INTERNET_HANDLE_TYPE_GOPHER_FILE</span></span></td>
<td><span data-ttu-id="e503d-178">La configuración de opciones asociada a esta descarga de recursos Gopher.</span><span class="sxs-lookup"><span data-stu-id="e503d-178">The option settings associated with this Gopher resource download.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e503d-179">Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="e503d-179">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e503d-180">INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</span><span class="sxs-lookup"><span data-stu-id="e503d-180">INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</span></span></td>
<td><span data-ttu-id="e503d-181">La configuración de opciones asociada a esta descarga de recursos Gopher tiene el formato HTML.</span><span class="sxs-lookup"><span data-stu-id="e503d-181">The option settings associated with this Gopher resource download formatted in HTML.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e503d-182">Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="e503d-182">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e503d-183">INTERNET_HANDLE_TYPE_GOPHER_FIND</span><span class="sxs-lookup"><span data-stu-id="e503d-183">INTERNET_HANDLE_TYPE_GOPHER_FIND</span></span></td>
<td><span data-ttu-id="e503d-184">La configuración de opciones asociada a esta búsqueda de archivos en un servidor gopher.</span><span class="sxs-lookup"><span data-stu-id="e503d-184">The option settings associated with this search of files on an Gopher server.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e503d-185">Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="e503d-185">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e503d-186">INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</span><span class="sxs-lookup"><span data-stu-id="e503d-186">INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</span></span></td>
<td><span data-ttu-id="e503d-187">La configuración de opciones asociada a esta búsqueda de archivos en un servidor gopher con formato HTML.</span><span class="sxs-lookup"><span data-stu-id="e503d-187">The option settings associated with this search of files on an Gopher server formatted in HTML.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e503d-188">Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="e503d-188">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e503d-189">INTERNET_HANDLE_TYPE_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="e503d-189">INTERNET_HANDLE_TYPE_HTTP_REQUEST</span></span></td>
<td><span data-ttu-id="e503d-190">Configuración de opciones asociada a esta solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="e503d-190">The option settings associated with this HTTP request.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e503d-191">INTERNET_HANDLE_TYPE_INTERNET</span><span class="sxs-lookup"><span data-stu-id="e503d-191">INTERNET_HANDLE_TYPE_INTERNET</span></span></td>
<td><span data-ttu-id="e503d-192">Configuración de opciones asociada a esta instancia de las funciones de WinINet.</span><span class="sxs-lookup"><span data-stu-id="e503d-192">The option settings associated with this instance of the WinINet functions.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="setting-individual-options"></a><span data-ttu-id="e503d-193">Establecer opciones individuales</span><span class="sxs-lookup"><span data-stu-id="e503d-193">Setting Individual Options</span></span>

<span data-ttu-id="e503d-194">Después de determinar las opciones de Internet que desea establecer y el ámbito que desea que se vea afectado por estas opciones, el establecimiento de opciones de Internet no es complicado.</span><span class="sxs-lookup"><span data-stu-id="e503d-194">After determining the Internet options you want to set and the scope you want affected by these options, setting Internet options is not complicated.</span></span> <span data-ttu-id="e503d-195">Lo único que debe hacer es llamar a la función [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) deseado, la marca de opción de Internet y un búfer que contiene la información que desea establecer.</span><span class="sxs-lookup"><span data-stu-id="e503d-195">All you would need to do is call the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function with desired [**HINTERNET**](appendix-a-hinternet-handles.md) handle, Internet option flag, and a buffer that contains the information you want set.</span></span>

<span data-ttu-id="e503d-196">En el ejemplo siguiente se muestra cómo establecer el nombre de usuario y la contraseña de proxy en un identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="e503d-196">The following example shows how to set the proxy user name and password on a specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>


```C++
// strUsername is a string buffer of cchMax characters or less.
// It contains the proxy user name.
size_t cchMax = 80;
size_t cchUserLength, cchPasswordLength;
HRESULT hr = StringCchLength(strUsername, cchMax, &cchUserLength);

if (SUCCEEDED(hr))
{
   // hOpen is the HINTERNET handle created by InternetConnect.
   InternetSetOption(hConnect, INTERNET_OPTION_PROXY_USERNAME,
      strUsername, DWORD(cchUserLength)+1);
}
else
{
   // Insert error handling code here.
}

// strPassword is the string buffer that contains the proxy password.
hr = StringCchLength(strPassword, cchMax, &cchPasswordLength);

InternetSetOption(hOpen, INTERNET_OPTION_PROXY_PASSWORD,
    strPassword, DWORD(cchPasswordLength)+1);
```



## <a name="retrieving-individual-options"></a><span data-ttu-id="e503d-197">Recuperación de opciones individuales</span><span class="sxs-lookup"><span data-stu-id="e503d-197">Retrieving Individual Options</span></span>

<span data-ttu-id="e503d-198">Las opciones de Internet se pueden recuperar mediante la función [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .</span><span class="sxs-lookup"><span data-stu-id="e503d-198">Internet options can be retrieved using the [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) function.</span></span> <span data-ttu-id="e503d-199">Para recuperar opciones de Internet:</span><span class="sxs-lookup"><span data-stu-id="e503d-199">To retrieve Internet options:</span></span>

1.  <span data-ttu-id="e503d-200">Determine el tamaño del búfer necesario para recuperar la información de la opción de Internet.</span><span class="sxs-lookup"><span data-stu-id="e503d-200">Determine the buffer size necessary to retrieve the Internet option information.</span></span>

    <span data-ttu-id="e503d-201">El tamaño del búfer se puede determinar usando **null** para la dirección del búfer y pasándole un tamaño de búfer de cero.</span><span class="sxs-lookup"><span data-stu-id="e503d-201">The buffer size can be determined by using **NULL** for the address of the buffer and passing it a buffer size of zero.</span></span>

    ```C++
    DWORD dwSize;
    InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);
    ```

    

    <span data-ttu-id="e503d-202">El valor devuelto por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) es la cantidad de memoria necesaria para recuperar la información, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e503d-202">The value returned by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) is the amount of memory required to retrieve the information, in bytes.</span></span>

2.  <span data-ttu-id="e503d-203">Asigne una memoria para el búfer.</span><span class="sxs-lookup"><span data-stu-id="e503d-203">Allocate a memory for the buffer.</span></span>
    ```C++
    char *lpszData;
    lpszData = new char[dwSize];
    ```

    

3.  <span data-ttu-id="e503d-204">Recupere los datos.</span><span class="sxs-lookup"><span data-stu-id="e503d-204">Retrieve the data.</span></span>
    ```C++
    InternetQueryOption( NULL, 
                         INTERNET_OPTION_USER_AGENT,
                         lpszData, &dwSize );
    ```

    

4.  <span data-ttu-id="e503d-205">Libere memoria.</span><span class="sxs-lookup"><span data-stu-id="e503d-205">Free the memory.</span></span>
    ```C++
    delete [] lpszData;
    ```

    

### <a name="complete-sample"></a><span data-ttu-id="e503d-206">Ejemplo completo</span><span class="sxs-lookup"><span data-stu-id="e503d-206">Complete Sample</span></span>

<span data-ttu-id="e503d-207">A continuación se muestra el ejemplo completo usado en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="e503d-207">The following is the complete sample used in the previous section.</span></span> <span data-ttu-id="e503d-208">En este ejemplo se muestra cómo recuperar la cadena de agente de usuario predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e503d-208">This sample shows how to retrieve the default user agent string.</span></span>


```C++
// This call determines the required buffer size.
DWORD dwSize;
InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);

// Allocate the necessary memory.
char *lpszData;
lpszData = new char[dwSize];

// Call InternetQueryOption again with the provided buffer.
InternetQueryOption( NULL, 
                     INTERNET_OPTION_USER_AGENT,
                     lpszData, &dwSize );

// Insert code here to use the user agent string data.

// Free the allocated memory.
delete [] lpszData;
```



## <a name="setting-connection-options"></a><span data-ttu-id="e503d-209">Establecer opciones de conexión</span><span class="sxs-lookup"><span data-stu-id="e503d-209">Setting Connection Options</span></span>

<span data-ttu-id="e503d-210">En Internet Explorer 5 y versiones posteriores, se pueden establecer opciones de Internet para en una conexión específica.</span><span class="sxs-lookup"><span data-stu-id="e503d-210">In Internet Explorer 5 and later, Internet options can be set for on a specific connection.</span></span> <span data-ttu-id="e503d-211">Anteriormente, todas las conexiones compartían la misma configuración de opciones de Internet.</span><span class="sxs-lookup"><span data-stu-id="e503d-211">Previously, all connections shared the same Internet option settings.</span></span> <span data-ttu-id="e503d-212">Para establecer opciones para una conexión determinada:</span><span class="sxs-lookup"><span data-stu-id="e503d-212">To set options for a particular connection:</span></span>

1.  <span data-ttu-id="e503d-213">Cree una estructura de [**\_ lista de \_ \_ opciones \_ de Internet por**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) conexión.</span><span class="sxs-lookup"><span data-stu-id="e503d-213">Create an [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure.</span></span>
2.  <span data-ttu-id="e503d-214">Asigne la memoria para las opciones de Internet individuales que desea establecer para la conexión.</span><span class="sxs-lookup"><span data-stu-id="e503d-214">Allocate the memory for the individual Internet options that you want to set for the connection.</span></span>
3.  <span data-ttu-id="e503d-215">Establezca las opciones de las estructuras de opciones de [**Internet \_ por \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) conexión.</span><span class="sxs-lookup"><span data-stu-id="e503d-215">Set the options in [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span>
4.  <span data-ttu-id="e503d-216">Establezca las opciones mediante [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="e503d-216">Set the options using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="e503d-217">En el ejemplo de código siguiente se muestra cómo establecer los datos de proxy para una conexión LAN.</span><span class="sxs-lookup"><span data-stu-id="e503d-217">The following code example shows how to set proxy data for a LAN connection.</span></span>


```C++
BOOL SetConnectionOptions()
{
    INTERNET_PER_CONN_OPTION_LIST list;
    BOOL    bReturn;
    DWORD   dwBufSize = sizeof(list);

    // Fill the list structure.
    list.dwSize = sizeof(list);

    // NULL == LAN, otherwise connectoid name.
    list.pszConnection = NULL;

    // Set three options.
    list.dwOptionCount = 3;
    list.pOptions = new INTERNET_PER_CONN_OPTION[3];

    // Ensure that the memory was allocated.
    if(NULL == list.pOptions)
    {
        // Return FALSE if the memory wasn't allocated.
        return FALSE;
    }

    // Set flags.
    list.pOptions[0].dwOption = INTERNET_PER_CONN_FLAGS;
    list.pOptions[0].Value.dwValue = PROXY_TYPE_DIRECT |
        PROXY_TYPE_PROXY;

    // Set proxy name.
    list.pOptions[1].dwOption = INTERNET_PER_CONN_PROXY_SERVER;
    list.pOptions[1].Value.pszValue = TEXT("https://proxy:80");

    // Set proxy override.
    list.pOptions[2].dwOption = INTERNET_PER_CONN_PROXY_BYPASS;
    list.pOptions[2].Value.pszValue = TEXT("local");

    // Set the options on the connection.
    bReturn = InternetSetOption(NULL,
        INTERNET_OPTION_PER_CONNECTION_OPTION, &list, dwBufSize);

    // Free the allocated memory.
    delete [] list.pOptions;

    return bReturn;
}
```



## <a name="retrieving-connection-options"></a><span data-ttu-id="e503d-218">Recuperación de opciones de conexión</span><span class="sxs-lookup"><span data-stu-id="e503d-218">Retrieving Connection Options</span></span>

<span data-ttu-id="e503d-219">En Internet Explorer 5 y versiones posteriores, las opciones de Internet se pueden recuperar de una conexión específica.</span><span class="sxs-lookup"><span data-stu-id="e503d-219">In Internet Explorer 5 and later, Internet options can be retrieved from a specific connection.</span></span> <span data-ttu-id="e503d-220">Para recuperar opciones de una conexión determinada:</span><span class="sxs-lookup"><span data-stu-id="e503d-220">To retrieve options from a particular connection:</span></span>

1.  <span data-ttu-id="e503d-221">Cree una estructura de [**\_ lista de \_ \_ opciones \_ de Internet por**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) conexión.</span><span class="sxs-lookup"><span data-stu-id="e503d-221">Create a [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure.</span></span>
2.  <span data-ttu-id="e503d-222">Asigne la memoria para las opciones de Internet individuales que se van a recuperar de la conexión.</span><span class="sxs-lookup"><span data-stu-id="e503d-222">Allocate the memory for the individual Internet options to retrieve from the connection.</span></span>
3.  <span data-ttu-id="e503d-223">Especifique las opciones mediante las estructuras de opciones de [**Internet \_ por \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) conexión.</span><span class="sxs-lookup"><span data-stu-id="e503d-223">Specify the options using [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span>
4.  <span data-ttu-id="e503d-224">Recupere las opciones mediante [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="e503d-224">Retrieve the options using [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>
5.  <span data-ttu-id="e503d-225">Use los datos de la opción.</span><span class="sxs-lookup"><span data-stu-id="e503d-225">Utilize the option data.</span></span>
6.  <span data-ttu-id="e503d-226">Libere la memoria, asignada para contener los datos de la opción, mediante la función [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="e503d-226">Free the memory, allocated to hold the option data, using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span>

> [!Note]  
> <span data-ttu-id="e503d-227">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="e503d-227">WinINet does not support server implementations.</span></span> <span data-ttu-id="e503d-228">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="e503d-228">In addition, it should not be used from a service.</span></span> <span data-ttu-id="e503d-229">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="e503d-229">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e503d-230">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e503d-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e503d-231">Controlar la autenticación</span><span class="sxs-lookup"><span data-stu-id="e503d-231">Handling Authentication</span></span>](handling-authentication.md)
</dt> <dt>

[<span data-ttu-id="e503d-232">Controladores de HINTERNET</span><span class="sxs-lookup"><span data-stu-id="e503d-232">HINTERNET Handles</span></span>](appendix-a-hinternet-handles.md)
</dt> </dl>

 

