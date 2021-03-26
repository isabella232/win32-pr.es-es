---
description: Una matriz de asociación es una lista ordenada de ubicaciones del registro que se utiliza para almacenar información sobre un tipo de elemento, incluidos los controladores, los verbos y otros atributos, como el icono y el nombre para mostrar del tipo.
title: Matrices de asociación
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9ECD19CA-833E-4565-A0EF-FB16BF7B3F44
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 75d42a8758e5c6380414c7b93979b4f93cafd013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154131"
---
# <a name="association-arrays"></a><span data-ttu-id="8e583-103">Matrices de asociación</span><span class="sxs-lookup"><span data-stu-id="8e583-103">Association Arrays</span></span>

<span data-ttu-id="8e583-104">Una matriz de asociación es una lista ordenada de ubicaciones del registro que se utiliza para almacenar información sobre un tipo de elemento, incluidos los controladores, los verbos y otros atributos, como el icono y el nombre para mostrar del tipo.</span><span class="sxs-lookup"><span data-stu-id="8e583-104">An association array is an ordered list of registry locations used to store information about an item type, including handlers, verbs, and other attributes like the icon and display name of the type.</span></span> <span data-ttu-id="8e583-105">El shell utiliza matrices de Asociación para consultar un conjunto predefinido de ubicaciones del registro que pueden contener información sobre un elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="8e583-105">The Shell uses association arrays to query a predefined set of registry locations that might contain information about a Shell item.</span></span>

<span data-ttu-id="8e583-106">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e583-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="8e583-107">Acerca de las matrices de asociación</span><span class="sxs-lookup"><span data-stu-id="8e583-107">About Association Arrays</span></span>](#about-association-arrays)
-   [<span data-ttu-id="8e583-108">Consultar matrices de asociación</span><span class="sxs-lookup"><span data-stu-id="8e583-108">Querying Association Arrays</span></span>](#querying-association-arrays)
-   [<span data-ttu-id="8e583-109">Trabajar con matrices de Asociación para un origen de datos de Shell determinado</span><span class="sxs-lookup"><span data-stu-id="8e583-109">Working with Association Arrays for a Particular Shell Data Source</span></span>](#working-with-association-arrays-for-a-particular-shell-data-source)
    -   [<span data-ttu-id="8e583-110">Matrices de Asociación de orígenes de datos de Shell</span><span class="sxs-lookup"><span data-stu-id="8e583-110">Shell Data Source Association Arrays</span></span>](#shell-data-source-association-arrays)
-   [<span data-ttu-id="8e583-111">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8e583-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="8e583-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8e583-112">Related topics</span></span>](#related-topics)

## <a name="about-association-arrays"></a><span data-ttu-id="8e583-113">Acerca de las matrices de asociación</span><span class="sxs-lookup"><span data-stu-id="8e583-113">About Association Arrays</span></span>

<span data-ttu-id="8e583-114">Una matriz de asociación es una lista ordenada de ubicaciones del registro que contienen información sobre un tipo de elemento, incluidos los controladores, los verbos y otros atributos, como el icono y el nombre para mostrar del tipo.</span><span class="sxs-lookup"><span data-stu-id="8e583-114">An association array is an ordered list of registry locations that contain information about an item type, including handlers, verbs, and other attributes such as the icon and display name of the type.</span></span> <span data-ttu-id="8e583-115">Esta información sobre el tipo de elemento se puede registrar en distintos niveles de especificidad.</span><span class="sxs-lookup"><span data-stu-id="8e583-115">This information about the item type can be registered at varying levels of specificity.</span></span> <span data-ttu-id="8e583-116">Por ejemplo, puede registrar un verbo que se mostrará solo para un tipo de archivo específico (como. jpg) o para todos los elementos que tengan el mismo System. Kind (por ejemplo, System. Kind = Picture) o para todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="8e583-116">For example, you can register a verb that will show up only for a specific file type (such as .jpg), or for all items with the same System.Kind (for example, System.kind = picture), or for all items.</span></span>

<span data-ttu-id="8e583-117">El shell utiliza matrices de Asociación para consultar un conjunto predefinido de ubicaciones del registro que podrían contener información sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="8e583-117">The Shell uses association arrays to query a predefined set of registry locations that might potentially contain information about the item.</span></span> <span data-ttu-id="8e583-118">Las API de la matriz de asociación se pueden usar para recuperar de la subclave del registro un valor único que contiene la información solicitada, con ese valor procedente de la primera entrada de la matriz que lo proporciona.</span><span class="sxs-lookup"><span data-stu-id="8e583-118">The association array APIs can be used to retrieve from the registry subkey a single value that contains the requested information, with that value coming from the first entry in the array that provides it.</span></span> <span data-ttu-id="8e583-119">Por ejemplo, el valor del icono predeterminado se recupera de esta manera.</span><span class="sxs-lookup"><span data-stu-id="8e583-119">For example, the default icon value is retrieved this way.</span></span> <span data-ttu-id="8e583-120">La matriz de asociación también se puede utilizar para recuperar un conjunto de valores que se almacenan en las subclaves del registro.</span><span class="sxs-lookup"><span data-stu-id="8e583-120">The association array can also be used to retrieve a set of values that are stored in the registry subkeys.</span></span> <span data-ttu-id="8e583-121">Por ejemplo, la lista de verbos se genera a partir de los verbos que se registran en todas las subclaves.</span><span class="sxs-lookup"><span data-stu-id="8e583-121">For example, the list of verbs is built from those verbs that are registered under all the subkeys.</span></span>

<span data-ttu-id="8e583-122">Una vez que el shell consulta un conjunto predefinido de ubicaciones del registro para obtener información sobre un elemento de Shell, coloca las ubicaciones del registro en una matriz en orden desde la ubicación más específica a la más general.</span><span class="sxs-lookup"><span data-stu-id="8e583-122">After the Shell queries a predefined set of registry locations for information about a Shell item, it puts the registry locations into an array in order from the most specific location to the most general.</span></span>

<span data-ttu-id="8e583-123">Dado que las matrices de asociación son listas ordenadas, proporcionan a los desarrolladores de aplicaciones un mecanismo para agregar información al registro que se devolverá para un tipo de elemento específico.</span><span class="sxs-lookup"><span data-stu-id="8e583-123">Because association arrays are ordered lists, they provide application developers with a mechanism for adding information to the registry that will be returned for a specific type of item.</span></span> <span data-ttu-id="8e583-124">Del mismo modo, las matrices de asociación permiten a los desarrolladores de aplicaciones agregar información al registro para un grupo específico de elementos cuando esos elementos se registran en una ubicación más general.</span><span class="sxs-lookup"><span data-stu-id="8e583-124">Likewise, association arrays permit application developers to add information to the registry for a specific group of items when those items are registered at a more general location.</span></span> <span data-ttu-id="8e583-125">Esta lógica informa de la decisión sobre la ubicación más adecuada en el registro para almacenar información sobre los elementos de Shell.</span><span class="sxs-lookup"><span data-stu-id="8e583-125">This logic informs your decision about the most appropriate location in the registry to store information about Shell items.</span></span>

<span data-ttu-id="8e583-126">En un sistema Windows predeterminado, un archivo. jpg tiene la siguiente matriz de asociación:</span><span class="sxs-lookup"><span data-stu-id="8e583-126">On a default Windows system a .jpg file has the following association array:</span></span>

-   <span data-ttu-id="8e583-127">**HKEY \_ Jpgfile \_ raíz de clases** \\ </span><span class="sxs-lookup"><span data-stu-id="8e583-127">**HKEY\_CLASSES\_ROOT**\\**jpgfile**</span></span>
-   <span data-ttu-id="8e583-128">**HKEY \_ Clases \_ raíz** \\ **SystemFileAssociations** \\ **. jpg**</span><span class="sxs-lookup"><span data-stu-id="8e583-128">**HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ **.jpg**</span></span>
-   <span data-ttu-id="8e583-129">**HKEY \_ Imagen \_ raíz de clases** \\ </span><span class="sxs-lookup"><span data-stu-id="8e583-129">**HKEY\_CLASSES\_ROOT**\\**image**</span></span>
-   <span data-ttu-id="8e583-130">**HKEY \_ \_raíz de clases** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="8e583-130">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>
-   <span data-ttu-id="8e583-131">_ *HKEY \_ classes \_ root **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="8e583-131">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span>

<span data-ttu-id="8e583-132">Para obtener información sobre cómo registrar matrices de asociación, vea [registro de aplicaciones](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="8e583-132">For information on registering association arrays, see [Application Registration](app-registration.md).</span></span>

## <a name="querying-association-arrays"></a><span data-ttu-id="8e583-133">Consultar matrices de asociación</span><span class="sxs-lookup"><span data-stu-id="8e583-133">Querying Association Arrays</span></span>

<span data-ttu-id="8e583-134">Hay API de Shell para recuperar información de un intervalo de subclaves del registro, desde la subclave del registro más específica hasta un supraconjunto de la información en todas las subclaves del registro.</span><span class="sxs-lookup"><span data-stu-id="8e583-134">There are Shell APIs to retrieve information from a range of registry subkeys, from the most specific registry subkey to a superset of the information across all registry subkeys.</span></span>

<span data-ttu-id="8e583-135">El uso más común de una matriz de asociación es consultar un valor único que el shell devuelve del elemento más específico de la matriz que tiene la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="8e583-135">The most common use of an association array is to query for a single value that the Shell returns from the most specific element in the array that has the requested information.</span></span> <span data-ttu-id="8e583-136">En el ejemplo de código siguiente se muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="8e583-136">The following code example shows how to do that.</span></span>


```
IQueryAssociations *pqa;

// pShellItem is assumed to be an existing IShellItem object.
hr = pShellItem->BindToHandler(NULL, BHID_AssociationArray, IID_PPV_ARGS(&pqa));
if (SUCCEEDED(hr))
{
    wchar_t szValue[256];
    DWORD cbValue = sizeof(szValue);      // Count of bytes in the array

    hr = pqa->GetData(0, ASSOCDATA_VALUE, L"InfoTip", szValue, &cbValue);
    if (SUCCEEDED(hr))
    {
        // The "InfoTip" value is used to compute the infotip string from
        // properties of an item.
    }
    pqa->Release();
}
```



<span data-ttu-id="8e583-137">Las siguientes API se pueden usar para consultar una matriz de asociación o para construir un objeto de [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) de matriz de asociación que se pueda consultar:</span><span class="sxs-lookup"><span data-stu-id="8e583-137">The following APIs can be used to query an association array or to construct an association array [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) object that can be queried:</span></span>

-   <span data-ttu-id="8e583-138">[**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (anterior a Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="8e583-138">[**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (prior to Windows Vista)</span></span>
-   [<span data-ttu-id="8e583-139">**AssocCreateForClasses**</span><span class="sxs-lookup"><span data-stu-id="8e583-139">**AssocCreateForClasses**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses)
-   [<span data-ttu-id="8e583-140">**AssocQueryString**</span><span class="sxs-lookup"><span data-stu-id="8e583-140">**AssocQueryString**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)

## <a name="working-with-association-arrays-for-a-particular-shell-data-source"></a><span data-ttu-id="8e583-141">Trabajar con matrices de Asociación para un origen de datos de Shell determinado</span><span class="sxs-lookup"><span data-stu-id="8e583-141">Working with Association Arrays for a Particular Shell Data Source</span></span>

<span data-ttu-id="8e583-142">Cada origen de datos de Shell define la matriz de asociaciones para sus elementos.</span><span class="sxs-lookup"><span data-stu-id="8e583-142">Each Shell data source defines the association array for its items.</span></span> <span data-ttu-id="8e583-143">La definición de una matriz de asociación suele ser una función del tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="8e583-143">Defining an association array is usually a function of the type of item.</span></span> <span data-ttu-id="8e583-144">Los implementadores de orígenes de datos de Shell deben definir y documentar las matrices de Asociación para permitir que las aplicaciones amplíen el comportamiento de esos tipos, como para registrar verbos u otra información.</span><span class="sxs-lookup"><span data-stu-id="8e583-144">Shell data source implementers should define and document the association arrays to enable applications to extend the behavior of those types, such as for registering verbs or other information.</span></span> <span data-ttu-id="8e583-145">Las aplicaciones pueden extender el comportamiento de los elementos basándose en la adición de datos a las subclaves de la matriz de asociación, como agregar verbos para los elementos.</span><span class="sxs-lookup"><span data-stu-id="8e583-145">Applications can extend the behavior of items based on adding data to the association array subkeys, such as adding verbs for items.</span></span>

<span data-ttu-id="8e583-146">El origen de datos del sistema de archivos crea una matriz de asociaciones para los archivos basados en las siguientes subclaves del registro y ProgID especiales:</span><span class="sxs-lookup"><span data-stu-id="8e583-146">The file system data source builds an association array for files based on the following registry subkeys and special ProgIDs:</span></span>

-   <span data-ttu-id="8e583-147">Si el archivo tiene un ProgID registrado, se utilizará el ProgID **\_ \_ raíz de las clases HKEY** \\  .</span><span class="sxs-lookup"><span data-stu-id="8e583-147">If the file has a registered ProgID, **HKEY\_CLASSES\_ROOT**\\*ProgID* is used.</span></span> <span data-ttu-id="8e583-148">En caso contrario, se usa **HKEY \_ classes \_ root** \\ **Unknown** .</span><span class="sxs-lookup"><span data-stu-id="8e583-148">Otherwise **HKEY\_CLASSES\_ROOT**\\**Unknown** is used.</span></span>
-   <span data-ttu-id="8e583-149">La extensión de nombre de archivo se registra en **HKEY \_ classes \_ root** \\ **SystemFileAssociations** \\ *. fileExtension* subclave.</span><span class="sxs-lookup"><span data-stu-id="8e583-149">The file name extension is registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ *.fileExtension* subkey.</span></span>
-   <span data-ttu-id="8e583-150">En la tabla siguiente se muestran los ProgID especiales.</span><span class="sxs-lookup"><span data-stu-id="8e583-150">Special ProgIDs are shown in the following table.</span></span> 

    | <span data-ttu-id="8e583-151">ProgID especial</span><span class="sxs-lookup"><span data-stu-id="8e583-151">Special progID</span></span>                                    | <span data-ttu-id="8e583-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e583-152">Description</span></span>                   |
    |---------------------------------------------------|-------------------------------|
    | <span data-ttu-id="8e583-153">**HKEY \_ \_raíz de clases** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="8e583-153">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>                   | <span data-ttu-id="8e583-154">Todos los archivos (no carpetas)</span><span class="sxs-lookup"><span data-stu-id="8e583-154">All files (non-folders)</span></span>       |
    | <span data-ttu-id="8e583-155">_ *HKEY \_ classes \_ root **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="8e583-155">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span> | <span data-ttu-id="8e583-156">Archivos y carpetas del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="8e583-156">Files and file system folders</span></span> |
    | <span data-ttu-id="8e583-157">**HKEY \_ Directorio \_ raíz de clases** \\ </span><span class="sxs-lookup"><span data-stu-id="8e583-157">**HKEY\_CLASSES\_ROOT**\\**Directory**</span></span>            | <span data-ttu-id="8e583-158">Carpetas del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="8e583-158">File system folders</span></span>           |
    | <span data-ttu-id="8e583-159">**HKEY \_ Carpeta \_ raíz de clases** \\ </span><span class="sxs-lookup"><span data-stu-id="8e583-159">**HKEY\_CLASSES\_ROOT**\\**Folder**</span></span>               | <span data-ttu-id="8e583-160">Contenedores de Shell</span><span class="sxs-lookup"><span data-stu-id="8e583-160">Shell containers</span></span>              |

    

     

### <a name="shell-data-source-association-arrays"></a><span data-ttu-id="8e583-161">Matrices de Asociación de orígenes de datos de Shell</span><span class="sxs-lookup"><span data-stu-id="8e583-161">Shell Data Source Association Arrays</span></span>

<span data-ttu-id="8e583-162">La lista siguiente representa algunas de las matrices de asociación del almacén de datos de Shell que se pueden usar para los propósitos descritos en este tema:</span><span class="sxs-lookup"><span data-stu-id="8e583-162">The following list represents some of the Shell data store association arrays that can be used for the purposes described in this topic:</span></span>

-   <span data-ttu-id="8e583-163">**HKEY \_ \_raíz de clases** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="8e583-163">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>
-   <span data-ttu-id="8e583-164">_ *HKEY \_ classes \_ root **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="8e583-164">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span>
-   <span data-ttu-id="8e583-165">**HKEY \_Kind.Doc\_ raíz de clases** \\ **ument**</span><span class="sxs-lookup"><span data-stu-id="8e583-165">**HKEY\_CLASSES\_ROOT**\\**Kind.Document**</span></span>
-   <span data-ttu-id="8e583-166">**HKEY \_ Resultados \_ raíz de clases** \\ </span><span class="sxs-lookup"><span data-stu-id="8e583-166">**HKEY\_CLASSES\_ROOT**\\**Results**</span></span>
-   <span data-ttu-id="8e583-167">**HKEY \_ Clases \_ raíz** \\ **SystemFileAssociations** \\ **. docx**</span><span class="sxs-lookup"><span data-stu-id="8e583-167">**HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ **.docx**</span></span>
-   <span data-ttu-id="8e583-168">**HKEY \_ Clases \_ raíz** \\ **Word.Document. 12**</span><span class="sxs-lookup"><span data-stu-id="8e583-168">**HKEY\_CLASSES\_ROOT**\\**Word.Document.12**</span></span>

<span data-ttu-id="8e583-169">Las matrices de Asociación de orígenes de datos de Shell que se pueden usar para DBFolder (un almacén de datos de Shell que representa los elementos de los resultados de la búsqueda y las vistas basadas en consultas) son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="8e583-169">Shell data source association arrays that can be used for DBFolder (a Shell data store that represents items in search results and query-based views) are as follows:</span></span>

-   <span data-ttu-id="8e583-170">Unidades</span><span class="sxs-lookup"><span data-stu-id="8e583-170">Drives</span></span>
-   <span data-ttu-id="8e583-171">Red</span><span class="sxs-lookup"><span data-stu-id="8e583-171">Network</span></span>
-   <span data-ttu-id="8e583-172">RegItems</span><span class="sxs-lookup"><span data-stu-id="8e583-172">RegItems</span></span>
-   <span data-ttu-id="8e583-173">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="8e583-173">Examples:</span></span>
    -   <span data-ttu-id="8e583-174">ContentView</span><span class="sxs-lookup"><span data-stu-id="8e583-174">ContentView</span></span>
    -   <span data-ttu-id="8e583-175">Verbos</span><span class="sxs-lookup"><span data-stu-id="8e583-175">Verbs</span></span>

<span data-ttu-id="8e583-176">Otras matrices de asociaciones comunes incluyen carpetas e impresoras.</span><span class="sxs-lookup"><span data-stu-id="8e583-176">Other common association arrays include Folder and Printers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e583-177">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8e583-177">Additional Resources</span></span>

-   <span data-ttu-id="8e583-178">Para crear un almacén de datos de Shell, vea [implementar las interfaces de objeto de carpeta básicas](nse-implement.md).</span><span class="sxs-lookup"><span data-stu-id="8e583-178">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e583-179">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8e583-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e583-180">Registro de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8e583-180">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="8e583-181">Tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="8e583-181">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="8e583-182">Cómo funcionan las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="8e583-182">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="8e583-183">Vista de contenido por tipo de archivo o tipo</span><span class="sxs-lookup"><span data-stu-id="8e583-183">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="8e583-184">Comprobador de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="8e583-184">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="8e583-185">Controladores de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="8e583-185">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="8e583-186">Identificadores de programación</span><span class="sxs-lookup"><span data-stu-id="8e583-186">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="8e583-187">Tipos percibidos</span><span class="sxs-lookup"><span data-stu-id="8e583-187">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> </dl>

 

 
