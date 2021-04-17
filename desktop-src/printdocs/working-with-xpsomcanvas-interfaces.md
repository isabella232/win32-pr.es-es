---
title: Interfaces visual y canvas de XPS OM
description: En este tema se describe cómo usar las interfaces relacionadas con canvas de la API de documento XPS en un OM de XPS.
ms.assetid: 368b8c47-9803-42ee-a3a8-681bf55315ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8bd15333c2786801900b09b32eb6cd59121af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697271"
---
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a><span data-ttu-id="f7a4b-103">Trabajar con las interfaces visual y canvas de XPS OM</span><span class="sxs-lookup"><span data-stu-id="f7a4b-103">Working with XPS OM Canvas and Visual Interfaces</span></span>

<span data-ttu-id="f7a4b-104">En este tema se describe cómo usar las interfaces relacionadas con canvas de la API de documento XPS en un OM de XPS.</span><span class="sxs-lookup"><span data-stu-id="f7a4b-104">This topic describes how to use the canvas-related interfaces of the XPS Document API in an XPS OM.</span></span>

| <span data-ttu-id="f7a4b-105">Nombre de interfaz</span><span class="sxs-lookup"><span data-stu-id="f7a4b-105">Interface name</span></span>                                  | <span data-ttu-id="f7a4b-106">Interfaces secundarias lógicas</span><span class="sxs-lookup"><span data-stu-id="f7a4b-106">Logical child interfaces</span></span>                                                                                                                    | <span data-ttu-id="f7a4b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7a4b-107">Description</span></span>                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7a4b-108">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="f7a4b-108">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [<span data-ttu-id="f7a4b-109">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="f7a4b-109">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="f7a4b-110">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="f7a4b-110">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="f7a4b-111">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="f7a4b-111">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | <span data-ttu-id="f7a4b-112">La clase base de las interfaces que definen objetos visuales, como texto y gráficos.</span><span class="sxs-lookup"><span data-stu-id="f7a4b-112">The base class of the interfaces that define visual objects, such as text and graphics.</span></span><br/> <span data-ttu-id="f7a4b-113">Los objetos visuales se pueden recopilar en una interfaz [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) .</span><span class="sxs-lookup"><span data-stu-id="f7a4b-113">Visual objects can be collected in an [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) interface.</span></span><br/> |
| [<span data-ttu-id="f7a4b-114">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="f7a4b-114">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [<span data-ttu-id="f7a4b-115">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="f7a4b-115">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="f7a4b-116">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="f7a4b-116">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="f7a4b-117">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="f7a4b-117">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | <span data-ttu-id="f7a4b-118">Colección de objetos visuales que se puede tratar como un objeto visual único.</span><span class="sxs-lookup"><span data-stu-id="f7a4b-118">A collection of visual objects that can be treated as a single visual object.</span></span><br/>                                                                                                                                |
<span data-ttu-id="f7a4b-119">[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) es la interfaz base; los objetos visibles de una página heredan de él.</span><span class="sxs-lookup"><span data-stu-id="f7a4b-119">[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) is the base interface; the visible objects of a page inherit from it.</span></span> <span data-ttu-id="f7a4b-120">[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) hereda de [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) y permite agrupar muchos otros elementos visuales y actuar como un elemento visual único.</span><span class="sxs-lookup"><span data-stu-id="f7a4b-120">[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) inherits from [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) and enables many other visual elements to be grouped and acted upon as a single visual element.</span></span> <span data-ttu-id="f7a4b-121">Por ejemplo, puede usar una interfaz [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) para crear un titular de página que contenga una colección de texto y elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="f7a4b-121">For example, you could use an [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) interface to create a page banner that contains a collection of text and graphical elements.</span></span> <span data-ttu-id="f7a4b-122">Este banner podría contener un logotipo, el lema de la empresa y la dirección de la empresa.</span><span class="sxs-lookup"><span data-stu-id="f7a4b-122">Such a banner might contain a logo, the company slogan, and the company address.</span></span> <span data-ttu-id="f7a4b-123">Puede colocar todos estos elementos en el [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) de una interfaz [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) y, a continuación, aplicar una transformación única al objeto [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) para cambiar su tamaño a una página determinada.</span><span class="sxs-lookup"><span data-stu-id="f7a4b-123">You could place all these elements into the [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) of an [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) interface, and then apply a single transform to the [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) object to resize it to a particular page.</span></span> <span data-ttu-id="f7a4b-124">Es mucho más sencillo que calcular y aplicar una transformación a cada componente visual individual en el banner.</span><span class="sxs-lookup"><span data-stu-id="f7a4b-124">This is much simpler than computing and applying a transform to each individual visual component in the banner.</span></span>

<span data-ttu-id="f7a4b-125">También puede usar un lienzo para cambiar el tamaño del contenido de la página para ajustarse al tamaño de página actual.</span><span class="sxs-lookup"><span data-stu-id="f7a4b-125">You can also use a canvas to resize the page contents to fit the current page size.</span></span> <span data-ttu-id="f7a4b-126">Para ello, coloque todo el contenido de la página en un solo lienzo y, a continuación, aplique la transformación adecuada para ajustar el lienzo al tamaño de página actual.</span><span class="sxs-lookup"><span data-stu-id="f7a4b-126">To accomplish this, place all contents of the page into a single canvas, then apply the appropriate transform to fit the canvas to the current page size.</span></span> <span data-ttu-id="f7a4b-127">Esto también es mucho más sencillo que intentar cambiar el tamaño de cada elemento visual en la colección de objetos visuales de la página.</span><span class="sxs-lookup"><span data-stu-id="f7a4b-127">This is also much simpler than trying to resize each visual element in the collection of visuals in the page.</span></span>

## <a name="move-page-contents-to-a-canvas"></a><span data-ttu-id="f7a4b-128">Trasladar el contenido de la página a un lienzo</span><span class="sxs-lookup"><span data-stu-id="f7a4b-128">Move page contents to a canvas</span></span>

<span data-ttu-id="f7a4b-129">En el ejemplo de código siguiente se mueve el contenido de una página a un lienzo.</span><span class="sxs-lookup"><span data-stu-id="f7a4b-129">The following code example moves the contents of a page to a canvas.</span></span>

```C++
    HRESULT                   hr = S_OK;

    IXpsOMVisualCollection    *pageVisuals;
    IXpsOMVisualCollection    *canvasVisuals;
    IXpsOMVisual              *oneVisual;
    IXpsOMCanvas              *newPageCanvas;

    UINT32 numVisuals = 0;
    UINT32 thisVisual;

    // get the page's visual collection
    // and how many objects it contains
    hr = page->GetVisuals( &pageVisuals );
    hr = pageVisuals->GetCount ( &numVisuals );

    // create the new canvas object and
    // its (empty) visual collection
    hr = xpsFactory->CreateCanvas ( &newPageCanvas );
    hr = newPageCanvas->GetVisuals ( &canvasVisuals );

    // go through the page's list of visual objects,
    //  move each one from the page's list to the canvas' list
    //  release the local pointer
    //  remove it from the page's collection
    thisVisual = 0;
    while (thisVisual < numVisuals) {
        hr = pageVisuals->GetAt (0, &oneVisual);
        hr = canvasVisuals->Append (oneVisual);
        hr = pageVisuals->RemoveAt (0);
        thisVisual++;
    }
    // the page's visual collection should be empty
    hr = pageVisuals->GetCount (&numVisuals);
    _ASSERT (0 == numVisuals);

    // add the new canvas to the page's visual collection
    pageVisuals->Append ( newPageCanvas );

```

## <a name="related-topics"></a><span data-ttu-id="f7a4b-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f7a4b-130">Related topics</span></span>

<dl> 
  <span data-ttu-id="f7a4b-131">Interfaz <dt>[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>interface
  <dt>[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>interface
  <dt>[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</span><span class="sxs-lookup"><span data-stu-id="f7a4b-131"><dt>[**IXpsOMCanvas Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>
  <dt>[**IXpsOMVisual Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>
  <dt>[**IXpsOMVisualCollection Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</span></span></dl>
