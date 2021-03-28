---
description: Gran parte de la implementación de un objeto de controlador de extensión de Shell está dictada por su tipo. Sin embargo, hay algunos elementos comunes. En este tema se describen los aspectos de la implementación que comparten todos los controladores de extensión de Shell.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Inicializar controladores de extensión de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a27b6273c5e342dc4caf545fb3593cdad66261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986050"
---
# <a name="initializing-shell-extension-handlers"></a><span data-ttu-id="80448-105">Inicializar controladores de extensión de Shell</span><span class="sxs-lookup"><span data-stu-id="80448-105">Initializing Shell Extension Handlers</span></span>

<span data-ttu-id="80448-106">Gran parte de la implementación de un objeto de controlador de extensión de Shell está dictada por su tipo.</span><span class="sxs-lookup"><span data-stu-id="80448-106">Much of the implementation of a Shell extension handler object is dictated by its type.</span></span> <span data-ttu-id="80448-107">Sin embargo, hay algunos elementos comunes.</span><span class="sxs-lookup"><span data-stu-id="80448-107">There are, however, some common elements.</span></span> <span data-ttu-id="80448-108">En este tema se describen los aspectos de la implementación que comparten todos los controladores de extensión de Shell.</span><span class="sxs-lookup"><span data-stu-id="80448-108">This topic discusses those aspects of implementation that are shared by all Shell extension handlers.</span></span>

<span data-ttu-id="80448-109">Todos los controladores de extensión de Shell son objetos de modelo de objetos componentes (COM) en proceso.</span><span class="sxs-lookup"><span data-stu-id="80448-109">All Shell extension handlers are in-process Component Object Model (COM) objects.</span></span> <span data-ttu-id="80448-110">Se les debe asignar un GUID y registrarse como se describe en [registrar controladores de extensión de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="80448-110">They must be assigned a GUID and registered as described in [Registering Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="80448-111">Se implementan como archivos dll y deben exportar las siguientes funciones estándar:</span><span class="sxs-lookup"><span data-stu-id="80448-111">They are implemented as DLLs and must export the following standard functions:</span></span>

-   <span data-ttu-id="80448-112">[**DllMain**](../dlls/dllmain.md).</span><span class="sxs-lookup"><span data-stu-id="80448-112">[**DllMain**](../dlls/dllmain.md).</span></span> <span data-ttu-id="80448-113">Punto de entrada estándar al archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="80448-113">The standard entry point to the DLL.</span></span>
-   <span data-ttu-id="80448-114">[**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject).</span><span class="sxs-lookup"><span data-stu-id="80448-114">[**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject).</span></span> <span data-ttu-id="80448-115">Expone el generador de clases del objeto.</span><span class="sxs-lookup"><span data-stu-id="80448-115">Exposes the object's class factory.</span></span>
-   <span data-ttu-id="80448-116">[**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow).</span><span class="sxs-lookup"><span data-stu-id="80448-116">[**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow).</span></span> <span data-ttu-id="80448-117">COM llama a esta función para determinar si el objeto atiende a los clientes.</span><span class="sxs-lookup"><span data-stu-id="80448-117">COM calls this function to determine whether the object is serving any clients.</span></span> <span data-ttu-id="80448-118">De lo contrario, el sistema puede descargar el archivo DLL y liberar la memoria asociada.</span><span class="sxs-lookup"><span data-stu-id="80448-118">If not, the system can unload the DLL and free the associated memory.</span></span>

<span data-ttu-id="80448-119">Al igual que todos los objetos COM, los controladores de la extensión de Shell deben implementar una interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y un [generador de clases](../com/implementing-iclassfactory.md).</span><span class="sxs-lookup"><span data-stu-id="80448-119">Like all COM objects, Shell extension handlers must implement an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface and a [class factory](../com/implementing-iclassfactory.md).</span></span> <span data-ttu-id="80448-120">La mayoría también debe implementar una interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) o [**ISHELLEXTINIT**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) en Windows XP o versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="80448-120">Most must also implement either an [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) or [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface in Windows XP or earlier.</span></span> <span data-ttu-id="80448-121">Se reemplazaron por [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) y [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="80448-121">These were replaced by [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) and [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista.</span></span> <span data-ttu-id="80448-122">El shell usa estas interfaces para inicializar el controlador.</span><span class="sxs-lookup"><span data-stu-id="80448-122">The Shell uses these interfaces to initialize the handler.</span></span>

<span data-ttu-id="80448-123">La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) debe implementarse de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="80448-123">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface must be implemented by the following:</span></span>

-   <span data-ttu-id="80448-124">Controladores de iconos</span><span class="sxs-lookup"><span data-stu-id="80448-124">Icon handlers</span></span>
-   <span data-ttu-id="80448-125">Controladores de datos</span><span class="sxs-lookup"><span data-stu-id="80448-125">Data handlers</span></span>
-   <span data-ttu-id="80448-126">Quitar controladores</span><span class="sxs-lookup"><span data-stu-id="80448-126">Drop handlers</span></span>

<span data-ttu-id="80448-127">La interfaz [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) debe implementarse de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="80448-127">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface must be implemented by the following:</span></span>

-   <span data-ttu-id="80448-128">Controladores de menú contextual</span><span class="sxs-lookup"><span data-stu-id="80448-128">Shortcut menu handlers</span></span>
-   <span data-ttu-id="80448-129">Controladores de arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="80448-129">Drag-and-drop handlers</span></span>
-   <span data-ttu-id="80448-130">Controladores de hoja de propiedades</span><span class="sxs-lookup"><span data-stu-id="80448-130">Property sheet handlers</span></span>

<span data-ttu-id="80448-131">En el resto de este tema se tratan los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="80448-131">The following subjects are discussed in the remainder of this topic:</span></span>

-   [<span data-ttu-id="80448-132">Implementar IPersistFile</span><span class="sxs-lookup"><span data-stu-id="80448-132">Implementing IPersistFile</span></span>](#implementing-ipersistfile)
-   [<span data-ttu-id="80448-133">Implementación de IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="80448-133">Implementing IShellExtInit</span></span>](#implementing-ishellextinit)
-   [<span data-ttu-id="80448-134">Personalización de recuadro informativo</span><span class="sxs-lookup"><span data-stu-id="80448-134">Infotip Customization</span></span>](#infotip-customization)
-   [<span data-ttu-id="80448-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80448-135">Related topics</span></span>](#related-topics)

## <a name="implementing-ipersistfile"></a><span data-ttu-id="80448-136">Implementar IPersistFile</span><span class="sxs-lookup"><span data-stu-id="80448-136">Implementing IPersistFile</span></span>

<span data-ttu-id="80448-137">La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) está diseñada para permitir la carga o el almacenamiento de un objeto en un archivo de disco.</span><span class="sxs-lookup"><span data-stu-id="80448-137">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is designed to permit an object to be loaded from or saved to a disk file.</span></span> <span data-ttu-id="80448-138">Tiene seis métodos además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), cinco de los suyos propios y el método [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) que hereda de [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist).</span><span class="sxs-lookup"><span data-stu-id="80448-138">It has six methods in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), five of its own, and the [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) method that it inherits from [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist).</span></span> <span data-ttu-id="80448-139">Con las extensiones de Shell, **IPersist** solo se usa para inicializar un objeto de controlador de extensión de Shell.</span><span class="sxs-lookup"><span data-stu-id="80448-139">With Shell extensions, **IPersist** is used only to initialize a Shell extension handler object.</span></span> <span data-ttu-id="80448-140">Dado que normalmente no es necesario leer o escribir en el disco, solo los métodos **GetClassID** y [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) requieren una implementación sin token.</span><span class="sxs-lookup"><span data-stu-id="80448-140">Because there is typically no need to read from or write to the disk, only the **GetClassID** and [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) methods require a nontoken implementation.</span></span>

<span data-ttu-id="80448-141">El shell llama primero a [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) y la función devuelve el identificador de clase (CLSID) del objeto de controlador de extensión.</span><span class="sxs-lookup"><span data-stu-id="80448-141">The Shell calls [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) first, and the function returns the class identifier (CLSID) of the extension handler object.</span></span> <span data-ttu-id="80448-142">Después, el shell llama a [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) y pasa dos valores.</span><span class="sxs-lookup"><span data-stu-id="80448-142">The Shell then calls [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) and passes in two values.</span></span> <span data-ttu-id="80448-143">La primera, *pszFile*, es una cadena Unicode con el nombre del archivo o carpeta en el que está a punto de trabajar el shell.</span><span class="sxs-lookup"><span data-stu-id="80448-143">The first, *pszFile*, is a Unicode string with the name of the file or folder that Shell is about to operate on.</span></span> <span data-ttu-id="80448-144">La segunda es *dwMode*, que indica el modo de acceso a archivos.</span><span class="sxs-lookup"><span data-stu-id="80448-144">The second is *dwMode*, which indicates the file access mode.</span></span> <span data-ttu-id="80448-145">Dado que normalmente no es necesario tener acceso a los archivos, *dwMode* suele ser cero.</span><span class="sxs-lookup"><span data-stu-id="80448-145">Because there is normally no need to access files, *dwMode* is typically zero.</span></span> <span data-ttu-id="80448-146">El método almacena estos valores según sea necesario para su posterior referencia.</span><span class="sxs-lookup"><span data-stu-id="80448-146">The method stores these values as needed for later reference.</span></span>

<span data-ttu-id="80448-147">En el fragmento de código siguiente se muestra cómo un controlador de extensión de Shell típico implementa los métodos [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) y [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) .</span><span class="sxs-lookup"><span data-stu-id="80448-147">The following code fragment illustrates how a typical Shell extension handler implements the [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) and [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) methods.</span></span> <span data-ttu-id="80448-148">Está diseñado para controlar ANSI o Unicode.</span><span class="sxs-lookup"><span data-stu-id="80448-148">It is designed to handle either ANSI or Unicode.</span></span> <span data-ttu-id="80448-149">CLSID \_ SampleExtHandler es el GUID del objeto del controlador de extensión y CSampleShellExtension es el nombre de la clase que se usa para implementar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="80448-149">CLSID\_SampleExtHandler is the extension handler object's GUID, and CSampleShellExtension is the name of the class used to implement the interface.</span></span> <span data-ttu-id="80448-150">Las variables **m \_ szFileName** y **m \_ dwMode** son variables privadas que se usan para almacenar el nombre y las marcas de acceso del archivo.</span><span class="sxs-lookup"><span data-stu-id="80448-150">The **m\_szFileName** and **m\_dwMode** variables are private variables that are used to store the file's name and access flags.</span></span>


```C++
class CSampleShellExtension : public IPersistFile
{
    // Method declarations not included

    private:
    WCHAR m_szFileName[MAX_PATH];    // The file name
    DWORD m_dwMode;                  // The file access mode
}

IFACEMETHODIMP CSampleShellExtension::GetClassID(__out CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

IFACEMETHODIMP CSampleShellExtension::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(m_szFileName, ARRAYSIZE(m_szFileName), pszFile); 
}

// The implementation sample is continued in the next section.
```



## <a name="implementing-ishellextinit"></a><span data-ttu-id="80448-151">Implementación de IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="80448-151">Implementing IShellExtInit</span></span>

<span data-ttu-id="80448-152">La interfaz [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) tiene solo un método, [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="80448-152">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface has only one method, [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="80448-153">El método tiene tres parámetros que el shell puede usar para pasar varios tipos de información.</span><span class="sxs-lookup"><span data-stu-id="80448-153">The method has three parameters that the Shell can use to pass in various types of information.</span></span> <span data-ttu-id="80448-154">Los valores pasados dependen del tipo de controlador y otros pueden establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="80448-154">The values passed in depend on the type of handler, and some can be set to **NULL**.</span></span>

-   <span data-ttu-id="80448-155">*pidlFolder* contiene el puntero de una carpeta a una lista de identificadores de elementos (PIDL).</span><span class="sxs-lookup"><span data-stu-id="80448-155">*pidlFolder* holds a folder's pointer to an item identifier list (PIDL).</span></span> <span data-ttu-id="80448-156">Se trata de una PIDL absoluta.</span><span class="sxs-lookup"><span data-stu-id="80448-156">This is an absolute PIDL.</span></span> <span data-ttu-id="80448-157">Para las extensiones de la hoja de propiedades, este valor es **null**.</span><span class="sxs-lookup"><span data-stu-id="80448-157">For property sheet extensions, this value is **NULL**.</span></span> <span data-ttu-id="80448-158">En el caso de las extensiones de menú contextual, es el PIDL de la carpeta que contiene el elemento cuyo menú contextual se muestra.</span><span class="sxs-lookup"><span data-stu-id="80448-158">For shortcut menu extensions, it is the PIDL of the folder that contains the item whose shortcut menu is being displayed.</span></span> <span data-ttu-id="80448-159">En el caso de los controladores no predeterminados de arrastrar y colocar, es el PIDL de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="80448-159">For nondefault drag-and-drop handlers, it is the PIDL of the target folder.</span></span>
-   <span data-ttu-id="80448-160">*pDataObject* contiene un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de un objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="80448-160">*pDataObject* holds a pointer to a data object's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="80448-161">El objeto de datos contiene uno o varios nombres de archivo en formato [ \_ HDROP de CF](dragdrop.md) .</span><span class="sxs-lookup"><span data-stu-id="80448-161">The data object holds one or more file names in [CF\_HDROP](dragdrop.md) format.</span></span>
-   <span data-ttu-id="80448-162">*hRegKey* contiene una clave del registro para el tipo de carpeta o objeto de archivo.</span><span class="sxs-lookup"><span data-stu-id="80448-162">*hRegKey* holds a registry key for the file object or folder type.</span></span>

<span data-ttu-id="80448-163">El método [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) almacena el nombre de archivo, el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) y la clave del registro según sea necesario para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="80448-163">The [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method stores the file name, [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer, and registry key as needed for later use.</span></span> <span data-ttu-id="80448-164">En el fragmento de código siguiente se muestra una implementación de **IShellExtInit:: Initialize**.</span><span class="sxs-lookup"><span data-stu-id="80448-164">The following code fragment illustrates an implementation of **IShellExtInit::Initialize**.</span></span> <span data-ttu-id="80448-165">Para simplificar, en este ejemplo se da por supuesto que el objeto de datos contiene un solo archivo.</span><span class="sxs-lookup"><span data-stu-id="80448-165">For simplicity, this example assumes that the data object contains only a single file.</span></span> <span data-ttu-id="80448-166">En general, el objeto de datos puede contener varios archivos, cada uno de los cuales tendrá que extraerse.</span><span class="sxs-lookup"><span data-stu-id="80448-166">In general, the data object might contain multiple files, each of which will need to be extracted.</span></span>


```C++
// This code continues the CSampleShellExtension sample shown in the
// "Implementing IPersistFile" section above.

class CSampleShellExtension : public IShellExtInit
{
    // Method declarations not included
    
    private:
    // IDList of the folder for extensions invoked on the folder, such as 
    // background context menu handlers or nondefault drag-and-drop handlers. 
    PIDLIST_ABSOLUTE m_pidlFolder;
    
    // The data object contains an expression of the items that the handler is 
    // being initialized for. Use SHCreateShellItemArrayFromDataObject to 
    // convert this object to an array of items. Use SHGetItemFromObject if you
    // are only interested in a single Shell item. If you need a file system
    // path, use IShellItem::GetDisplayName(SIGDN_FILESYSPATH, ...).
    IDataObject *m_pdtobj;
    
    // For context menu handlers, the registry key provides access to verb 
    // instance data that might be stored there. This is a rare feature to use 
    // so most extensions do not need this variable.
    HKEY m_hRegKey;             
}
    
// This method must be very efficient. Do not do any unnecessary work here.
// Use Initialize to acquire resources that will be used later.

IFACEMETHODIMP CSampleShellExtension::Initialize(__in_opt PCIDLIST_ABSOLUTE pidlFolder,
                                                 __in_opt IDataObject *pDataObject, 
                                                 __in_opt HKEY hRegKey) 
{ 
    // In some cases, handlers are initialized multiple times. Therefore, 
    // clear any previous state here.
    CoTaskMemFree(m_pidlFolder);
    m_pidlFolder = NULL;
    
    if (m_pdtobj)
    { 
        m_pdtobj->Release(); 
    }
    
    if (m_hRegKey)
    {
        RegCloseKey(m_hRegKey);
        m_hRegKey = NULL;
    }
    
    // Capture the inputs for use later.
    HRESULT hr = S_OK;
    
    if (pidlFolder)
    {
        m_pidlFolder = ILClone(pidlFolder);   // Make a copy to use later.
        hr = m_pidlFolder ? S_OK : E_OUTOFMEMORY;
    }
    
    if (SUCCEEDED(hr))
    {
        // If a data object pointer was passed into the method, save it and
        // extract the file name. 
        if (pDataObject) 
        { 
            m_pdtobj = pDataObject; 
            m_pdtobj->AddRef(); 
        }
    
        // It is uncommon to use the registry handle, but if you need it,
        // duplicate it now.
        if (hRegKey)
        {
            LSTATUS const result = RegOpenKeyEx(hRegKey, NULL, 0, KEY_READ, &m_hRegKey); 
            hr = HRESULT_FROM_WIN32(result);
        }
    }
    
    return hr;
}
```



## <a name="infotip-customization"></a><span data-ttu-id="80448-167">Personalización de recuadro informativo</span><span class="sxs-lookup"><span data-stu-id="80448-167">Infotip Customization</span></span>

<span data-ttu-id="80448-168">Hay dos maneras de personalizar recuadros informativos.</span><span class="sxs-lookup"><span data-stu-id="80448-168">There are two ways to customize infotips.</span></span> <span data-ttu-id="80448-169">Una forma consiste en implementar un objeto que admita [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) y, a continuación, registrar el objeto bajo la subclave adecuada en el registro (vea más abajo).</span><span class="sxs-lookup"><span data-stu-id="80448-169">One way is to implement an object that supports [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) and then register the object under the proper subkey in the registry (see below).</span></span> <span data-ttu-id="80448-170">Como alternativa, puede especificar una cadena fija o una lista de determinadas propiedades de archivo que se van a mostrar.</span><span class="sxs-lookup"><span data-stu-id="80448-170">Alternatively, you can specify either a fixed string or a list of certain file properties to be displayed.</span></span>

<span data-ttu-id="80448-171">Para mostrar una cadena fija para una extensión de espacio de nombres, cree  una subclave denominada recuadro informativo debajo de la clave CLSID de la extensión de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="80448-171">To display a fixed string for a namespace extension, create a subkey called **InfoTip** beneath the CLSID key of your namespace extension.</span></span> <span data-ttu-id="80448-172">Establezca los datos de esa subclave en la cadena que desea mostrar.</span><span class="sxs-lookup"><span data-stu-id="80448-172">Set the data of that subkey to be the string you want to be displayed.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

<span data-ttu-id="80448-173">Para mostrar una cadena fija para un tipo de archivo, cree una subclave **denominada** recuadro informativo debajo de la clave **ProgID** del tipo de archivo para el que desea proporcionar recuadros informativos.</span><span class="sxs-lookup"><span data-stu-id="80448-173">To display a fixed string for a file type, create a subkey called **InfoTip** beneath the **ProgID** key of the file type for which you want to supply infotips.</span></span> <span data-ttu-id="80448-174">Establezca los datos de esa subclave en la cadena que desea mostrar.</span><span class="sxs-lookup"><span data-stu-id="80448-174">Set the data of that subkey to be the string you want to be displayed.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

<span data-ttu-id="80448-175">Si desea que el shell muestre determinadas propiedades de archivo en el recuadro informativo para un tipo de archivo específico  , cree una subclave denominada recuadro informativo debajo de la clave **ProgID** de ese tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="80448-175">If you want the Shell to show certain file properties in the infotip for a specific file type, create a subkey called **InfoTip** beneath the **ProgID** key of that file type.</span></span> <span data-ttu-id="80448-176">Establezca los datos de esa subclave en una lista delimitada por punto y coma de nombres de propiedad canónicos o {fmtid}, pares PID en los que *NombreDePropiedad* es un nombre de propiedad canónico y *{fmtid}, el PID* es un [**par fmtid/PID**](./objects.md).</span><span class="sxs-lookup"><span data-stu-id="80448-176">Set the data of that subkey to be a semicolon-delineated list of canonical property names or {fmtid}, pid pairs where *propname* is a canonical property name and *{fmtid},pid* is a [**FMTID/PID pair**](./objects.md).</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

<span data-ttu-id="80448-177">Se pueden usar los siguientes nombres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="80448-177">The following property names can be used.</span></span>



| <span data-ttu-id="80448-178">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="80448-178">Property Name</span></span>    | <span data-ttu-id="80448-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="80448-179">Description</span></span>                   | <span data-ttu-id="80448-180">Recuperado de</span><span class="sxs-lookup"><span data-stu-id="80448-180">Retrieved From</span></span>                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="80448-181">Autor</span><span class="sxs-lookup"><span data-stu-id="80448-181">Author</span></span>           | <span data-ttu-id="80448-182">Autor del documento</span><span class="sxs-lookup"><span data-stu-id="80448-182">Author of the document</span></span>        | [<span data-ttu-id="80448-183">**autor de PIDSI \_**</span><span class="sxs-lookup"><span data-stu-id="80448-183">**PIDSI\_AUTHOR**</span></span>](../stg/the-summary-information-property-set.md)                             |
| <span data-ttu-id="80448-184">Title</span><span class="sxs-lookup"><span data-stu-id="80448-184">Title</span></span>            | <span data-ttu-id="80448-185">Título del documento</span><span class="sxs-lookup"><span data-stu-id="80448-185">Title of the document</span></span>         | [<span data-ttu-id="80448-186">**título de PIDSI \_**</span><span class="sxs-lookup"><span data-stu-id="80448-186">**PIDSI\_TITLE**</span></span>](../stg/the-summary-information-property-set.md)                              |
| <span data-ttu-id="80448-187">Asunto</span><span class="sxs-lookup"><span data-stu-id="80448-187">Subject</span></span>          | <span data-ttu-id="80448-188">Resumen de asunto</span><span class="sxs-lookup"><span data-stu-id="80448-188">Subject summary</span></span>               | [<span data-ttu-id="80448-189">**\_asunto PIDSI**</span><span class="sxs-lookup"><span data-stu-id="80448-189">**PIDSI\_SUBJECT**</span></span>](../stg/the-summary-information-property-set.md)                            |
| <span data-ttu-id="80448-190">Comentario</span><span class="sxs-lookup"><span data-stu-id="80448-190">Comment</span></span>          | <span data-ttu-id="80448-191">Comentarios del documento</span><span class="sxs-lookup"><span data-stu-id="80448-191">Document comments</span></span>             | <span data-ttu-id="80448-192">[**PIDSI \_**](../stg/the-summary-information-property-set.md) Propiedades de comentario o carpeta/unidad</span><span class="sxs-lookup"><span data-stu-id="80448-192">[**PIDSI\_COMMENT**](../stg/the-summary-information-property-set.md) or folder/drive properties</span></span> |
| <span data-ttu-id="80448-193">PageCount</span><span class="sxs-lookup"><span data-stu-id="80448-193">PageCount</span></span>        | <span data-ttu-id="80448-194">Número de páginas</span><span class="sxs-lookup"><span data-stu-id="80448-194">Number of pages</span></span>               | [<span data-ttu-id="80448-195">**PIDSI \_ PAGECOUNT**</span><span class="sxs-lookup"><span data-stu-id="80448-195">**PIDSI\_PAGECOUNT**</span></span>](../stg/the-summary-information-property-set.md)                          |
| <span data-ttu-id="80448-196">Nombre</span><span class="sxs-lookup"><span data-stu-id="80448-196">Name</span></span>             | <span data-ttu-id="80448-197">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="80448-197">Friendly name</span></span>                 | <span data-ttu-id="80448-198">Vista de carpetas estándar</span><span class="sxs-lookup"><span data-stu-id="80448-198">Standard folder view</span></span>                                                                      |
| <span data-ttu-id="80448-199">OriginalLocation</span><span class="sxs-lookup"><span data-stu-id="80448-199">OriginalLocation</span></span> | <span data-ttu-id="80448-200">Ubicación del archivo original</span><span class="sxs-lookup"><span data-stu-id="80448-200">Location of original file</span></span>     | <span data-ttu-id="80448-201">Carpeta de mi maletín y carpeta de la papelera de reciclaje</span><span class="sxs-lookup"><span data-stu-id="80448-201">Briefcase folder and Recycle Bin folder</span></span>                                                   |
| <span data-ttu-id="80448-202">DateDeleted</span><span class="sxs-lookup"><span data-stu-id="80448-202">DateDeleted</span></span>      | <span data-ttu-id="80448-203">Se eliminó el archivo de fecha</span><span class="sxs-lookup"><span data-stu-id="80448-203">Date file was deleted</span></span>         | <span data-ttu-id="80448-204">Carpeta de la papelera de reciclaje</span><span class="sxs-lookup"><span data-stu-id="80448-204">Recycle Bin folder</span></span>                                                                        |
| <span data-ttu-id="80448-205">Tipo</span><span class="sxs-lookup"><span data-stu-id="80448-205">Type</span></span>             | <span data-ttu-id="80448-206">Tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="80448-206">Type of file</span></span>                  | <span data-ttu-id="80448-207">Vista de detalles de carpetas estándar</span><span class="sxs-lookup"><span data-stu-id="80448-207">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="80448-208">Tamaño</span><span class="sxs-lookup"><span data-stu-id="80448-208">Size</span></span>             | <span data-ttu-id="80448-209">Tamaño del archivo</span><span class="sxs-lookup"><span data-stu-id="80448-209">Size of file</span></span>                  | <span data-ttu-id="80448-210">Vista de detalles de carpetas estándar</span><span class="sxs-lookup"><span data-stu-id="80448-210">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="80448-211">SyncCopyIn</span><span class="sxs-lookup"><span data-stu-id="80448-211">SyncCopyIn</span></span>       | <span data-ttu-id="80448-212">Igual que OriginalLocation</span><span class="sxs-lookup"><span data-stu-id="80448-212">Same as OriginalLocation</span></span>      | <span data-ttu-id="80448-213">Igual que OriginalLocation</span><span class="sxs-lookup"><span data-stu-id="80448-213">Same as OriginalLocation</span></span>                                                                  |
| <span data-ttu-id="80448-214">Modificado</span><span class="sxs-lookup"><span data-stu-id="80448-214">Modified</span></span>         | <span data-ttu-id="80448-215">Fecha de última modificación</span><span class="sxs-lookup"><span data-stu-id="80448-215">Date last modified</span></span>            | <span data-ttu-id="80448-216">Vista de detalles de carpetas estándar</span><span class="sxs-lookup"><span data-stu-id="80448-216">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="80448-217">Creado</span><span class="sxs-lookup"><span data-stu-id="80448-217">Created</span></span>          | <span data-ttu-id="80448-218">Fecha de creación</span><span class="sxs-lookup"><span data-stu-id="80448-218">Date created</span></span>                  | <span data-ttu-id="80448-219">Vista de detalles de carpetas estándar</span><span class="sxs-lookup"><span data-stu-id="80448-219">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="80448-220">Acceso</span><span class="sxs-lookup"><span data-stu-id="80448-220">Accessed</span></span>         | <span data-ttu-id="80448-221">Fecha de último acceso</span><span class="sxs-lookup"><span data-stu-id="80448-221">Date last accessed</span></span>            | <span data-ttu-id="80448-222">Vista de detalles de carpetas estándar</span><span class="sxs-lookup"><span data-stu-id="80448-222">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="80448-223">InFolder</span><span class="sxs-lookup"><span data-stu-id="80448-223">InFolder</span></span>         | <span data-ttu-id="80448-224">Directorio que contiene el archivo</span><span class="sxs-lookup"><span data-stu-id="80448-224">Directory containing the file</span></span> | <span data-ttu-id="80448-225">Resultados de búsqueda de documentos</span><span class="sxs-lookup"><span data-stu-id="80448-225">Document search results</span></span>                                                                   |
| <span data-ttu-id="80448-226">Rango</span><span class="sxs-lookup"><span data-stu-id="80448-226">Rank</span></span>             | <span data-ttu-id="80448-227">Calidad de coincidencia de búsqueda</span><span class="sxs-lookup"><span data-stu-id="80448-227">Quality of search match</span></span>       | <span data-ttu-id="80448-228">Resultados de búsqueda de documentos</span><span class="sxs-lookup"><span data-stu-id="80448-228">Document search results</span></span>                                                                   |
| <span data-ttu-id="80448-229">FreeSpace</span><span class="sxs-lookup"><span data-stu-id="80448-229">FreeSpace</span></span>        | <span data-ttu-id="80448-230">Espacio de almacenamiento disponible</span><span class="sxs-lookup"><span data-stu-id="80448-230">Available storage space</span></span>       | <span data-ttu-id="80448-231">Unidades de disco</span><span class="sxs-lookup"><span data-stu-id="80448-231">Disk drives</span></span>                                                                               |
| <span data-ttu-id="80448-232">NumberOfVisits</span><span class="sxs-lookup"><span data-stu-id="80448-232">NumberOfVisits</span></span>   | <span data-ttu-id="80448-233">Número de visitas</span><span class="sxs-lookup"><span data-stu-id="80448-233">Number of visits</span></span>              | <span data-ttu-id="80448-234">carpeta Favoritos</span><span class="sxs-lookup"><span data-stu-id="80448-234">Favorites folder</span></span>                                                                          |
| <span data-ttu-id="80448-235">Atributos</span><span class="sxs-lookup"><span data-stu-id="80448-235">Attributes</span></span>       | <span data-ttu-id="80448-236">Atributos de archivo</span><span class="sxs-lookup"><span data-stu-id="80448-236">File Attributes</span></span>               | <span data-ttu-id="80448-237">Vista de detalles de carpetas estándar</span><span class="sxs-lookup"><span data-stu-id="80448-237">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="80448-238">Compañía</span><span class="sxs-lookup"><span data-stu-id="80448-238">Company</span></span>          | <span data-ttu-id="80448-239">Nombre de la compañía</span><span class="sxs-lookup"><span data-stu-id="80448-239">Company name</span></span>                  | [<span data-ttu-id="80448-240">**\_empresa PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="80448-240">**PIDDSI\_COMPANY**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| <span data-ttu-id="80448-241">Category</span><span class="sxs-lookup"><span data-stu-id="80448-241">Category</span></span>         | <span data-ttu-id="80448-242">Categoría del documento</span><span class="sxs-lookup"><span data-stu-id="80448-242">Document category</span></span>             | [<span data-ttu-id="80448-243">**\_categoría PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="80448-243">**PIDDSI\_CATEGORY**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| <span data-ttu-id="80448-244">Copyright</span><span class="sxs-lookup"><span data-stu-id="80448-244">Copyright</span></span>        | <span data-ttu-id="80448-245">Copyright de los medios</span><span class="sxs-lookup"><span data-stu-id="80448-245">Media copyright</span></span>               | [<span data-ttu-id="80448-246">**COPYRIGHT de PIDMSI \_**</span><span class="sxs-lookup"><span data-stu-id="80448-246">**PIDMSI\_COPYRIGHT**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| <span data-ttu-id="80448-247">HTMLInfoTipFile</span><span class="sxs-lookup"><span data-stu-id="80448-247">HTMLInfoTipFile</span></span>  | <span data-ttu-id="80448-248">Archivo recuadro informativo HTML</span><span class="sxs-lookup"><span data-stu-id="80448-248">HTML InfoTip file</span></span>             | <span data-ttu-id="80448-249">Desktop.ini archivo para la carpeta</span><span class="sxs-lookup"><span data-stu-id="80448-249">Desktop.ini file for folder</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="80448-250">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80448-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80448-251">Registrando controladores de extensión de Shell</span><span class="sxs-lookup"><span data-stu-id="80448-251">Registering Shell Extension Handlers</span></span>](reg-shell-exts.md)
</dt> </dl>

 

 
