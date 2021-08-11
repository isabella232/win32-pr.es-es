---
description: Estado de &8212; región de recorte, transformaciones y configuración de \# calidad &8212; se almacena en \# un objeto Graphics.
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: Contenedores de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26af00a17f793a1f3ce587963343556b8c4ad685f930b707bd81de1008d610ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248674"
---
# <a name="graphics-containers"></a>Contenedores de gráficos

El estado de los gráficos (región de recorte, transformaciones y configuración de calidad) se almacena en un [**objeto Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Windows GDI+ permite reemplazar o aumentar temporalmente parte del estado en un objeto **Graphics** mediante un contenedor. Para iniciar un contenedor, llame al método [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) de un objeto **Graphics** y finalice un contenedor mediante una llamada al [**método Graphics::EndContainer.**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) Entre **Graphics::BeginContainer** y **Graphics::EndContainer**, los cambios de estado que realice en el objeto **Graphics** pertenecen al contenedor y no sobrescriben el estado existente del **objeto Graphics.**

En el ejemplo siguiente se crea un contenedor dentro de un [**objeto Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) La transformación del mundo del objeto **Graphics** es una traducción de 200 unidades a la derecha y la transformación del mundo del contenedor es una traducción de 100 unidades hacia abajo.


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



Tenga en cuenta que, en el ejemplo anterior, la instrucción realizada entre las llamadas `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` a [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) y [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) genera un rectángulo diferente de la misma instrucción realizada después de la llamada a **Graphics::EndContainer**. Solo la traducción horizontal se aplica a la **llamada DrawRectangle** realizada fuera del contenedor. Ambas transformaciones (la traducción horizontal de 200 unidades y la traducción vertical de 100 unidades) se aplican a la llamada [**Graphics::D rawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) realizada dentro del contenedor. En la ilustración siguiente se muestran los dos rectángulos.

![captura de pantalla de una ventana con dos rectángulos dibujados con un lápiz azul, uno situado encima del otro](images/aboutgdip05-art17.png)

Los contenedores se pueden anidar dentro de los contenedores. En el ejemplo siguiente se crea un contenedor dentro de un [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y otro contenedor dentro del primer contenedor. La transformación world del objeto **Graphics es** una traducción de 100 unidades en la dirección x y 80 unidades en la dirección y. La transformación del mundo del primer contenedor es una rotación de 30 grados. La transformación del mundo del segundo contenedor es un escalado por un factor de 2 en la dirección x. Se realiza una llamada [**al método Graphics::D rawVelopse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) dentro del segundo contenedor.


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

![captura de pantalla de una ventana que contiene una elipse azul girada con su centro etiquetado como (100,80)](images/aboutgdip05-art18.png)

Tenga en cuenta que las tres transformaciones se aplican a la llamada [**a Graphics::D rawVelopse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) realizada en el segundo contenedor (más interno). Tenga en cuenta también el orden de las transformaciones: primero escale, luego rote y, a continuación, traduzca. La transformación más interna se aplica primero y la transformación más externa se aplica en último lugar.

Cualquier propiedad de un [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) se puede establecer dentro de un contenedor (entre llamadas a [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) y [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)). Por ejemplo, una región de recorte se puede establecer dentro de un contenedor. Cualquier dibujo que se haga dentro del contenedor se restringirá a la región de recorte de ese contenedor y también se restringirá a las regiones de recorte de los contenedores externos y a la región de recorte del propio objeto **Graphics.**

Las propiedades que se han analizado hasta ahora (la transformación mundial y la región de recorte) se combinan mediante contenedores anidados. Otras propiedades se reemplazan temporalmente por un contenedor anidado. Por ejemplo, si establece el modo de suavizado en SmoothingModeAntiAlias dentro de un contenedor, todos los métodos de dibujo a los que se llame dentro de ese contenedor usarán el modo de suavizado antialias, pero los métodos de dibujo llamados después de [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) usarán el modo de suavizado que estaba en su lugar antes de la llamada a [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).

Para otro ejemplo de combinación de las transformaciones del mundo de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un contenedor, supongamos que quiere dibujar un ojo y colocarlo en varias ubicaciones en una secuencia de caras. En el ejemplo siguiente se dibuja un ojo centrado en el origen del sistema de coordenadas.


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

![ilustración en la que se muestra un ojo compuesto por tres puntos suspensivos: uno para el contorno, el iris y la alumno](images/aboutgdip05-art19.png)

La función DrawEye, definida en el ejemplo anterior, recibe la dirección de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y crea inmediatamente un contenedor dentro de ese **objeto Graphics.** Este contenedor aísla cualquier código que llame a la función DrawEye de la configuración de propiedades realizada durante la ejecución de la función DrawEye. Por ejemplo, el código de la función DrawEye establece la región de recorte del objeto **Graphics,** pero cuando DrawEye devuelve el control a la rutina de llamada, la región de recorte será como antes de la llamada a DrawEye.

En el ejemplo siguiente se dibujan tres elipses (caras), cada una con un ojo dentro.


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

![captura de pantalla de una ventana con tres puntos suspensivos, cada uno de los cuales contiene un ojo con un tamaño y rotación diferentes](images/aboutgdip05-art20.png)

En el ejemplo anterior, todos los puntos suspensivos se dibujan con la llamada , que dibuja una elipse centrada en el origen `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` del sistema de coordenadas. Los puntos suspensivos se alejan de la esquina superior izquierda del área cliente estableciendo la transformación world del [**objeto Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) La instrucción hace que la primera elipse se centre en (100, 100). La instrucción hace que el centro de la segunda elipse sea de 100 unidades a la derecha del centro de la primera elipse. Del mismo modo, el centro de la tercera elipse está a 100 unidades a la derecha del centro de la segunda elipse.

Los contenedores del ejemplo anterior se usan para transformar el ojo en relación con el centro de una elipse determinada. El primer ojo se dibuja en el centro de la elipse sin transformación, por lo que la llamada a DrawEye no está dentro de un contenedor. El segundo ojo gira 40 grados y se dibuja 30 unidades por encima del centro de la elipse, por lo que la función DrawEye y los métodos que establecen la transformación se llaman dentro de un contenedor. El tercer ojo se extiende, gira y dibuja en el centro de la elipse. Al igual que con el segundo ojo, la función DrawEye y los métodos que establecen la transformación se llaman dentro de un contenedor.

 

 
