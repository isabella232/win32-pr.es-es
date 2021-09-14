---
title: Porting Polygons and Quadri drones (Porting Polygons and Quadri drones)
description: Tenga en cuenta los siguientes puntos al portear polígonos y cuadráteros.
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- Porte de IRIS GL, cuadrrículos
- porting from IRIS GL,quadrilaterals
- porting to OpenGL from IRIS GL,quadri deltas
- Porte de OpenGL desde IRIS GL, cuadrrículos
- funciones de dibujo, cuadriláteros
- Cuadriláteros
- Porte de IRIS GL, polígonos
- porting from IRIS GL,polygons
- porting to OpenGL from IRIS GL,polygons
- Porte de OpenGL desde IRIS GL, polygons
- funciones de dibujo, polígonos
- polygons,porting from IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7900b44051cab9590be11198c8b01af0b7c10244
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073998"
---
# <a name="porting-polygons-and-quadrilaterals"></a>Porting Polygons and Quadri drones (Porting Polygons and Quadri drones)

Tenga en cuenta los siguientes puntos al portear polígonos y cuadráteros:

-   No hay ningún equivalente directo para **cóncavo****(TRUE).** En su lugar, puede usar las rutinas de teselación en GLU, descritas en [Polígonos de teselación](tessellating-polygons.md).
-   Los modos de polígono se establecen de forma diferente.
-   Estas funciones de dibujo de polígono no tienen equivalentes directos en OpenGL: la **familia poly** de rutinas; la **familia polf** de rutinas; **pmv**, **pdr** y **pclos**; **rpmv** y **rpdr**; **splf**; y **spclos**.

Si el código GL de IRIS usa estas funciones, tendrá que volver a escribir el código mediante [**glBegin**](glbegin.md) \_ (GL POLYGON).

En la tabla siguiente se enumeran las funciones de dibujo de polígonos IRIS GL y sus funciones OpenGL equivalentes.



| Función IRIS GL         | Función OpenGL                                                    | Significado                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| **bgnpolygonendpolygon** | [**glBegin**](glbegin.md) ( GL \_ POLYGON )[**glEnd**](glend.md)   | Los vértices definen el límite de un polígono convexa simple.    |
|                          | **glBegin**(GL \_ QUADS )**glEnd**<br/>                       | Interpreta los vértices de los vértices como cuadrículos.    |
| **bgnqstripendqstrip**   | [**glBegin**](glbegin.md) ( GL \_ QUAD STRIP ) \_ **glEnd**<br/> | Interpreta los vértices como franjas vinculadas de cuadrículos. |
|                          | [glEdgeFlag](gledgeflag-functions.md)                             |                                                         |
| **polymode**             | [**glPolygonMode**](glpolygonmode.md)                             | Establece el modo de dibujo de polígono.                              |
| **rectrectf**<br/> | [glRect](glrect-functions.md)                                     | Dibuja un rectángulo.                                      |
| **sboxsboxf**<br/> |                                                                    | Dibuja un rectángulo alineado con la pantalla.                       |



 

??

## <a name="porting-polygon-modes"></a>Porte de modos de polígono

La función OpenGL [**glPolygonMode**](glpolygonmode.md) permite especificar a qué lado de un polígono (la parte posterior o la parte delantera) se aplica el modo. La sintaxis es:

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

donde face es uno de los siguientes:



|Valor de GLenum                      |  Significado                                                          |
|----------------------|------------------------------------------------------------|
| GL \_ FRONT            | modo que se aplica a los polígonos orientados al frente                |
| GL \_ BACK             | modo que se aplica a los polígonos orientados hacia atrás                 |
| GL \_ FRONT \_ Y \_ BACK | modo que se aplica a los polígonos orientados hacia delante y hacia atrás |



 

El modo \_ GL FRONT AND BACK es equivalente a la función \_ \_ **polymode** IRIS GL. En la tabla siguiente se enumeran los modos de polígono IRIS GL y sus modos OpenGL equivalentes.



| Modo GL de IRIS | Modo OpenGL | Significado                                       |
|--------------|-------------|-----------------------------------------------|
| PYM \_ POINT   | GL \_ POINT   | Dibuja los vértices como puntos.                     |
| PYM \_ LINE    | GL \_ LINE    | Dibuja los bordes de los límites como segmentos de línea.        |
| PYM \_ FILL    | GL \_ FILL    | Dibuja relleno interior de polígono.                |
| PYM \_ HOLLOW  |             | Rellena solo los píxeles interiores en los límites. |



 

## <a name="porting-polygon-stipples"></a>Porting Polygon PolygonPples

Al portear polígonos IRIS GL, tenga en cuenta los siguientes puntos:

-   OpenGL no usa tablas para polígonos de polígonos. solo se mantiene un patrón detippla. Puede usar listas para mostrar para almacenar diferentes patrones de información sobre la información.
-   El tamaño del mapa de bits de latippla de polígono OpenGL siempre es un patrón de 32 x 32 bits.
-   La codificación de stipple se ve afectada [**por glPixelStore.**](glpixelstore-functions.md)

Para obtener más información sobre cómo portear polígonos, vea [Porting Pixel Operations](porting-pixel-operations.md).

En la tabla siguiente se enumeran las funciones detippla de polígono de IRIS GL y sus funciones OpenGL equivalentes.



| Función IRIS GL | Función OpenGL                                    | Significado                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| **defpattern**   | [**glPolygonStipple**](glpolygonstipple.md)       | Establece el patrón detippla.                             |
| **setpattern**   |                                                    | OpenGL mantiene solo un patrón detippla de polígono.        |
| **getpattern**   | [**glGetPolygonStipple**](glgetpolygonstipple.md) | Devuelve el mapa de bits de stipple (que se usa para devolver un índice). |



 

En OpenGL, puede habilitar y deshabilitar la tuplida de polígonos pasando GL POLYGON STIPPLE como parámetro para \_ \_ [**glEnable**](glenable.md) [**y glDisable.**](gldisable.md)

En el siguiente ejemplo de código OpenGL se muestra la liza de polígonos:


```C++
void display(void) 
{ 
    GLubyte fly[] = { 
      0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 
      0x03, 0x80, 0x01, 0xC0, 0x06, 0xC0, 0x03, 0x60, 
      0x04, 0x60, 0x06, 0x20, 0x04, 0x30, 0x0C, 0x20, 
      0x04, 0x18, 0x18, 0x20, 0x04, 0x0C, 0x30, 0x20, 
      0x04, 0x06, 0x60, 0x20, 0x44, 0x03, 0xC0, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x66, 0x01, 0x80, 0x66, 0x33, 0x01, 0x80, 0xCC, 
      0x19, 0x81, 0x81, 0x98, 0x0C, 0xC1, 0x83, 0x30, 
      0x07, 0xe1, 0x87, 0xe0, 0x03, 0x3f, 0xfc, 0xc0, 
      0x03, 0x31, 0x8c, 0xc0, 0x03, 0x33, 0xcc, 0xc0, 
      0x06, 0x64, 0x26, 0x60, 0x0c, 0xcc, 0x33, 0x30, 
      0x18, 0xcc, 0x33, 0x18, 0x10, 0xc4, 0x23, 0x08, 
      0x10, 0x63, 0xC6, 0x08, 0x10, 0x30, 0x0c, 0x08, 
      0x10, 0x18, 0x18, 0x08, 0x10, 0x00, 0x00, 0x08 
    }; 
    GLubyte halftone[] = { 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55 
    }; 
 
    glClear (GL_COLOR_BUFFER_BIT); 
 
/*  draw all polygons in white*/ 
    glColor3f (1.0, 1.0, 1.0); 
 
/*  draw one solid, unstippled rectangle,*/ 
/*  then two stippled rectangles*/ 
    glRectf (25.0, 25.0, 125.0, 125.0); 
    glEnable (GL_POLYGON_STIPPLE); 
    glPolygonStipple (fly); 
    glRectf (125.0, 25.0, 225.0, 125.0); 
    glPolygonStipple (halftone); 
    glRectf (225.0, 25.0, 325.0, 125.0); 
    glDisable (GL_POLYGON_STIPPLE); 
 
    glFlush (); 
}
```



## <a name="porting-tessellated-polygons"></a>Porting Tessellated Polygons

En IRIS GL, se usa **cóncavo**(**TRUE**) y, a continuación, **bgnpolygon** para dibujar polígonos cóncavos. OpenGL GLU incluye funciones que puede usar para dibujar polígonos cóncavos.

**Para dibujar un polígono cóncavo con OpenGL**

1.  Cree un objeto de teselación.
2.  Defina las devoluciones de llamada que se usarán para procesar los triángulos generados por el teselador.
3.  Especifique el polígono cóncavo que se va a teselar.

En la tabla siguiente se enumeran las funciones de OpenGL para dibujar polígonos teselados.



| Función GLU de OpenGL                        | Significado                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [**gluNewTess**](glunewtess.md)           | Crea un nuevo objeto de teselación.                                 |
| [**gluDeleteTess**](gludeletetess.md)     | Elimina un objeto de teselación.                                     |
| [*gluTessCallback*](glutess.md)           |                                                                    |
| [**gluBeginPolygon**](glubeginpolygon.md) | Comienza la especificación del polígono.                                  |
| [**gluTessVertex**](glutessvertex.md)     | Especifica un vértice de polígono en un contorno.                           |
| [**gluNextContour**](glunextcontour.md)   | Indica que la siguiente serie de vértices describe un nuevo contorno. |
| [**gluEndPolygon**](gluendpolygon.md)     | Finaliza la especificación del polígono.                                    |



 

 

 





