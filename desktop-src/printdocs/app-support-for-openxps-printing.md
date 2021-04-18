---
description: OpenXPS es el formato de especificación de papel XML abierto para los documentos, y se basa en la especificación estándar de la Asociación Europea de los responsables de cartón (ECMA).
ms.assetid: 52FB5B3F-BEBF-4851-8BE9-5DC7AE535313
title: Compatibilidad de aplicaciones para la impresión en OpenXPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914d8c365209ea3486bedd5e0352e63a8e31086f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706297"
---
# <a name="app-support-for-openxps-printing"></a><span data-ttu-id="9213c-103">Compatibilidad de aplicaciones para la impresión en OpenXPS</span><span class="sxs-lookup"><span data-stu-id="9213c-103">App Support for OpenXPS Printing</span></span>

<span data-ttu-id="9213c-104">OpenXPS es el formato de especificación de papel XML abierto para los documentos y se basa en la especificación estándar de la Asociación Europea de fabricantes de informática (ECMA).</span><span class="sxs-lookup"><span data-stu-id="9213c-104">OpenXPS is the Open XML Paper Specification format for documents, and it’s based on the European Computer Manufacturers Association (ECMA) standard specification.</span></span>

<span data-ttu-id="9213c-105">Windows 8 proporciona compatibilidad total con la impresión de OpenXPS a través del modelo de controlador de impresión V4, en paralelo con la compatibilidad continua con el formato XPS de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9213c-105">Windows 8 provides full support for OpenXPS printing via the v4 print driver model, side-by-side with continued support for the Microsoft XPS format.</span></span> <span data-ttu-id="9213c-106">Y este tema se centra en la parte de este soporte que es relevante para los desarrolladores de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="9213c-106">And this topic focuses on the portion of this support that is relevant to Windows application developers.</span></span> <span data-ttu-id="9213c-107">Para obtener información sobre los requisitos de controladores para la compatibilidad con OpenXPS, consulte [compatibilidad de controladores con OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).</span><span class="sxs-lookup"><span data-stu-id="9213c-107">For information about driver requirements for OpenXPS support, see [Driver Support for OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).</span></span>

## <a name="sending-xps-data-to-the-print-system"></a><span data-ttu-id="9213c-108">Envío de datos XPS al sistema de impresión</span><span class="sxs-lookup"><span data-stu-id="9213c-108">Sending XPS data to the Print System</span></span>

<span data-ttu-id="9213c-109">Se recomienda usar [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) para enviar todos los trabajos de impresión XPS al sistema de impresión.</span><span class="sxs-lookup"><span data-stu-id="9213c-109">We recommend that you use [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) for sending all XPS print jobs to the print system.</span></span> <span data-ttu-id="9213c-110">**IPrintDocumentPackageTarget** acepta el modelo de objetos XPS (OM) sin serialización y ayuda a mejorar el rendimiento general.</span><span class="sxs-lookup"><span data-stu-id="9213c-110">**IPrintDocumentPackageTarget** accepts the XPS object model (OM) without serialization, and that helps to improve the overall performance.</span></span>

<span data-ttu-id="9213c-111">A continuación se muestra un breve resumen de la interfaz **IPrintDocumentPackageTarget** :</span><span class="sxs-lookup"><span data-stu-id="9213c-111">Here's a brief summary of the **IPrintDocumentPackageTarget** interface:</span></span>

-   <span data-ttu-id="9213c-112">Esta interfaz admite la impresión desde soluciones personalizadas, así como aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="9213c-112">This interface supports printing from tailored solutions as well as desktop applications.</span></span>

-   <span data-ttu-id="9213c-113">En el caso de las aplicaciones de escritorio, se puede usar en lugar de [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).</span><span class="sxs-lookup"><span data-stu-id="9213c-113">For desktops apps, this can be used in place of [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).</span></span>

-   <span data-ttu-id="9213c-114">Disponible en Windows 7 con Service Pack 1 (SP1) + actualización de la plataforma y Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9213c-114">Available on Windows 7 with Service Pack 1 (SP1) + Platform Update, and Windows 8.</span></span>

-   <span data-ttu-id="9213c-115">Incluya *DocumentTarget. h* en los proyectos para usar estas API.</span><span class="sxs-lookup"><span data-stu-id="9213c-115">Include *DocumentTarget.h* in projects to use these APIs.</span></span>

<span data-ttu-id="9213c-116">Las aplicaciones que consumen documentos OpenXPS deben tener en cuenta que el tipo MIME para OpenXPS es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="9213c-116">Applications that consume OpenXPS documents should note that the MIME type for OpenXPS is as follows:</span></span>

<dl> <span data-ttu-id="9213c-117">oxps de aplicación \\</span><span class="sxs-lookup"><span data-stu-id="9213c-117">application\\oxps</span></span>  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a><span data-ttu-id="9213c-118">Envío de datos de OpenXPS a la API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="9213c-118">Sending OpenXPS data to the XPS Print API</span></span>

<span data-ttu-id="9213c-119">Específico de OpenXPS, XPS OM acepta MSXPS y OpenXPS, y proporciona métodos para la conversión y serialización en cualquier formato.</span><span class="sxs-lookup"><span data-stu-id="9213c-119">Specific to OpenXPS, XPS OM accepts both MSXPS and OpenXPS, and provides methods for conversion and serialization to either format.</span></span> <span data-ttu-id="9213c-120">Esto permite a los desarrolladores de aplicaciones ser independientes del controlador de destino, si así lo desean.</span><span class="sxs-lookup"><span data-stu-id="9213c-120">This allows application developers to be agnostic of the target driver, if they want.</span></span> <span data-ttu-id="9213c-121">Esto también significa que los desarrolladores de aplicaciones siempre pueden enviar trabajos de impresión como OM de XPS a StartXpsPrintJob1 o IDocumentPackageTarget, sabiendo que el sistema de impresión administrará cualquier conversión necesaria.</span><span class="sxs-lookup"><span data-stu-id="9213c-121">This also means that app developers can always submit print jobs as XPS OM to either StartXpsPrintJob1 or IDocumentPackageTarget, knowing that the print system will handle any necessary conversion.</span></span>

<span data-ttu-id="9213c-122">Por supuesto, si se impide la conversión entre formatos XPS, se mejorará el rendimiento de un extremo a otro.</span><span class="sxs-lookup"><span data-stu-id="9213c-122">Of course, preventing conversion between XPS formats will improve end-to-end performance.</span></span> <span data-ttu-id="9213c-123">Desde la aplicación, el desarrollador puede comprobar la siguiente clave del registro para determinar el formato XPS preferido del controlador de impresión de destino:</span><span class="sxs-lookup"><span data-stu-id="9213c-123">From the application, the developer can check the following registry key to determine the preferred XPS format of the targeted print driver:</span></span>

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

<span data-ttu-id="9213c-124">Una vez que se haya determinado el formato XPS preferido, la aplicación puede proporcionar objetos XPS OM que no requieran conversión.</span><span class="sxs-lookup"><span data-stu-id="9213c-124">Once the preferred XPS format has been determined, the application can provide XPS OM objects that will not require conversion.</span></span> <span data-ttu-id="9213c-125">Una nota concreta es el uso de la foto HD en MSXPS y JPEGXR en OpenXPS.</span><span class="sxs-lookup"><span data-stu-id="9213c-125">Of particular note is the use of HD Photo in MSXPS and JPEGXR in OpenXPS.</span></span> <span data-ttu-id="9213c-126">La conversión de JPEGXR en HD Photo es relativamente ligera, ya que la principal diferencia en esta conversión es que HD Photo omite 4 bits de control que requiere JPEGXR.</span><span class="sxs-lookup"><span data-stu-id="9213c-126">Converting from JPEGXR to HD Photo is relatively lightweight since the primary difference in this conversion is that HD Photo ignores 4 control bits that JPEGXR requires.</span></span> <span data-ttu-id="9213c-127">Sin embargo, la conversión de la foto de HD a JPEGXR requiere que se vuelva a codificar la imagen completa para generar los bits de control necesarios.</span><span class="sxs-lookup"><span data-stu-id="9213c-127">However, converting from HD Photo to JPEGXR requires the entire image to be re-encoded in order to generate the required control bits.</span></span> <span data-ttu-id="9213c-128">Por lo tanto, proporcionar imágenes de JPEGXR para imágenes de alta resolución garantizará la compatibilidad con OpenXPS y minimizará el costo de conversión de la imagen de MSXPS.</span><span class="sxs-lookup"><span data-stu-id="9213c-128">Thus, providing JPEGXR images for high-resolution images will ensure compatibility with OpenXPS and minimize the conversion cost of the image for MSXPS.</span></span>

<span data-ttu-id="9213c-129">El encabezado *Xpsobjectmodel \_ 1. h* define las API y los objetos adicionales para OpenXPS.</span><span class="sxs-lookup"><span data-stu-id="9213c-129">The *Xpsobjectmodel\_1.h* header defines the additional APIs and objects for OpenXPS.</span></span> <span data-ttu-id="9213c-130">Y la interfaz IXpsOMObjectFactory1 proporciona métodos adicionales para la conversión de imágenes.</span><span class="sxs-lookup"><span data-stu-id="9213c-130">And the IXpsOMObjectFactory1 interface provides additional methods for image conversion.</span></span> <span data-ttu-id="9213c-131">Esta es la sintaxis:</span><span class="sxs-lookup"><span data-stu-id="9213c-131">Here's the syntax:</span></span>


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



<span data-ttu-id="9213c-132">Windows 8 proporciona las siguientes enumeraciones nuevas y actualizadas.</span><span class="sxs-lookup"><span data-stu-id="9213c-132">Windows 8 provides the following new and updated enumerations.</span></span>

<span data-ttu-id="9213c-133">Nueva enumeración:</span><span class="sxs-lookup"><span data-stu-id="9213c-133">New enumeration:</span></span>

<dl>

[<span data-ttu-id="9213c-134">**\_tipo de documento XPS \_**</span><span class="sxs-lookup"><span data-stu-id="9213c-134">**XPS\_DOCUMENT\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

<span data-ttu-id="9213c-135">Enumeración actualizada</span><span class="sxs-lookup"><span data-stu-id="9213c-135">Updated enumeration</span></span>

<dl>

[<span data-ttu-id="9213c-136">**\_tipo de imagen XPS \_**</span><span class="sxs-lookup"><span data-stu-id="9213c-136">**XPS\_IMAGE\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

<span data-ttu-id="9213c-137">Los nuevos métodos de Getdocumenttype (permiten que una aplicación determine el formato XPS de los documentos.</span><span class="sxs-lookup"><span data-stu-id="9213c-137">The new GetDocumentType methods allow an application to determine the XPS format of documents.</span></span> <span data-ttu-id="9213c-138">Están disponibles en [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)y [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1).</span><span class="sxs-lookup"><span data-stu-id="9213c-138">These are available in [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1), and [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1).</span></span> <span data-ttu-id="9213c-139">Esta es una lista de los métodos.</span><span class="sxs-lookup"><span data-stu-id="9213c-139">Here's a list of the methods.</span></span>

<dl>

[<span data-ttu-id="9213c-140">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span><span class="sxs-lookup"><span data-stu-id="9213c-140">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[<span data-ttu-id="9213c-141">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span><span class="sxs-lookup"><span data-stu-id="9213c-141">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[<span data-ttu-id="9213c-142">**IXpsOMPackage1:: Getdocumenttype (**</span><span class="sxs-lookup"><span data-stu-id="9213c-142">**IXpsOMPackage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[<span data-ttu-id="9213c-143">**IXpsOMPage1:: Getdocumenttype (**</span><span class="sxs-lookup"><span data-stu-id="9213c-143">**IXpsOMPage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

<span data-ttu-id="9213c-144">Windows 8 proporciona los siguientes códigos de error nuevos en compatibilidad con OpenXPS:</span><span class="sxs-lookup"><span data-stu-id="9213c-144">Windows 8 provides the following new error codes in support of OpenXPS:</span></span>

<dl> <span data-ttu-id="9213c-145">espacio de nombres de XPS \_ E no \_ coincidente \_ .</span><span class="sxs-lookup"><span data-stu-id="9213c-145">XPS\_E\_MISMATCHED\_NAMESPACE.</span></span> <dl> <span data-ttu-id="9213c-146">Se devuelve este error si hay un espacio de nombres no coincidente.</span><span class="sxs-lookup"><span data-stu-id="9213c-146">This error is returned, if there is a mismatched namespace.</span></span>  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> <span data-ttu-id="9213c-147">Este error se devuelve si MSXPS usa URI absolutos en referencias internas o intenta usar referencias internas para serializar en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="9213c-147">This error is returned if MSXPS uses absolute URIs in internal references, or attempts to use internal references to serialize in the stream.</span></span> <span data-ttu-id="9213c-148">Esto se debe a que el modelo de objetos de XPS genera identificadores URI relativos.</span><span class="sxs-lookup"><span data-stu-id="9213c-148">That is because XPS OM generates relative URIs.</span></span> <span data-ttu-id="9213c-149">Aunque MSXPS admite los URI relativos y absolutos, OpenXPS requiere URI relativos.</span><span class="sxs-lookup"><span data-stu-id="9213c-149">And although MSXPS supports both relative and absolute URIs, OpenXPS requires relative URIs.</span></span>  
</dl> </dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="9213c-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9213c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9213c-151">Compatibilidad de controladores para OpenXPS</span><span class="sxs-lookup"><span data-stu-id="9213c-151">Driver Support for OpenXPS</span></span>](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[<span data-ttu-id="9213c-152">**IPrintDocumentPackageTarget**</span><span class="sxs-lookup"><span data-stu-id="9213c-152">**IPrintDocumentPackageTarget**</span></span>](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[<span data-ttu-id="9213c-153">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span><span class="sxs-lookup"><span data-stu-id="9213c-153">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[<span data-ttu-id="9213c-154">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span><span class="sxs-lookup"><span data-stu-id="9213c-154">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[<span data-ttu-id="9213c-155">**IXpsOMPackage1:: Getdocumenttype (**</span><span class="sxs-lookup"><span data-stu-id="9213c-155">**IXpsOMPackage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[<span data-ttu-id="9213c-156">**IXpsOMPage1:: Getdocumenttype (**</span><span class="sxs-lookup"><span data-stu-id="9213c-156">**IXpsOMPage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[<span data-ttu-id="9213c-157">**\_tipo de documento XPS \_**</span><span class="sxs-lookup"><span data-stu-id="9213c-157">**XPS\_DOCUMENT\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[<span data-ttu-id="9213c-158">**\_tipo de imagen XPS \_**</span><span class="sxs-lookup"><span data-stu-id="9213c-158">**XPS\_IMAGE\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
