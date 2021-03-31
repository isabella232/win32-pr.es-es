---
description: El explorador de Windows controla la creación de un conector de búsqueda para un controlador de protocolo a través de entradas de clave del registro. A través del registro, tanto los implementadores como los de terceros pueden permitir que los controladores de protocolos nuevos y heredados participen en la búsqueda de Windows 7.
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: Crear un conector de búsqueda para un controlador de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b43fd7eac53ca2c89d6c8b0d2cd36fd813e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153986"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a><span data-ttu-id="86e59-104">Crear un conector de búsqueda para un controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="86e59-104">Creating a Search Connector for a Protocol Handler</span></span>

<span data-ttu-id="86e59-105">El explorador de Windows controla la creación de un conector de búsqueda para un controlador de protocolo a través de entradas de clave del registro.</span><span class="sxs-lookup"><span data-stu-id="86e59-105">Windows Explorer controls the creation of a search connector for a protocol handler through registry key entries.</span></span> <span data-ttu-id="86e59-106">A través del registro, tanto los implementadores como los de terceros pueden permitir que los controladores de protocolos nuevos y heredados participen en la búsqueda de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="86e59-106">Through the registry both implementers and third parties can enable new and legacy protocol handlers to participate in Windows 7 Search.</span></span>

<span data-ttu-id="86e59-107">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="86e59-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="86e59-108">Acerca de los conectores de búsqueda para los controladores de protocolo en Windows 7</span><span class="sxs-lookup"><span data-stu-id="86e59-108">About Search Connectors for Protocol Handlers in Windows 7</span></span>](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [<span data-ttu-id="86e59-109">Habilitar los controladores de protocolo para participar en la búsqueda</span><span class="sxs-lookup"><span data-stu-id="86e59-109">Enabling Protocol Handlers to Participate in Search</span></span>](#enabling-protocol-handlers-to-participate-in-search)
    -   [<span data-ttu-id="86e59-110">Deshabilitando la creación del conector de búsqueda del controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="86e59-110">Disabling Protocol Handler Search Connector Creation</span></span>](#disabling-protocol-handler-search-connector-creation)
    -   [<span data-ttu-id="86e59-111">Personalización del nombre, la descripción o el FolderType para un conector de búsqueda de controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="86e59-111">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [<span data-ttu-id="86e59-112">Usar el redireccionamiento de cadenas del registro</span><span class="sxs-lookup"><span data-stu-id="86e59-112">Using Registry String Redirection</span></span>](#using-registry-string-redirection)
    -   [<span data-ttu-id="86e59-113">Restaurar un conector de búsqueda de controlador de protocolo eliminado</span><span class="sxs-lookup"><span data-stu-id="86e59-113">Restoring a Deleted Protocol Handler Search Connector</span></span>](#restoring-a-deleted-protocol-handler-search-connector)
-   [<span data-ttu-id="86e59-114">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="86e59-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="86e59-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86e59-115">Related topics</span></span>](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a><span data-ttu-id="86e59-116">Acerca de los conectores de búsqueda para los controladores de protocolo en Windows 7</span><span class="sxs-lookup"><span data-stu-id="86e59-116">About Search Connectors for Protocol Handlers in Windows 7</span></span>

<span data-ttu-id="86e59-117">En Windows 7, las búsquedas desde el menú **Inicio** o el explorador de Windows incluyen solo archivos en ubicaciones indizadas y elementos del sistema que no son de archivos como los almacenes de datos remotos o los elementos de controlador de protocolo que tienen un conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="86e59-117">In Windows 7, searches from the **Start** menu or Windows Explorer include only files in indexed locations, and non-file system items such as remote data stores or protocol handler items that have a search connector.</span></span> <span data-ttu-id="86e59-118">Además de incluir los elementos de controlador de protocolo en el ámbito del menú **Inicio** y las búsquedas de Shell, el conector de búsqueda permite que el menú **Inicio** agrupe los elementos del controlador de protocolo en los resultados del menú **Inicio** , con la ventaja resultante de que el usuario puede hacer clic en el encabezado de grupo y ver los resultados solo desde el controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="86e59-118">In addition to including the protocol handler items in the scope of **Start** menu and Shell searches, the search connector enables the **Start** menu to group protocol handler items together in **Start** menu results, with the resulting benefit that the user can click the group header and view results from only the protocol handler.</span></span> <span data-ttu-id="86e59-119">Como alternativa, el usuario puede ir a la carpeta **búsquedas** , abrir el archivo del conector de búsqueda y realizar una búsqueda que incluya solo los elementos del controlador de protocolo específico asociado a ese conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="86e59-119">Alternatively, the user can navigate to the **Searches** folder, open the search connector file, and perform a search that includes only items from the specific protocol handler associated with that search connector.</span></span>

<span data-ttu-id="86e59-120">Cuando un usuario inicia por primera vez una aplicación que registra un controlador de protocolo, el explorador de Windows genera un archivo de conector de búsqueda (. searchConnector-MS) para el controlador de protocolo en la carpeta **búsquedas** del usuario.</span><span class="sxs-lookup"><span data-stu-id="86e59-120">When a user first starts an application that registers a protocol handler, Windows Explorer generates a search connector file (.searchConnector-ms) for the protocol handler in the user's **Searches** folder.</span></span> <span data-ttu-id="86e59-121">Las aplicaciones con controladores de protocolo pueden optar por deshabilitar este comportamiento o personalizar el nombre y la descripción del conector de búsqueda del controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="86e59-121">Applications with protocol handlers can choose to disable this behavior or customize the name and description of the protocol handler search connector.</span></span>

> [!Note]  
> <span data-ttu-id="86e59-122">La ubicación de la carpeta **búsquedas** del usuario es% userprofile% \\ búsquedas o FOLDERID \_ SavedSearches.</span><span class="sxs-lookup"><span data-stu-id="86e59-122">The location of the user's **Searches** folder is %userprofile%\\Searches, or FOLDERID\_SavedSearches.</span></span> <span data-ttu-id="86e59-123">El GUID para FOLDERID \_ SavedSearches es {7d1d3a04-Debb-4115-95cF-2f29da2920da}.</span><span class="sxs-lookup"><span data-stu-id="86e59-123">The GUID for FOLDERID\_SavedSearches is {7d1d3a04-debb-4115-95cf-2f29da2920da}.</span></span>

 

<span data-ttu-id="86e59-124">El explorador de Windows controla la creación de un conector de búsqueda para un controlador de protocolo a través de las entradas de clave del registro descritas en las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="86e59-124">Windows Explorer controls the creation of a search connector for a protocol handler through registry key entries described in the following sections:</span></span>

-   [<span data-ttu-id="86e59-125">Habilitar los controladores de protocolo para participar en la búsqueda</span><span class="sxs-lookup"><span data-stu-id="86e59-125">Enabling Protocol Handlers to Participate in Search</span></span>](#enabling-protocol-handlers-to-participate-in-search)
-   [<span data-ttu-id="86e59-126">Deshabilitando la creación del conector de búsqueda del controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="86e59-126">Disabling Protocol Handler Search Connector Creation</span></span>](#disabling-protocol-handler-search-connector-creation)
-   [<span data-ttu-id="86e59-127">Personalización del nombre, la descripción o el FolderType para un conector de búsqueda de controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="86e59-127">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [<span data-ttu-id="86e59-128">Restaurar un conector de búsqueda de controlador de protocolo eliminado</span><span class="sxs-lookup"><span data-stu-id="86e59-128">Restoring a Deleted Protocol Handler Search Connector</span></span>](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> <span data-ttu-id="86e59-129">No hay ningún medio de programación para crear un conector de búsqueda para un controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="86e59-129">There are no programmatic means to create a search connector for a protocol handler.</span></span> <span data-ttu-id="86e59-130">Deben configurarse a través del registro.</span><span class="sxs-lookup"><span data-stu-id="86e59-130">They must be configured through the registry.</span></span>

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a><span data-ttu-id="86e59-131">Habilitar los controladores de protocolo para participar en la búsqueda</span><span class="sxs-lookup"><span data-stu-id="86e59-131">Enabling Protocol Handlers to Participate in Search</span></span>

<span data-ttu-id="86e59-132">Las claves del registro y sus valores posibles se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="86e59-132">Registry keys and their possible values are outlined in the following table.</span></span> <span data-ttu-id="86e59-133">Un controlador de protocolo puede rellenar algunas o todas estas claves del registro <protocol> , donde se reemplaza por el nombre real de su Protocolo, como MAPI, archivo o CSC, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="86e59-133">A protocol handler can populate some or all of these registry keys where <protocol> is replaced with the actual name of its protocol, such as MAPI, file, or csc, for example.</span></span>



| <span data-ttu-id="86e59-134">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="86e59-134">Registry key</span></span>                                                                                                                 | <span data-ttu-id="86e59-135">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="86e59-135">Possible value(s)</span></span>                                                                                                                     | <span data-ttu-id="86e59-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="86e59-136">Type</span></span>       | <span data-ttu-id="86e59-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86e59-137">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86e59-138">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ versión</span><span class="sxs-lookup"><span data-stu-id="86e59-138">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Version</span></span>                     | <span data-ttu-id="86e59-139">No existe (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="86e59-139">Does not exist (default).</span></span> <span data-ttu-id="86e59-140">De lo contrario, es 1 o superior.</span><span class="sxs-lookup"><span data-stu-id="86e59-140">Otherwise it is 1 or greater.</span></span>                                                                               | <span data-ttu-id="86e59-141">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="86e59-141">REG\_DWORD</span></span> | <span data-ttu-id="86e59-142">Este valor se usa para detectar los cambios en los registros de la plantilla de ubicación para las raíces de búsqueda que ya se han procesado.</span><span class="sxs-lookup"><span data-stu-id="86e59-142">This value is used to detect changes to the location template registrations for search roots that have already been processed.</span></span> <span data-ttu-id="86e59-143">Si no existe, use 0 como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="86e59-143">If does not exist, use 0 as a default.</span></span> <span data-ttu-id="86e59-144">También puede incrementar la versión para informar al explorador de Windows de que el conector de búsqueda debe volver a generarse porque se ha instalado una versión más reciente del controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="86e59-144">Alternatively, increment the version to inform Windows Explorer that the search connector should be regenerated because a newer version of the protocol handler has been installed.</span></span> |
| <span data-ttu-id="86e59-145">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ DoNotCreateSearchConnectors</span><span class="sxs-lookup"><span data-stu-id="86e59-145">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\DoNotCreateSearchConnectors</span></span> | <span data-ttu-id="86e59-146">No existe (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="86e59-146">Does not exist (default).</span></span> <span data-ttu-id="86e59-147">De lo contrario, se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="86e59-147">Otherwise set to 1.</span></span>                                                                                         | <span data-ttu-id="86e59-148">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="86e59-148">REG\_DWORD</span></span> | <span data-ttu-id="86e59-149">Si no existe, cree un archivo. searchconnector-MS en la carpeta búsquedas.</span><span class="sxs-lookup"><span data-stu-id="86e59-149">If it does not exist, create a .searchconnector-ms file in the Searches folder.</span></span> <span data-ttu-id="86e59-150">Si es 1, marcar como procesado y no hacer nada.</span><span class="sxs-lookup"><span data-stu-id="86e59-150">If 1, mark as processed and do nothing.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="86e59-151">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ default \\ Description</span><span class="sxs-lookup"><span data-stu-id="86e59-151">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\Description</span></span>        | <span data-ttu-id="86e59-152">Una cadena localizable que contiene la descripción del conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="86e59-152">A localizable string containing the description of the search connector.</span></span>                                                              | <span data-ttu-id="86e59-153">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="86e59-153">REG\_SZ</span></span>    | <span data-ttu-id="86e59-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="86e59-154">Optional.</span></span> <span data-ttu-id="86e59-155">Se usa en el elemento Description del archivo. searchconnector-ms.</span><span class="sxs-lookup"><span data-stu-id="86e59-155">It is used in the Description element of the .searchconnector-ms file.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="86e59-156">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ \\ nombre predeterminado</span><span class="sxs-lookup"><span data-stu-id="86e59-156">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\Name</span></span>               | <span data-ttu-id="86e59-157">Una cadena localizada para asignar un nombre al conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="86e59-157">A localized string to name the search connector.</span></span> <span data-ttu-id="86e59-158">Se usa como nombre del archivo. searchconnector-ms.</span><span class="sxs-lookup"><span data-stu-id="86e59-158">Used as the name of the .searchconnector-ms file.</span></span>                                    | <span data-ttu-id="86e59-159">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="86e59-159">REG\_SZ</span></span>    | <span data-ttu-id="86e59-160">Cada ubicación debe tener un nombre único.</span><span class="sxs-lookup"><span data-stu-id="86e59-160">Each location must have a unique name.</span></span> <span data-ttu-id="86e59-161">En ausencia de este valor, se usará el nombre para mostrar proporcionado por la [interfaz IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) del controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="86e59-161">In the absence of this value, the display name provided by the protocol handler's [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) will be used.</span></span>                                                                                                                             |
| <span data-ttu-id="86e59-162">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ default \\ FolderType</span><span class="sxs-lookup"><span data-stu-id="86e59-162">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\FolderType</span></span>         | <span data-ttu-id="86e59-163">GUID que identifica el [FOLDERTYPEID](../shell/foldertypeid.md) que se va a aplicar al conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="86e59-163">A GUID identifying the [FOLDERTYPEID](../shell/foldertypeid.md) to apply to the search connector.</span></span> | <span data-ttu-id="86e59-164">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="86e59-164">REG\_SZ</span></span>    | <span data-ttu-id="86e59-165">Opcional.</span><span class="sxs-lookup"><span data-stu-id="86e59-165">Optional.</span></span> <span data-ttu-id="86e59-166">Se usa en el elemento folderType del archivo. searchconnector-ms para indicar qué plantillas deben usarse para mostrar los resultados.</span><span class="sxs-lookup"><span data-stu-id="86e59-166">Used in the folderType element of the .searchconnector-ms file to indicate what templates should be used to display results.</span></span> <span data-ttu-id="86e59-167">Por ejemplo, el valor GUID de FOLDERTYPEID \_ Documents.</span><span class="sxs-lookup"><span data-stu-id="86e59-167">For example, the GUID value of FOLDERTYPEID\_Documents.</span></span>                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a><span data-ttu-id="86e59-168">Deshabilitando la creación del conector de búsqueda del controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="86e59-168">Disabling Protocol Handler Search Connector Creation</span></span>

<span data-ttu-id="86e59-169">Si la aplicación expone elementos a través de un controlador de protocolo para su uso en la propia aplicación y no desea exponer los elementos a través del shell (en el menú **Inicio** y búsquedas del explorador de Windows), debe deshabilitar la creación de un conector de búsqueda para el controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="86e59-169">If your application exposes items through a protocol handler for use in the application itself and you do not want to expose the items through the Shell (in **Start** menu and Windows Explorer searches), you need to disable the creation of a search connector for your protocol handler.</span></span>

<span data-ttu-id="86e59-170">Para deshabilitar la creación del conector de búsqueda, establezca DoNotCreateSearchConnectors en 0x00000001 (1), tal y como se muestra en el siguiente ejemplo de clave del registro.</span><span class="sxs-lookup"><span data-stu-id="86e59-170">To disable search connector creation set DoNotCreateSearchConnectors to 0x00000001(1), as shown in the following registry key example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

<span data-ttu-id="86e59-171">Si DoNotCreateSearchConnectors se establece en 1, se recomienda que exponga la propiedad [System. Shell. OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) en cada elemento expuesto por el controlador de protocolo y establezca el valor de esta propiedad en **true**.</span><span class="sxs-lookup"><span data-stu-id="86e59-171">If DoNotCreateSearchConnectors is set to 1, then we recommend that you expose the [System.Shell.OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) property on each item exposed by the protocol handler, and set the value of this property to **TRUE**.</span></span> <span data-ttu-id="86e59-172">Esto impedirá que los elementos del controlador de protocolo aparezcan en el grupo **archivos** del menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="86e59-172">Doing so will prevent the protocol handler items from appearing under the **Start** menu **Files** group.</span></span>

<span data-ttu-id="86e59-173">Si DoNotCreateSearchConnectors está presente y se establece en cero, el explorador de Windows creará un conector de búsqueda para el controlador de protocolo y los elementos del controlador de protocolo se devolverán en el menú **Inicio** y las búsquedas del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="86e59-173">If DoNotCreateSearchConnectors is present and set to zero, then Windows Explorer will create a search connector for the protocol handler, and the protocol handler items will be returned in in **Start** menu and Windows Explorer searches.</span></span>

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a><span data-ttu-id="86e59-174">Personalización del nombre, la descripción o el FolderType para un conector de búsqueda de controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="86e59-174">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>

<span data-ttu-id="86e59-175">El nombre del conector de búsqueda se usa no solo para identificar el conector de búsqueda en la carpeta **búsquedas** , sino como el encabezado de grupo de los resultados en las búsquedas en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="86e59-175">The search connector name is used not only to identify the search connector in the **Searches** folder, but as the group header for the results in **Start** menu searches.</span></span> <span data-ttu-id="86e59-176">Por lo tanto, es importante proporcionar un nombre descriptivo para el conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="86e59-176">Hence, it is important to provide a descriptive name for the search connector.</span></span> <span data-ttu-id="86e59-177">Si no se proporciona un nombre en la clave del registro, de forma predeterminada el explorador de Windows utiliza el nombre proporcionado por la [interfaz IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) para la raíz de búsqueda del controlador de protocolo y la descripción en blanco.</span><span class="sxs-lookup"><span data-stu-id="86e59-177">If a name is not provided in the registry key, by default Windows Explorer uses the name provided by [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) for the protocol handler's search root and blank description.</span></span> <span data-ttu-id="86e59-178">Puede invalidar el nombre predeterminado a través de una entrada de clave del registro sin tener que cambiar el nombre de la interfaz IShellFolder.</span><span class="sxs-lookup"><span data-stu-id="86e59-178">You can override the default name through a registry key entry without having to rename the IShellFolder Interface.</span></span> <span data-ttu-id="86e59-179">Aunque no es tan visible como el nombre del conector de búsqueda, también puede invalidar la descripción del conector de búsqueda proporcionando su propia descripción.</span><span class="sxs-lookup"><span data-stu-id="86e59-179">Although it is not as visible as the search connector name, you can also override the description for the search connector by providing your own description.</span></span>

<span data-ttu-id="86e59-180">Para reemplazar el nombre o la descripción predeterminados, establezca las entradas tal como se muestra en el siguiente ejemplo del registro.</span><span class="sxs-lookup"><span data-stu-id="86e59-180">To override the default name or description, set the entries as shown in the following registry example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     Name
                     Description
```

<span data-ttu-id="86e59-181">Además, la entrada FolderType se puede establecer en uno de los GUID de [FOLDERTYPEID](../shell/foldertypeid.md) .</span><span class="sxs-lookup"><span data-stu-id="86e59-181">In addition, the FolderType entry can be set to one of the [FOLDERTYPEID](../shell/foldertypeid.md) GUIDs.</span></span> <span data-ttu-id="86e59-182">El valor debe ser el GUID real, no su nombre.</span><span class="sxs-lookup"><span data-stu-id="86e59-182">The value should be the actual GUID, and not its name.</span></span> <span data-ttu-id="86e59-183">Por ejemplo, {94d6ddcc-4a68-4175-A374-bd584a510b78} en lugar de FOLDERTYPEID \_ Music.</span><span class="sxs-lookup"><span data-stu-id="86e59-183">For example, {94d6ddcc-4a68-4175-a374-bd584a510b78} rather than FOLDERTYPEID\_Music.</span></span> <span data-ttu-id="86e59-184">El GUID de una FOLDERTYPEID se puede obtener en el archivo de encabezado Shlguid. h en el [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="86e59-184">The GUID for a FOLDERTYPEID can be obtained in the Shlguid.h header file in the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     FolderType = {94d6ddcc-4a68-4175-a374-bd584a510b78}
```

### <a name="using-registry-string-redirection"></a><span data-ttu-id="86e59-185">Usar el redireccionamiento de cadenas del registro</span><span class="sxs-lookup"><span data-stu-id="86e59-185">Using Registry String Redirection</span></span>

<span data-ttu-id="86e59-186">Puede usar una [cadena redirigida](../intl/using-registry-string-redirection.md) para asegurarse de que se puede localizar el nombre proporcionado para el conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="86e59-186">You can use a [redirected string](../intl/using-registry-string-redirection.md) to ensure that the name you provide for the search connector can be localized.</span></span> <span data-ttu-id="86e59-187">Puede incluir cadenas localizables para las claves del registro Name y Description en lugar de escribir la cadena real en el registro.</span><span class="sxs-lookup"><span data-stu-id="86e59-187">You can include localizable strings for the name and description registry keys instead of entering the actual string into the registry.</span></span>

<span data-ttu-id="86e59-188">Para incluir una cadena localizable para los valores de nombre o descripción, establezca el valor como se muestra en el siguiente ejemplo de clave del registro.</span><span class="sxs-lookup"><span data-stu-id="86e59-188">To include a localizable string for the Name or Description values, set the value as shown in the following registry key example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Name = @dllname.dll,-resourceID
```

<span data-ttu-id="86e59-189">La cadena traducible tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="86e59-189">The localizable string takes the following format:</span></span>

-   <span data-ttu-id="86e59-190">@dllname.dll,-resourceID, donde:</span><span class="sxs-lookup"><span data-stu-id="86e59-190">@dllname.dll,-resourceID, where:</span></span>
    -   <span data-ttu-id="86e59-191">@dllname.dll es la ruta de acceso al archivo DLL que contiene el recurso de cadena.</span><span class="sxs-lookup"><span data-stu-id="86e59-191">@dllname.dll is the path to the DLL that contains the string resource</span></span>
    -   <span data-ttu-id="86e59-192">resourceID es el identificador de recurso entero del recurso de cadena</span><span class="sxs-lookup"><span data-stu-id="86e59-192">resourceID is the integer resource ID of the string resource</span></span>

<span data-ttu-id="86e59-193">El formato de una cadena indirecta y una cadena indirecta anexada con un modificador de versión se describen en la [función SHLoadIndirectString](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span><span class="sxs-lookup"><span data-stu-id="86e59-193">The format for an indirect string, and an indirect string appended with a version modifier, is described in [SHLoadIndirectString Function](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span></span>

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a><span data-ttu-id="86e59-194">Restaurar un conector de búsqueda de controlador de protocolo eliminado</span><span class="sxs-lookup"><span data-stu-id="86e59-194">Restoring a Deleted Protocol Handler Search Connector</span></span>

<span data-ttu-id="86e59-195">Dado que los conectores de búsqueda son archivos en el equipo del usuario, se pueden eliminar por error.</span><span class="sxs-lookup"><span data-stu-id="86e59-195">Because search connectors are files on the user's computer, they can be mistakenly deleted.</span></span> <span data-ttu-id="86e59-196">Para restaurar todos los conectores de búsqueda del controlador de protocolo eliminados, restaure las bibliotecas predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="86e59-196">To restore all deleted protocol handler search connectors, restore the default libraries.</span></span> <span data-ttu-id="86e59-197">Para ello, abra el explorador de Windows, haga clic con el botón secundario en la carpeta **bibliotecas** y, a continuación, seleccione **restaurar bibliotecas predeterminadas**.</span><span class="sxs-lookup"><span data-stu-id="86e59-197">To so do, open Windows Explorer, right-click the **Libraries** folder, and then select **Restore Default Libraries**.</span></span>

![captura de pantalla que muestra la opción de menú restaurar bibliotecas predeterminadas](images/libraries.png)

## <a name="additional-resources"></a><span data-ttu-id="86e59-199">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="86e59-199">Additional Resources</span></span>

-   [<span data-ttu-id="86e59-200">IShellItem:: GetDisplayName</span><span class="sxs-lookup"><span data-stu-id="86e59-200">IShellItem::GetDisplayName</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [<span data-ttu-id="86e59-201">SIGDN \_ NORMALDISPLAY</span><span class="sxs-lookup"><span data-stu-id="86e59-201">SIGDN\_NORMALDISPLAY</span></span>](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a><span data-ttu-id="86e59-202">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86e59-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="86e59-203">**Vista**</span><span class="sxs-lookup"><span data-stu-id="86e59-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="86e59-204">Descripción de los controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="86e59-204">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="86e59-205">Desarrollar controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="86e59-205">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="86e59-206">Notificar el índice de cambios</span><span class="sxs-lookup"><span data-stu-id="86e59-206">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="86e59-207">Agregar iconos y menús contextuales</span><span class="sxs-lookup"><span data-stu-id="86e59-207">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="86e59-208">Código de ejemplo: extensiones de Shell para controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="86e59-208">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="86e59-209">Instalar y registrar controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="86e59-209">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="86e59-210">Controladores de protocolo de depuración</span><span class="sxs-lookup"><span data-stu-id="86e59-210">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
