---
title: Llamar a WDS desde la línea de comandos
description: Puede iniciar la interfaz de usuario de búsqueda de escritorio de Microsoft Windows (WDS) con un filtro, un almacén y una consulta específicos desde otra aplicación o una página web que use el objeto auxiliar de explorador (BHO) mediante el uso de la sintaxis de la línea de comandos de windowssearch.exe.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efae7aebc13f578e9c5c32542b451d3600a93a2b
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2020
ms.locfileid: "103789160"
---
# <a name="calling-wds-from-the-command-line"></a><span data-ttu-id="197b8-103">Llamar a WDS desde la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="197b8-103">Calling WDS from the Command Line</span></span>

> [!NOTE]
> <span data-ttu-id="197b8-104">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="197b8-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="197b8-105">En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="197b8-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="197b8-106">Puede iniciar la interfaz de usuario de búsqueda de escritorio de Microsoft Windows (WDS) con un filtro, un almacén y una consulta específicos desde otra aplicación o una página web que use el objeto auxiliar de explorador (BHO) mediante el uso de la sintaxis de la línea de comandos de windowssearch.exe.</span><span class="sxs-lookup"><span data-stu-id="197b8-106">You can launch the Microsoft Windows Desktop Search (WDS) user interface with a specific filter, store, and query from another application or a webpage that uses the Browser Helper Object (BHO) by using the windowssearch.exe command line syntax.</span></span> <span data-ttu-id="197b8-107">Cuando se llama a WDS desde la línea de comandos, no se devuelve información sobre las acciones o la selección del usuario en la ventana de WDS a la aplicación o página web que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="197b8-107">When calling WDS from the command line, no information about the user's actions or selection in the WDS window is returned to the calling application or webpage.</span></span>

<span data-ttu-id="197b8-108">La ruta de instalación de WDS se especifica en la configuración del registro InstallDir en HKEY_LOCAL_MACHINE \\ software \\ Microsoft \\ Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="197b8-108">The WDS installation path is specified in the InstallDir registry setting under HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows Desktop Search.</span></span> <span data-ttu-id="197b8-109">La ruta de acceso predeterminada en la que se instala windowssearch.exe es archivos de programa de \\ Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="197b8-109">The default path that windowssearch.exe is installed to is Program Files\\Windows Desktop Search.</span></span>

## <a name="command-line-syntax"></a><span data-ttu-id="197b8-110">Sintaxis de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="197b8-110">Command Line Syntax</span></span>

<span data-ttu-id="197b8-111">La siguiente sintaxis se aplica a la interfaz de la línea de comandos de Windows Desktop Search 2. x.</span><span class="sxs-lookup"><span data-stu-id="197b8-111">The following syntax applies to the Windows Desktop Search 2.x command-line interface.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="197b8-112">Opciones</span><span class="sxs-lookup"><span data-stu-id="197b8-112">Options</span></span></th>
<th><span data-ttu-id="197b8-113">Parámetro</span><span class="sxs-lookup"><span data-stu-id="197b8-113">Parameter</span></span></th>
<th><span data-ttu-id="197b8-114">Significado</span><span class="sxs-lookup"><span data-stu-id="197b8-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="197b8-115">/startup</span><span class="sxs-lookup"><span data-stu-id="197b8-115">/startup</span></span></td>

<td><span data-ttu-id="197b8-116">Inicializa la búsqueda en el escritorio de Windows</span><span class="sxs-lookup"><span data-stu-id="197b8-116">Initializes Windows Desktop Search</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="197b8-117">/indexnow</span><span class="sxs-lookup"><span data-stu-id="197b8-117">/indexnow</span></span></td>

<td><span data-ttu-id="197b8-118">Desactiva el retroceso de la indización y vuelve a examinar todas las ubicaciones de los índices</span><span class="sxs-lookup"><span data-stu-id="197b8-118">Turns off indexing back-off and rescans all index locations</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="197b8-119">/showstatus</span><span class="sxs-lookup"><span data-stu-id="197b8-119">/showstatus</span></span></td>

<td><span data-ttu-id="197b8-120">Muestra la ventana de estado de indización</span><span class="sxs-lookup"><span data-stu-id="197b8-120">Shows the indexing status window</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="197b8-121">/launchsearchwindow o/URL</span><span class="sxs-lookup"><span data-stu-id="197b8-121">/launchsearchwindow or /url</span></span></td>

<td><span data-ttu-id="197b8-122">Abre una ventana de WDS con una consulta vacía</span><span class="sxs-lookup"><span data-stu-id="197b8-122">Opens a WDS window with an empty query</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="197b8-123">/URL</span><span class="sxs-lookup"><span data-stu-id="197b8-123">/url</span></span></td>
<td><span data-ttu-id="197b8-124">buscar: [tienda | Mostrar | consulta] cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="197b8-124">search:[store|show|query] query string</span></span></td>
<td><span data-ttu-id="197b8-125">Abre una ventana de WDS con una consulta y un filtro en función de los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="197b8-125">Opens a WDS window with a query and filter based on the following parameters:</span></span>
<ul>
<li><p><span data-ttu-id="197b8-126">almacén: especifica el origen de datos que se va a consultar: archivos, Outlook, outlookexpress.</span><span class="sxs-lookup"><span data-stu-id="197b8-126">store - Specifies the data source to query: files, outlook, outlookexpress.</span></span> <span data-ttu-id="197b8-127">Si no se especifica, se buscará en todos los almacenes.</span><span class="sxs-lookup"><span data-stu-id="197b8-127">If not specified all stores will be searched.</span></span> <br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="197b8-128">Aunque la sintaxis de consulta avanzada admite hacer referencia a Microsoft Outlook como ' OE ', el parámetro Store de la línea de comandos debe ser ' outlookexpress '.</span><span class="sxs-lookup"><span data-stu-id="197b8-128">While Advanced Query Syntax supports referencing Microsoft Outlook as 'oe', the store parameter on the command line must be 'outlookexpress'.</span></span>
</blockquote>
<p><br/></p></li>
<li><p><span data-ttu-id="197b8-129">Show: especifica el tipo de resultados percibido que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="197b8-129">show - Specifies which perceived type of results to return.</span></span> <span data-ttu-id="197b8-130">Vea <a href="-search-2x-wds-perceivedtype.md">tipos percibidos</a> para obtener una lista completa de tipos.</span><span class="sxs-lookup"><span data-stu-id="197b8-130">See <a href="-search-2x-wds-perceivedtype.md">Perceived Types</a> for a complete list of types.</span></span> <span data-ttu-id="197b8-131">Si no se especifica, se devolverán todos los tipos.</span><span class="sxs-lookup"><span data-stu-id="197b8-131">If not specified, all types will be returned.</span></span> <br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="197b8-132">Hay tres diferencias entre los valores de tipo percibidos y los valores de show.</span><span class="sxs-lookup"><span data-stu-id="197b8-132">There are three differences between the perceived type values and the values for show.</span></span> <span data-ttu-id="197b8-133">Para <code>show</code> , use ' Documents ' en lugar de ' doc ', ' Pictures ' en lugar de ' pics ' y ' textdocuments ' en lugar de ' text '.</span><span class="sxs-lookup"><span data-stu-id="197b8-133">For <code>show</code>, use 'documents' instead of 'doc', 'pictures' instead of 'pics', and 'textdocuments' instead of 'text'.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="197b8-134">consulta: especifica los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="197b8-134">query - Specifies the search criteria.</span></span> <span data-ttu-id="197b8-135">Este valor admite parámetros de <a href="-search-2x-wds-aqsreference.md">Sintaxis de consulta avanzada</a> para refinar los resultados.</span><span class="sxs-lookup"><span data-stu-id="197b8-135">This value supports <a href="-search-2x-wds-aqsreference.md">Advanced Query Syntax</a> parameters to refine the results.</span></span> <span data-ttu-id="197b8-136">El parámetro de consulta debe ser el último parámetro de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="197b8-136">The query parameter must be the last parameter in the URL.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a><span data-ttu-id="197b8-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="197b8-137">Example</span></span>

<span data-ttu-id="197b8-138">Por ejemplo, para buscar imágenes que coincidan con los criterios ' papel tapiz ', use el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="197b8-138">For example, to search all files for pictures matching the criteria 'wallpaper' use the following command:</span></span>

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a><span data-ttu-id="197b8-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="197b8-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="197b8-140">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="197b8-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="197b8-141">Sintaxis de consulta avanzada</span><span class="sxs-lookup"><span data-stu-id="197b8-141">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="197b8-142">Tipos percibidos</span><span class="sxs-lookup"><span data-stu-id="197b8-142">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="197b8-143">Llamar a WDS desde páginas web</span><span class="sxs-lookup"><span data-stu-id="197b8-143">Calling WDS from Web Pages</span></span>](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





