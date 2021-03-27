---
description: Para rellenar una forma con un color sólido, cree un objeto SolidBrush y, a continuación, pase la dirección de ese objeto SolidBrush como argumento a uno de los métodos Fill de la clase Graphics.
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: Rellenar una forma con un color sólido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4a6221d84c4a891d377d974f168468917799e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997497"
---
# <a name="filling-a-shape-with-a-solid-color"></a>Rellenar una forma con un color sólido

Para rellenar una forma con un color sólido, cree un objeto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) y, a continuación, pase la dirección de ese objeto **SolidBrush** como argumento a uno de los métodos Fill de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . En el ejemplo siguiente se muestra cómo rellenar una elipse con el color rojo:


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



En el ejemplo anterior, el constructor [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) toma una referencia de objeto de [**color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) como su único argumento. Los valores utilizados por el constructor de **color** representan los componentes alfa, rojo, verde y azul del color. Cada uno de estos valores debe estar en el intervalo comprendido entre 0 y 255. El primer 255 indica que el color es totalmente opaco y el segundo 255 indica que el componente rojo tiene una intensidad máxima. Los dos ceros indican que los componentes verde y azul tienen una intensidad de 0.

Los cuatro números (0, 0, 100, 60) pasados al método [**Graphics:: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) especifican la ubicación y el tamaño del rectángulo delimitador de la elipse. El rectángulo tiene una esquina superior izquierda de (0,0), un ancho de 100 y un alto de 60.

 

 
