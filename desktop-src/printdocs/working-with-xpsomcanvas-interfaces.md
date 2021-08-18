---
title: XpS OM Canvas e interfaces visuales
description: En este tema se describe cómo usar las interfaces relacionadas con el lienzo de la API de documentos XPS en un OM XPS.
ms.assetid: 368b8c47-9803-42ee-a3a8-681bf55315ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f7214a06779d997331f57a22ae29217e5cabdd635d0c3feac85bd8a3070065
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469274"
---
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a>Trabajar con xps om canvas e interfaces visuales

En este tema se describe cómo usar las interfaces relacionadas con el lienzo de la API de documentos XPS en un OM XPS.

| Nombre de la interfaz                                  | Interfaces secundarias lógicas                                                                                                                    | Descripción                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Clase base de las interfaces que definen objetos visuales, como texto y gráficos.<br/> Los objetos visuales se pueden recopilar en una [**interfaz IXpsOMVisualCollection.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)<br/> |
| [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Colección de objetos visuales que se pueden tratar como un único objeto visual.<br/>                                                                                                                                |

[**IXpsOMVisual es**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) la interfaz base; los objetos visibles de una página heredan de ella. [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) hereda de [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) y permite agrupar muchos otros elementos visuales y actuar sobre ellos como un único elemento visual. Por ejemplo, podría usar una interfaz [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) para crear un banner de página que contenga una colección de texto y elementos gráficos. Este banner puede contener un logotipo, el logotipo de la empresa y la dirección de la empresa. Puede colocar todos estos elementos en [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) de una interfaz [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) y, a continuación, aplicar una única transformación al objeto [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) para cambiar su tamaño a una página determinada. Esto es mucho más sencillo que calcular y aplicar una transformación a cada componente visual individual del banner.

También puede usar un lienzo para cambiar el tamaño del contenido de la página para ajustarlo al tamaño de página actual. Para ello, coloque todo el contenido de la página en un solo lienzo y, a continuación, aplique la transformación adecuada para ajustar el lienzo al tamaño de página actual. Esto también es mucho más sencillo que intentar cambiar el tamaño de cada elemento visual de la colección de objetos visuales de la página.

## <a name="move-page-contents-to-a-canvas"></a>Mover el contenido de la página a un lienzo

En el ejemplo de código siguiente se mueve el contenido de una página a un lienzo.

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

## <a name="related-topics"></a>Temas relacionados

<dl> 
  <dt>[**IXpsOMCanvas Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>
  <dt>[**IXpsOMVisual Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>
  <dt>[**IXpsOMVisualCollection (Interfaz IXpsOMVisualCollection)**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</dl>
