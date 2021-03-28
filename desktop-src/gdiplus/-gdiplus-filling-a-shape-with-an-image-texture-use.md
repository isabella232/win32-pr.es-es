---
description: Puede rellenar una forma cerrada con una textura mediante la clase Image y la clase TextureBrush.
ms.assetid: 12e1e132-a93f-4438-8a1d-9036a43a8fd8
title: Rellenar una forma con una textura de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3f1bf6ba04311310ab1985de1d1aaccd45db43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156188"
---
# <a name="filling-a-shape-with-an-image-texture"></a>Rellenar una forma con una textura de imagen

Puede rellenar una forma cerrada con una textura mediante la clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y la clase [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .

En el ejemplo siguiente se rellena una elipse con una imagen. El código crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y, a continuación, pasa la dirección de ese objeto de **imagen** como argumento a un constructor [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) . La tercera instrucción de código escala la imagen y la cuarta instrucción rellena la elipse con copias repetidas de la imagen escalada:


```
Image image(L"ImageFile.jpg");
TextureBrush tBrush(&image);
stat = tBrush.SetTransform(&Matrix(75.0/640.0, 0.0f, 0.0f,
   75.0/480.0, 0.0f, 0.0f));
stat = graphics.FillEllipse(&tBrush,Rect(0, 150, 150, 250));
```



En el ejemplo de código anterior, el método [**TextureBrush:: SetTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) establece la transformación que se aplica a la imagen antes de dibujarse. Supongamos que la imagen original tiene un ancho de 640 píxeles y un alto de 480 píxeles. La transformación reduce la imagen a 75 × 75, estableciendo los valores de escalado horizontal y vertical.

> [!Note]  
> En el ejemplo anterior, el tamaño de la imagen es 75 × 75 y el tamaño de la elipse es 150 × 250. Dado que la imagen es más pequeña que la elipse que está rellenando, la elipse se coloca en mosaico con la imagen. La disposición en mosaico significa que la imagen se repite horizontal y verticalmente hasta que se alcanza el límite de la forma. Para obtener más información sobre el mosaico, vea [organizar una forma en mosaico con una imagen](-gdiplus-tiling-a-shape-with-an-image-use.md).

 

 

 



