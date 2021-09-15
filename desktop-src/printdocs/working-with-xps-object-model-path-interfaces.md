---
description: En esta sección se describe cómo usar las interfaces relacionadas con la ruta de acceso de la API de documentos XPS en una INSTANCIA DE XPS.
ms.assetid: 4e76355a-ad53-4177-b8c7-3e768a1d4e3f
title: Trabajar con interfaces de ruta de acceso de OM xps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca66b65c6f20dc3b585de706e223df1f76d518a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570532"
---
# <a name="working-with-xps-om-path-interfaces"></a>Trabajar con interfaces de ruta de acceso de OM xps

En esta sección se describe cómo usar las interfaces relacionadas con la ruta de acceso de la API de documentos XPS en una INSTANCIA DE XPS.



| Nombre de la interfaz                                                            | Secundarios conceptuales                                                                                                                                                                                                                                                                                                                                                                                                                                         | Descripción                                                                                                                                                                                       |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                               | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Describe un elemento gráfico de ruta de acceso.<br/>                                                                                                                                                    |
| [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/>                             | [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/> [**IXpsOMTileBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)<br/> [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/> [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/> [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)<br/> [**IXpsOMLinearGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> [**IXpsOMRadialGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | Un pincel se usa para rellenar un área o una línea.<br/>                                                                                                                                             |
| [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/>         | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Proporciona rellenos o trazos de color sólido. <br/>                                                                                                                                                |
| [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/>                 | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Proporciona un objeto visual como una ruta de acceso, un glifo o un lienzo, o un objeto visual parcial que se va a usar como relleno de tiling o trazo. <br/>                                                                  |
| [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/>                   | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Proporciona una imagen (o una imagen parcial) que se va a usar como relleno de tiling o trazo. <br/>                                                                                                           |
| [**IXpsOMLinearGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Proporciona un degradado lineal que se va a usar como relleno o trazo. <br/>                                                                                                                            |
| [**IXpsOMRadialGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Proporciona un degradado radial que se usará como relleno o trazo. <br/>                                                                                                                            |
| [**IXpsOMGradientStop**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop)<br/>               | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Define un único punto de inflexión de valor de color dentro de un degradado lineal o radial. <br/>                                                                                                     |
| [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/>                       | [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>                                                                                                                                                                                                                                                                                                                                                                                             | Proporciona una definición de una región vectorial que se usará como región de recorte o definición de ruta de acceso. Consta de una o varias [**interfaces IXpsOMGeometryFigure.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) <br/> |
| [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>           | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Parte de una definición de región a la que hace referencia una [**interfaz IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) y que consta de uno o varios segmentos. <br/>                                    |
| [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/>         | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Especifica la transformación de matriz afín que se va a aplicar al objeto durante la representación. <br/>                                                                                              |



 

## <a name="contents"></a>Contenido

-   [Pinceles DE OM XPS](xps-object-model-brushes.md)
-   [Degradados DE OM xpS](xps-object-model-gradients.md)
-   [Objetos de geometría XPS OM](xps-object-model-geometry-objects.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IXpsOMPath (interfaz)**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[**IXpsOMDashCollection (interfaz)**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)
</dt> <dt>

[**IXpsOMMatrixTransform (interfaz)**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)
</dt> </dl>

 

 




