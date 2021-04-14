---
description: En este tema se describe qué son las bibliotecas y cómo pueden beneficiar a los usuarios y desarrolladores.
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: Acerca de las bibliotecas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e577e7b5df0a1e072a07a096434af84ff8e2c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564870"
---
# <a name="about-libraries"></a><span data-ttu-id="6129f-103">Acerca de las bibliotecas</span><span class="sxs-lookup"><span data-stu-id="6129f-103">About Libraries</span></span>

<span data-ttu-id="6129f-104">En este tema se describe qué son las bibliotecas y cómo pueden beneficiar a los usuarios y desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="6129f-104">This topic describes what libraries are and how they can benefit users and developers.</span></span>

<span data-ttu-id="6129f-105">Las bibliotecas son colecciones de carpetas definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="6129f-105">Libraries are user-defined collections of folders.</span></span> <span data-ttu-id="6129f-106">Una biblioteca realiza un seguimiento de la ubicación física de almacenamiento de cada carpeta, lo que libera al usuario y al software de esa tarea.</span><span class="sxs-lookup"><span data-stu-id="6129f-106">A library keeps track of each folder's physical storage location, which relieves the user and the software of that task.</span></span> <span data-ttu-id="6129f-107">Los usuarios pueden agrupar las carpetas relacionadas en una biblioteca aunque dichas carpetas estén almacenadas en diferentes unidades de disco duro o en equipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="6129f-107">Users can group related folders together in a library even if those folders are stored on different hard drives or different computers.</span></span>

<span data-ttu-id="6129f-108">En una biblioteca, las carpetas y los archivos aparecen al usuario como una sola colección y, mediante la API de la biblioteca de Shell, el contenido de la biblioteca también puede aparecer en una única ubicación para un programa.</span><span class="sxs-lookup"><span data-stu-id="6129f-108">In a library, the folders and files appear to the user as a single collection and, using the Shell Library API, the library's contents can also appear to be in a single location to a program.</span></span>

<span data-ttu-id="6129f-109">En una biblioteca, el contenido, como documentos, fotos, vídeos o música de un usuario, se puede ordenar y mostrar como el usuario desea y no simplemente como requiere el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="6129f-109">In a library, the contents, such as a user's documents, photos, videos, or music, can be sorted and displayed as the user wants and not simply as how the file system requires.</span></span> <span data-ttu-id="6129f-110">Por ejemplo, los usuarios pueden organizar el contenido de una biblioteca mediante las propiedades de los elementos de la biblioteca para que los elementos relacionados se ordenen juntos incluso si se almacenan en carpetas diferentes.</span><span class="sxs-lookup"><span data-stu-id="6129f-110">For example, users can organize the contents of a library using the properties of the items in the library so that related items will sort together even if they are stored in different folders.</span></span>

![captura de pantalla de la interfaz de usuario de bibliotecas](images/libraries-whatare.png)

<span data-ttu-id="6129f-112">En este tema:</span><span class="sxs-lookup"><span data-stu-id="6129f-112">In this topic:</span></span>

-   [<span data-ttu-id="6129f-113">Ventajas de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="6129f-113">Library Benefits</span></span>](#library-benefits)
    -   [<span data-ttu-id="6129f-114">Ventajas del usuario</span><span class="sxs-lookup"><span data-stu-id="6129f-114">User Benefits</span></span>](#user-benefits)
    -   [<span data-ttu-id="6129f-115">Ventajas para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="6129f-115">Developer Benefits</span></span>](#developer-benefits)
-   [<span data-ttu-id="6129f-116">Administrar carpetas en bibliotecas</span><span class="sxs-lookup"><span data-stu-id="6129f-116">Managing Folders in Libraries</span></span>](#managing-folders-in-libraries)
-   [<span data-ttu-id="6129f-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6129f-117">Related topics</span></span>](#related-topics)

## <a name="library-benefits"></a><span data-ttu-id="6129f-118">Ventajas de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="6129f-118">Library Benefits</span></span>

<span data-ttu-id="6129f-119">En esta sección se describen algunas de las ventajas de las bibliotecas desde la perspectiva del usuario final y la perspectiva del desarrollador del programa.</span><span class="sxs-lookup"><span data-stu-id="6129f-119">This section describes some of the benefits of libraries from the end-user's perspective and the program developer's perspective.</span></span>

### <a name="user-benefits"></a><span data-ttu-id="6129f-120">Ventajas del usuario</span><span class="sxs-lookup"><span data-stu-id="6129f-120">User Benefits</span></span>

<span data-ttu-id="6129f-121">La incorporación de compatibilidad con la biblioteca al programa proporciona las siguientes ventajas al usuario:</span><span class="sxs-lookup"><span data-stu-id="6129f-121">Adding library support to your program provides the following benefits to the user:</span></span>

-   <span data-ttu-id="6129f-122">**Las bibliotecas proporcionan una interfaz de usuario coherente en Windows 7**</span><span class="sxs-lookup"><span data-stu-id="6129f-122">**Libraries provide a consistent user interface in Windows 7**</span></span>

    <span data-ttu-id="6129f-123">Los cuadros de diálogo de archivos comunes admiten bibliotecas y proporcionan la misma experiencia de usuario que el explorador de Windows en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6129f-123">The common file dialog boxes support libraries and provide the same user experience as the Windows Explorer in Windows 7.</span></span> <span data-ttu-id="6129f-124">Las bibliotecas auxiliares del programa le ayudarán a proporcionar una interacción más fluida para el usuario al usar el programa en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6129f-124">Supporting libraries in your program will help provide a more seamless interaction for the user when using your program in Windows 7.</span></span>

-   <span data-ttu-id="6129f-125">**Los usuarios deciden dónde almacenar el contenido**</span><span class="sxs-lookup"><span data-stu-id="6129f-125">**Users decide where to store content**</span></span>

    <span data-ttu-id="6129f-126">Las bibliotecas permiten a los usuarios controlar dónde se almacena su contenido.</span><span class="sxs-lookup"><span data-stu-id="6129f-126">Libraries make it possible for users to control where their content is stored.</span></span> <span data-ttu-id="6129f-127">Al mismo tiempo, las bibliotecas proporcionan valores predeterminados razonables para los usuarios que no desean administrar dicho nivel de detalle en su equipo.</span><span class="sxs-lookup"><span data-stu-id="6129f-127">At the same time, libraries provide reasonable defaults for users who do not want to manage that level of detail in their computer.</span></span> <span data-ttu-id="6129f-128">Los usuarios deciden cuántos, o cuántos controlan, desean ejercitar dónde y cómo se almacena su contenido y la biblioteca funciona bien en cualquier caso.</span><span class="sxs-lookup"><span data-stu-id="6129f-128">Users decide how much, or how little, control they want to exercise over where and how their content is stored and the library works fine either way.</span></span>

### <a name="developer-benefits"></a><span data-ttu-id="6129f-129">Ventajas para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="6129f-129">Developer Benefits</span></span>

<span data-ttu-id="6129f-130">Puede usar las bibliotecas de su programa para proporcionar una interfaz de usuario más flexible y cómoda sin tener que agregar una gran cantidad de código de programa complejo.</span><span class="sxs-lookup"><span data-stu-id="6129f-130">You can use libraries in your program to provide a more flexible and convenient user interface without having to add a lot of complex program code.</span></span> <span data-ttu-id="6129f-131">Estas son algunas de las ventajas de agregar compatibilidad de biblioteca:</span><span class="sxs-lookup"><span data-stu-id="6129f-131">Some of the advantages of adding library support include:</span></span>

-   <span data-ttu-id="6129f-132">**Bibliotecas compatibles con el acceso a la biblioteca y al sistema de archivos**</span><span class="sxs-lookup"><span data-stu-id="6129f-132">**Libraries support library and file-system access**</span></span>

    <span data-ttu-id="6129f-133">Con la [**API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)de la biblioteca de Shell, los programas pueden proporcionar compatibilidad de biblioteca al usuario a la vez que se reduce la complejidad del código de administración de archivos y carpetas.</span><span class="sxs-lookup"><span data-stu-id="6129f-133">Using the [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary), programs can provide library support for the user while reducing the complexity of their file and folder management code.</span></span> <span data-ttu-id="6129f-134">Si el programa ya usa la API del sistema de archivos, puede conservar todo el código existente que desee y, aun así, proporcionar al usuario la información necesaria para la biblioteca obteniendo la información necesaria del sistema de archivos de la API de la **biblioteca de Shell**.</span><span class="sxs-lookup"><span data-stu-id="6129f-134">If your program already uses the file-system API, you can preserve as much of that existing code as you want and still provide library support to the user by getting the necessary file-system information from the **Shell Library API**.</span></span>

-   <span data-ttu-id="6129f-135">**Notificación de cambio más sencilla**</span><span class="sxs-lookup"><span data-stu-id="6129f-135">**Simpler change notification**</span></span>

    <span data-ttu-id="6129f-136">Tanto el sistema de archivos como la API de Shell pueden notificar al programa cuando cambia el contenido de una carpeta o biblioteca supervisada.</span><span class="sxs-lookup"><span data-stu-id="6129f-136">Both the file-system and the Shell API can notify your program when the contents of a monitored folder or library change.</span></span> <span data-ttu-id="6129f-137">Sin embargo, mediante la API de Shell, puede supervisar todas las carpetas de la biblioteca con una sola notificación, aunque la carpeta de la biblioteca se puede almacenar en unidades diferentes o incluso en equipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="6129f-137">Using the Shell API, however, you can monitor all the folders in the library with a single notification, even though the folder in the library may be stored on different drives or even different computers.</span></span>

-   <span data-ttu-id="6129f-138">**Las bibliotecas usan propiedades de archivo**</span><span class="sxs-lookup"><span data-stu-id="6129f-138">**Libraries use file properties**</span></span>

    <span data-ttu-id="6129f-139">Los programas pueden usar las propiedades de archivo para controlar qué archivos se muestran durante las operaciones de apertura y guardado que usan los cuadros de diálogo de archivos comunes.</span><span class="sxs-lookup"><span data-stu-id="6129f-139">Programs can use the file properties to control which files are displayed during open and save operations that use the common file dialog boxes.</span></span> <span data-ttu-id="6129f-140">Los programas también pueden tener acceso a las propiedades de archivo mediante el uso de las interfaces [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="6129f-140">Programs can also have access to file properties by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces.</span></span> <span data-ttu-id="6129f-141">Los cuadros de diálogo de archivos comunes también se pueden configurar para permitir a los usuarios actualizar las propiedades que están asociadas con su contenido.</span><span class="sxs-lookup"><span data-stu-id="6129f-141">The common file dialog boxes can also be configured allow users to update the properties that are associated with their content.</span></span>

-   <span data-ttu-id="6129f-142">**Los programas pueden crear bibliotecas dedicadas**</span><span class="sxs-lookup"><span data-stu-id="6129f-142">**Programs can create dedicated libraries**</span></span>

    <span data-ttu-id="6129f-143">Se puede crear una nueva biblioteca cuando las bibliotecas de usuario existentes no satisfacen las necesidades del programa, por ejemplo, si un programa crea un nuevo tipo de contenido de usuario.</span><span class="sxs-lookup"><span data-stu-id="6129f-143">A new library can be created when an existing user libraries does not meet the program's needs—for example, if a program creates a new type of user content.</span></span> <span data-ttu-id="6129f-144">La nueva biblioteca se puede configurar con un icono único que representa su contenido y facilita la identificación de la biblioteca en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="6129f-144">The new library can be configured with a unique icon that represents their content and makes the library easy to identify in the Windows Explorer.</span></span>

## <a name="managing-folders-in-libraries"></a><span data-ttu-id="6129f-145">Administrar carpetas en bibliotecas</span><span class="sxs-lookup"><span data-stu-id="6129f-145">Managing Folders in Libraries</span></span>

<span data-ttu-id="6129f-146">Los usuarios pueden organizar sus bibliotecas agregando, moviendo o quitando carpetas en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6129f-146">Users can organize their libraries by adding, moving, or removing folders in the library.</span></span> <span data-ttu-id="6129f-147">Sin embargo, no todas las carpetas admiten todas las funciones que puede proporcionar una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6129f-147">Not all folders, however, support all the functionality that a library can provide.</span></span> <span data-ttu-id="6129f-148">Muchas características de la biblioteca requieren un acceso rápido a las distintas propiedades de la carpeta y su contenido que solo están disponibles a través de Windows Search.</span><span class="sxs-lookup"><span data-stu-id="6129f-148">Many library features require quick access to the different properties of the folder and its contents that are only available through Windows Search.</span></span> <span data-ttu-id="6129f-149">Para proporcionar toda la funcionalidad de la biblioteca, la búsqueda de Windows debe ser capaz de indexar una carpeta.</span><span class="sxs-lookup"><span data-stu-id="6129f-149">To provide full library functionality, a folder must be able to be indexed by Windows Search.</span></span>

<span data-ttu-id="6129f-150">Una biblioteca no permite a un usuario agregar carpetas que no proporcionan funcionalidad completa de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6129f-150">A library does not allow a user to add folders that do not provide full library functionality.</span></span> <span data-ttu-id="6129f-151">Sin embargo, la API de la [**biblioteca de Shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) puede agregar estas carpetas.</span><span class="sxs-lookup"><span data-stu-id="6129f-151">The [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) can, however, add such folders.</span></span> <span data-ttu-id="6129f-152">Si una biblioteca contiene una carpeta que no admite la funcionalidad de biblioteca completa, la biblioteca funcionará en modo seguro y proporcionará una funcionalidad limitada.</span><span class="sxs-lookup"><span data-stu-id="6129f-152">If a library contains a folder that does not support full library functionality, the library will operate in a safe mode and provide a limited functionality.</span></span> <span data-ttu-id="6129f-153">En la tabla siguiente se describen las carpetas que admiten la funcionalidad de la biblioteca completa y las que no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="6129f-153">The following table describes the folders that support full library functionality and those that do not.</span></span>



| <span data-ttu-id="6129f-154">Tipos de carpeta que admiten la funcionalidad de biblioteca completa</span><span class="sxs-lookup"><span data-stu-id="6129f-154">Folder types that support full library functionality</span></span>                                                               | <span data-ttu-id="6129f-155">Tipos de carpeta que no admiten la funcionalidad de biblioteca completa</span><span class="sxs-lookup"><span data-stu-id="6129f-155">Folder types that do not support full library functionality</span></span>                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6129f-156">Discos duros NTFS y FAT32 fijos y externos.</span><span class="sxs-lookup"><span data-stu-id="6129f-156">Fixed and external NTFS and FAT32 hard drives.</span></span>                                                                     | <span data-ttu-id="6129f-157">Unidades extraíbles, como unidades flash USB o tarjetas de memoria Secure Digital (SD).</span><span class="sxs-lookup"><span data-stu-id="6129f-157">Removable drives such as USB flash drives or Secure Digital (SD) memory cards.</span></span>               |
| <span data-ttu-id="6129f-158">Recursos compartidos de archivos que se indexan mediante Windows Search, como servidores departamentales, Windows 7 o equipos domésticos de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6129f-158">File shares that are indexed by Windows Search such as departmental servers, Windows 7, or Windows Vista home PCs.</span></span> | <span data-ttu-id="6129f-159">Medios extraíbles, como CD-ROM o DVD.</span><span class="sxs-lookup"><span data-stu-id="6129f-159">Removable media such as CD-ROM or DVD media.</span></span>                                                 |
| <span data-ttu-id="6129f-160">Recursos compartidos de archivos que están disponibles sin conexión, como una carpeta redirigida **Mis documentos** o una memoria caché de Client-Side.</span><span class="sxs-lookup"><span data-stu-id="6129f-160">File shares that are available offline such as a redirected **My Documents** folder or a Client-Side Cache.</span></span>        | <span data-ttu-id="6129f-161">Recursos compartidos de red que no están disponibles sin conexión ni indexados de forma remota, como las unidades NAS.</span><span class="sxs-lookup"><span data-stu-id="6129f-161">Network shares that are neither available offline nor remotely indexed such as NAS drives.</span></span>   |
|                                                                                                                    | <span data-ttu-id="6129f-162">Otros orígenes de datos, como Microsoft SharePoint, Microsoft Exchange y Microsoft OneDrive.</span><span class="sxs-lookup"><span data-stu-id="6129f-162">Other data sources such as Microsoft SharePoint, Microsoft Exchange, and Microsoft OneDrive.</span></span> |



 

<span data-ttu-id="6129f-163">En la imagen siguiente se muestra la presentación limitada del contenido de la biblioteca en modo seguro.</span><span class="sxs-lookup"><span data-stu-id="6129f-163">The following image shows the limited display of library contents while in safe mode.</span></span>

![abrir el cuadro de diálogo cuando las bibliotecas están en modo seguro](images/libraries-supportedfolders.png)

## <a name="related-topics"></a><span data-ttu-id="6129f-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6129f-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6129f-166">Acerca de las bibliotecas</span><span class="sxs-lookup"><span data-stu-id="6129f-166">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="6129f-167">**IShellLibrary**</span><span class="sxs-lookup"><span data-stu-id="6129f-167">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="6129f-168">Vínculos de Shell</span><span class="sxs-lookup"><span data-stu-id="6129f-168">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="6129f-169">Carpetas conocidas</span><span class="sxs-lookup"><span data-stu-id="6129f-169">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="6129f-170">Esquema de descripción de biblioteca</span><span class="sxs-lookup"><span data-stu-id="6129f-170">Library Description Schema</span></span>](library-schema-entry.md)
</dt> </dl>

 

 
