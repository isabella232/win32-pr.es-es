---
description: En este tema se describe cómo navegar por un OM XPS y obtener acceso a diferentes partes del documento en memoria.
ms.assetid: 90b726aa-29da-4cfb-9c69-f471c2acb678
title: Navegar por el OM de XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ec33543867f66dd4da65ef95aab0cdfd8cfe0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688132"
---
# <a name="navigate-the-xps-om"></a><span data-ttu-id="c30a9-103">Navegar por el OM de XPS</span><span class="sxs-lookup"><span data-stu-id="c30a9-103">Navigate the XPS OM</span></span>

<span data-ttu-id="c30a9-104">En este tema se describe cómo navegar por un OM XPS y obtener acceso a diferentes partes del documento en memoria.</span><span class="sxs-lookup"><span data-stu-id="c30a9-104">This topic describes how to navigate an XPS OM and to access different parts of the in-memory document.</span></span>

<span data-ttu-id="c30a9-105">La organización de la API de documentos XPS refleja la organización de un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="c30a9-105">The organization of the XPS Document API mirrors the organization of an XPS document.</span></span> <span data-ttu-id="c30a9-106">En la tabla siguiente se muestra cómo se relacionan las interfaces de la API de documentos XPS con los componentes de un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="c30a9-106">The following table illustrates how the interfaces of the XPS Document API relate to the components of an XPS document.</span></span>



| <span data-ttu-id="c30a9-107">Componente de documento XPS</span><span class="sxs-lookup"><span data-stu-id="c30a9-107">XPS document component</span></span>                                         | <span data-ttu-id="c30a9-108">Interfaz de la API de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="c30a9-108">XPS Document API interface</span></span>                                          | <span data-ttu-id="c30a9-109">Método que se va a llamar para el siguiente nivel hacia abajo en la jerarquía</span><span class="sxs-lookup"><span data-stu-id="c30a9-109">Method to call for the next level down in the hierarchy</span></span>                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c30a9-110">Archivo de documento XPS (contiene el paquete OPC)</span><span class="sxs-lookup"><span data-stu-id="c30a9-110">XPS document file (contains OPC package)</span></span><br/>            | [<span data-ttu-id="c30a9-111">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="c30a9-111">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>                   | [<span data-ttu-id="c30a9-112">**GetDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="c30a9-112">**GetDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-getdocumentsequence)<br/>                                                                   |
| <span data-ttu-id="c30a9-113">Elemento FixedDocumentSequence</span><span class="sxs-lookup"><span data-stu-id="c30a9-113">FixedDocumentSequence part</span></span><br/>                          | [<span data-ttu-id="c30a9-114">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="c30a9-114">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> | [<span data-ttu-id="c30a9-115">**GetDocuments**</span><span class="sxs-lookup"><span data-stu-id="c30a9-115">**GetDocuments**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getdocuments)<br/>                                                                        |
| <span data-ttu-id="c30a9-116">Elemento FixedDocument</span><span class="sxs-lookup"><span data-stu-id="c30a9-116">FixedDocument part</span></span><br/>                                  | [<span data-ttu-id="c30a9-117">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="c30a9-117">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                 | [<span data-ttu-id="c30a9-118">**GetPageReferences**</span><span class="sxs-lookup"><span data-stu-id="c30a9-118">**GetPageReferences**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getpagereferences)<br/>                                                                      |
| <span data-ttu-id="c30a9-119">Elemento **PageContent** en el marcado FixedDocument</span><span class="sxs-lookup"><span data-stu-id="c30a9-119">**PageContent** element in the FixedDocument markup</span></span><br/> | [<span data-ttu-id="c30a9-120">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="c30a9-120">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>       | [<span data-ttu-id="c30a9-121">**GetPage**</span><span class="sxs-lookup"><span data-stu-id="c30a9-121">**GetPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage)<br/> [<span data-ttu-id="c30a9-122">**CollectPartResources**</span><span class="sxs-lookup"><span data-stu-id="c30a9-122">**CollectPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources)<br/> |
| <span data-ttu-id="c30a9-123">Elemento FixedPage</span><span class="sxs-lookup"><span data-stu-id="c30a9-123">FixedPage part</span></span><br/>                                      | [<span data-ttu-id="c30a9-124">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="c30a9-124">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                         | [<span data-ttu-id="c30a9-125">**GetVisuals**</span><span class="sxs-lookup"><span data-stu-id="c30a9-125">**GetVisuals**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getvisuals)<br/>                                                                                        |
| <span data-ttu-id="c30a9-126">Elemento **Canvas** en el marcado FixedPage</span><span class="sxs-lookup"><span data-stu-id="c30a9-126">**Canvas** element in the FixedPage markup</span></span><br/>          | [<span data-ttu-id="c30a9-127">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="c30a9-127">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/>                     | [<span data-ttu-id="c30a9-128">**GetVisuals**</span><span class="sxs-lookup"><span data-stu-id="c30a9-128">**GetVisuals**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getvisuals)<br/>                                                                                      |
| <span data-ttu-id="c30a9-129">Elemento **path** en el marcado FixedPage</span><span class="sxs-lookup"><span data-stu-id="c30a9-129">**Path** element in the FixedPage markup</span></span><br/>            | [<span data-ttu-id="c30a9-130">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="c30a9-130">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                         | <span data-ttu-id="c30a9-131">Fin de la jerarquía de documentos.</span><span class="sxs-lookup"><span data-stu-id="c30a9-131">End of document hierarchy.</span></span><br/>                                                                                                         |
| <span data-ttu-id="c30a9-132">Elemento **Glyphs** en el marcado FixedPage</span><span class="sxs-lookup"><span data-stu-id="c30a9-132">**Glyphs** element in the FixedPage markup</span></span><br/>          | [<span data-ttu-id="c30a9-133">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="c30a9-133">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/>                     | <span data-ttu-id="c30a9-134">Fin de la jerarquía de documentos.</span><span class="sxs-lookup"><span data-stu-id="c30a9-134">End of document hierarchy.</span></span><br/>                                                                                                         |
| <span data-ttu-id="c30a9-135">Parte de fuente</span><span class="sxs-lookup"><span data-stu-id="c30a9-135">Font part</span></span><br/>                                           | [<span data-ttu-id="c30a9-136">**IXpsOMFontResource**</span><span class="sxs-lookup"><span data-stu-id="c30a9-136">**IXpsOMFontResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)<br/>         | <span data-ttu-id="c30a9-137">Fin de la jerarquía de documentos.</span><span class="sxs-lookup"><span data-stu-id="c30a9-137">End of document hierarchy.</span></span><br/>                                                                                                         |
| <span data-ttu-id="c30a9-138">Elemento de imagen</span><span class="sxs-lookup"><span data-stu-id="c30a9-138">Image part</span></span><br/>                                          | [<span data-ttu-id="c30a9-139">**IXpsOMImageResource**</span><span class="sxs-lookup"><span data-stu-id="c30a9-139">**IXpsOMImageResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)<br/>       | <span data-ttu-id="c30a9-140">Fin de la jerarquía de documentos.</span><span class="sxs-lookup"><span data-stu-id="c30a9-140">End of document hierarchy.</span></span><br/>                                                                                                         |



 

<span data-ttu-id="c30a9-141">Antes de usar los siguientes ejemplos de código en el programa, lea la declinación de responsabilidades en [las tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="c30a9-141">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="c30a9-142">Ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="c30a9-142">Code Example</span></span>

<span data-ttu-id="c30a9-143">En el siguiente ejemplo de código se presupone la existencia de un OM XPS inicializado y el *paquete* apunta a una interfaz [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) que representa ese OM XPS.</span><span class="sxs-lookup"><span data-stu-id="c30a9-143">The following code example assumes the existence of an initialized XPS OM, and *package* points to an [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface that represents that XPS OM.</span></span> <span data-ttu-id="c30a9-144">Para obtener información acerca de cómo crear un OM XPS, consulte [leer un documento XPS en un OM XPS](read-an-xps-document-into-an-xps-om.md) o [crear un OM XPS en blanco](create-a-blank-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="c30a9-144">For information about creating an XPS OM, see [Read an XPS Document into an XPS OM](read-an-xps-document-into-an-xps-om.md) or [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>


```C++
    HRESULT                        hr = S_OK;

    IXpsOMDocumentSequence         *docSeq = NULL;
    IXpsOMDocumentCollection       *docs = NULL;
    IXpsOMDocument                 *doc = NULL;
    IXpsOMPageReferenceCollection  *pages = NULL;
    IXpsOMPageReference            *pageRef = NULL;
    IXpsOMPage                     *page = NULL;
    IXpsOMCanvas                   *canvas = NULL;
    IXpsOMPath                     *path = NULL;
    IXpsOMPartResources            *pageParts = NULL;
    IXpsOMGlyphs                   *glyphs = NULL;
    IXpsOMFontResourceCollection   *fonts = NULL; 
    IXpsOMFontResource             *font = NULL;
    IXpsOMImageResourceCollection  *images = NULL;
    IXpsOMImageResource            *image = NULL;
    IXpsOMVisualCollection         *visuals = NULL;
    IXpsOMVisual                   *visual = NULL;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    UINT32  numVisuals = 0;
    UINT32  thisVisual = 0;

    UINT32  numFonts = 0;
    UINT32  thisFont = 0;

    UINT32  numImages = 0;
    UINT32  thisImage = 0;

    XPS_OBJECT_TYPE  visualType;
 
    // package points to the IXpsOMPackage interface to walk.

    // Get the fixed document sequence of the package.
    hr = package->GetDocumentSequence(&docSeq);

    // Get the fixed documents in the fixed document sequence.
    hr = docSeq->GetDocuments(&docs);

    // Walk the collection of documents.
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
        
        // Get the doc contents.
        hr = doc->GetPageReferences(&pages);
        
        // Walk the collection of page references
        hr = pages->GetCount(&numPageRefs);
        thisPageRef = 0;
        while (thisPageRef < numPageRefs) {
            // Get this page reference.
            hr = pages->GetAt(thisPageRef, &pageRef);

            // Get the page content of this page reference.
            {
                hr = pageRef->GetPage (&page);

                // Get the visual tree of this page.
                hr = page->GetVisuals (&visuals);
                
                // Walk the visuals.
                hr = visuals->GetCount (&numVisuals);
                thisVisual = 0;
                while (thisVisual < numVisuals) {
                    hr = visuals->GetAt (thisVisual, &visual);
                    // Get visual type.
                    hr = visual->GetType( &visualType );
                    
                    // Do other stuff with the visual.

                    // Release the visual.
                    if (NULL != visual) {visual->Release(); visual = NULL;}
                    thisVisual++; // Get next visual in collection.
                }
                if (NULL != visuals) {visuals->Release(); visuals = NULL;}
                if (NULL != page) {page->Release(); page = NULL;}
            }
            // Get the part resources used by this page.
            hr = pageRef->CollectPartResources (&pageParts);

            // Get the font resources.
            {
                hr = pageParts->GetFontResources (&fonts);
                
                // Walk the fonts.
                hr = fonts->GetCount (&numFonts);
                thisFont = 0;
                while (thisFont < numFonts) {
                    hr = fonts->GetAt(thisFont, &font);
                    if (NULL != font) {font->Release(); font = NULL;}

                    thisFont++; // Get the next font in collection.
                }
                if (NULL != fonts) {fonts->Release(); fonts = NULL;}
            }

            // Get the image resources.
            {
                hr = pageParts->GetImageResources (&images);

                // walk the images
                hr = images->GetCount (&numImages);
                thisImage = 0;
                while (thisImage < numImages) {
                    hr = images->GetAt(thisImage, &image);
                    thisImage++;
                    if (NULL != image) {image->Release(); image = NULL;}
                }
                if (NULL != images) {images->Release(); images = NULL;}
            }
            if (NULL != pageRef) {pageRef->Release(); pageRef = NULL;}
            thisPageRef++; // Get next page in doc.
        }
        if (NULL != pages) {pages->Release(); pages = NULL;}
        if (NULL != doc) {doc->Release(); doc = NULL;}
        thisDoc++; // Get next doc in collection.
    }

    // Release interface pointers.
    if (NULL != docs) docs->Release();
    if (NULL != docSeq) docSeq->Release();

```



## <a name="related-topics"></a><span data-ttu-id="c30a9-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c30a9-145">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c30a9-146">**Pasos siguientes**</span><span class="sxs-lookup"><span data-stu-id="c30a9-146">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="c30a9-147">Escribir texto en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="c30a9-147">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="c30a9-148">Dibujar gráficos en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="c30a9-148">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="c30a9-149">Colocar imágenes en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="c30a9-149">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="c30a9-150">**Se usa en esta página**</span><span class="sxs-lookup"><span data-stu-id="c30a9-150">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="c30a9-151">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="c30a9-151">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[<span data-ttu-id="c30a9-152">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="c30a9-152">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[<span data-ttu-id="c30a9-153">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="c30a9-153">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="c30a9-154">**IXpsOMFontResource**</span><span class="sxs-lookup"><span data-stu-id="c30a9-154">**IXpsOMFontResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[<span data-ttu-id="c30a9-155">**IXpsOMFontResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="c30a9-155">**IXpsOMFontResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)
</dt> <dt>

[<span data-ttu-id="c30a9-156">**IXpsOMImageResource**</span><span class="sxs-lookup"><span data-stu-id="c30a9-156">**IXpsOMImageResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)
</dt> <dt>

[<span data-ttu-id="c30a9-157">**IXpsOMImageResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="c30a9-157">**IXpsOMImageResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)
</dt> <dt>

[<span data-ttu-id="c30a9-158">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="c30a9-158">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="c30a9-159">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="c30a9-159">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="c30a9-160">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="c30a9-160">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="c30a9-161">**IXpsOMPageReferenceCollection**</span><span class="sxs-lookup"><span data-stu-id="c30a9-161">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[<span data-ttu-id="c30a9-162">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="c30a9-162">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[<span data-ttu-id="c30a9-163">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="c30a9-163">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="c30a9-164">**Para obtener más información**</span><span class="sxs-lookup"><span data-stu-id="c30a9-164">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="c30a9-165">Inicializar un OM XPS</span><span class="sxs-lookup"><span data-stu-id="c30a9-165">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="c30a9-166">Leer un documento XPS en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="c30a9-166">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="c30a9-167">Crear un OM XPS en blanco</span><span class="sxs-lookup"><span data-stu-id="c30a9-167">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)
</dt> <dt>

[<span data-ttu-id="c30a9-168">API de empaquetado</span><span class="sxs-lookup"><span data-stu-id="c30a9-168">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="c30a9-169">Referencia de la API de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="c30a9-169">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="c30a9-170">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="c30a9-170">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

