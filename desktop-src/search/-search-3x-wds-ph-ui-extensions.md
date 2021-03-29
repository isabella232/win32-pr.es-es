---
description: Para asegurarse de que los datos se indizan y presentan correctamente al usuario durante las búsquedas, debe implementar los almacenes de datos de Shell (también conocidos como extensiones de espacio de nombres de Shell) y los controladores de tipo de archivo (también conocidos como extensiones de Shell, controladores de extensión o controladores de extensión de Shell).
ms.assetid: 38cebb3c-51bf-439c-8d4e-445344f6cb66
title: Agregar iconos, vistas previas y menús contextuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501006227f6192b7d81a2a88ba915c368a9cc398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540734"
---
# <a name="adding-icons-previews-and-shortcut-menus"></a><span data-ttu-id="74b90-103">Agregar iconos, vistas previas y menús contextuales</span><span class="sxs-lookup"><span data-stu-id="74b90-103">Adding Icons, Previews and Shortcut Menus</span></span>

<span data-ttu-id="74b90-104">Para asegurarse de que los datos se indizan y presentan correctamente al usuario durante las búsquedas, debe implementar los almacenes de datos de Shell (también conocidos como [extensiones de espacio de nombres de Shell](../shell/nse-works.md)) y los controladores de tipo de archivo (también conocidos como extensiones de Shell, controladores de [extensión](../shell/handlers.md)o controladores de extensión de Shell).</span><span class="sxs-lookup"><span data-stu-id="74b90-104">To ensure that your data is indexed and presented correctly to the user during searches, you need to implement Shell data stores (also known as [Shell Namespace Extensions](../shell/nse-works.md)), and file type handlers (also known as Shell extensions, [extension handlers](../shell/handlers.md), or Shell extension handlers).</span></span>

<span data-ttu-id="74b90-105">En este tema se describen las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="74b90-105">This topic describes the following interfaces:</span></span>

-   [<span data-ttu-id="74b90-106">Implementar controladores de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="74b90-106">Implementing File Type Handlers</span></span>](#implementing-file-type-handlers)
    -   [<span data-ttu-id="74b90-107">IPersist</span><span class="sxs-lookup"><span data-stu-id="74b90-107">IPersist</span></span>](#ipersist)
    -   [<span data-ttu-id="74b90-108">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="74b90-108">IPersistFolder</span></span>](#ipersistfolder)
    -   [<span data-ttu-id="74b90-109">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="74b90-109">IShellFolder</span></span>](#ishellfolder)
    -   [<span data-ttu-id="74b90-110">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="74b90-110">IContextMenu</span></span>](#icontextmenu)
    -   [<span data-ttu-id="74b90-111">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="74b90-111">IExtractIcon</span></span>](#iextracticon)
    -   [<span data-ttu-id="74b90-112">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="74b90-112">IPreviewHandler</span></span>](#ipreviewhandler)
-   [<span data-ttu-id="74b90-113">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="74b90-113">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="74b90-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74b90-114">Related topics</span></span>](#related-topics)

## <a name="implementing-file-type-handlers"></a><span data-ttu-id="74b90-115">Implementar controladores de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="74b90-115">Implementing File Type Handlers</span></span>

<span data-ttu-id="74b90-116">Estas extensiones de shell o controladores de tipo de archivo proporcionan a los usuarios las siguientes experiencias de Shell:</span><span class="sxs-lookup"><span data-stu-id="74b90-116">These Shell extensions or file type handlers provide your users with the following Shell experiences:</span></span>

-   <span data-ttu-id="74b90-117">La vista de resultados muestra un icono específico para el tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="74b90-117">The results view displays a specific icon for your item type.</span></span>
-   <span data-ttu-id="74b90-118">La vista de resultados muestra una vista previa del elemento cuando el usuario selecciona el elemento.</span><span class="sxs-lookup"><span data-stu-id="74b90-118">The results view displays a preview of the item when the user selects the item.</span></span>
-   <span data-ttu-id="74b90-119">Los usuarios pueden hacer doble clic en los elementos para iniciar eventos, como abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="74b90-119">Users can double-click items to initiate events such as opening the file.</span></span>
-   <span data-ttu-id="74b90-120">Los usuarios pueden hacer clic con el botón secundario en los elementos para tener acceso a un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="74b90-120">Users can right-click items to access a shortcut (context) menu.</span></span>
-   <span data-ttu-id="74b90-121">Los usuarios pueden arrastrar y colocar elementos.</span><span class="sxs-lookup"><span data-stu-id="74b90-121">Users can drag-and-drop items.</span></span>

<span data-ttu-id="74b90-122">Al igual que todos los objetos del modelo de objetos componentes (COM), los controladores de tipo de archivo deben implementar una interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) y un generador de clases.</span><span class="sxs-lookup"><span data-stu-id="74b90-122">Like all Component Object Model (COM) objects, file type handlers must implement an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface and a class factory.</span></span>

<span data-ttu-id="74b90-123">En Windows XP o versiones anteriores, los controladores también deben implementar:</span><span class="sxs-lookup"><span data-stu-id="74b90-123">In Windows XP or earlier, handlers should also implement:</span></span>

-   <span data-ttu-id="74b90-124">Una [interfaz IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)</span><span class="sxs-lookup"><span data-stu-id="74b90-124">Either [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile)</span></span>
-   <span data-ttu-id="74b90-125">O [IShellExtInit (interfaz](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) )</span><span class="sxs-lookup"><span data-stu-id="74b90-125">Or [IShellExtInit Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)</span></span>

<span data-ttu-id="74b90-126">En Windows Vista, la interfaz [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) y la [interfaz IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) se reemplazaron por las tres interfaces siguientes para que Shell inicialice el controlador:</span><span class="sxs-lookup"><span data-stu-id="74b90-126">In Windows Vista, [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [IShellExtInit Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) were replaced by the following three interfaces for Shell to initialize the handler:</span></span>

-   [<span data-ttu-id="74b90-127">Interfaz IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="74b90-127">IInitializeWithStream Interface</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="74b90-128">Interfaz IInitializeWithItem</span><span class="sxs-lookup"><span data-stu-id="74b90-128">IInitializeWithItem Interface</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [<span data-ttu-id="74b90-129">Interfaz IInitializeWithFile</span><span class="sxs-lookup"><span data-stu-id="74b90-129">IInitializeWithFile Interface</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)

<span data-ttu-id="74b90-130">Para proporcionar una experiencia de usuario razonable, debe proporcionar un almacén de datos de Shell con el controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="74b90-130">To provide a reasonable user experience you must provide a Shell data store with your protocol handler.</span></span> <span data-ttu-id="74b90-131">A continuación, ese almacén de datos sirve como "fábrica" para los controladores de iconos, los controladores de menús contextuales, los controladores de vista previa, etc.</span><span class="sxs-lookup"><span data-stu-id="74b90-131">That data store then serves as the "factory" for icon handlers, shortcut menu handlers, preview handlers, and so forth.</span></span> <span data-ttu-id="74b90-132">Las implementaciones mínimas de la interfaz [IPersist](/windows/desktop/api/objidl/nn-objidl-ipersist) y la interfaz [IPersistFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) son necesarias para la [interfaz IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), y se requiere una implementación mínima de la interfaz IShellFolder para [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) y [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).</span><span class="sxs-lookup"><span data-stu-id="74b90-132">Minimal implementations of [IPersist Interface](/windows/desktop/api/objidl/nn-objidl-ipersist) and [IPersistFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) are required by [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), and a minimal implementation of IShellFolder Interface is required for the [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) and [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).</span></span>

> [!Note]  
> <span data-ttu-id="74b90-133">Se debe implementar el mismo identificador de clase (CLSID) para **IPersist**, **IPersistFolder** y **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="74b90-133">The same class identifier (CLSID) should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="74b90-134">Para obtener más información sobre cómo crear un almacén de datos de Shell para admitir un controlador de protocolo, vea [implementar las interfaces de objeto de carpeta básicas](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="74b90-134">For more information about creating a Shell data store to support a protocol handler, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

### <a name="ipersist"></a><span data-ttu-id="74b90-135">IPersist</span><span class="sxs-lookup"><span data-stu-id="74b90-135">IPersist</span></span>

<span data-ttu-id="74b90-136">La interfaz **IPersist** define el único método **GetClassID**, que está diseñado para proporcionar el CLSID de un objeto que se puede almacenar de forma persistente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="74b90-136">The **IPersist** interface defines the single method **GetClassID**, which is designed to supply the CLSID of an object that can be stored persistently in the system.</span></span>



| <span data-ttu-id="74b90-137">Método</span><span class="sxs-lookup"><span data-stu-id="74b90-137">Method</span></span>     | <span data-ttu-id="74b90-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="74b90-138">Description</span></span>                                      |
|------------|--------------------------------------------------|
| <span data-ttu-id="74b90-139">GetClassID</span><span class="sxs-lookup"><span data-stu-id="74b90-139">GetClassID</span></span> | <span data-ttu-id="74b90-140">Devuelve el CLSID del objeto de almacén de datos de Shell.</span><span class="sxs-lookup"><span data-stu-id="74b90-140">Returns the CLSID of the Shell data store object</span></span> |



 

### <a name="ipersistfolder"></a><span data-ttu-id="74b90-141">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="74b90-141">IPersistFolder</span></span>

<span data-ttu-id="74b90-142">La interfaz **IPersistFolder** se usa para inicializar los objetos de la carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="74b90-142">The **IPersistFolder** interface is used to initialize Shell folder objects.</span></span> <span data-ttu-id="74b90-143">La implementación de esta interfaz, que se deriva de **IPersist**, es cómo se indica a la carpeta dónde se encuentra en el espacio de nombres del shell.</span><span class="sxs-lookup"><span data-stu-id="74b90-143">Implementation of this interface, which is derived from **IPersist**, is how the folder is told where it is in the Shell namespace.</span></span> <span data-ttu-id="74b90-144">No utilice esta interfaz directamente.</span><span class="sxs-lookup"><span data-stu-id="74b90-144">You do not use this interface directly.</span></span> <span data-ttu-id="74b90-145">Lo usa la implementación del sistema de archivos del [método IShellFolder:: BindToObject](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) cuando Inicializa un objeto de carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="74b90-145">It is used by the file system implementation of [IShellFolder::BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) when it initializes a Shell folder object.</span></span>



| <span data-ttu-id="74b90-146">Método</span><span class="sxs-lookup"><span data-stu-id="74b90-146">Method</span></span>     | <span data-ttu-id="74b90-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="74b90-147">Description</span></span>                                                                                            |
|------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74b90-148">Inicialización</span><span class="sxs-lookup"><span data-stu-id="74b90-148">Initialize</span></span> | <span data-ttu-id="74b90-149">Indica a un objeto de carpeta de Shell que se inicialice a sí mismo basándose en la información que se pasa y devuelve S \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="74b90-149">Instructs a Shell folder object to initialize itself based on the information passed and returns S\_OK</span></span> |



 

### <a name="ishellfolder"></a><span data-ttu-id="74b90-150">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="74b90-150">IShellFolder</span></span>

<span data-ttu-id="74b90-151">La interfaz de la [interfaz IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) se usa para administrar carpetas y se requiere una implementación parcial para que el icono y las interfaces de contexto implementadas para un controlador de protocolo se comporten correctamente en la interfaz de usuario de los resultados de Windows Search.</span><span class="sxs-lookup"><span data-stu-id="74b90-151">The [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is used to manage folders, and a partial implementation is required so that the icon and context interfaces implemented for a protocol handler will behave correctly in the Windows Search results user interface.</span></span> <span data-ttu-id="74b90-152">La mayor parte de la funcionalidad requerida se expone a través del método **GetUIObjectOf** .</span><span class="sxs-lookup"><span data-stu-id="74b90-152">Most of the functionality required is exposed through the **GetUIObjectOf** method.</span></span> <span data-ttu-id="74b90-153">Este método permite que un complemento consulte las interfaces **IExtractIcon** y **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="74b90-153">This method enables an add-in to query for the **IExtractIcon** and **IContextMenu** interfaces.</span></span>

<span data-ttu-id="74b90-154">La interfaz de la [interfaz IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) utiliza PIDL en lugar de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="74b90-154">The [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface uses PIDLs instead of URLs.</span></span> <span data-ttu-id="74b90-155">A diferencia de los requisitos de un almacén de datos de Shell completo, los complementos pueden usar una estructura IDL simple que solo contiene la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="74b90-155">In contrast to the requirements of a complete Shell data store, add-ins can use a simple IDL structure that contains only the URL.</span></span>

<span data-ttu-id="74b90-156">Se deben implementar los siguientes métodos de la [interfaz IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .</span><span class="sxs-lookup"><span data-stu-id="74b90-156">The following methods of [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) must be implemented.</span></span> <span data-ttu-id="74b90-157">Cinco de estos métodos requieren una implementación mínima.</span><span class="sxs-lookup"><span data-stu-id="74b90-157">Five of these methods require minimal implementation.</span></span>



| <span data-ttu-id="74b90-158">Método</span><span class="sxs-lookup"><span data-stu-id="74b90-158">Method</span></span>           | <span data-ttu-id="74b90-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="74b90-159">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74b90-160">BindToObject</span><span class="sxs-lookup"><span data-stu-id="74b90-160">BindToObject</span></span>     | <span data-ttu-id="74b90-161">Devuelve E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="74b90-161">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="74b90-162">BindToStorage</span><span class="sxs-lookup"><span data-stu-id="74b90-162">BindToStorage</span></span>    | <span data-ttu-id="74b90-163">Devuelve E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="74b90-163">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="74b90-164">CreateViewObject</span><span class="sxs-lookup"><span data-stu-id="74b90-164">CreateViewObject</span></span> | <span data-ttu-id="74b90-165">Devuelve E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="74b90-165">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="74b90-166">SetNameOf</span><span class="sxs-lookup"><span data-stu-id="74b90-166">SetNameOf</span></span>        | <span data-ttu-id="74b90-167">Devuelve E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="74b90-167">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="74b90-168">ParseDisplayName</span><span class="sxs-lookup"><span data-stu-id="74b90-168">ParseDisplayName</span></span> | <span data-ttu-id="74b90-169">Convierte una dirección URL en la estructura PIDL</span><span class="sxs-lookup"><span data-stu-id="74b90-169">Converts a URL to the PIDL structure</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="74b90-170">CompareIDs</span><span class="sxs-lookup"><span data-stu-id="74b90-170">CompareIDs</span></span>       | <span data-ttu-id="74b90-171">Compara dos valores de PIDL</span><span class="sxs-lookup"><span data-stu-id="74b90-171">Compares two PIDL values</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="74b90-172">GetDisplayNameOf</span><span class="sxs-lookup"><span data-stu-id="74b90-172">GetDisplayNameOf</span></span> | <span data-ttu-id="74b90-173">Devuelve la dirección URL de un PIDL</span><span class="sxs-lookup"><span data-stu-id="74b90-173">Returns the URL for a PIDL</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="74b90-174">GetUIObjectOf</span><span class="sxs-lookup"><span data-stu-id="74b90-174">GetUIObjectOf</span></span>    | <span data-ttu-id="74b90-175">Este método es similar al [método IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="74b90-175">This method is similar to the [IUnknown::QueryInterface Method](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="74b90-176">Si se solicita un icono, el autor de la llamada solicita el IID \_ IExtractIcon; si se solicita un menú contextual, el autor de la llamada solicita el IID \_ IContextMenu</span><span class="sxs-lookup"><span data-stu-id="74b90-176">If an icon is requested, the caller requests the IID\_IExtractIcon; if a shortcut menu is requested, the caller requests the IID\_IContextMenu</span></span> |



 

<span data-ttu-id="74b90-177">**IShellFolder** no se utiliza para enumerar carpetas.</span><span class="sxs-lookup"><span data-stu-id="74b90-177">**IShellFolder** is not used to enumerate folders.</span></span> <span data-ttu-id="74b90-178">Esto significa que el nombre para mostrar de una carpeta será la dirección URL física.</span><span class="sxs-lookup"><span data-stu-id="74b90-178">This means that the display name of a folder will be the physical URL.</span></span> <span data-ttu-id="74b90-179">Esto puede cambiar en el futuro.</span><span class="sxs-lookup"><span data-stu-id="74b90-179">This may change in the future.</span></span>

### <a name="icontextmenu"></a><span data-ttu-id="74b90-180">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="74b90-180">IContextMenu</span></span>

<span data-ttu-id="74b90-181">Cuando Windows Search muestra los resultados al usuario, puede hacer clic con el botón secundario en un elemento y ver un menú contextual definido por la interfaz **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="74b90-181">When Windows Search displays results to the user, the user can right-click an item and see a shortcut menu defined by your **IContextMenu** interface.</span></span> <span data-ttu-id="74b90-182">Los menús contextuales también se conocen como menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="74b90-182">Shortcut menus are also known as context menus.</span></span>

<span data-ttu-id="74b90-183">La acción predeterminada en el menú contextual es la misma acción que se realiza cuando se hace doble clic en el elemento.</span><span class="sxs-lookup"><span data-stu-id="74b90-183">The default action on the context menu is the same action taken when the item is double-clicked.</span></span> <span data-ttu-id="74b90-184">Sin las interfaces de **IShellFolder** o **IContextMenu** correspondientes para el elemento, el comportamiento predeterminado para un evento de doble clic es pasar la dirección URL como un argumento a la función de [función ShellExecute](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="74b90-184">Without the corresponding **IShellFolder** or **IContextMenu** interfaces for the item, the default behavior for a double-click event is to pass the URL as an argument to the [ShellExecute Function](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function.</span></span>

<span data-ttu-id="74b90-185">Consulte [creación de controladores de menús contextuales](../shell/context-menu-handlers.md) para obtener más información sobre cómo crear controladores de menús contextuales y [ejemplos: extensiones de Shell para controladores de protocolo](-search-3x-wds-ph-ui-samplecode.md) para el código de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="74b90-185">Refer to [Creating Context Menu Handlers](../shell/context-menu-handlers.md) for more information on creating shortcut menu handlers, and [Sample: Shell Extensions for Protocol Handlers](-search-3x-wds-ph-ui-samplecode.md) for sample code.</span></span>

### <a name="iextracticon"></a><span data-ttu-id="74b90-186">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="74b90-186">IExtractIcon</span></span>

<span data-ttu-id="74b90-187">**IExtractIcon** recupera un icono para la interfaz de usuario de búsqueda de Windows basado en la dirección URL en el PIDL proporcionado por el controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="74b90-187">**IExtractIcon** retrieves an icon for the Windows Search user interface based on the URL in the PIDL provided by your protocol handler.</span></span>

<span data-ttu-id="74b90-188">Consulte [crear controladores de iconos](../shell/how-to-create-icon-handlers.md) para obtener más información sobre cómo crear controladores de iconos y [ejemplos: extensiones de Shell para controladores de protocolo](-search-3x-wds-ph-ui-samplecode.md) para el código de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="74b90-188">Refer to [Creating Icon Handlers](../shell/how-to-create-icon-handlers.md) for more information on creating icon handlers and [Sample: Shell Extensions for Protocol Handlers](-search-3x-wds-ph-ui-samplecode.md) for sample code.</span></span>

### <a name="ipreviewhandler"></a><span data-ttu-id="74b90-189">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="74b90-189">IPreviewHandler</span></span>

<span data-ttu-id="74b90-190">[IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) representa una vista previa enriquecida de un elemento seleccionado en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="74b90-190">The [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) renders a rich preview of a selected item in Windows Explorer.</span></span> <span data-ttu-id="74b90-191">Las versiones preliminares están disponibles en Windows Search 4,0 o en Windows Vista con Windows Desktop Search 3. x.</span><span class="sxs-lookup"><span data-stu-id="74b90-191">Previews are available in Windows Search 4.0, or in Windows Vista with Windows Desktop Search 3.x.</span></span>

<span data-ttu-id="74b90-192">Para crear un controlador de vista previa personalizado:</span><span class="sxs-lookup"><span data-stu-id="74b90-192">To create a custom preview handler:</span></span>

1.  <span data-ttu-id="74b90-193">Implemente un [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) que tome una [IStream](/windows/win32/api/objidl/nn-objidl-istream), siguiendo las instrucciones proporcionadas en los [controladores de vista previa](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="74b90-193">Implement an [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) that takes an [IStream](/windows/win32/api/objidl/nn-objidl-istream), following the guidelines provided in [Preview Handlers](../shell/preview-handlers.md).</span></span>
2.  <span data-ttu-id="74b90-194">Registre el controlador de vista previa:</span><span class="sxs-lookup"><span data-stu-id="74b90-194">Register your preview handler:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx\{8895b1c6-b41f-4c1c-a562-0d564250836f}
       @ = {<Your_PreviewHandler_GUID>}
    ```

3.  <span data-ttu-id="74b90-195">Complete los dos pasos siguientes para implementar una carpeta de Shell para su dirección URL:</span><span class="sxs-lookup"><span data-stu-id="74b90-195">Complete the following two steps to implement a Shell folder for your URL:</span></span>
    1.  <span data-ttu-id="74b90-196">En el [método IShellFolder:: GetUIObjectOf](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), controle [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) y devuelva la Asociación para los elementos de Shell, tal como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="74b90-196">In [IShellFolder::GetUIObjectOf Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), handle [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) and return your association for your Shell items, as shown in the following code sample.</span></span>

        ```
        CComPtr<IQueryAssociations> spqa;
        AssocCreate(CLSID_QueryAssociations, __uuidof(IQueryAssociations), &spqa);
        spqa->Init(0, L"Your_Object_Type", NULL, NULL);
        spqa->QueryInterface(riid, ppvReturn);
        ```

        

    2.  <span data-ttu-id="74b90-197">Una vez que el shell consulta la carpeta de Shell para que el flujo de datos inicialice el controlador de vista previa, vaya al método [IShellFolder:: BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) , controle el IID \_ IStream y devuelva una [IStream](/windows/win32/api/objidl/nn-objidl-istream) a la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="74b90-197">After the Shell queries your Shell folder for the data stream to initialize the preview handler, go to your [IShellFolder::BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) method, handle IID\_IStream and return an [IStream](/windows/win32/api/objidl/nn-objidl-istream) to your URL.</span></span>

<span data-ttu-id="74b90-198">Para volver a usar un controlador de vista previa existente para el tipo de archivo, siga estos dos pasos:</span><span class="sxs-lookup"><span data-stu-id="74b90-198">To reuse an existing preview handler for your file type, follow these two steps:</span></span>

1.  <span data-ttu-id="74b90-199">Registre el controlador de vista previa para el tipo de archivo mediante el CLSID del controlador de vista previa existente en lugar de <el \_ GUID de PreviewHandler \_>.</span><span class="sxs-lookup"><span data-stu-id="74b90-199">Register that preview handler for your file type using the CLSID of the existing preview handler in place of <Your\_PreviewHandler\_GUID>.</span></span>
2.  <span data-ttu-id="74b90-200">Implemente una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="74b90-200">Implement a Shell folder.</span></span>

<span data-ttu-id="74b90-201">Para obtener más información sobre la creación de controladores de vista previa, vea [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) y [controladores de vista previa](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="74b90-201">For more information on creating preview handlers, see [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) and [Preview Handlers](../shell/preview-handlers.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74b90-202">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="74b90-202">Additional Resources</span></span>

-   <span data-ttu-id="74b90-203">Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="74b90-203">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="74b90-204">Para obtener información sobre cómo crear controladores, vea [registrar extensiones de Shell](../shell/reg-shell-exts.md), [crear controladores de extensiones de Shell](../shell/handlers.md), [menú contextual](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [extensiones de espacio de nombres de Shell](../shell/nse-works.md) y [controladores de vista previa](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="74b90-204">For information about creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md), [Creating Shell Extension Handlers](../shell/handlers.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [Shell Namespace Extensions](../shell/nse-works.md) and [Preview Handlers](../shell/preview-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="74b90-205">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74b90-205">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="74b90-206">**Vista**</span><span class="sxs-lookup"><span data-stu-id="74b90-206">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="74b90-207">Desarrollar controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="74b90-207">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="74b90-208">Descripción de los controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="74b90-208">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="74b90-209">Notificar el índice de cambios</span><span class="sxs-lookup"><span data-stu-id="74b90-209">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="74b90-210">Código de ejemplo: extensiones de Shell para controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="74b90-210">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="74b90-211">Instalar y registrar controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="74b90-211">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="74b90-212">Crear un conector de búsqueda para un controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="74b90-212">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="74b90-213">Controladores de protocolo de depuración</span><span class="sxs-lookup"><span data-stu-id="74b90-213">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
