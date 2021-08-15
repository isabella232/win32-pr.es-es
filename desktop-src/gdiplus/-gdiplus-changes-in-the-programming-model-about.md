---
description: En las secciones siguientes se describen varias maneras en que la programación con Windows GDI+ es diferente de la programación con Windows Interfaz de dispositivo gráfico (GDI).
ms.assetid: 89a154c1-6a49-45d6-a73c-94b0b1567408
title: Cambios en el modelo de programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05dd8b74662d0141405b9d11b9b4446ffb19dd4ef3bfdec788afe7a51a8c681a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249892"
---
# <a name="changes-in-the-programming-model"></a>Cambios en el modelo de programación

En las secciones siguientes se describen varias maneras en que la programación con Windows GDI+ es diferente de la programación con Windows Interfaz de dispositivo gráfico (GDI).

-   [Contextos de dispositivo, identificadores y objetos gráficos](#device-contexts-handles-and-graphics-objects)
-   [Dos maneras de dibujar una línea](#two-ways-to-draw-a-line)
    -   [Dibujar una línea con GDI](#drawing-a-line-with-gdi)
    -   [Dibujar una línea con GDI+ y la interfaz de clase de C++](#drawing-a-line-with-gdi-and-the-c-class-interface)
-   [Lápices, pinceles, rutas de acceso, imágenes y fuentes como parámetros](#pens-brushes-paths-images-and-fonts-as-parameters)
-   [Sobrecarga de métodos](#method-overloading)
-   [No más posición actual](#no-more-current-position)
-   [Métodos independientes para draw y fill](#separate-methods-for-draw-and-fill)
-   [Construcción de regiones](#constructing-regions)

## <a name="device-contexts-handles-and-graphics-objects"></a>Contextos de dispositivo, identificadores y objetos gráficos

Si ha escrito programas con GDI (la interfaz de dispositivo gráfico incluida en versiones anteriores de Windows), está familiarizado con la idea de un contexto de dispositivo (DC). Un contexto de dispositivo es una estructura que Windows para almacenar información sobre las funcionalidades de un dispositivo de visualización determinado y los atributos que especifican cómo se dibujarán los elementos en ese dispositivo. Un contexto de dispositivo para una pantalla de vídeo también está asociado a una ventana determinada de la pantalla. En primer lugar, se obtiene un identificador a un contexto de dispositivo (HDC) y, después, se pasa ese identificador como argumento a las funciones GDI que realmente hacen el dibujo. También se pasa el identificador como argumento a funciones GDI que obtienen o establecen los atributos del contexto del dispositivo.

Al usar GDI+, no tiene que preocuparse tanto por los identificadores y los contextos de dispositivo como cuando se usa GDI. Basta con crear un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y, a continuación, invocar sus métodos en el conocido estilo orientado a objetos: myGraphicsObject.DrawLine(*parameters*). El **objeto Graphics** se encuentra en el núcleo de GDI+ igual que el contexto del dispositivo se encuentra en el núcleo de GDI. El contexto del dispositivo y el objeto **Gráfico** desempeñan roles similares, pero hay algunas diferencias fundamentales entre el modelo de programación basado en identificadores usado con contextos de dispositivo (GDI) y el modelo orientado a objetos que se usa con objetos **gráficos** (GDI+).

El [**objeto Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) al igual que el contexto del dispositivo, está asociado a una ventana determinada de la pantalla y contiene atributos (por ejemplo, el modo de suavizado y la sugerencia de representación de texto) que especifican cómo se dibujarán los elementos. Sin embargo, **el objeto Graphics** no está asociado a un lápiz, pincel, ruta de acceso, imagen o fuente como un contexto de dispositivo. Por ejemplo, en GDI, para poder usar un contexto de dispositivo para dibujar una línea, debe llamar a [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) para asociar un objeto de lápiz al contexto del dispositivo. Esto se conoce como seleccionar el lápiz en el contexto del dispositivo. Todas las líneas dibujadas en el contexto del dispositivo usarán ese lápiz hasta que seleccione otro lápiz. Con GDI+, se pasa un [**objeto Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) como argumento al [método DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) de la **clase Graphics.** Puede usar un objeto **Pen** diferente en cada una de las series de llamadas a DrawLine sin tener que asociar un objeto **Pen** determinado a un **objeto Graphics.**

## <a name="two-ways-to-draw-a-line"></a>Dos maneras de dibujar una línea

Los dos ejemplos siguientes dibujan una línea roja de ancho 3 desde la ubicación (20, 10) hasta la ubicación (200 100). El primer ejemplo llama a GDI y el segundo llama a GDI+ a través de la interfaz de clase de C++.

-   [Dibujar una línea con GDI](#drawing-a-line-with-gdi)
-   [Dibujar una línea con GDI+ y la interfaz de clase de C++](#drawing-a-line-with-gdi-and-the-c-class-interface)

### <a name="drawing-a-line-with-gdi"></a>Dibujar una línea con GDI

Para dibujar una línea con GDI, necesita dos objetos: un contexto de dispositivo y un lápiz. Para obtener un identificador para un contexto de dispositivo, llame a [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)y un identificador a un lápiz mediante una llamada a [CreatePen](/windows/win32/api/wingdi/nf-wingdi-createpen). A continuación, llame a [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) para seleccionar el lápiz en el contexto del dispositivo. Establezca la posición del lápiz en (20, 10) llamando a [MoveToEx](/windows/win32/api/wingdi/nf-wingdi-movetoex) y, a continuación, dibuje una línea desde esa posición de lápiz a (200, 100) llamando a **LineTo**. Tenga en cuenta que MoveToEx y [LineTo](/windows/win32/api/wingdi/nf-wingdi-lineto) reciben **hdc** como argumento.


```
HDC          hdc;
PAINTSTRUCT  ps;
HPEN         hPen;
HPEN         hPenOld;
hdc = BeginPaint(hWnd, &ps);
   hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
   hPenOld = (HPEN)SelectObject(hdc, hPen);
   MoveToEx(hdc, 20, 10, NULL);
   LineTo(hdc, 200, 100);
   SelectObject(hdc, hPenOld);
   DeleteObject(hPen);
EndPaint(hWnd, &ps);
```



### <a name="drawing-a-line-with-gdi-and-the-c-class-interface"></a>Dibujar una línea con GDI+ y la interfaz de clase de C++

Para dibujar una línea con GDI+ y la interfaz de clase de C++, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Pen.**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Tenga en cuenta que no Windows identificadores para estos objetos. En su lugar, se usan constructores para crear una instancia de la clase **Graphics** (un objeto **Graphics)** y una instancia de la clase **Pen** (un **objeto Pen).** Dibujar una línea implica llamar al [**método Graphics::D rawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) de la **clase Graphics.** El primer parámetro del método **Graphics::D rawLine** es un puntero al **objeto Pen.** Se trata de un esquema más sencillo y flexible que seleccionar un lápiz en un contexto de dispositivo, como se muestra en el ejemplo de GDI anterior.


```
HDC          hdc;
PAINTSTRUCT  ps;
Pen*         myPen;
Graphics*    myGraphics;
hdc = BeginPaint(hWnd, &ps);
   myPen = new Pen(Color(255, 255, 0, 0), 3);
   myGraphics = new Graphics(hdc);
   myGraphics->DrawLine(myPen, 20, 10, 200, 100);
   delete myGraphics;
   delete myPen;
EndPaint(hWnd, &ps);
```



## <a name="pens-brushes-paths-images-and-fonts-as-parameters"></a>Lápices, pinceles, rutas de acceso, imágenes y fuentes como parámetros

En los ejemplos anteriores se muestra que [**los objetos Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) se pueden crear y mantener por separado del objeto [**Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) que proporciona los métodos de dibujo. [**Los**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush)objetos Brush , [**GraphicsPath,**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)y [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) también se pueden crear y mantener por separado del **objeto Graphics.** Muchos de los métodos de dibujo proporcionados por la **clase Graphics** reciben un objeto **Brush**, **GraphicsPath,** **Image** **o Font** como argumento. Por ejemplo, la dirección de un objeto **Brush** se pasa como argumento al método [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) y la dirección de un objeto **GraphicsPath** se pasa como argumento al método [**Graphics::D rawPath.**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) De forma similar, las direcciones **de los objetos Image** y **Font** se pasan a los métodos [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_)) [y DrawString.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) Esto contrasta con GDI, donde se selecciona un pincel, una ruta de acceso, una imagen o una fuente en el contexto del dispositivo y, a continuación, se pasa un identificador al contexto del dispositivo como argumento a una función de dibujo.

## <a name="method-overloading"></a>Sobrecarga de métodos

Muchos de los métodos GDI+ están sobrecargados; es decir, varios métodos comparten el mismo nombre, pero tienen listas de parámetros diferentes. Por ejemplo, el [método DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) de la [**clase Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tiene los siguientes formatos:


```
Status DrawLine(IN const Pen* pen,
                IN REAL x1,
                IN REAL y1,
                IN REAL x2,
                IN REAL y2);
Status DrawLine(IN const Pen* pen,
                IN const PointF& pt1,
                IN const PointF& pt2);
Status DrawLine(IN const Pen* pen,
                IN INT x1,
                IN INT y1,
                IN INT x2,
                IN INT y2);
    
Status DrawLine(IN const Pen* pen,
                IN const Point& pt1,
                IN const Point& pt2);
```



Las cuatro variaciones [drawline](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) anteriores reciben un puntero a un objeto [**Pen,**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) las coordenadas del punto inicial y las coordenadas del punto final. Las dos primeras variaciones reciben las coordenadas como números de punto flotante y las dos últimas variaciones reciben las coordenadas como enteros. La primera y la tercera variaciones reciben las coordenadas como una lista de cuatro números independientes, mientras que la segunda y la cuarta variaciones reciben las coordenadas como un par de objetos Point [**(o**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) [**PointF).**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)

## <a name="no-more-current-position"></a>No más posición actual

Tenga en cuenta que en los [métodos DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) mostrados anteriormente tanto el punto inicial como el punto final de la línea se reciben como argumentos. Se trata de una salida del esquema GDI donde se llama a **MoveToEx** para establecer la posición del lápiz actual seguido de **LineTo** para dibujar una línea que comienza en (**x1**, **y1**) y termina en (**x2**, **y2**). GDI+ como un todo ha abandonado la noción de posición actual.

## <a name="separate-methods-for-draw-and-fill"></a>Métodos independientes para draw y fill

GDI+ es más flexible que GDI cuando se trata de dibujar los contornos y rellenar los interiores de formas como rectángulos. GDI tiene una [función Rectangle](/windows/win32/api/wingdi/nf-wingdi-rectangle) que dibuja el contorno y rellena el interior de un rectángulo en un solo paso. El contorno se dibuja con el lápiz seleccionado actualmente y el interior se rellena con el pincel seleccionado actualmente.


```
hBrush = CreateHatchBrush(HS_CROSS, RGB(0, 0, 255));
hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
SelectObject(hdc, hBrush);
SelectObject(hdc, hPen);
Rectangle(hdc, 100, 50, 200, 80);
```



GDI+ métodos independientes para dibujar el contorno y rellenar el interior de un rectángulo. El [método DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tiene la dirección de un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) como uno de sus parámetros y el método [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) tiene la dirección de un objeto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) como uno de sus parámetros.


```
HatchBrush* myHatchBrush = new HatchBrush(
   HatchStyleCross,
   Color(255, 0, 255, 0),
   Color(255, 0, 0, 255));
Pen* myPen = new Pen(Color(255, 255, 0, 0), 3);
myGraphics.FillRectangle(myHatchBrush, 100, 50, 100, 30);
myGraphics.DrawRectangle(myPen, 100, 50, 100, 30);
```



Tenga en cuenta que los métodos [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) y [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) de GDI+ reciben argumentos que especifican el borde izquierdo, la parte superior, el ancho y el alto del rectángulo. Esto contrasta con la función GDI[Rectangle,](/windows/win32/api/wingdi/nf-wingdi-rectangle) que toma argumentos que especifican el borde izquierdo, el borde derecho, la parte superior y la parte inferior del rectángulo. Tenga en cuenta también que el constructor de la [**clase Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) GDI+ tiene cuatro parámetros. Los tres últimos parámetros son los valores rojo, verde y azul habituales. el primer parámetro es el valor alfa, que especifica la medida en que el color que se dibuja se combina con el color de fondo.

## <a name="constructing-regions"></a>Construcción de regiones

GDI proporciona varias funciones para crear regiones: CreateRectRgn, CreateEllpticRgn, CreateRoundRectRgn, CreatePolygonRgn y CreatePolyPolygonRgn. Es posible que la clase [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) de GDI+ tenga constructores análogos que toman rectángulos, elipses, rectángulos redondeados y polígonos como argumentos, pero ese no es el caso. La **clase Region** de GDI+ proporciona un constructor que recibe una referencia de objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) y otro constructor que recibe la dirección de un objeto [**GraphicsPath.**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) Si desea construir una región basada en una elipse, un rectángulo redondeado o un polígono, puede hacerlo fácilmente mediante la creación de un objeto **GraphicsPath** (que contiene una elipse, por ejemplo) y, a continuación, pasar la dirección de ese objeto **GraphicsPath** a un constructor **Region.**

GDI+ facilita la formación de regiones complejas mediante la combinación de formas y rutas de acceso. La [**clase Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) tiene [métodos Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstrectf_)) e [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstgraphicspath)) que puede usar para aumentar una región existente con una ruta de acceso u otra región. Una característica interesante del esquema GDI+ es que un objeto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) no se destruye cuando se pasa como argumento a un constructor **Region.** En GDI, puede convertir una ruta de acceso a una región con la función [PathToRegion,](/windows/win32/api/wingdi/nf-wingdi-pathtoregion) pero la ruta de acceso se destruye en el proceso. Además, un objeto **GraphicsPath** no se destruye cuando su dirección se pasa como argumento a un método Union o Intersect, por lo que puede usar una ruta de acceso determinada como bloque de creación para varias regiones independientes. Esto se muestra en el ejemplo siguiente. Suponga que **onePath es** un puntero a un objeto **GraphicsPath** (simple o complejo) que ya se ha inicializado.


```
Region  region1(rect1);
Region  region2(rect2);
region1.Union(onePath);
region2.Intersect(onePath);
```



 

 
