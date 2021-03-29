---
title: Asistente para impresión en línea
description: El Asistente para impresión en línea de Windows Vista ayuda a los usuarios a solicitar copias impresas de fotografías de los distribuidores de impresiones en línea.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Asistente para impresión en línea
- iconos, Asistente para impresión en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8536eea7a51eddb2dbb46d10c9291a60edfdc74e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358960"
---
# <a name="online-printing-wizard"></a><span data-ttu-id="54cfc-105">Asistente para impresión en línea</span><span class="sxs-lookup"><span data-stu-id="54cfc-105">Online Printing Wizard</span></span>

<span data-ttu-id="54cfc-106">El Asistente para impresión en línea de Windows Vista ayuda a los usuarios a solicitar copias impresas de fotografías de los distribuidores de impresiones en línea.</span><span class="sxs-lookup"><span data-stu-id="54cfc-106">The Windows Vista Online Printing Wizard helps users order prints of photos from participating online printing retailers.</span></span> <span data-ttu-id="54cfc-107">Este asistente está diseñado para que se pueda invocar mediante programación por cualquier aplicación que desee ofrecer a los usuarios la posibilidad de solicitar impresiones de fotografías.</span><span class="sxs-lookup"><span data-stu-id="54cfc-107">This wizard is designed so that it can be invoked programmatically by any application that wants to offer users the ability to order prints of photos.</span></span> <span data-ttu-id="54cfc-108">El Asistente para impresión de fotografías está disponible en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="54cfc-108">The Photo Printing Wizard is available on Windows Vista.</span></span> <span data-ttu-id="54cfc-109">PIX para Windows</span><span class="sxs-lookup"><span data-stu-id="54cfc-109">PIX for Windows</span></span>

-   [<span data-ttu-id="54cfc-110">Características proporcionadas por el Asistente para impresión en línea</span><span class="sxs-lookup"><span data-stu-id="54cfc-110">Features Provided by the Online Print Wizard</span></span>](#features-provided-by-the-online-print-wizard)
-   [<span data-ttu-id="54cfc-111">Formatos de archivo fotográfico admitidos</span><span class="sxs-lookup"><span data-stu-id="54cfc-111">Supported Photo File Formats</span></span>](#supported-photo-file-formats)
-   [<span data-ttu-id="54cfc-112">Inicio mediante programación del Asistente para impresión en línea</span><span class="sxs-lookup"><span data-stu-id="54cfc-112">Programmatically Launching the Online Print Wizard</span></span>](#programmatically-launching-the-online-print-wizard)
-   [<span data-ttu-id="54cfc-113">Acceso al icono del Asistente para impresión en línea</span><span class="sxs-lookup"><span data-stu-id="54cfc-113">Accessing the Online Print Wizard Icon</span></span>](#accessing-the-online-print-wizard-icon)
-   [<span data-ttu-id="54cfc-114">Propiedades MRU del Asistente para impresión en línea</span><span class="sxs-lookup"><span data-stu-id="54cfc-114">Online Print Wizard MRU Properties</span></span>](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a><span data-ttu-id="54cfc-115">Características proporcionadas por el Asistente para impresión en línea</span><span class="sxs-lookup"><span data-stu-id="54cfc-115">Features Provided by the Online Print Wizard</span></span>

<span data-ttu-id="54cfc-116">El Asistente para impresión en línea de Windows Vista permite a los usuarios ordenar copias fotográficas a partir de una selección de distribuidores de impresión en línea participantes.</span><span class="sxs-lookup"><span data-stu-id="54cfc-116">The Windows Vista Online Printing Wizard enables users to order prints from a selection of participating online printing retailers.</span></span> <span data-ttu-id="54cfc-117">Cuando se invoca, el asistente:</span><span class="sxs-lookup"><span data-stu-id="54cfc-117">When invoked, the wizard:</span></span>

1.  <span data-ttu-id="54cfc-118">Acepta un archivo o una lista de archivos para los que se van a ordenar las impresiones.</span><span class="sxs-lookup"><span data-stu-id="54cfc-118">Accepts a file or list of files for which prints are to be ordered.</span></span>
2.  <span data-ttu-id="54cfc-119">Recupera automáticamente la lista actual de los distribuidores de impresión en línea participantes y permite al usuario seleccionar el distribuidor desde el que desea comprar las fotos fotográficas.</span><span class="sxs-lookup"><span data-stu-id="54cfc-119">Automatically retrieves the current list of participating online printing retailers, and enables the user to select the retailer from which to purchase the photo prints.</span></span>
3.  <span data-ttu-id="54cfc-120">Guía al usuario a través del proceso o la ordenación de copias fotográficas.</span><span class="sxs-lookup"><span data-stu-id="54cfc-120">Guides the user through the process or ordering prints.</span></span>

<span data-ttu-id="54cfc-121">Cualquier aplicación puede beneficiarse de las características que ofrece el Asistente para impresión en línea de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="54cfc-121">Any application can benefit from the features offered by the Windows Vista Online Printing Wizard.</span></span> <span data-ttu-id="54cfc-122">Una aplicación solo necesita pasar el archivo o los archivos para los que se van a ordenar las impresiones y el asistente guía al usuario a través del proceso de ordenación.</span><span class="sxs-lookup"><span data-stu-id="54cfc-122">An application need only pass in the file or files for which prints will be ordered, and the wizard guides the user through the ordering process.</span></span>

<span data-ttu-id="54cfc-123">En la siguiente ilustración se muestra el Asistente para impresión en línea de Windows Vista, donde se muestra una lista de ejemplo de los distribuidores de impresión en línea participantes.</span><span class="sxs-lookup"><span data-stu-id="54cfc-123">The following figure shows the Windows Vista Online Printing Wizard displaying an example list of participating online printing retailers.</span></span>

![Asistente para impresión en línea de Windows Vista](images/opw.png)

## <a name="supported-photo-file-formats"></a><span data-ttu-id="54cfc-125">Formatos de archivo fotográfico admitidos</span><span class="sxs-lookup"><span data-stu-id="54cfc-125">Supported Photo File Formats</span></span>

<span data-ttu-id="54cfc-126">El Asistente para impresión en línea de Windows Vista admite cualquier formato de archivo de imagen para el que esté instalado un códec de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="54cfc-126">The Windows Vista Online Printing Wizard supports any image file format for which a Windows Imaging Component (WIC) codec is installed.</span></span> <span data-ttu-id="54cfc-127">WIC proporciona varios códecs estándar, entre los que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="54cfc-127">WIC provides several standard codecs, including:</span></span>

-   <span data-ttu-id="54cfc-128">Mapa de bits (BMP)</span><span class="sxs-lookup"><span data-stu-id="54cfc-128">Bitmap (BMP)</span></span>
-   <span data-ttu-id="54cfc-129">Formato de intercambio de gráficos (GIF)</span><span class="sxs-lookup"><span data-stu-id="54cfc-129">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="54cfc-130">Formato de icono (ICO)</span><span class="sxs-lookup"><span data-stu-id="54cfc-130">Icon Format (ICO)</span></span>
-   <span data-ttu-id="54cfc-131">Formato JPEG (Joint Photographic Experts Group)</span><span class="sxs-lookup"><span data-stu-id="54cfc-131">Joint Photographic Experts Group (JPEG)</span></span>
-   <span data-ttu-id="54cfc-132">Formato PNG (Portable Network Graphics)</span><span class="sxs-lookup"><span data-stu-id="54cfc-132">Portable Network Graphics (PNG)</span></span>
-   <span data-ttu-id="54cfc-133">Tagged Image File Format (TIFF)</span><span class="sxs-lookup"><span data-stu-id="54cfc-133">Tagged Image File Format (TIFF)</span></span>
-   <span data-ttu-id="54cfc-134">Formato de Windows Media Photo</span><span class="sxs-lookup"><span data-stu-id="54cfc-134">Windows Media Photo format</span></span>

<span data-ttu-id="54cfc-135">Para obtener más información acerca de los códecs WIC y WIC, vea [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="54cfc-135">For more information about WIC and WIC codecs, see [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).</span></span>

<span data-ttu-id="54cfc-136">Los formatos de archivo que admiten los distribuidores de impresión en línea varían de un distribuidor a un distribuidor; es posible que un distribuidor determinado no admita todos los formatos de archivo admitidos por el Asistente para impresión en línea de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="54cfc-136">File formats supported by online printing retailers vary from retailer to retailer; it is possible that a particular retailer may not support all of the file formats supported by the Windows Vista Online Printing Wizard.</span></span> <span data-ttu-id="54cfc-137">Si el usuario intenta pedir copias fotográficas en un formato no admitido por el distribuidor seleccionado, el Asistente para impresión en línea de Windows Vista notifica al usuario que el distribuidor seleccionado no admite el formato de archivo enviado.</span><span class="sxs-lookup"><span data-stu-id="54cfc-137">If the user attempts to order prints in a format that is not supported by the selected retailer, the Windows Vista Online Printing Wizard notifies the user that the selected retailer does not support the submitted file format.</span></span>

## <a name="programmatically-launching-the-online-print-wizard"></a><span data-ttu-id="54cfc-138">Inicio mediante programación del Asistente para impresión en línea</span><span class="sxs-lookup"><span data-stu-id="54cfc-138">Programmatically Launching the Online Print Wizard</span></span>

<span data-ttu-id="54cfc-139">Para invocar el Asistente para impresión en línea de Windows Vista, llame a la interfaz [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) con el siguiente identificador de clase (CLSID):</span><span class="sxs-lookup"><span data-stu-id="54cfc-139">To invoke the Windows Vista Online Printing Wizard, call the [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface with the following class identifier (CLSID):</span></span>


```
CLSID_PublishDropTarget
```



<span data-ttu-id="54cfc-140">Este CLSID se define en shobjidl. h y shobjidl. idl.</span><span class="sxs-lookup"><span data-stu-id="54cfc-140">This CLSID is defined in Shobjidl.h and Shobjidl.idl.</span></span> <span data-ttu-id="54cfc-141">Los archivos que se van a procesar mediante el Asistente para impresión en línea de Windows Vista se especifican en un objeto [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="54cfc-141">The files to be processed by the Windows Vista Online Printing Wizard are specified in an [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) object.</span></span>

<span data-ttu-id="54cfc-142">En el ejemplo de código siguiente se muestra cómo invocar el Asistente para impresión en línea de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="54cfc-142">The following code example demonstrates how to invoke the Windows Vista Online Printing Wizard.</span></span>


```
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PublishDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



## <a name="accessing-the-online-print-wizard-icon"></a><span data-ttu-id="54cfc-143">Acceso al icono del Asistente para impresión en línea</span><span class="sxs-lookup"><span data-stu-id="54cfc-143">Accessing the Online Print Wizard Icon</span></span>

<span data-ttu-id="54cfc-144">El Asistente para impresión en línea de Windows Vista exporta un icono al que pueden tener acceso y mostrar las aplicaciones que lo llaman.</span><span class="sxs-lookup"><span data-stu-id="54cfc-144">The Windows Vista Online Printing Wizard exports an icon that can be accessed and displayed by applications which call it.</span></span> <span data-ttu-id="54cfc-145">En la siguiente ilustración se muestra el icono del Asistente para impresión en línea de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="54cfc-145">The following figure shows the Windows Vista Online Printing Wizard icon.</span></span>

![icono del Asistente para impresión en línea de Windows Vista](images/opw-icon.png)

<span data-ttu-id="54cfc-147">En el ejemplo de código siguiente se muestra cómo recuperar el índice para el icono del Asistente para impresión en línea de Windows Vista mediante la lectura de la propiedad **OPWIcon** .</span><span class="sxs-lookup"><span data-stu-id="54cfc-147">The following code example demonstrates how to retrieve the index for the Windows Vista Online Printing Wizard icon by reading the **OPWIcon** property.</span></span>


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;

spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

// Read the icon index from the properties set. 
CComVariant vtIcon;
int nIndex;
hr = spPropsBag->Read(L"OPWIcon", &vtIcon, NULL);

if SUCCEEDED(hr)
{
    nIndex = vtIcon.lVal;
}
```



## <a name="online-print-wizard-mru-properties"></a><span data-ttu-id="54cfc-148">Propiedades MRU del Asistente para impresión en línea</span><span class="sxs-lookup"><span data-stu-id="54cfc-148">Online Print Wizard MRU Properties</span></span>

<span data-ttu-id="54cfc-149">El Asistente para impresión en línea de Windows Vista define tres propiedades relacionadas con el distribuidor de impresión en línea usado más recientemente (MRU).</span><span class="sxs-lookup"><span data-stu-id="54cfc-149">The Windows Vista Online Printing Wizard defines three properties that are related to the most recently used (MRU) online printing retailer.</span></span>



| <span data-ttu-id="54cfc-150">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="54cfc-150">Property Name</span></span> | <span data-ttu-id="54cfc-151">Valor o función de la propiedad</span><span class="sxs-lookup"><span data-stu-id="54cfc-151">Property Value/Function</span></span>                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54cfc-152">**MRUIcon**</span><span class="sxs-lookup"><span data-stu-id="54cfc-152">**MRUIcon**</span></span>   | <span data-ttu-id="54cfc-153">El índice del icono del distribuidor de impresión en línea usado más recientemente se puede leer desde esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="54cfc-153">The index of the icon for the most recently used online printing retailer can be read from this property.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="54cfc-154">**MRUName**</span><span class="sxs-lookup"><span data-stu-id="54cfc-154">**MRUName**</span></span>   | <span data-ttu-id="54cfc-155">El nombre del distribuidor de impresión en línea usado más recientemente se puede leer desde esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="54cfc-155">The name of the most recently used online printing retailer can be read from this property.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="54cfc-156">**UseMRU**</span><span class="sxs-lookup"><span data-stu-id="54cfc-156">**UseMRU**</span></span>    | <span data-ttu-id="54cfc-157">Un valor booleano de VT de **tipo** \*\* \_ bool\*\* que indica si el asistente debe omitir la página de selección del distribuidor de impresión en línea y usar en su lugar el distribuidor de impresión en línea usado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="54cfc-157">A **VARIANT** **VT\_BOOL** value indicating whether the wizard should skip the online printing retailer selection page, and just use the most recently used online printing retailer instead.</span></span> <span data-ttu-id="54cfc-158">Establezca esta propiedad en **Variant \_ true** para omitir la página de selección del distribuidor.</span><span class="sxs-lookup"><span data-stu-id="54cfc-158">Set this property to **VARIANT\_TRUE** to skip the retailer selection page.</span></span> |



 

<span data-ttu-id="54cfc-159">En el ejemplo de código siguiente se muestra cómo establecer la propiedad UseMRU para que el Asistente para impresión en línea de Windows Vista omita la página de selección del distribuidor de impresión en línea y seleccione automáticamente el distribuidor usado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="54cfc-159">The following code example demonstrates how to set the UseMRU property so the Windows Vista Online Printing Wizard bypasses the online printing retailer selection page and automatically selects the most recently used retailer.</span></span>


```
// A data object that contains the list of photos to order prints for.
IDataObject* pDataObject;

// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Set the UserMRU property to true to skip retailer selection and use 
// the MRU retailer instead.    
CComQIPtr<IPropertyBag> spPropsBag(spDropTarget);
if(spPropsBag) 
{
    VARIANT varTrue = {0};
    varTrue.vt = VT_BOOL;
    varTrue.boolVal = VARIANT_TRUE;
    spPropsBag->Write(L"UseMRU", &varTrue);
}

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);
```



<span data-ttu-id="54cfc-160">En el ejemplo de código siguiente se muestra cómo leer las propiedades MRUName y MRUIcon.</span><span class="sxs-lookup"><span data-stu-id="54cfc-160">The following code example demonstrates how to read the MRUName and MRUIcon properties.</span></span>


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;
spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

CComVariant vtMRUName, vtMRUIconIndex;
CComBSTR bstrMRUName;
int nMRUIconIndex;

// Get the MRU name value.
hr = spPropsBag->Read(L"MRUName", &vtMRUName, NULL);
if SUCCEEDED(hr) 
{
    bstrMRUName = vtMRUName.bstrVal;
}

// Get the MRU icon index value.
hr = spPropsBag->Read(L"MRUIcon", &vtMRUIconIndex, NULL);
if SUCCEEDED(hr)
{
    nMRUIconIndex = vtMRUIconIndex.lVal;
}
```



 

 