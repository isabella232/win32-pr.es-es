---
description: Para rellenar una forma con un color sólido, cree un objeto SolidBrush y, a continuación, pase la dirección de ese objeto SolidBrush como argumento a uno de los métodos de relleno de la clase Graphics.
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: Rellenar una forma con un color sólido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ad3ecb5efb3bde32f696db8b97319d89834886eb63a70cd45289e49db03863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036723"
---
# <a name="filling-a-shape-with-a-solid-color"></a>Rellenar una forma con un color sólido

Para rellenar una forma con un color sólido, cree un objeto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) y, a continuación, pase la dirección de ese objeto **SolidBrush** como argumento a uno de los métodos de relleno de la [**clase Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) En el ejemplo siguiente se muestra cómo rellenar una elipse con el color rojo:


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



En el ejemplo anterior, el constructor [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) toma una referencia de objeto [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) como único argumento. Los valores utilizados por el constructor **Color** representan los componentes alfa, rojo, verde y azul del color. Cada uno de estos valores debe estar en el intervalo de 0 a 255. El primer 255 indica que el color es totalmente opaco y el segundo 255 indica que el componente rojo tiene una intensidad completa. Los dos ceros indican que los componentes verde y azul tienen una intensidad de 0.

Los cuatro números (0, 0, 100, 60) pasados al método [**Graphics::FillVelopse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) especifican la ubicación y el tamaño del rectángulo delimitador para la elipse. El rectángulo tiene una esquina superior izquierda de (0, 0), un ancho de 100 y un alto de 60.

 

 
