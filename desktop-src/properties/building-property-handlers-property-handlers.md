---
description: En este tema se explica cómo crear y registrar controladores de propiedades para trabajar con el sistema de propiedades de Windows.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Inicializar controladores de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8eb11bc44217e508313bfb477c65925b44216e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277066"
---
# <a name="initializing-property-handlers"></a><span data-ttu-id="84b7d-103">Inicializar controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="84b7d-103">Initializing Property Handlers</span></span>

<span data-ttu-id="84b7d-104">En este tema se explica cómo crear y registrar controladores de propiedades para trabajar con el sistema de propiedades de Windows.</span><span class="sxs-lookup"><span data-stu-id="84b7d-104">This topic explains how to create and register property handlers to work with the Windows property system.</span></span>

<span data-ttu-id="84b7d-105">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="84b7d-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="84b7d-106">Controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="84b7d-106">Property Handlers</span></span>](#property-handlers)
-   [<span data-ttu-id="84b7d-107">Antes de comenzar</span><span class="sxs-lookup"><span data-stu-id="84b7d-107">Before You Begin</span></span>](#before-you-begin)
-   [<span data-ttu-id="84b7d-108">Inicializar controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="84b7d-108">Initializing Property Handlers</span></span>](#initializing-property-handlers)
-   [<span data-ttu-id="84b7d-109">Almacén de propiedades en memoria</span><span class="sxs-lookup"><span data-stu-id="84b7d-109">In-Memory Property Store</span></span>](#in-memory-property-store)
-   [<span data-ttu-id="84b7d-110">Trabajar con PROPVARIANT-Based valores</span><span class="sxs-lookup"><span data-stu-id="84b7d-110">Dealing with PROPVARIANT-Based Values</span></span>](#dealing-with-propvariant-based-values)
-   [<span data-ttu-id="84b7d-111">Compatibilidad con metadatos abiertos</span><span class="sxs-lookup"><span data-stu-id="84b7d-111">Supporting Open Metadata</span></span>](#supporting-open-metadata)
-   [<span data-ttu-id="84b7d-112">Contenido de texto completo</span><span class="sxs-lookup"><span data-stu-id="84b7d-112">Full-Text Contents</span></span>](#full-text-contents)
-   [<span data-ttu-id="84b7d-113">Proporcionar valores para las propiedades</span><span class="sxs-lookup"><span data-stu-id="84b7d-113">Providing Values for Properties</span></span>](#providing-values-for-properties)
-   [<span data-ttu-id="84b7d-114">Escribir valores hacia atrás</span><span class="sxs-lookup"><span data-stu-id="84b7d-114">Writing Back Values</span></span>](#writing-back-values)
-   [<span data-ttu-id="84b7d-115">Implementación de IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="84b7d-115">Implementing IPropertyStoreCapabilities</span></span>](#implementing-ipropertystorecapabilities)
-   [<span data-ttu-id="84b7d-116">Registrar y distribuir controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="84b7d-116">Registering and Distributing Property Handlers</span></span>](#registering-and-distributing-property-handlers)
-   [<span data-ttu-id="84b7d-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84b7d-117">Related topics</span></span>](#related-topics)

## <a name="property-handlers"></a><span data-ttu-id="84b7d-118">Controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="84b7d-118">Property Handlers</span></span>

<span data-ttu-id="84b7d-119">Los controladores de propiedades son una parte fundamental del sistema de propiedades.</span><span class="sxs-lookup"><span data-stu-id="84b7d-119">Property handlers are a crucial part of the property system.</span></span> <span data-ttu-id="84b7d-120">El indexador los invoca en proceso para leer e indexar los valores de propiedad, y el explorador de Windows también los invoca en el proceso para leer y escribir los valores de propiedad directamente en los archivos.</span><span class="sxs-lookup"><span data-stu-id="84b7d-120">They are invoked in-process by the indexer to read and index property values, and are also invoked by Windows Explorer in-process to read and write property values directly in the files.</span></span> <span data-ttu-id="84b7d-121">Estos controladores deben escribirse y probarse cuidadosamente para evitar el rendimiento degradado o la pérdida de datos en los archivos afectados.</span><span class="sxs-lookup"><span data-stu-id="84b7d-121">These handlers need to be carefully written and tested to prevent degraded performance or the loss of data in the affected files.</span></span> <span data-ttu-id="84b7d-122">Para obtener más información sobre las consideraciones específicas del indexador que afectan a la implementación del controlador de propiedades, vea [desarrollar controladores de propiedades para Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).</span><span class="sxs-lookup"><span data-stu-id="84b7d-122">For more information on indexer-specific considerations that affect property handler implementation, see [Developing Property Handlers for Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).</span></span>

<span data-ttu-id="84b7d-123">En este tema se describe un ejemplo de formato de archivo basado en XML que describe una receta con una extensión de nombre de archivo. receta.</span><span class="sxs-lookup"><span data-stu-id="84b7d-123">This topic discusses a sample XML-based file format that describes a recipe with a .recipe file name extension.</span></span> <span data-ttu-id="84b7d-124">La extensión de nombre de archivo. Recipe se registra como su propio formato de archivo distinto en lugar de basarse en el formato de archivo. XML más genérico, cuyo controlador usa un flujo secundario para almacenar propiedades.</span><span class="sxs-lookup"><span data-stu-id="84b7d-124">The .recipe file name extension is registered as its own distinct file format rather than relying on the more generic .xml file format, whose handler uses a secondary stream to store properties.</span></span> <span data-ttu-id="84b7d-125">Se recomienda registrar las extensiones de nombre de archivo únicas para los tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="84b7d-125">We recommend that you register unique file name extensions for your file types.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="84b7d-126">Antes de empezar</span><span class="sxs-lookup"><span data-stu-id="84b7d-126">Before You Begin</span></span>

<span data-ttu-id="84b7d-127">Los controladores de propiedades son objetos COM que crean la abstracción [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para un formato de archivo específico.</span><span class="sxs-lookup"><span data-stu-id="84b7d-127">Property handlers are COM objects that create the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) abstraction for a specific file format.</span></span> <span data-ttu-id="84b7d-128">Leen (analizan) y escriben este formato de archivo de forma que se ajuste a su especificación.</span><span class="sxs-lookup"><span data-stu-id="84b7d-128">They read (parse) and write this file format in a manner that conforms to its specification.</span></span> <span data-ttu-id="84b7d-129">Algunos controladores de propiedades realizan su trabajo en función de las API que abstraen el acceso a un formato de archivo específico.</span><span class="sxs-lookup"><span data-stu-id="84b7d-129">Some property handlers do their work based on APIs that abstract access to a specific file format.</span></span> <span data-ttu-id="84b7d-130">Antes de desarrollar un controlador de propiedades para el formato de archivo, debe comprender cómo el formato de archivo almacena las propiedades y cómo se asignan esas propiedades (nombres y valores) en la abstracción del almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="84b7d-130">Before you develop a property handler for your file format, you need to understand how your file format stores properties, and how those properties (names and values) are mapped into the property store abstraction.</span></span>

<span data-ttu-id="84b7d-131">Al planear la implementación, recuerde que los controladores de propiedades son componentes de bajo nivel que se cargan en el contexto de procesos como el explorador de Windows, el indizador de Windows Search y aplicaciones de terceros que utilizan el modelo de programación de elementos de Shell.</span><span class="sxs-lookup"><span data-stu-id="84b7d-131">When planning your implementation, remember that property handlers are low-level components that are loaded in the context of processes like Windows Explorer, the Windows Search indexer, and third-party applications that use the Shell item programming model.</span></span> <span data-ttu-id="84b7d-132">Como resultado, los controladores de propiedades no se pueden implementar en código administrado y deben implementarse en C++.</span><span class="sxs-lookup"><span data-stu-id="84b7d-132">As a result, property handlers cannot be implemented in managed code, and should be implemented in C++.</span></span> <span data-ttu-id="84b7d-133">Si el controlador usa cualquier API o servicio para realizar su trabajo, debe asegurarse de que esos servicios pueden funcionar correctamente en los entornos en los que se carga el controlador de propiedades.</span><span class="sxs-lookup"><span data-stu-id="84b7d-133">If your handler uses any APIs or services to do its work, you must ensure that those services can function properly in the environment(s) in which your property handler is loaded.</span></span>

> [!Note]  
> <span data-ttu-id="84b7d-134">Los controladores de propiedades siempre se asocian a tipos de archivo específicos; por lo tanto, si el formato de archivo contiene propiedades que requieren un controlador de propiedades personalizado, debe registrar siempre una extensión de nombre de archivo única para cada formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="84b7d-134">Property handlers are always associated with specific file types; thus, if your file format contains properties that require a custom property handler, you should always register a unique file name extension for each file format.</span></span>

 

## <a name="initializing-property-handlers"></a><span data-ttu-id="84b7d-135">Inicializar controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="84b7d-135">Initializing Property Handlers</span></span>

<span data-ttu-id="84b7d-136">Antes de que el sistema use una propiedad, se inicializa llamando a una implementación de [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream).</span><span class="sxs-lookup"><span data-stu-id="84b7d-136">Before a property is used by the system, it is initialized by calling an implementation of [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream).</span></span> <span data-ttu-id="84b7d-137">El controlador de propiedad debe inicializarse haciendo que el sistema lo asigne a una secuencia en lugar de dejar esa asignación a la implementación del controlador.</span><span class="sxs-lookup"><span data-stu-id="84b7d-137">The property handler should be initialized by having the system assign it a stream rather than leaving that assignment to the handler implementation.</span></span> <span data-ttu-id="84b7d-138">Este método de inicialización garantiza lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="84b7d-138">This method of initialization ensures the following things:</span></span>

-   <span data-ttu-id="84b7d-139">El controlador de propiedades puede ejecutarse en un proceso restringido (una característica de seguridad importante) sin tener derechos de acceso para leer o escribir archivos directamente, en lugar de tener acceso a su contenido a través de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="84b7d-139">The property handler can run in a restricted process (an important security feature) without having access rights to directly read or write files, rather accessing their content through the stream.</span></span>
-   <span data-ttu-id="84b7d-140">Se puede confiar en el sistema para controlar el archivo bloqueos oportunistas correctamente, que es una medida de confiabilidad importante.</span><span class="sxs-lookup"><span data-stu-id="84b7d-140">The system can be trusted to handle the file oplocks correctly, which is an important reliability measure.</span></span>
-   <span data-ttu-id="84b7d-141">El sistema de propiedades proporciona un servicio de almacenamiento seguro automático sin ninguna funcionalidad adicional requerida por la implementación del controlador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="84b7d-141">The property system provides an automatic safe saving service without any extra functionality required from the property handler implementation.</span></span> <span data-ttu-id="84b7d-142">Para obtener más información sobre las secuencias, consulte la sección [escritura de valores de reserva](#writing-back-values) .</span><span class="sxs-lookup"><span data-stu-id="84b7d-142">See the [Writing Back Values](#writing-back-values) section for more information about streams.</span></span>
-   <span data-ttu-id="84b7d-143">El uso de [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) abstrae la implementación de los detalles del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="84b7d-143">Use of the [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) abstracts your implementation from file system details.</span></span> <span data-ttu-id="84b7d-144">Esto permite al controlador admitir la inicialización a través de almacenamientos alternativos, como una carpeta de protocolo de transferencia de archivos (FTP) o un archivo comprimido con la extensión de nombre de archivo. zip.</span><span class="sxs-lookup"><span data-stu-id="84b7d-144">This enables the handler to support initialization through alternative storages such as a File Transfer Protocol (FTP) folder or a compressed file with a .zip file name extension.</span></span>

<span data-ttu-id="84b7d-145">Hay casos en los que no es posible la inicialización con secuencias.</span><span class="sxs-lookup"><span data-stu-id="84b7d-145">There are cases where initialization with streams is not possible.</span></span> <span data-ttu-id="84b7d-146">En esas situaciones, hay dos interfaces adicionales que los controladores de propiedades pueden implementar: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) y [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem).</span><span class="sxs-lookup"><span data-stu-id="84b7d-146">In those situations, there are two further interfaces that property handlers can implement: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) and [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem).</span></span> <span data-ttu-id="84b7d-147">Si un controlador de propiedad no implementa [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), debe dejar de ejecutarse en el proceso aislado en el que el indexador del sistema la colocaría de forma predeterminada si se produjeron cambios en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="84b7d-147">If a property handler does not implement the [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), it must opt out of running in the isolated process into which the system indexer would place it by default if there were a change to the stream.</span></span> <span data-ttu-id="84b7d-148">Para no participar en esta característica, establezca el siguiente valor del registro.</span><span class="sxs-lookup"><span data-stu-id="84b7d-148">To opt out of this feature, set the following registry value.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

<span data-ttu-id="84b7d-149">Sin embargo, es mucho mejor implementar [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) y realizar una inicialización basada en streaming.</span><span class="sxs-lookup"><span data-stu-id="84b7d-149">However, it is far better to implement [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) and do a stream-based initialization.</span></span> <span data-ttu-id="84b7d-150">El controlador de propiedades será más seguro y confiable como resultado.</span><span class="sxs-lookup"><span data-stu-id="84b7d-150">Your property handler will be safer and more reliable as a result.</span></span> <span data-ttu-id="84b7d-151">Generalmente, la deshabilitación del aislamiento de procesos está destinada únicamente a los controladores de propiedades heredadas y se debe evitar por cualquier nuevo código.</span><span class="sxs-lookup"><span data-stu-id="84b7d-151">Disabling process isolation is generally intended only for legacy property handlers and should be strenuously avoided by any new code.</span></span>

<span data-ttu-id="84b7d-152">Para examinar la implementación de un controlador de propiedades en detalle, examine el siguiente ejemplo de código, que es una implementación de [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span><span class="sxs-lookup"><span data-stu-id="84b7d-152">To examine the implementation of a property handler in detail, look at the following code example, which is an implementation of [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span></span> <span data-ttu-id="84b7d-153">El controlador se inicializa cargando un documento receta basado en XML a través de un puntero a la instancia de [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) asociada de ese documento.</span><span class="sxs-lookup"><span data-stu-id="84b7d-153">The handler is initialized by loading an XML-based recipe document through a pointer to that document's associated [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) instance.</span></span> <span data-ttu-id="84b7d-154">La variable **\_ spDocEle** que se usa cerca del final del ejemplo de código se define anteriormente en el ejemplo como MSXML2:: IXMLDOMElementPtr.</span><span class="sxs-lookup"><span data-stu-id="84b7d-154">The **\_spDocEle** variable used near the end of the code example is defined earlier in the sample as an MSXML2::IXMLDOMElementPtr.</span></span>

> [!Note]  
> <span data-ttu-id="84b7d-155">Lo siguiente y todos los ejemplos de código siguientes se han tomado del ejemplo de controlador de recetas incluido en el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="84b7d-155">The following and all subsequent code examples are taken from the recipe handler sample included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="84b7d-156">.</span><span class="sxs-lookup"><span data-stu-id="84b7d-156">.</span></span>

 


```
HRESULT CRecipePropertyStore::Initialize(IStream *pStream, DWORD grfMode)
{
    HRESULT hr = E_FAIL;
    
    try
    {
        if (!_spStream)
        {
            hr = _spDomDoc.CreateInstance(__uuidof(MSXML2::DOMDocument60));
            
            if (SUCCEEDED(hr))
            {
                if (VARIANT_TRUE == _spDomDoc->load(static_cast<IUnknown *>(pStream)))
                {
                    _spDocEle = _spDomDoc->documentElement;
                }
```



<span data-ttu-id="84b7d-157">Ti</span><span class="sxs-lookup"><span data-stu-id="84b7d-157">Â</span></span> 

<span data-ttu-id="84b7d-158">Una vez cargado el propio documento, las propiedades que se van a mostrar en el explorador de Windows se cargan llamando al método **\_ LoadProperties** protegido, como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="84b7d-158">After the document itself is loaded, the properties to be displayed in Windows Explorer are loaded by calling the protected **\_LoadProperties** method, as illustrated in the following code example.</span></span> <span data-ttu-id="84b7d-159">Este proceso se examina en detalle en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="84b7d-159">This process is examined in detail in the next section.</span></span>


```
                if (_spDocEle)
                {
                    hr = _LoadProperties();
    
                    if (SUCCEEDED(hr))
                    {
                        _spStream = pStream;
                    }
                }
                else
                {
                    hr = E_FAIL;  // parse error
                }
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
    }
    
    catch (_com_error &e)
    {
        hr = e.Error();
    }
    
    return hr;
}
```



<span data-ttu-id="84b7d-160">Si el flujo es de solo lectura, pero el parámetro *grfMode* contiene la \_ marca ReadWrite de STGM, se debe producir un error en la inicialización y devolver STG \_ E \_ ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="84b7d-160">If the stream is read-only but the *grfMode* parameter contains the STGM\_READWRITE flag, the initialization should fail and return STG\_E\_ACCESSDENIED.</span></span> <span data-ttu-id="84b7d-161">Sin esta comprobación, el explorador de Windows muestra los valores de propiedad como de escritura, aunque no lo hacen, lo que provoca una experiencia de usuario final confusa.</span><span class="sxs-lookup"><span data-stu-id="84b7d-161">Without this check, Windows Explorer shows the property values as writable even though they are not, leading to a confusing end-user experience.</span></span>

<span data-ttu-id="84b7d-162">El controlador de propiedad se inicializa una sola vez en su duración.</span><span class="sxs-lookup"><span data-stu-id="84b7d-162">The property handler is initialized only once in its lifetime.</span></span> <span data-ttu-id="84b7d-163">Si se solicita una segunda inicialización, el controlador debe devolver `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` .</span><span class="sxs-lookup"><span data-stu-id="84b7d-163">If a second initialization is requested, the handler should return `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)`.</span></span>

## <a name="in-memory-property-store"></a><span data-ttu-id="84b7d-164">In-Memory almacén de propiedades</span><span class="sxs-lookup"><span data-stu-id="84b7d-164">In-Memory Property Store</span></span>

<span data-ttu-id="84b7d-165">Antes de examinar la implementación de **\_ LoadProperties**, debe comprender la matriz **PropertyMap** utilizada en el ejemplo para asignar las propiedades del documento XML a las propiedades existentes en el sistema de propiedades a través de sus valores PKEY.</span><span class="sxs-lookup"><span data-stu-id="84b7d-165">Before looking at the implementation of **\_LoadProperties**, you should understand the **PropertyMap** array used in the sample to map properties in the XML document to existing properties in the property system through their PKEY values.</span></span>

<span data-ttu-id="84b7d-166">No debe exponer todos los elementos y atributos del archivo XML como una propiedad.</span><span class="sxs-lookup"><span data-stu-id="84b7d-166">You should not expose every element and attribute in the XML file as a property.</span></span> <span data-ttu-id="84b7d-167">En su lugar, seleccione solo aquellos que cree que serán útiles para los usuarios finales de la organización de sus documentos (en este caso, recetas).</span><span class="sxs-lookup"><span data-stu-id="84b7d-167">Instead, select only those that you believe will be useful to end users in the organization of their documents (in this case, recipes).</span></span> <span data-ttu-id="84b7d-168">Este es un concepto importante que hay que tener en cuenta al desarrollar los controladores de propiedades: la diferencia entre la información que es realmente útil para los escenarios de la organización y la información que pertenece a los detalles del archivo y se puede ver abriendo el propio archivo.</span><span class="sxs-lookup"><span data-stu-id="84b7d-168">This is an important concept to keep in mind as you develop your property handlers: the difference between information that is truly useful for organizational scenarios, and information that belongs to the details of your file and can be seen by opening the file itself.</span></span> <span data-ttu-id="84b7d-169">Las propiedades no pretenden ser una duplicación completa de un archivo XML.</span><span class="sxs-lookup"><span data-stu-id="84b7d-169">Properties are not intended to be a full duplication of an XML file.</span></span>


```
PropertyMap c_rgPropertyMap[] =
{
{ L"Recipe/Title", PKEY_Title, 
                   VT_LPWSTR, 
                   NULL, 
                   PKEY_Null },
{ L"Recipe/Comments", PKEY_Comment, 
                      VT_LPWSTR, 
                      NULL, 
                      PKEY_Null },
{ L"Recipe/Background", PKEY_Author, 
                        VT_VECTOR | VT_LPWSTR, 
                        L"Author", 
                        PKEY_Null },
{ L"Recipe/RecipeKeywords", PKEY_Keywords, 
                            VT_VECTOR | VT_LPWSTR, 
                            L"Keyword", 
                            PKEY_KeywordCount },
};
```



<span data-ttu-id="84b7d-170">Esta es la implementación completa del método **\_ LoadProperties** llamado por [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span><span class="sxs-lookup"><span data-stu-id="84b7d-170">Here is the full implementation of the **\_LoadProperties** method called by [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span></span>


```
HRESULT CRecipePropertyStore::_LoadProperties()
{
    HRESULT hr = E_FAIL;    
    
    if (_spCache)
    {
        hr = <mark type="const">S_OK</mark>;
    }
    else
    {
        // Create the in-memory property store.
        hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&_spCache));
    
        if (SUCCEEDED(hr))
        {
            // Cycle through each mapped property.
            for (UINT i = 0; i < ARRAYSIZE(c_rgPropertyMap); ++i)
            {
                _LoadProperty(c_rgPropertyMap[i]);
            }
    
            _LoadExtendedProperties();
            _LoadSearchContent();
        }
    }
    return hr;
}
```



<span data-ttu-id="84b7d-171">El método **\_ LoadProperties** llama a la función auxiliar de Shell [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) para crear un almacén de propiedades en memoria (caché) para las propiedades controladas.</span><span class="sxs-lookup"><span data-stu-id="84b7d-171">The **\_LoadProperties** method calls the Shell helper function [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create an in-memory property store (cache) for the handled properties.</span></span> <span data-ttu-id="84b7d-172">Mediante el uso de una memoria caché, se realiza un seguimiento de los cambios.</span><span class="sxs-lookup"><span data-stu-id="84b7d-172">By using a cache, changes are tracked for you.</span></span> <span data-ttu-id="84b7d-173">Esto le libera del seguimiento de si se ha cambiado un valor de propiedad en la memoria caché, pero aún no se ha guardado en el almacenamiento persistente.</span><span class="sxs-lookup"><span data-stu-id="84b7d-173">This frees you from tracking whether a property value has been changed in the cache but not yet saved to persisted storage.</span></span> <span data-ttu-id="84b7d-174">También le libera de la persistencia innecesaria de valores de propiedad que no han cambiado.</span><span class="sxs-lookup"><span data-stu-id="84b7d-174">It also frees you from needlessly persisting property values that have not changed.</span></span>

<span data-ttu-id="84b7d-175">El método **\_ LoadProperties** también llama a **\_ LoadProperty** cuya implementación se muestra en el código siguiente) una vez para cada propiedad asignada.</span><span class="sxs-lookup"><span data-stu-id="84b7d-175">The **\_LoadProperties** method also calls **\_LoadProperty** whose implementation is illustrated in the following code) once for each mapped property.</span></span> <span data-ttu-id="84b7d-176">**\_ LoadProperty** obtiene el valor de la propiedad tal y como se especifica en el elemento **PROPERTYMAP** de la secuencia XML y lo asigna a la memoria caché en memoria a través de una llamada a [**IPropertyStoreCache:: SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate).</span><span class="sxs-lookup"><span data-stu-id="84b7d-176">**\_LoadProperty** gets the value of the property as specified in the **PropertyMap** element in the XML stream and assigns it to the in-memory cache through a call to [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate).</span></span> <span data-ttu-id="84b7d-177">La \_ marca de PSC normal en la llamada a **IPropertyStoreCache:: SetValueAndState** indica que el valor de propiedad no se ha modificado desde el momento en que entró en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="84b7d-177">The PSC\_NORMAL flag in the call to **IPropertyStoreCache::SetValueAndState** indicates that the property value has not been altered since the time it entered the cache.</span></span>


```
HRESULT CRecipePropertyStore::_LoadProperty(PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    
    MSXML2::IXMLDOMNodePtr spXmlNode(_spDomDoc->selectSingleNode(map.pszXPath));
    if (spXmlNode)
    {
        PROPVARIANT propvar = { 0 };
        propvar.vt = map.vt;
        
        if (map.vt == (VT_VECTOR | VT_LPWSTR))
        {
            hr = _LoadVectorProperty(spXmlNode, &propvar, map);
        }
        else
        {
            // If there is no value, set to VT_EMPTY to indicate
            // that it is not there. Do not return failure.
            if (spXmlNode->text.length() == 0)
            {
                propvar.vt = VT_EMPTY;
                hr = <mark type="const">S_OK</mark>;
            }
            else
            {
                // SimplePropVariantFromString is a helper function.
                // particular to the sample. It is found in Util.cpp.
                hr = SimplePropVariantFromString(spXmlNode->text, &propvar);
            }
        }
    
        if (S_OK == hr)
        {
            hr = _spCache->SetValueAndState(map.key, &propvar, PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    return hr;
}
```



## <a name="dealing-with-propvariant-based-values"></a><span data-ttu-id="84b7d-178">Trabajar con PROPVARIANT-Based valores</span><span class="sxs-lookup"><span data-stu-id="84b7d-178">Dealing with PROPVARIANT-Based Values</span></span>

<span data-ttu-id="84b7d-179">En la implementación de **\_ LoadProperty**, se proporciona un valor de propiedad en forma de [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="84b7d-179">In the implementation of **\_LoadProperty**, a property value is provided in the form of a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="84b7d-180">Se proporciona un conjunto de API en el kit de desarrollo de software (SDK) para convertir tipos primitivos como **PWSTR** o **int** a o desde tipos **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="84b7d-180">A set of APIs in the software development kit (SDK) is provided to convert from primitive types such as **PWSTR** or **int** to or from **PROPVARIANT** types.</span></span> <span data-ttu-id="84b7d-181">Estas API se encuentran en Propvarutil. h.</span><span class="sxs-lookup"><span data-stu-id="84b7d-181">These APIs are found in Propvarutil.h.</span></span>

<span data-ttu-id="84b7d-182">Por ejemplo, para convertir un [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en una cadena, puede usar [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="84b7d-182">For example, to convert a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to a string, you can use [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) as illustrated here.</span></span>


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



<span data-ttu-id="84b7d-183">Para inicializar un PROPVARIANT de una cadena, puede usar [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).</span><span class="sxs-lookup"><span data-stu-id="84b7d-183">To initialize a PROPVARIANT from a string, you can use [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).</span></span>


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



<span data-ttu-id="84b7d-184">Como puede ver en cualquiera de los archivos de recetas incluidos en el ejemplo, puede haber más de una palabra clave en cada archivo.</span><span class="sxs-lookup"><span data-stu-id="84b7d-184">As you can see in any of the recipe files included in the sample, there can be more than one keyword in each file.</span></span> <span data-ttu-id="84b7d-185">Para tener en cuenta esto, el sistema de propiedades admite cadenas de varios valores que se representan como un vector de cadenas (por ejemplo, "VT \_ Vector \| VT \_ LPWStr").</span><span class="sxs-lookup"><span data-stu-id="84b7d-185">To account for this, the property system supports multi-valued strings represented as a vector of strings (for instance "VT\_VECTOR \| VT\_LPWSTR").</span></span> <span data-ttu-id="84b7d-186">El método **\_ LoadVectorProperty** del ejemplo utiliza valores basados en vectores.</span><span class="sxs-lookup"><span data-stu-id="84b7d-186">The **\_LoadVectorProperty** method in the example uses vector-based values.</span></span>


```
HRESULT CRecipePropertyStore::_LoadVectorProperty
                                (MSXML2::IXMLDOMNode *pNodeParent,
                                 PROPVARIANT *ppropvar,
                                 struct PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = pNodeParent->selectNodes(map.pszSubNodeName);
    
    if (spList)
    {
        UINT cElems = spList->length;
        ppropvar->calpwstr.cElems = cElems;
        ppropvar->calpwstr.pElems = (PWSTR*)CoTaskMemAlloc(sizeof(PWSTR)*cElems);
    
        if (ppropvar->calpwstr.pElems)
        {
            for (UINT i = 0; (SUCCEEDED(hr) && i < cElems); ++i)
            {
                hr = SHStrDup(spList->item[i]->text, 
                              &(ppropvar->calpwstr.pElems[i]));
            }
    
            if (SUCCEEDED(hr))
            {
                if (!IsEqualPropertyKey(map.keyCount, PKEY_Null))
                {
                    PROPVARIANT propvarCount = { VT_UI4 };
                    propvarCount.uintVal = cElems;
                    
                    _spCache->SetValueAndState(map.keyCount,
                                               &propvarCount, 
                                               PSC_NORMAL);
                }
            }
            else
            {
                PropVariantClear(ppropvar);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    
    return hr;
}
```



<span data-ttu-id="84b7d-187">Si un valor no existe en el archivo, no devuelva un error.</span><span class="sxs-lookup"><span data-stu-id="84b7d-187">If a value does not exist in the file, do not return an error.</span></span> <span data-ttu-id="84b7d-188">En su lugar, establezca el valor en VT \_ vacío y devuelva los valores **\_ correctos**.</span><span class="sxs-lookup"><span data-stu-id="84b7d-188">Instead, set the value to VT\_EMPTY and return **S\_OK**.</span></span> <span data-ttu-id="84b7d-189">VT \_ vacío indica que el valor de la propiedad no existe.</span><span class="sxs-lookup"><span data-stu-id="84b7d-189">VT\_EMPTY indicates that the property value does not exist.</span></span>

## <a name="supporting-open-metadata"></a><span data-ttu-id="84b7d-190">Compatibilidad con metadatos abiertos</span><span class="sxs-lookup"><span data-stu-id="84b7d-190">Supporting Open Metadata</span></span>

<span data-ttu-id="84b7d-191">En este ejemplo se usa un formato de archivo basado en XML.</span><span class="sxs-lookup"><span data-stu-id="84b7d-191">This example uses an XML-based file format.</span></span> <span data-ttu-id="84b7d-192">Su esquema se puede extender para admitir propiedades que no se han considerado durante developmet, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="84b7d-192">Its schema can be extended to support properties that were not thought of during developmet, for example.</span></span> <span data-ttu-id="84b7d-193">Este sistema se conoce como metadatos abiertos.</span><span class="sxs-lookup"><span data-stu-id="84b7d-193">This system is known as open metadata.</span></span> <span data-ttu-id="84b7d-194">En este ejemplo se amplía el sistema de propiedades mediante la creación de un nodo bajo el elemento **Recipe** denominado **ExtendedProperties**, como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="84b7d-194">This example extends the property system by creating a node under the **Recipe** element called **ExtendedProperties**, as illustrated in the following code example.</span></span>


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



<span data-ttu-id="84b7d-195">Para cargar propiedades extendidas persistentes durante la inicialización, implemente el método **\_ LoadExtendedProperties** , como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="84b7d-195">To load persisted extended properties during initialization, implement the **\_LoadExtendedProperties** method, as illustrated in the following code example.</span></span>


```
HRESULT CRecipePropertyStore::_LoadExtendedProperties()
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = 
                  _spDomDoc->selectNodes(L"Recipe/ExtendedProperties/Property");
    
    if (spList)
    {
        UINT cElems = spList->length;
        
        for (UINT i = 0; i < cElems; ++i)
        {
            MSXML2::IXMLDOMElementPtr spElement;
            
            if (SUCCEEDED(spList->item[i]->QueryInterface(IID_PPV_ARGS(&spElement))))
            {
                PROPERTYKEY key;
                _bstr_t bstrPropName = spElement->getAttribute(L"Name").bstrVal;
    
                if (!!bstrPropName &&
                    (SUCCEEDED(PropertyKeyFromString(bstrPropName, &key))))
                {
                    PROPVARIANT propvar = { 0 };
                    _bstr_t bstrEncodedValue = 
                               spElement->getAttribute(L"EncodedValue").bstrVal;
                   
                    if (!!bstrEncodedValue)
                    {
                        // DeserializePropVariantFromString is a helper function
                        // particular to the sample. It is found in Util.cpp.
                        hr = DeserializePropVariantFromString(bstrEncodedValue, 
                                                              &propvar);
                    }
```



<span data-ttu-id="84b7d-196">Las API de serialización declaradas en propsys. h se utilizan para serializar y deserializar los tipos de [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en blobs de datos y, a continuación, se usa la codificación base64 para serializar esos blobs en cadenas que se pueden guardar en el XML.</span><span class="sxs-lookup"><span data-stu-id="84b7d-196">Serialization APIs declared in Propsys.h are used to serialize and deserialize [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) types into blobs of data, and then Base64 encoding is used to serialize those blobs into strings that can be saved in the XML.</span></span> <span data-ttu-id="84b7d-197">Estas cadenas se almacenan en el atributo **EncodedValue** del elemento **ExtendedProperties** .</span><span class="sxs-lookup"><span data-stu-id="84b7d-197">These strings are stored in the **EncodedValue** attribute of the **ExtendedProperties** element.</span></span> <span data-ttu-id="84b7d-198">El siguiente método de utilidad, implementado en el archivo util. cpp del ejemplo, realiza la serialización.</span><span class="sxs-lookup"><span data-stu-id="84b7d-198">The following utility method, implemented in the sample's Util.cpp file, performs the serialization.</span></span> <span data-ttu-id="84b7d-199">Comienza con una llamada a la función [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) para realizar la serialización binaria, como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="84b7d-199">It begins with a call to the [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) function to perform the binary serialization, as illustrated in the following code example.</span></span>


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



<span data-ttu-id="84b7d-200">A continuación, la función [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa), declarada en Wincrypt. h, realiza la conversión Base64.</span><span class="sxs-lookup"><span data-stu-id="84b7d-200">Next, the [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)Â function, declared in Wincrypt.h, performs the Base64 conversion.</span></span>


```
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        DWORD cchString;
        
        if (CryptBinaryToString((BYTE *)pBlob, 
                                cbBlob,
                                CRYPT_STRING_BASE64, 
                                NULL, 
                                &cchString))
        {
            *pszOut = (PWSTR)CoTaskMemAlloc(sizeof(WCHAR) *cchString);
    
            if (*pszOut)
            {
                if (CryptBinaryToString((BYTE *)pBlob, 
                                         cbBlob,
                                         CRYPT_STRING_BASE64,
                                         *pszOut, 
                                         &cchString))
                {
                    hr = <mark type="const">S_OK</mark>;
                }
                else
                {
                    CoTaskMemFree(*pszOut);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
    }
    
    return <mark type="const">S_OK</mark>;}
```



<span data-ttu-id="84b7d-201">La función **DeserializePropVariantFromString** , que también se encuentra en util. cpp, invierte la operación y deserializa los valores del archivo XML.</span><span class="sxs-lookup"><span data-stu-id="84b7d-201">The **DeserializePropVariantFromString** function, also found in Util.cpp, reverses the operation, deserializing values from the XML file.</span></span>

<span data-ttu-id="84b7d-202">Para obtener información sobre la compatibilidad con los metadatos abiertos, vea "tipos de archivo que admiten metadatos abiertos" en [tipos de archivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="84b7d-202">For information about support for open metadata, see "File Types that Support Open Metadata" in [File Types](../shell/fa-file-types.md).</span></span>

## <a name="full-text-contents"></a><span data-ttu-id="84b7d-203">Contenido de Full-Text</span><span class="sxs-lookup"><span data-stu-id="84b7d-203">Full-Text Contents</span></span>

<span data-ttu-id="84b7d-204">Los controladores de propiedades también pueden facilitar una búsqueda de texto completo del contenido del archivo, y son una manera sencilla de proporcionar esa funcionalidad si el formato del archivo no es demasiado complicado.</span><span class="sxs-lookup"><span data-stu-id="84b7d-204">Property handlers can also facilitate a full-text search of the file contents, and they are an easy way to provide that functionality if the file format is not overly complicated.</span></span> <span data-ttu-id="84b7d-205">Existe una forma alternativa y más eficaz de proporcionar el texto completo del archivo a través de la implementación de la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="84b7d-205">There is an alternative, more powerful way to provide the full text of the file through the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface implementation.</span></span>

<span data-ttu-id="84b7d-206">En la tabla siguiente se resumen las ventajas de cada enfoque mediante [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) o [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="84b7d-206">The following table summarizes the benefits of each approach using either [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) or [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>



| <span data-ttu-id="84b7d-207">Capacidad</span><span class="sxs-lookup"><span data-stu-id="84b7d-207">Capability</span></span>                                   | <span data-ttu-id="84b7d-208">Imaging</span><span class="sxs-lookup"><span data-stu-id="84b7d-208">IFilter</span></span>                      | <span data-ttu-id="84b7d-209">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="84b7d-209">IPropertyStore</span></span> |
|----------------------------------------------|------------------------------|----------------|
| <span data-ttu-id="84b7d-210">¿Permite la escritura de datos en archivos?</span><span class="sxs-lookup"><span data-stu-id="84b7d-210">Allows write back to files?</span></span>                  | <span data-ttu-id="84b7d-211">No</span><span class="sxs-lookup"><span data-stu-id="84b7d-211">No</span></span>                           | <span data-ttu-id="84b7d-212">Sí</span><span class="sxs-lookup"><span data-stu-id="84b7d-212">Yes</span></span>            |
| <span data-ttu-id="84b7d-213">¿Proporciona una combinación de contenido y propiedades?</span><span class="sxs-lookup"><span data-stu-id="84b7d-213">Provides mix of content and properties?</span></span>      | <span data-ttu-id="84b7d-214">Sí</span><span class="sxs-lookup"><span data-stu-id="84b7d-214">Yes</span></span>                          | <span data-ttu-id="84b7d-215">Sí</span><span class="sxs-lookup"><span data-stu-id="84b7d-215">Yes</span></span>            |
| <span data-ttu-id="84b7d-216">Entornos?</span><span class="sxs-lookup"><span data-stu-id="84b7d-216">Multilingual?</span></span>                                | <span data-ttu-id="84b7d-217">Sí</span><span class="sxs-lookup"><span data-stu-id="84b7d-217">Yes</span></span>                          | <span data-ttu-id="84b7d-218">No</span><span class="sxs-lookup"><span data-stu-id="84b7d-218">No</span></span>             |
| <span data-ttu-id="84b7d-219">¿MIME/Embedded?</span><span class="sxs-lookup"><span data-stu-id="84b7d-219">MIME/Embedded?</span></span>                               | <span data-ttu-id="84b7d-220">Sí</span><span class="sxs-lookup"><span data-stu-id="84b7d-220">Yes</span></span>                          | <span data-ttu-id="84b7d-221">No</span><span class="sxs-lookup"><span data-stu-id="84b7d-221">No</span></span>             |
| <span data-ttu-id="84b7d-222">¿Límites de texto?</span><span class="sxs-lookup"><span data-stu-id="84b7d-222">Text boundaries?</span></span>                             | <span data-ttu-id="84b7d-223">Oración, párrafo, capítulo</span><span class="sxs-lookup"><span data-stu-id="84b7d-223">Sentence, paragraph, chapter</span></span> | <span data-ttu-id="84b7d-224">None</span><span class="sxs-lookup"><span data-stu-id="84b7d-224">None</span></span>           |
| <span data-ttu-id="84b7d-225">¿La implementación es compatible con SP/SQL Server?</span><span class="sxs-lookup"><span data-stu-id="84b7d-225">Implementation supported for SPS/SQL Server?</span></span> | <span data-ttu-id="84b7d-226">Sí</span><span class="sxs-lookup"><span data-stu-id="84b7d-226">Yes</span></span>                          | <span data-ttu-id="84b7d-227">No</span><span class="sxs-lookup"><span data-stu-id="84b7d-227">No</span></span>             |
| <span data-ttu-id="84b7d-228">Implementación</span><span class="sxs-lookup"><span data-stu-id="84b7d-228">Implementation</span></span>                               | <span data-ttu-id="84b7d-229">Complex</span><span class="sxs-lookup"><span data-stu-id="84b7d-229">Complex</span></span>                      | <span data-ttu-id="84b7d-230">Simple</span><span class="sxs-lookup"><span data-stu-id="84b7d-230">Simple</span></span>         |



 

<span data-ttu-id="84b7d-231">En el ejemplo de controlador de recetas, el formato de archivo receta no tiene ningún requisito complejo, por lo que solo se ha implementado [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para la compatibilidad de texto completo.</span><span class="sxs-lookup"><span data-stu-id="84b7d-231">In the recipe handler sample, the recipe file format does not have any complex requirements, so only [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) has been implemented for full-text support.</span></span> <span data-ttu-id="84b7d-232">La búsqueda de texto completo se implementa para los nodos XML nombrados en la matriz siguiente.</span><span class="sxs-lookup"><span data-stu-id="84b7d-232">Full-text search is implemented for the XML nodes named in the following array.</span></span>


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



<span data-ttu-id="84b7d-233">El sistema de propiedades contiene la `System.Search.Contents` propiedad (contenido de búsqueda de PKEY \_ \_ ), que se creó para proporcionar contenido de texto completo al indexador.</span><span class="sxs-lookup"><span data-stu-id="84b7d-233">The property system contains the `System.Search.Contents` (PKEY\_Search\_Contents) property, which was created to provide full-text content to the indexer.</span></span> <span data-ttu-id="84b7d-234">El valor de esta propiedad nunca se muestra directamente en la interfaz de usuario; el texto de todos los nodos XML nombrados en la matriz anterior se concatena en una sola cadena.</span><span class="sxs-lookup"><span data-stu-id="84b7d-234">This property's value is never displayed directly in the UI; the text from all of the XML nodes named in the array above are concatenated into a single string.</span></span> <span data-ttu-id="84b7d-235">A continuación, esa cadena se proporciona al indexador como el contenido de texto completo del archivo receta a través de una llamada a [**IPropertyStoreCache:: SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="84b7d-235">That string is then provided to the indexer as the full-text content of the recipe file through a call to [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) as illustrated in the following code example.</span></span>


```
HRESULT CRecipePropertyStore::_LoadSearchContent()
{
    HRESULT hr = S_FALSE;
    _bstr_t bstrContent;
    
    for (UINT i = 0; i < ARRAYSIZE(c_rgszContentXPath); ++i)
    {
        MSXML2::IXMLDOMNodeListPtr spList = 
                                  _spDomDoc->selectNodes(c_rgszContentXPath[i]);
    
        if (spList)
        {
            UINT cElems = spList->length;
            
            for (UINT elt = 0; elt < cElems; ++elt)
            {
                bstrContent += L" ";
                bstrContent += spList->item[elt]->text;
            }
        }
    }
    
    if (bstrContent.length() > 0)
    {
        PROPVARIANT propvar = { VT_LPWSTR };
        hr = SHStrDup(bstrContent, &(propvar.pwszVal));
    
        if (SUCCEEDED(hr))
        {
            hr = _spCache->SetValueAndState(PKEY_Search_Contents, 
                                            &propvar, 
                                            PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    
    return hr;}
```



## <a name="providing-values-for-properties"></a><span data-ttu-id="84b7d-236">Proporcionar valores para las propiedades</span><span class="sxs-lookup"><span data-stu-id="84b7d-236">Providing Values for Properties</span></span>

<span data-ttu-id="84b7d-237">Cuando se usa para leer valores, normalmente se invocan los controladores de propiedades por una de las razones siguientes:</span><span class="sxs-lookup"><span data-stu-id="84b7d-237">When used to read values, property handlers are usually invoked for one of the following reasons:</span></span>

-   <span data-ttu-id="84b7d-238">Para enumerar todos los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="84b7d-238">To enumerate all property values.</span></span>
-   <span data-ttu-id="84b7d-239">Para obtener el valor de una propiedad específica.</span><span class="sxs-lookup"><span data-stu-id="84b7d-239">To get the value of a specific property.</span></span>

<span data-ttu-id="84b7d-240">Para la enumeración, se pide a un controlador de propiedades que Enumere sus propiedades durante la indización o cuando el cuadro de diálogo Propiedades pida que se muestren las propiedades en el **otro** grupo.</span><span class="sxs-lookup"><span data-stu-id="84b7d-240">For enumeration, a property handler is asked to enumerate its properties either during indexing or when the properties dialog box asks for properties to display in the **Other** group.</span></span> <span data-ttu-id="84b7d-241">La indexación se activa constantemente como una operación en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="84b7d-241">Indexing goes on constantly as a background operation.</span></span> <span data-ttu-id="84b7d-242">Cada vez que un archivo cambia, se notifica al indexador y vuelve a indizar el archivo pidiendo al controlador de propiedades que Enumere sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="84b7d-242">Whenever a file changes, the indexer is notified, and it re-indexes the file by asking the property handler to enumerate its properties.</span></span> <span data-ttu-id="84b7d-243">Por lo tanto, es fundamental que los controladores de propiedades se implementen de manera eficaz y devuelvan los valores de propiedad lo más rápido posible.</span><span class="sxs-lookup"><span data-stu-id="84b7d-243">Therefore, it is critical that property handlers are implemented efficiently and return property values as quickly as possible.</span></span> <span data-ttu-id="84b7d-244">Enumere todas las propiedades para las que tiene valores, del mismo modo que lo haría para cualquier colección, pero no enumere las propiedades que impliquen cálculos de uso intensivo de memoria o solicitudes de red que podrían ralentizar la recuperación.</span><span class="sxs-lookup"><span data-stu-id="84b7d-244">Enumerate all the properties for which you have values, just as you would for any collection, but do not enumerate properties that involve memory-intensive calculations or network requests that could make them slow to retrieve.</span></span>

<span data-ttu-id="84b7d-245">Al escribir un controlador de propiedades, normalmente es necesario tener en cuenta los dos conjuntos de propiedades siguientes.</span><span class="sxs-lookup"><span data-stu-id="84b7d-245">When writing a property handler, you usually need to consider the following two sets of properties.</span></span>

-   <span data-ttu-id="84b7d-246">Propiedades principales: propiedades que el tipo de archivo admite de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="84b7d-246">Primary properties: Properties that your file type supports natively.</span></span> <span data-ttu-id="84b7d-247">Por ejemplo, un controlador de propiedades de fotografía para metadatos de archivo de imagen intercambiable (EXIF) es compatible de forma nativa con `System.Photo.FNumber` .</span><span class="sxs-lookup"><span data-stu-id="84b7d-247">For example, a photo property handler for Exchangeable Image File (EXIF) metadata natively supports `System.Photo.FNumber`.</span></span>
-   <span data-ttu-id="84b7d-248">Propiedades extendidas: propiedades que admite el tipo de archivo como parte de los metadatos abiertos.</span><span class="sxs-lookup"><span data-stu-id="84b7d-248">Extended properties: Properties that your file type supports as part of open metadata.</span></span>

<span data-ttu-id="84b7d-249">Dado que el ejemplo usa la memoria caché en memoria, la implementación de métodos [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) es simplemente una cuestión de delegar en esa caché, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="84b7d-249">Because the sample uses in-memory cache, implementing [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) methods is just a matter of delegating to that cache, as illustrated in the following code example.</span></span>


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



<span data-ttu-id="84b7d-250">Si decide no delegar en la memoria caché en memoria, debe implementar los métodos para proporcionar> el siguiente comportamiento esperado:</span><span class="sxs-lookup"><span data-stu-id="84b7d-250">If you choose not to delegate to the in-memory cache, you must implement your methods to provide> the following expected behavior:</span></span>

-   <span data-ttu-id="84b7d-251">[**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): Si no hay ninguna propiedad, este método devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="84b7d-251">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): If there are no properties, this method returns **S\_OK**.</span></span>
-   <span data-ttu-id="84b7d-252">[**IPropertyStore:: getatt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): Si *iProp* es mayor o igual que *CProps*, este método devuelve e \_ INVALIDARG y la estructura a la que apunta el parámetro *PKEY* se rellena con ceros.</span><span class="sxs-lookup"><span data-stu-id="84b7d-252">[**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): If *iProp* is greater than or equal to *cProps*, this method returns E\_INVALIDARG and the structure pointed to by the *pkey* parameter is filled with zeroes.</span></span>
-   <span data-ttu-id="84b7d-253">[**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) y [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) reflejan el estado actual del controlador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="84b7d-253">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) and [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) reflect the current state of the property handler.</span></span> <span data-ttu-id="84b7d-254">Si se agrega o se quita un [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) del archivo a través de [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), estos dos métodos deben reflejar ese cambio la próxima vez que se llamen.</span><span class="sxs-lookup"><span data-stu-id="84b7d-254">If a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) is added to or removed from the file through [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), these two methods must reflect that change the next time they are called.</span></span>
-   <span data-ttu-id="84b7d-255">[**IPropertyStore:: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): si se solicita a este método un valor que no existe, devuelve **S \_ OK** con el valor que se indica como VT \_ vacío.</span><span class="sxs-lookup"><span data-stu-id="84b7d-255">[**IPropertyStore::GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): If this method is asked for a value that does not exist, it returns **S\_OK** with the value reported as VT\_EMPTY.</span></span>

## <a name="writing-back-values"></a><span data-ttu-id="84b7d-256">Escribir valores hacia atrás</span><span class="sxs-lookup"><span data-stu-id="84b7d-256">Writing Back Values</span></span>

<span data-ttu-id="84b7d-257">Cuando el controlador de propiedades escribe el valor de una propiedad mediante [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), no escribe el valor en el archivo hasta que se llama a [**IPropertyStore:: commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="84b7d-257">When the property handler writes the value of a property using [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), it does not write the value to the file until [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) is called.</span></span> <span data-ttu-id="84b7d-258">La caché en memoria puede ser útil para implementar este esquema.</span><span class="sxs-lookup"><span data-stu-id="84b7d-258">The in-memory cache can be useful in implementing this scheme.</span></span> <span data-ttu-id="84b7d-259">En el código de ejemplo, la implementación **IPropertyStore:: SetValue** simplemente establece el nuevo valor en la memoria caché en memoria y establece el estado de esa propiedad en PSC \_ sucio.</span><span class="sxs-lookup"><span data-stu-id="84b7d-259">In the sample code the **IPropertyStore::SetValue** implementation simply sets the new value in the in-memory cache and sets the state of that property to PSC\_DIRTY.</span></span>


```
HRESULT CRecipePropertyStore::SetValue(REFPROPERTYKEY key, const PROPVARIANT *pPropVar)
    {
    
    HRESULT hr = E_FAIL;
    
    if (IsEqualPropertyKey(key, PKEY_Search_Contents))
    {
        // This property is read-only
        hr = HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED);  
    }
    else
    {
        hr = _spCache->SetValueAndState(key, pPropVar, PSC_DIRTY);
    }
    
    return hr;
}
```



<span data-ttu-id="84b7d-260">En cualquier implementación de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , se espera el siguiente comportamiento de [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="84b7d-260">In any [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) implementation, the following behavior is expected from [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):</span></span>

-   <span data-ttu-id="84b7d-261">Si la propiedad ya existe, se establece el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="84b7d-261">If the property already exists, the value of the property is set.</span></span>
-   <span data-ttu-id="84b7d-262">Si la propiedad no existe, se agrega la nueva propiedad y se establece su valor.</span><span class="sxs-lookup"><span data-stu-id="84b7d-262">If the property does not exist, the new property is added and its value set.</span></span>
-   <span data-ttu-id="84b7d-263">Si el valor de la propiedad no se puede conservar con la misma precisión que se indica (por ejemplo, truncamiento debido a las limitaciones de tamaño en el formato de archivo), el valor se establece en la medida de lo posible y se devuelve la InPlace \_ S \_ truncada.</span><span class="sxs-lookup"><span data-stu-id="84b7d-263">If the property value cannot be persisted at the same accuracy as given (for instance, truncation due to size limitations in the file format), the value is set as far as possible and INPLACE\_S\_TRUNCATED is returned.</span></span>
-   <span data-ttu-id="84b7d-264">Si el controlador de propiedad no admite la propiedad, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` se devuelve.</span><span class="sxs-lookup"><span data-stu-id="84b7d-264">If the property is not supported by the property handler, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` is returned.</span></span>
-   <span data-ttu-id="84b7d-265">Si hay otro motivo por el que no se puede establecer el valor de la propiedad, como el archivo que se está bloqueando o la falta de derechos de edición a través de las listas de control de acceso (ACL), \_ \_ se devuelve STG E ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="84b7d-265">If there is another reason that the property value cannot be set, such as the file being locked or lack of rights to edit through access control lists (ACLs), then STG\_E\_ACCESSDENIED is returned.</span></span>

<span data-ttu-id="84b7d-266">Una ventaja importante del uso de secuencias, como el ejemplo, es la confiabilidad.</span><span class="sxs-lookup"><span data-stu-id="84b7d-266">One major advantage of using streams, as the sample, is reliability.</span></span> <span data-ttu-id="84b7d-267">Los controladores de propiedades siempre deben tener en cuenta que no pueden dejar un archivo en un estado incoherente en caso de que se produzca un error catastrófico.</span><span class="sxs-lookup"><span data-stu-id="84b7d-267">Property handlers must always consider that they cannot leave a file in an inconsistent state in the case of a catastrophic failure.</span></span> <span data-ttu-id="84b7d-268">Obviamente, se deben evitar los daños en los archivos de un usuario y la mejor manera de hacerlo es con un mecanismo de "copia en escritura".</span><span class="sxs-lookup"><span data-stu-id="84b7d-268">Corrupting a user's files obviously should be avoided, and the best way to do this is with a "copy-on-write" mechanism.</span></span> <span data-ttu-id="84b7d-269">Si el controlador de propiedad usa una secuencia para tener acceso a un archivo, este comportamiento se obtiene automáticamente. el sistema escribe cualquier cambio en la secuencia, reemplazando el archivo con la nueva copia solo durante la operación de confirmación.</span><span class="sxs-lookup"><span data-stu-id="84b7d-269">If your property handler uses a stream to access a file, you get this behavior automatically; the system writes any changes to the stream, replacing the file with the new copy only during the commit operation.</span></span>

<span data-ttu-id="84b7d-270">Para invalidar este comportamiento y controlar el proceso de guardado de archivos manualmente, puede dejar de participar en el comportamiento de guardado seguro estableciendo el valor de ManualSafeSave en la entrada del registro del controlador, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="84b7d-270">To override this behavior and control the file saving process manually, you can opt out of the safe save behavior by setting the ManualSafeSave value in your handler's registry entry as illustrated here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

<span data-ttu-id="84b7d-271">Cuando un controlador especifica el valor de ManualSafeSave, la secuencia con la que se inicializa no es una secuencia de transacción (STGM \_ ).</span><span class="sxs-lookup"><span data-stu-id="84b7d-271">When a handler specifies the ManualSafeSave value, the stream with which it is initialized is not a transacted stream (STGM\_TRANSACTED).</span></span> <span data-ttu-id="84b7d-272">El propio controlador debe implementar la función Safe Save para asegurarse de que el archivo no esté dañado si se interrumpe la operación de guardar.</span><span class="sxs-lookup"><span data-stu-id="84b7d-272">The handler itself must implement the safe save function to ensure that the file is not corrupted if the save operation is interrupted.</span></span> <span data-ttu-id="84b7d-273">Si el controlador implementa la escritura en contexto, se escribirá en la secuencia que se proporciona.</span><span class="sxs-lookup"><span data-stu-id="84b7d-273">If the handler implements in-place writing, it will write to the stream that it is given.</span></span> <span data-ttu-id="84b7d-274">Si el controlador no admite esta característica, debe recuperar una secuencia con la que escribir la copia actualizada del archivo mediante [**IDestinationStreamFactory:: GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream).</span><span class="sxs-lookup"><span data-stu-id="84b7d-274">If the handler does not support this feature, then it must retrieve a stream with which to write the updated copy of the file using [**IDestinationStreamFactory::GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream).</span></span> <span data-ttu-id="84b7d-275">Una vez que el controlador ha terminado de escribir, debe llamar a [**IPropertyStore:: commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) en el flujo original para completar la operación y reemplazar el contenido de la secuencia original con la nueva copia del archivo.</span><span class="sxs-lookup"><span data-stu-id="84b7d-275">After the handler is done writing, it should call [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) on the original stream to complete the operation, and replace the contents of the original stream with the new copy of the file.</span></span>

<span data-ttu-id="84b7d-276">ManualSafeSave es también la situación predeterminada si no inicializa el controlador con una secuencia.</span><span class="sxs-lookup"><span data-stu-id="84b7d-276">ManualSafeSave is also the default situation if you do not initialize your handler with a stream.</span></span> <span data-ttu-id="84b7d-277">Sin un flujo original para recibir el contenido de la secuencia temporal, debe utilizar [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) para realizar una sustitución atómica del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="84b7d-277">Without an original stream to receive the contents of the temporary stream, you must use [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) to perform an atomic replacement of the source file.</span></span>

<span data-ttu-id="84b7d-278">Los formatos de archivo de gran tamaño que se usarán de forma que generen archivos de más de 1 MB deben implementar la compatibilidad con la escritura de propiedades en contexto; de lo contrario, el comportamiento de rendimiento no cumple las expectativas de los clientes del sistema de propiedades.</span><span class="sxs-lookup"><span data-stu-id="84b7d-278">Large file formats that will be used in a way that produces files greater than 1 MB should implement support for in-place property writing; otherwise, the performance behavior does not meet the expectations of clients of the property system.</span></span> <span data-ttu-id="84b7d-279">En este escenario, el tiempo necesario para escribir propiedades no debe verse afectado por el tamaño del archivo.</span><span class="sxs-lookup"><span data-stu-id="84b7d-279">In this scenario, the time required to write properties should not be affected by the file size.</span></span>

<span data-ttu-id="84b7d-280">En el caso de archivos muy grandes, por ejemplo, un archivo de vídeo de 1 GB o más, se requiere una solución diferente.</span><span class="sxs-lookup"><span data-stu-id="84b7d-280">For very large files, for example a video file of 1 GB or more, a different solution is required.</span></span> <span data-ttu-id="84b7d-281">Si no hay espacio suficiente en el archivo para realizar la escritura en contexto, el controlador puede producir un error en la actualización de la propiedad si se ha agotado la cantidad de espacio reservado para la escritura de propiedades en contexto.</span><span class="sxs-lookup"><span data-stu-id="84b7d-281">If there is not enough space in the file to perform in-place writing, the handler may fail the property update if the amount of space reserved for in-place property writing has been exhausted.</span></span> <span data-ttu-id="84b7d-282">Este error se produce para evitar un bajo rendimiento derivado de 2 GB de e/s (1 para leer, 1 para escribir).</span><span class="sxs-lookup"><span data-stu-id="84b7d-282">This failure occurs to avoid poor performance arising from 2 GB of IO (1 to read, 1 to write).</span></span> <span data-ttu-id="84b7d-283">Debido a este posible error, estos formatos de archivo deben reservar suficiente espacio para la escritura de propiedades en contexto.</span><span class="sxs-lookup"><span data-stu-id="84b7d-283">Because of this potential failure, these file formats should reserve enough space for in-place property writing.</span></span>

<span data-ttu-id="84b7d-284">Si el archivo tiene espacio suficiente en el encabezado para escribir metadatos y la escritura de esos metadatos no hace que el archivo aumente o se reduzca, podría ser seguro escribir en contexto.</span><span class="sxs-lookup"><span data-stu-id="84b7d-284">If the file has enough space in its header to write metadata, and if the writing of that metadata does not cause the file to grow or shrink, it might be safe to write in-place.</span></span> <span data-ttu-id="84b7d-285">Se recomienda 64 KB como punto de partida.</span><span class="sxs-lookup"><span data-stu-id="84b7d-285">We recommend 64 KB as a starting point.</span></span> <span data-ttu-id="84b7d-286">Escribir en contexto es equivalente al controlador que solicita ManualSafeSave y llamar a [**IStream:: commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) en la implementación de [**IPropertyStore:: commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), y tiene un rendimiento mucho mejor que la copia en escritura.</span><span class="sxs-lookup"><span data-stu-id="84b7d-286">Writing in-place is equivalent to the handler asking for ManualSafeSave and calling [**IStream::Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) in the implementation of [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), and has much better performance than copy-on-write.</span></span> <span data-ttu-id="84b7d-287">Si cambia el tamaño del archivo debido a cambios en el valor de la propiedad, no se debe intentar escribir en contexto debido a la posibilidad de que un archivo esté dañado en caso de que se produzca una terminación anómala.</span><span class="sxs-lookup"><span data-stu-id="84b7d-287">If the file size changes due to property value changes, writing in-place should not be attempted because of the potential for a corrupted file in the event of an abnormal termination.</span></span>

> [!Note]  
> <span data-ttu-id="84b7d-288">Por motivos de rendimiento, se recomienda usar la opción ManualSafeSave con controladores de propiedades que trabajen con archivos de 100 KB o más.</span><span class="sxs-lookup"><span data-stu-id="84b7d-288">For performance reasons we recommend that the ManualSafeSave option be used with property handlers working with files that are 100 KB or larger.</span></span>

 

<span data-ttu-id="84b7d-289">Tal y como se muestra en la siguiente implementación de ejemplo de [**IPropertyStore:: commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), el controlador de ManualSafeSave se registra para ilustrar la opción de guardado Safe manual.</span><span class="sxs-lookup"><span data-stu-id="84b7d-289">As illustrated in the following sample implementation of [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), the handler for ManualSafeSave is registered to illustrate the manual safe save option.</span></span> <span data-ttu-id="84b7d-290">El método **\_ SaveCacheToDom** escribe los valores de propiedad almacenados en la memoria caché en memoria en el objeto XMLdocument.</span><span class="sxs-lookup"><span data-stu-id="84b7d-290">The **\_SaveCacheToDom** method writes the property values stored in the in-memory cache to the XMLdocument object.</span></span>


```
HRESULT CRecipePropertyStore::Commit()
{
    HRESULT hr = E_UNEXPECTED;
    if (_pCache)
    {
        // Check grfMode to ensure writes are allowed.
        hr = STG_E_ACCESSDENIED;
        if (_grfMode & STGM_READWRITE)
        {
            // Save the internal value cache to XML DOM object.
            hr = _SaveCacheToDom();
            if (SUCCEEDED(hr))
            {
                // Reset the output stream.
                LARGE_INTEGER liZero = {};
                hr = _pStream->Seek(liZero, STREAM_SEEK_SET, NULL);
```



<span data-ttu-id="84b7d-291">A continuación, pregunte si el especificada admite [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).</span><span class="sxs-lookup"><span data-stu-id="84b7d-291">Next, ask whether the pecified supports [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).</span></span>


```
                        if (SUCCEEDED(hr))
                        {
                            // Write the XML out to the temprorary stream and commit it.
                            VARIANT varStream = {};
                            varStream.vt = VT_UNKNOWN;
                            varStream.punkVal = pStreamCommit;
                            hr = _pDomDoc->save(varStream);
                            if (SUCCEEDED(hr))
                            {
                                hr = pStreamCommit->Commit(STGC_DEFAULT);_
```



<span data-ttu-id="84b7d-292">A continuación, confirme la secuencia original, que vuelve a escribir los datos en el archivo original de una manera segura.</span><span class="sxs-lookup"><span data-stu-id="84b7d-292">Next, commit the original stream, which writes the data back to the original file in a safe manner.</span></span>


```
                        if (SUCCEEDED(hr))
                                {
                                    // Commit the real output stream.
                                    _pStream->Commit(STGC_DEFAULT);
                                }
                            }

                            pStreamCommit->Release();
                        }

                        pSafeCommit->Release();
                    }
                }
            }
        }
    }
```



<span data-ttu-id="84b7d-293">A continuación, examine la implementación de **\_ SaveCacheToDom** .</span><span class="sxs-lookup"><span data-stu-id="84b7d-293">Then examine the **\_SaveCacheToDom** implementation.</span></span>


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



<span data-ttu-id="84b7d-294">A continuación, obtenga el número de propiedades almacenadas en la memoria caché en memoria.</span><span class="sxs-lookup"><span data-stu-id="84b7d-294">Next, get the number of properties stored in the in-memory cache.</span></span>


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



<span data-ttu-id="84b7d-295">Ahora recorra en iteración las propiedades para determinar si el valor de una propiedad ha cambiado desde que se cargó en la memoria.</span><span class="sxs-lookup"><span data-stu-id="84b7d-295">Now iterate through the properties to determine whether the value of a property has been changed since it was loaded into memory.</span></span>


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



<span data-ttu-id="84b7d-296">El método [**IPropertyStoreCache:: GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) obtiene el estado de la propiedad en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="84b7d-296">The [**IPropertyStoreCache::GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) method gets the state of the property in the cache.</span></span> <span data-ttu-id="84b7d-297">La \_ marca de modificador de PSC, que se estableció en la implementación [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) , marca una propiedad como modificada.</span><span class="sxs-lookup"><span data-stu-id="84b7d-297">The PSC\_DIRTY flag, which was set in the [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) implementation, marks a property as changed.</span></span>


```
        if (SUCCEEDED(hr))
        {
            // check the cache state; only save dirty properties
            PSC_STATE psc;
            hr = _pCache->GetState(key, &psc);
            if (SUCCEEDED(hr) && psc == PSC_DIRTY)
            {
                // get the cached value
                PROPVARIANT propvar = {};
                hr = _pCache->GetValue(key, &propvar); 
```



<span data-ttu-id="84b7d-298">Asigne la propiedad al nodo XML tal y como se especifica en la matriz de **\_ rgPropertyMap de ejemplo** .</span><span class="sxs-lookup"><span data-stu-id="84b7d-298">Map the property to the XML node as specified in the **eg\_rgPropertyMap** array.</span></span>


```
if (SUCCEEDED(hr))
                {
                    // save as a native property if the key is in the property map
                    BOOL fIsNativeProperty = FALSE;
                    for (UINT i = 0; i < ARRAYSIZE(g_rgPROPERTYMAP); ++i)
                    {
                        if (IsEqualPropertyKey(key, *g_rgPROPERTYMAP[i].pkey))
                        {
                            fIsNativeProperty = TRUE;
                            hr = _SaveProperty(propvar, g_rgPROPERTYMAP[i]);
                            break;
                        }     
```



<span data-ttu-id="84b7d-299">Si una propiedad no está en el mapa, se trata de una nueva propiedad establecida por el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="84b7d-299">If a property is not in the map, it is a new property that was set by Windows Explorer.</span></span> <span data-ttu-id="84b7d-300">Dado que se admiten los metadatos abiertos, guarde la nueva propiedad en la sección **ExtendedProperties** del XML.</span><span class="sxs-lookup"><span data-stu-id="84b7d-300">Because open metadata is supported, save the new property in the **ExtendedProperties** section of the XML.</span></span>


```
                    
                    // Otherwise, save as an extended property.
                    if (!fIsNativeProperty)
                    {
                        hr = _SaveExtendedProperty(key, propvar);
                    }

                    PropVariantClear(&propvar);
                }
            }
        }
    }

    return hr;    
```



## <a name="implementing-ipropertystorecapabilities"></a><span data-ttu-id="84b7d-301">Implementación de IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="84b7d-301">Implementing IPropertyStoreCapabilities</span></span>

<span data-ttu-id="84b7d-302">[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informa a la interfaz de usuario del shell de si se puede editar una propiedad determinada en la interfaz de usuario del shell.</span><span class="sxs-lookup"><span data-stu-id="84b7d-302">[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informs the Shell UI whether a particular property can be edited in the Shell UI.</span></span> <span data-ttu-id="84b7d-303">Es importante tener en cuenta que esto se refiere únicamente a la capacidad de editar la propiedad en la interfaz de usuario, no de si se puede llamar correctamente a [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) en la propiedad.</span><span class="sxs-lookup"><span data-stu-id="84b7d-303">It is important to note that this relates only to the ability to edit the property in the UI, not whether you can successfully call [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) on the property.</span></span> <span data-ttu-id="84b7d-304">Una propiedad que genera un valor devuelto de S \_ false desde [**IPropertyStoreCapabilities:: IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) puede seguir siendo capaz de establecerse a través de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="84b7d-304">A property that provokes a return value of S\_FALSE from [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) might still be capable of being set through an application.</span></span>


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



<span data-ttu-id="84b7d-305">[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) devuelve **S \_ OK** para indicar que los usuarios finales deben tener permiso para editar la propiedad directamente. S \_ False indica que no deberían.</span><span class="sxs-lookup"><span data-stu-id="84b7d-305">[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) returns **S\_OK** to indicate that end users should be allowed to edit the property directly; S\_FALSE indicates that they should not.</span></span> <span data-ttu-id="84b7d-306">S \_ false puede significar que las aplicaciones son responsables de escribir la propiedad, no de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="84b7d-306">S\_FALSE can mean that applications are responsible for writing the property, not users.</span></span> <span data-ttu-id="84b7d-307">El shell deshabilita los controles de edición según corresponda en función de los resultados de las llamadas a este método.</span><span class="sxs-lookup"><span data-stu-id="84b7d-307">The Shell disables editing controls as appropriate based on the results of calls to this method.</span></span> <span data-ttu-id="84b7d-308">Se supone que un controlador que no implementa [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) admite metadatos abiertos a través de la compatibilidad con la escritura de cualquier propiedad.</span><span class="sxs-lookup"><span data-stu-id="84b7d-308">A handler that does not implement [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) is assumed to support open metadata through support for the writing of any property.</span></span>

<span data-ttu-id="84b7d-309">Si va a compilar un controlador que solo controla las propiedades de solo lectura, debe implementar el método **Initialize** ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)o [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) para que devuelva STG \_ E \_ ACCESSDENIED cuando se llame con la \_ marca ReadWrite STGM.</span><span class="sxs-lookup"><span data-stu-id="84b7d-309">If you are building a handler that handles only read-only properties, then you should implement your **Initialize** method ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem), or [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) so that it returns STG\_E\_ACCESSDENIED when called with the STGM\_READWRITE flag.</span></span>

<span data-ttu-id="84b7d-310">Algunas propiedades tienen el atributo [isInnate](./propdesc-schema-typeinfo.md) establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="84b7d-310">Some properties have their [isInnate](./propdesc-schema-typeinfo.md) attribute set to **true**.</span></span> <span data-ttu-id="84b7d-311">Las propiedades de INNATE tienen las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="84b7d-311">Innate properties have the following characteristics:</span></span>

-   <span data-ttu-id="84b7d-312">La propiedad se calcula normalmente de alguna manera.</span><span class="sxs-lookup"><span data-stu-id="84b7d-312">The property is usually calculated in some way.</span></span> <span data-ttu-id="84b7d-313">Por ejemplo, `System.Image.BitDepth` se calcula a partir de la propia imagen.</span><span class="sxs-lookup"><span data-stu-id="84b7d-313">For instance, `System.Image.BitDepth` is calculated from the image itself.</span></span>
-   <span data-ttu-id="84b7d-314">Cambiar la propiedad no tendría sentido sin cambiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="84b7d-314">Changing the property would not make sense without changing the file.</span></span> <span data-ttu-id="84b7d-315">Por ejemplo, cambiar `System.Image.Dimensions` no cambia el tamaño de la imagen, por lo que no tiene sentido permitir que el usuario la cambie.</span><span class="sxs-lookup"><span data-stu-id="84b7d-315">For instance, changing `System.Image.Dimensions` would not resize the image, so it does not make sense to allow the user to change it.</span></span>
-   <span data-ttu-id="84b7d-316">En algunos casos, el sistema proporciona automáticamente estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="84b7d-316">In some cases, these properties are provided automatically by the system.</span></span> <span data-ttu-id="84b7d-317">Entre los ejemplos `System.DateModified` se incluyen, proporcionado por el sistema de archivos, y `System.SharedWith` , que se basa en la persona con la que el usuario comparte el archivo.</span><span class="sxs-lookup"><span data-stu-id="84b7d-317">Examples include `System.DateModified`, which is provided by the file system, and `System.SharedWith`, which is based on who the user is sharing the file with.</span></span>

<span data-ttu-id="84b7d-318">Debido a estas características, las propiedades marcadas como *IsInnate* se proporcionan al usuario en la interfaz de usuario de Shell solo como propiedades de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="84b7d-318">Due to these characteristics, properties marked as *IsInnate* are provided to the user in the Shell UI only as read-only properties.</span></span> <span data-ttu-id="84b7d-319">Si una propiedad se marca como *IsInnate*, el sistema de propiedades no almacena esa propiedad en el controlador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="84b7d-319">If a property is marked as *IsInnate*, the property system does not store that property in the property handler.</span></span> <span data-ttu-id="84b7d-320">Por lo tanto, los controladores de propiedades no necesitan un código especial para tener en cuenta estas propiedades en sus implementaciones.</span><span class="sxs-lookup"><span data-stu-id="84b7d-320">Therefore, property handlers do not need special code to account for these properties in their implementations.</span></span> <span data-ttu-id="84b7d-321">Si el valor del atributo *IsInnate* no se especifica explícitamente para una propiedad determinada, el valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="84b7d-321">If the value of the *IsInnate* attribute is not explicitly stated for a particular property, the default value is **false**.</span></span>

## <a name="registering-and-distributing-property-handlers"></a><span data-ttu-id="84b7d-322">Registrar y distribuir controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="84b7d-322">Registering and Distributing Property Handlers</span></span>

<span data-ttu-id="84b7d-323">Con el controlador de propiedades implementado, debe estar registrado y su extensión de nombre de archivo asociada al controlador.</span><span class="sxs-lookup"><span data-stu-id="84b7d-323">With the property handler implemented, it must be registered and its file name extension associated with the handler.</span></span> <span data-ttu-id="84b7d-324">Para obtener más información, vea [registrar y distribuir controladores de propiedades](./prophand-reg-dist.md).</span><span class="sxs-lookup"><span data-stu-id="84b7d-324">For more information, see [Registering and Distributing Property Handlers](./prophand-reg-dist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84b7d-325">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84b7d-325">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84b7d-326">Descripción de los controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="84b7d-326">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="84b7d-327">Usar nombres de tipo</span><span class="sxs-lookup"><span data-stu-id="84b7d-327">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="84b7d-328">Usar listas de propiedades</span><span class="sxs-lookup"><span data-stu-id="84b7d-328">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="84b7d-329">Registrar y distribuir controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="84b7d-329">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="84b7d-330">Prácticas recomendadas y preguntas más frecuentes sobre controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="84b7d-330">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
