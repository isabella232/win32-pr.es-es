---
description: El estado de gráficos &\# 8212; la región de recorte, las transformaciones y la configuración de calidad &\# 8212; se almacenan en un objeto gráfico.
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: Contenedores de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8bf6469d0835137be1bb76b7727fd961bba16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104549993"
---
# <a name="graphics-containers"></a>Contenedores de gráficos

El estado de los gráficos (región de recorte, transformaciones y configuración de calidad) se almacena en un objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Windows GDI+ le permite reemplazar o aumentar temporalmente parte del estado en un objeto **gráfico** mediante un contenedor. Para iniciar un contenedor, debe llamar al método [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) de un objeto **Graphics** y finalizar un contenedor llamando al método [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) . Entre los **gráficos:: BeginContainer** y **Graphics:: EndContainer**, cualquier cambio de estado que realice en el objeto de **gráficos** pertenece al contenedor y no sobrescribe el estado existente del objeto de **gráficos** .

En el ejemplo siguiente se crea un contenedor dentro de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . La transformación universal del objeto **Graphics** es una traducción de 200 unidades a la derecha y la transformación universal del contenedor es una unidad de traducción de 100 unidades.


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



Tenga en cuenta que en el ejemplo anterior, la instrucción `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` realizada entre las llamadas a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) y [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) genera un rectángulo diferente al de la misma instrucción realizada después de la llamada a **Graphics:: EndContainer**. Solo la traducción horizontal se aplica a la llamada **DrawRectangle** realizada fuera del contenedor. Ambas transformaciones (la traslación horizontal de 200 unidades y la conversión vertical de las unidades 100) se aplican a la llamada de [**gráficos::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) realizada dentro del contenedor. En la ilustración siguiente se muestran los dos rectángulos.

![captura de pantalla de una ventana con dos rectángulos dibujados con un lápiz azul, uno situado encima del otro](images/aboutgdip05-art17.png)

Los contenedores se pueden anidar dentro de contenedores. En el ejemplo siguiente se crea un contenedor dentro de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y otro contenedor en el primer contenedor. La transformación universal del objeto **Graphics** es una traducción de 100 unidades en la dirección x y 80 unidades en la dirección y. La transformación universal del primer contenedor es una rotación de 30 grados. La transformación universal del segundo contenedor es un escalado mediante un factor de 2 en la dirección x. Se realiza una llamada al método [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) en el segundo contenedor.


```
myGraphics.TranslateTransform(100.0f, 80.0f, MatrixOrderAppend);

container1 = myGraphics.BeginContainer();
   myGraphics.RotateTransform(30.0f, MatrixOrderAppend);

   container2 = myGraphics.BeginContainer();
      myGraphics.ScaleTransform(2.0f, 1.0f);
      myGraphics.DrawEllipse(&myPen, -30, -20, 60, 40);
   myGraphics.EndContainer(container2);

myGraphics.EndContainer(container1);
```



En la ilustración siguiente se muestra la elipse.

![captura de pantalla de una ventana que contiene una elipse azul girada con su centro etiquetada como (100, 80)](images/aboutgdip05-art18.png)

Tenga en cuenta que las tres transformaciones se aplican a la llamada de [**gráficos::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) realizada en el segundo contenedor (interior). Tenga en cuenta también el orden de las transformaciones: primera escala, girar y después trasladar. La transformación más interna se aplica primero y la transformación más externa se aplica en último lugar.

Cualquier propiedad de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) se puede establecer dentro de un contenedor (entre las llamadas a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) y [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)). Por ejemplo, se puede establecer una región de recorte dentro de un contenedor. Cualquier dibujo realizado dentro del contenedor se restringe a la región de recorte de ese contenedor y también se restringe a las regiones de recorte de cualquier contenedor externo y la región de recorte del propio objeto de **gráficos** .

Las propiedades descritas hasta ahora, la transformación universal y la región de recorte, se combinan mediante contenedores anidados. Otras propiedades se reemplazan temporalmente por un contenedor anidado. Por ejemplo, si establece el modo de suavizado en SmoothingModeAntiAlias dentro de un contenedor, cualquier método de dibujo llamado dentro de ese contenedor usará el modo de suavizado antialias, pero los métodos de dibujo llamados después de [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) usarán el modo de suavizado que estaba antes de la llamada a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).

Para obtener otro ejemplo de cómo combinar las transformaciones del mundo de un objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un contenedor, supongamos que desea dibujar un ojo y colocarlo en varias ubicaciones en una secuencia de caras. En el ejemplo siguiente se dibuja un ojo centrado en el origen del sistema de coordenadas.


```
void DrawEye(Graphics* pGraphics)
{
   GraphicsContainer eyeContainer;
   
   eyeContainer = pGraphics->BeginContainer();

      Pen myBlackPen(Color(255, 0, 0, 0));
      SolidBrush myGreenBrush(Color(255, 0, 128, 0));
      SolidBrush myBlackBrush(Color(255, 0, 0, 0));

      GraphicsPath myTopPath;
      myTopPath.AddEllipse(-30, -50, 60, 60);

      GraphicsPath myBottomPath;
      myBottomPath.AddEllipse(-30, -10, 60, 60);

      Region myTopRegion(&myTopPath);
      Region myBottomRegion(&myBottomPath);

      // Draw the outline of the eye.
      // The outline of the eye consists of two ellipses.
      // The top ellipse is clipped by the bottom ellipse, and
      // the bottom ellipse is clipped by the top ellipse.
      pGraphics->SetClip(&myTopRegion);
      pGraphics->DrawPath(&myBlackPen, &myBottomPath);
      pGraphics->SetClip(&myBottomRegion);
      pGraphics->DrawPath(&myBlackPen, &myTopPath);

      // Fill the iris.
      // The iris is clipped by the bottom ellipse.
      pGraphics->FillEllipse(&myGreenBrush, -10, -15, 20, 22);

      // Fill the pupil.
      pGraphics->FillEllipse(&myBlackBrush, -3, -7, 6, 9);

   pGraphics->EndContainer(eyeContainer);
}
```



En la ilustración siguiente se muestra el ojo y los ejes de coordenadas.

![Ilustración en la que se muestra un ojo compuesto de tres puntos suspensivos: uno para el contorno, iris y Pupil](images/aboutgdip05-art19.png)

La función DrawEye, definida en el ejemplo anterior, recibe la dirección de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y crea inmediatamente un contenedor en ese objeto **Graphics** . Este contenedor aísla cualquier código que llame a la función DrawEye desde la configuración de propiedades realizada durante la ejecución de la función DrawEye. Por ejemplo, el código de la función DrawEye establece la región de recorte del objeto **Graphics** , pero cuando DrawEye devuelve el control a la rutina que realiza la llamada, la región de recorte será como estaba antes de la llamada a DrawEye.

En el ejemplo siguiente se dibujan tres elipses (caras), cada una de ellas con un ojo.


```
// Draw an ellipse with center at (100, 100).
myGraphics.TranslateTransform(100.0f, 100.0f);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Draw the eye at the center of the ellipse.
DrawEye(&myGraphics);

// Draw an ellipse with center at 200, 100.
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Rotate the eye 40 degrees, and draw it 30 units above
// the center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.RotateTransform(-40.0f);
   myGraphics.TranslateTransform(0.0f, -30.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);

// Draw a ellipse with center at (300.0f, 100.0f).
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Stretch and rotate the eye, and draw it at the 
// center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.ScaleTransform(2.0f, 1.5f);
   myGraphics.RotateTransform(45.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);
```



En la ilustración siguiente se muestran los tres puntos suspensivos.

![captura de pantalla de una ventana con tres elipses, cada una de las cuales contiene un ojo con un tamaño y una rotación diferentes](images/aboutgdip05-art20.png)

En el ejemplo anterior, todas las elipses se dibujan con la llamada `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` , que dibuja una elipse centrada en el origen del sistema de coordenadas. Las elipses se desplazan de la esquina superior izquierda del área cliente estableciendo la transformación universal del objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . La instrucción hace que la primera elipse se Centre en (100, 100). La instrucción hace que el centro de la segunda elipse sea 100 unidades a la derecha del centro de la primera elipse. Del mismo modo, el centro de la tercera elipse es 100 unidades a la derecha del centro de la segunda elipse.

Los contenedores del ejemplo anterior se usan para transformar el ojo en relación con el centro de una elipse determinada. El primer ojo se dibuja en el centro de la elipse sin transformación, por lo que la llamada a DrawEye no está dentro de un contenedor. El segundo ojo gira 40 grados y se dibujan 30 unidades por encima del centro de la elipse, por lo que se llama a la función DrawEye y a los métodos que establecen la transformación dentro de un contenedor. El tercer ojo se estira y gira y se dibuja en el centro de la elipse. Al igual que en el segundo ojo, se llama a la función DrawEye y a los métodos que establecen la transformación dentro de un contenedor.

 

 
