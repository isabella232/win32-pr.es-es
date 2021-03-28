---
description: Una transformación global es una transformación que se aplica a todos los elementos dibujados por un objeto gráfico determinado.
ms.assetid: 9f744c2a-f1f3-4a7e-ab0c-37aa1df01623
title: Transformaciones globales y locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2682fef6a6236b9da7ec0ec1e5ab5484ad9f90d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561233"
---
# <a name="global-and-local-transformations"></a>Transformaciones globales y locales

Una transformación global es una transformación que se aplica a todos los elementos dibujados por un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) determinado. Para crear una transformación global, construya un objeto **Graphics** y, a continuación, llame a su método [**Graphics:: SetTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) . El método **Graphics:: SetTransform** manipula un objeto de [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) que está asociado al objeto **Graphics** . La transformación almacenada en ese objeto de **matriz** se denomina *transformación universal*. La transformación universal puede ser una transformación afín simple o una secuencia compleja de transformaciones afines, pero independientemente de su complejidad, la transformación universal se almacena en un objeto de **matriz** único.

La clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona varios métodos para crear una transformación universal compuesta: [**Graphics:: MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics:: ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform)y [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform). En el ejemplo siguiente se dibuja una elipse dos veces: una vez antes de crear una transformación universal y otra después de. La transformación se escala primero mediante un factor de 0,5 en la dirección y, a continuación, convierte 50 unidades en la dirección x y, a continuación, gira 30 grados.


```
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
myGraphics.ScaleTransform(1.0f, 0.5f);
myGraphics.TranslateTransform(50.0f, 0.0f, MatrixOrderAppend);
myGraphics.RotateTransform(30.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
```



En la ilustración siguiente se muestra la elipse original y la elipse transformada.

![captura de pantalla de una ventana que contiene dos puntos suspensivos superpuestos; uno es más estrecho y girado](images/aboutgdip05-art14.png)

> [!Note]  
> En el ejemplo anterior, la elipse gira sobre el origen del sistema de coordenadas, que se encuentra en la esquina superior izquierda del área cliente. Esto genera un resultado diferente que la rotación de la elipse sobre su propio centro.

 

Una transformación local es una transformación que se aplica a un elemento específico que se va a dibujar. Por ejemplo, un objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) tiene un método [**GraphicsPath:: transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) que le permite transformar los puntos de datos de esa ruta de acceso. En el ejemplo siguiente se dibuja un rectángulo sin transformación y un trazado con una transformación de giro. (Suponga que no hay una transformación universal).


```
 
Matrix myMatrix;
myMatrix.Rotate(45.0f);
myGraphicsPath.Transform(&myMatrix);
myGraphics.DrawRectangle(&myPen, 10, 10, 100, 50);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



Puede combinar la transformación universal con transformaciones locales para lograr una variedad de resultados. Por ejemplo, puede usar la transformación universal para revisar el sistema de coordenadas y usar transformaciones locales para girar y escalar objetos dibujados en el nuevo sistema de coordenadas.

Supongamos que desea un sistema de coordenadas que tenga su origen de 200 píxeles desde el borde izquierdo del área cliente y 150 píxeles desde la parte superior del área cliente. Además, supongamos que desea que la unidad de medida sea el píxel, con el eje x que apunta hacia la derecha y el eje y que señala hacia arriba. El sistema de coordenadas predeterminado tiene el eje y apunta hacia abajo, por lo que debe realizar una reflexión en el eje horizontal. En la ilustración siguiente se muestra la matriz de este tipo de reflexión.

![Ilustración en la que se muestra una matriz de tres por tres](images/aboutgdip05-art15.png)

A continuación, supongamos que necesita realizar una traducción de 200 unidades a la derecha y las unidades de 150.

En el ejemplo siguiente se establece el sistema de coordenadas que se acaba de describir estableciendo la transformación universal de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .


```
Matrix myMatrix(1.0f, 0.0f, 0.0f, -1.0f, 0.0f, 0.0f);
myGraphics.SetTransform(&myMatrix);
myGraphics.TranslateTransform(200.0f, 150.0f, MatrixOrderAppend);
```



El código siguiente (colocado después del código en el ejemplo anterior) crea una ruta de acceso que consta de un único rectángulo con la esquina inferior izquierda en el origen del nuevo sistema de coordenadas. El rectángulo se rellena una vez sin transformación local y una vez con una transformación local. La transformación local se compone de un escalado horizontal mediante un factor de 2 seguido de una rotación de 30 grados.


```
// Create the path.
GraphicsPath myGraphicsPath;
Rect myRect(0, 0, 60, 60);
myGraphicsPath.AddRectangle(myRect);

// Fill the path on the new coordinate system.
// No local transformation
myGraphics.FillPath(&mySolidBrush1, &myGraphicsPath);

// Transform the path.
Matrix myPathMatrix;
myPathMatrix.Scale(2, 1);
myPathMatrix.Rotate(30, MatrixOrderAppend);
myGraphicsPath.Transform(&myPathMatrix);

// Fill the transformed path on the new coordinate system.
myGraphics.FillPath(&mySolidBrush2, &myGraphicsPath);
```



En la ilustración siguiente se muestra el nuevo sistema de coordenadas y los dos rectángulos.

![captura de pantalla de un eje x e y, y un cuadrado azul superpuesto con un rectagle semitransparente girado en torno a la esquina inferior izquierda](images/aboutgdip05-art16.png)

 

 



