---
title: Asistente para impresión fotográfica
description: El Asistente para impresión de fotografías ayuda a los usuarios a imprimir fotos proporcionando una interfaz de asistente fácil de usar.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Asistente para impresión fotográfica
- IDropTarget, Asistente para impresión fotográfica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708f051f658739cebd08e4f8643e5dd7fc0c6f7f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420690"
---
# <a name="photo-printing-wizard"></a><span data-ttu-id="07f0b-105">Asistente para impresión fotográfica</span><span class="sxs-lookup"><span data-stu-id="07f0b-105">Photo Printing Wizard</span></span>

<span data-ttu-id="07f0b-106">El Asistente para impresión de fotografías ayuda a los usuarios a imprimir fotos proporcionando una interfaz de asistente fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="07f0b-106">The Photo Printing Wizard helps users print photos by providing an easy-to-use wizard interface.</span></span> <span data-ttu-id="07f0b-107">El asistente permite al usuario especificar tamaños de impresión fotográfica y otras opciones de impresión y, a continuación, envía las fotos a la impresora.</span><span class="sxs-lookup"><span data-stu-id="07f0b-107">The wizard enables the user to specify photo print sizes and other print options, and then sends the photos to the printer.</span></span> <span data-ttu-id="07f0b-108">El asistente está diseñado para que se pueda invocar mediante programación por cualquier aplicación que desee ofrecer a los usuarios la posibilidad de imprimir fotografías y especificar el tamaño y otras opciones de impresión.</span><span class="sxs-lookup"><span data-stu-id="07f0b-108">The wizard is designed so that it can be invoked programmatically by any application that wants to offer users the ability to print photos and specify sizing and other print options.</span></span> <span data-ttu-id="07f0b-109">El Asistente para impresión de fotografías está disponible en Windows XP y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="07f0b-109">The Photo Printing Wizard is available on Windows XP and Windows Vista.</span></span>

-   [<span data-ttu-id="07f0b-110">Características proporcionadas por el Asistente para impresión fotográfica</span><span class="sxs-lookup"><span data-stu-id="07f0b-110">Features Provided by the Photo Print Wizard</span></span>](#features-provided-by-the-photo-print-wizard)
-   [<span data-ttu-id="07f0b-111">Formatos de archivo fotográfico admitidos</span><span class="sxs-lookup"><span data-stu-id="07f0b-111">Supported Photo File Formats</span></span>](#supported-photo-file-formats)
-   [<span data-ttu-id="07f0b-112">Inicio mediante programación del Asistente para impresión fotográfica</span><span class="sxs-lookup"><span data-stu-id="07f0b-112">Programmatically Launching the Photo Print Wizard</span></span>](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a><span data-ttu-id="07f0b-113">Características proporcionadas por el Asistente para impresión fotográfica</span><span class="sxs-lookup"><span data-stu-id="07f0b-113">Features Provided by the Photo Print Wizard</span></span>

<span data-ttu-id="07f0b-114">El Asistente para impresión fotográfica ofrece varias opciones que pueden no estar disponibles en los cuadros de diálogo de impresora comunes, como las plantillas de diseño múltiple con dimensiones precisas.</span><span class="sxs-lookup"><span data-stu-id="07f0b-114">The Photo Printing Wizard offers several options that may not be available on common printer dialogs, such as multi-layout templates with accurate dimensions.</span></span> <span data-ttu-id="07f0b-115">Las plantillas de diseño permiten a los usuarios hacer el uso más eficaz del espacio disponible en el papel de impresión fotográfica.</span><span class="sxs-lookup"><span data-stu-id="07f0b-115">The layout templates enable users to make the most efficient use of the space available on photographic printing paper.</span></span> <span data-ttu-id="07f0b-116">Otras opciones que se pueden especificar o a las que se puede tener acceso a través del Asistente para impresión fotográfica incluyen:</span><span class="sxs-lookup"><span data-stu-id="07f0b-116">Other options that can be specified or accessed through the Photo Print Wizard include:</span></span>

-   <span data-ttu-id="07f0b-117">Seleccionar una impresora de una lista de impresoras o destinos de impresión virtuales disponibles (por ejemplo, escritor de documentos XPS de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="07f0b-117">Selecting a printer from a list of available printers or virtual printing destinations (for example, Microsoft XPS Document Writer).</span></span> <span data-ttu-id="07f0b-118">En Windows Vista, pueden estar disponibles las siguientes opciones, en función de las capacidades de la impresora o del destino de impresión virtual:</span><span class="sxs-lookup"><span data-stu-id="07f0b-118">On Windows Vista, the following options may be available, depending on the capabilities of the printer or virtual printing destination:</span></span>
    -   <span data-ttu-id="07f0b-119">Tamaño del papel.</span><span class="sxs-lookup"><span data-stu-id="07f0b-119">Paper size.</span></span> <span data-ttu-id="07f0b-120">Por ejemplo, "Letter", "legal", "a3".</span><span class="sxs-lookup"><span data-stu-id="07f0b-120">For example, "Letter", "Legal", "A3".</span></span>
    -   <span data-ttu-id="07f0b-121">Calidad de impresión, en términos de resoluciones de puntos por pulgada (PPP) admitidas.</span><span class="sxs-lookup"><span data-stu-id="07f0b-121">Print quality, in terms of supported dots per inch (dpi) resolutions.</span></span>
    -   <span data-ttu-id="07f0b-122">Tipo de papel.</span><span class="sxs-lookup"><span data-stu-id="07f0b-122">Paper type.</span></span> <span data-ttu-id="07f0b-123">Por ejemplo, "Plain" o "satinada".</span><span class="sxs-lookup"><span data-stu-id="07f0b-123">For example, "Plain" or "Glossy".</span></span>
-   <span data-ttu-id="07f0b-124">Inicio de las preferencias de impresión y las propiedades de una impresora determinada.</span><span class="sxs-lookup"><span data-stu-id="07f0b-124">Launching the printing preferences and properties for a particular printer.</span></span>
-   <span data-ttu-id="07f0b-125">Establecer las **copias de cada imagen** (en Windows Vista) o el **número de veces que se usan** los valores del cuadro de número de cada imagen (en Windows XP).</span><span class="sxs-lookup"><span data-stu-id="07f0b-125">Setting the **Copies of each picture** (on Windows Vista) or **Number of times to use each picture** (on Windows XP) spin box values.</span></span>
-   <span data-ttu-id="07f0b-126">Especificar una plantilla de diseño de impresión.</span><span class="sxs-lookup"><span data-stu-id="07f0b-126">Specifying a print layout template.</span></span> <span data-ttu-id="07f0b-127">Por ejemplo, **fotos de página completa** o **impresiones de Wallet**.</span><span class="sxs-lookup"><span data-stu-id="07f0b-127">For example, **Full page photo** or **Wallet prints**.</span></span>
-   <span data-ttu-id="07f0b-128">Seleccionar la opción **ajustar la imagen al marco** (solo disponible en Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="07f0b-128">Selecting the **Fit picture to frame** option (available on Windows Vista only).</span></span>
-   <span data-ttu-id="07f0b-129">Obtener una vista previa de la foto impresa con las opciones especificadas actualmente.</span><span class="sxs-lookup"><span data-stu-id="07f0b-129">Previewing the printed photo with the currently specified options.</span></span>
-   <span data-ttu-id="07f0b-130">Obtener acceso a opciones de impresión avanzadas, como **enfocar para la impresión** y la **Administración del color** (solo disponible en Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="07f0b-130">Accesssing advanced print options, such as **Sharpen for printing** and **Color management** (available on Windows Vista only).</span></span>

<span data-ttu-id="07f0b-131">Cualquier aplicación puede beneficiarse de las características y la funcionalidad de impresión fotográfica que ofrece el Asistente para impresión fotográfica.</span><span class="sxs-lookup"><span data-stu-id="07f0b-131">Any application can benefit from the features and photo printing capability offered by the Photo Printing Wizard.</span></span> <span data-ttu-id="07f0b-132">Una aplicación puede pasar los archivos que se van a imprimir.</span><span class="sxs-lookup"><span data-stu-id="07f0b-132">An application can pass in the files to be printed.</span></span> <span data-ttu-id="07f0b-133">A continuación, el Asistente para impresión fotográfica se encarga de preparar el archivo para imprimirlo en función de las opciones especificadas por el usuario y de enviar los archivos preparados a la impresora.</span><span class="sxs-lookup"><span data-stu-id="07f0b-133">The Photo Printing Wizard then takes care of preparing the file for printing based on the options specified by the user and sends the prepared files to the printer.</span></span>

<span data-ttu-id="07f0b-134">En la siguiente ilustración se muestra la interfaz del Asistente para impresión fotográfica en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="07f0b-134">The following figure shows the Photo Printing Wizard interface on Windows Vista</span></span>

![el Asistente para impresión fotográfica en Windows Vista](images/ppw-vista.png)

<span data-ttu-id="07f0b-136">La siguiente ilustración muestra la interfaz del Asistente para impresión de fotografías en Windows XP</span><span class="sxs-lookup"><span data-stu-id="07f0b-136">The following figure shows the Photo Printing Wizard interface on Windows XP</span></span>

![el Asistente para impresión fotográfica en Windows XP](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a><span data-ttu-id="07f0b-138">Formatos de archivo fotográfico admitidos</span><span class="sxs-lookup"><span data-stu-id="07f0b-138">Supported Photo File Formats</span></span>

<span data-ttu-id="07f0b-139">En Windows XP, el Asistente para impresión fotográfica admite todos los formatos de archivo de gráficos compatibles con Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="07f0b-139">On Windows XP, the Photo Print Wizard supports all graphics file formats that are supported by Windows GDI+.</span></span> <span data-ttu-id="07f0b-140">Actualmente, estos formatos de archivo incluyen:</span><span class="sxs-lookup"><span data-stu-id="07f0b-140">Currently, these file formats include:</span></span>

-   <span data-ttu-id="07f0b-141">Mapa de bits (BMP)</span><span class="sxs-lookup"><span data-stu-id="07f0b-141">Bitmap (BMP)</span></span>
-   <span data-ttu-id="07f0b-142">Formato de intercambio de gráficos (GIF)</span><span class="sxs-lookup"><span data-stu-id="07f0b-142">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="07f0b-143">Formato JPEG (Joint Photographic Experts Group)</span><span class="sxs-lookup"><span data-stu-id="07f0b-143">Joint Photographic Experts Group (JPEG)</span></span>
-   <span data-ttu-id="07f0b-144">Archivo de imagen intercambiable (EXIF)</span><span class="sxs-lookup"><span data-stu-id="07f0b-144">Exchangeable Image File (EXIF)</span></span>
-   <span data-ttu-id="07f0b-145">Formato PNG (Portable Network Graphics)</span><span class="sxs-lookup"><span data-stu-id="07f0b-145">Portable Network Graphics (PNG)</span></span>
-   <span data-ttu-id="07f0b-146">Tagged Image File Format (TIFF)</span><span class="sxs-lookup"><span data-stu-id="07f0b-146">Tagged Image File Format (TIFF)</span></span>

<span data-ttu-id="07f0b-147">Para obtener más información sobre los formatos de archivo de gráficos compatibles con GDI+, vea [tipos de mapas de bits](../gdiplus/-gdiplus-types-of-bitmaps-about.md).</span><span class="sxs-lookup"><span data-stu-id="07f0b-147">For more information about graphics file formats supported by GDI+, see [Types of Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md).</span></span>

<span data-ttu-id="07f0b-148">En Windows Vista, el Asistente para impresión fotográfica admite cualquier formato de archivo de imagen para el que esté instalado un códec de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="07f0b-148">On Windows Vista, the Photo Print Wizard supports any image file format for which a Windows Imaging Component (WIC) codec is installed.</span></span> <span data-ttu-id="07f0b-149">WIC proporciona varios códecs estándar, entre los que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="07f0b-149">WIC provides several standard codecs, including:</span></span>

-   <span data-ttu-id="07f0b-150">Mapa de bits (BMP)</span><span class="sxs-lookup"><span data-stu-id="07f0b-150">Bitmap (BMP)</span></span>
-   <span data-ttu-id="07f0b-151">GIF</span><span class="sxs-lookup"><span data-stu-id="07f0b-151">GIF</span></span>
-   <span data-ttu-id="07f0b-152">Formato de icono (ICO)</span><span class="sxs-lookup"><span data-stu-id="07f0b-152">Icon Format (ICO)</span></span>
-   <span data-ttu-id="07f0b-153">JPEG</span><span class="sxs-lookup"><span data-stu-id="07f0b-153">JPEG</span></span>
-   <span data-ttu-id="07f0b-154">PNG</span><span class="sxs-lookup"><span data-stu-id="07f0b-154">PNG</span></span>
-   <span data-ttu-id="07f0b-155">TIFF</span><span class="sxs-lookup"><span data-stu-id="07f0b-155">TIFF</span></span>
-   <span data-ttu-id="07f0b-156">Formato de Windows Media Photo</span><span class="sxs-lookup"><span data-stu-id="07f0b-156">Windows Media Photo format</span></span>

<span data-ttu-id="07f0b-157">Para obtener más información acerca de los códecs WIC y WIC, vea [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="07f0b-157">For more information about WIC and WIC codecs, see [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)</span></span>

## <a name="programmatically-launching-the-photo-print-wizard"></a><span data-ttu-id="07f0b-158">Inicio mediante programación del Asistente para impresión fotográfica</span><span class="sxs-lookup"><span data-stu-id="07f0b-158">Programmatically Launching the Photo Print Wizard</span></span>

<span data-ttu-id="07f0b-159">Para invocar el Asistente para impresión de fotografías, llame a la interfaz [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) con el siguiente identificador de clase (CLSID):</span><span class="sxs-lookup"><span data-stu-id="07f0b-159">To invoke the Photo Printing Wizard, call the [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface with the following class identifier (CLSID):</span></span>


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



<span data-ttu-id="07f0b-160">Los archivos que se van a procesar mediante el Asistente para impresión fotográfica se especifican en un objeto [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="07f0b-160">The files to be processed by the Photo Printing Wizard are specified in an [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) object.</span></span>

<span data-ttu-id="07f0b-161">En el ejemplo de código siguiente se muestra cómo invocar el Asistente para impresión fotográfica.</span><span class="sxs-lookup"><span data-stu-id="07f0b-161">The following code example demonstrates how to invoke the Photo Printing Wizard.</span></span>


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
            
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PrintPhotosDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



 

 