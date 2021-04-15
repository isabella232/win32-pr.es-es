---
description: En esta sección se describe cómo usar las interfaces relacionadas con la ruta de acceso de la API de documento XPS en un OM XPS.
ms.assetid: 4e76355a-ad53-4177-b8c7-3e768a1d4e3f
title: Trabajar con las interfaces de ruta de acceso XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca66b65c6f20dc3b585de706e223df1f76d518a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545830"
---
# <a name="working-with-xps-om-path-interfaces"></a>Trabajar con las interfaces de ruta de acceso XPS OM

En esta sección se describe cómo usar las interfaces relacionadas con la ruta de acceso de la API de documento XPS en un OM XPS.



| Nombre de interfaz                                                            | Elementos secundarios conceptuales                                                                                                                                                                                                                                                                                                                                                                                                                                         | Descripción                                                                                                                                                                                       |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                               | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Describe un elemento de trazado gráfico.<br/>                                                                                                                                                    |
| [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/>                             | [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/> [**IXpsOMTileBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)<br/> [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/> [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/> [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)<br/> [**IXpsOMLinearGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> [**IXpsOMRadialGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | Un pincel se usa para rellenar un área o una línea.<br/>                                                                                                                                             |
| [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/>         | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Proporciona relleno o trazos de color sólidos. <br/>                                                                                                                                                |
| [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/>                 | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Proporciona un objeto visual como, por ejemplo, una ruta de acceso, glifo o lienzo, o un objeto visual parcial que se va a usar como relleno o trazo de mosaico. <br/>                                                                  |
| [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/>                   | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Proporciona una imagen (o imagen parcial) que se va a usar como relleno o trazo de mosaico. <br/>                                                                                                           |
| [**IXpsOMLinearGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Proporciona un degradado lineal que se va a utilizar como relleno o trazo. <br/>                                                                                                                            |
| [**IXpsOMRadialGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Proporciona un degradado radial que se va a usar como relleno o trazo. <br/>                                                                                                                            |
| [**IXpsOMGradientStop**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop)<br/>               | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Define un punto de inflexión de valor de color único dentro de un degradado lineal o radial. <br/>                                                                                                     |
| [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/>                       | [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>                                                                                                                                                                                                                                                                                                                                                                                             | Proporciona una definición de una región vectorial que se va a usar como una definición de ruta o región de recorte. Consta de una o más interfaces [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) . <br/> |
| [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>           | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Parte de una definición de región a la que hace referencia una interfaz [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) y que consta de uno o más segmentos. <br/>                                    |
| [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/>         | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Especifica la transformación de matriz afín que se va a aplicar al objeto durante la representación. <br/>                                                                                              |



 

## <a name="contents"></a>Contenido

-   [Pinceles de XPS OM](xps-object-model-brushes.md)
-   [Degradados de XPS OM](xps-object-model-gradients.md)
-   [Objetos de geometría de XPS OM](xps-object-model-geometry-objects.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[**Interfaz IXpsOMDashCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)
</dt> <dt>

[**Interfaz IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)
</dt> </dl>

 

 




