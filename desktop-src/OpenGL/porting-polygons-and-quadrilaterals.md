---
title: Trasladar polígonos y Quadrilaterals
description: Tenga en cuenta los siguientes puntos al trasladar polígonos y quadrilaterals
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- Migración de la contabilidad de IRIS, quadrilaterals
- portabilidad de IRIS GL, quadrilaterals
- migración a OpenGL desde IRIS GL, quadrilaterals
- Exportación de OpenGL desde IRIS GL, quadrilaterals
- funciones de dibujo, quadrilaterals
- quadrilaterals
- Migración de la contabilidad de IRIS, polígonos
- portabilidad de IRIS GL, polígonos
- trasladar a OpenGL desde IRIS GL, polígonos
- Exportación de OpenGL desde IRIS GL, polígonos
- dibujar funciones, polígonos
- polígonos, portabilidad de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c95d654b101c5eeb86cfcc4ea342e8196b8749e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778037"
---
# <a name="porting-polygons-and-quadrilaterals"></a>Trasladar polígonos y Quadrilaterals

Tenga en cuenta los siguientes puntos al trasladar polígonos y quadrilaterals:

-   No hay ningún equivalente directo para **cóncava**(**true**). En su lugar, puede usar las rutinas de teselación en GLU, que se describen en [polígonos de teselar](tessellating-polygons.md).
-   Los modos de polígono se establecen de manera diferente.
-   Estas funciones de dibujo de polígonos no tienen equivalentes directos en OpenGL **: la familia** de rutinas. familia **POLF** de rutinas; **PMV**, **PDR** y **PCLOS**; **rpmv** y **rpdr**; **SPLF**; y **spclos**.

Si el código de la contabilidad de IRIS usa estas funciones, tendrá que volver a escribir el código mediante [**glBegin**](glbegin.md)(GL \_ Polygon).

En la tabla siguiente se enumeran las funciones de dibujo de polígono GL de IRIS y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS         | Función OpenGL                                                    | Significado                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| **bgnpolygonendpolygon** | [**glBegin**](glbegin.md) (GL \_ polígono)[**glEnd**](glend.md)   | Los vértices definen el límite de un polígono convexo simple.    |
|                          | **glBegin**(GL \_ cuádruples)**glEnd**<br/>                       | Interpreta cuadruplican de los vértices como quadrilaterals.    |
| **bgnqstripendqstrip**   | [**glBegin**](glbegin.md) (GL \_ de \_ banda cuádruple)**glEnd**<br/> | Interpreta los vértices como franjas vinculadas de quadrilaterals. |
|                          | [glEdgeFlag](gledgeflag-functions.md)                             |                                                         |
| **Polimoda**             | [**glPolygonMode**](glpolygonmode.md)                             | Establece el modo de dibujo de polígono.                              |
| **rectrectf**<br/> | [glRect](glrect-functions.md)                                     | Dibuja un rectángulo.                                      |
| **sboxsboxf**<br/> |                                                                    | Dibuja un rectángulo alineado en la pantalla.                       |



 

??

## <a name="porting-polygon-modes"></a>Trasladar modos de polígono

La función [**glPolygonMode**](glpolygonmode.md) de OpenGL le permite especificar a qué lado de un polígono (hacia atrás o hacia delante) se aplica el modo. La sintaxis es:

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

donde la superficie es una de las siguientes:



|                      |                                                            |
|----------------------|------------------------------------------------------------|
| frontal de GL \_            | modo que se aplica a los polígonos frontales                |
| libro \_ de contabilidad             | el modo que se aplica a los polígonos de orientación                 |
| \_anverso \_ y \_ atrás de GL | modo que se aplica a los polígonos frontal y hacia delante |



 

El \_ modo frontal \_ y \_ trasero de contabilidad es equivalente a la función de **multimodo** de la contabilidad de iris. En la tabla siguiente se enumeran los modos de polígono de la contabilidad de IRIS y sus modos de OpenGL equivalentes.



| Modo de GL de IRIS | Modo OpenGL | Significado                                       |
|--------------|-------------|-----------------------------------------------|
| \_punto PYM   | punto de contabilidad \_   | Dibuja vértices como puntos.                     |
| \_línea PYM    | línea de contabilidad \_    | Dibuja los bordes del límite como segmentos de línea.        |
| relleno de PYM \_    | relleno de contabilidad \_    | Dibuja el interior del polígono relleno.                |
| PYM \_ hueco  |             | Rellena solo los píxeles interiores en los límites. |



 

## <a name="porting-polygon-stipples"></a>Trasladar punteas de polígono

Al migrar los elementos punteados de la contabilidad de IRIS, tenga en cuenta los puntos siguientes:

-   OpenGL no usa tablas para los punteados de polígonos; solo se mantiene un patrón punteado. Puede usar listas de visualización para almacenar diferentes patrones de punteado.
-   El tamaño del mapa de bits punteado de OpenGL es siempre un patrón de bits de 32x32.
-   La codificación en forma de punteado se ve afectada por [**glPixelStore**](glpixelstore-functions.md).

Para obtener más información sobre cómo trasladar a los polígonos, vea [portar las operaciones de píxeles](porting-pixel-operations.md).

En la tabla siguiente se enumeran las funciones de los elementos punteados de IRIS GL y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS | Función OpenGL                                    | Significado                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| **defpattern**   | [**glPolygonStipple**](glpolygonstipple.md)       | Establece el patrón punteado.                             |
| **setpattern**   |                                                    | OpenGL solo mantiene un patrón punteado de polígono.        |
| **GetPattern**   | [**glGetPolygonStipple**](glgetpolygonstipple.md) | Devuelve el mapa de bits punteado (que se usa para devolver un índice). |



 

En OpenGL, puede habilitar y deshabilitar el punteado de polígono pasando GL \_ Polygon \_ punteada como un parámetro para [**glEnable**](glenable.md) y [**glDisable**](gldisable.md).

El siguiente ejemplo de código OpenGL muestra el punteado de polígono:


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



## <a name="porting-tessellated-polygons"></a>Trasladar polígonos teselados

En IRIS GL, use **cóncava**(**true**) y, a continuación, **bgnpolygon** para dibujar polígonos cóncavos. OpenGL GLU incluye funciones que se pueden usar para dibujar polígonos cóncavos.

**Para dibujar un polígono cóncavo con OpenGL**

1.  Cree un objeto de teselación.
2.  Defina devoluciones de llamada que se usarán para procesar los triángulos generados por del teselador.
3.  Especifique el polígono cóncavo que se va a teselar.

En la tabla siguiente se enumeran las funciones de OpenGL para dibujar polígonos teselados.



| Función GLU de OpenGL                        | Significado                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [**gluNewTess**](glunewtess.md)           | Crea un nuevo objeto de teselación.                                 |
| [**gluDeleteTess**](gludeletetess.md)     | Elimina un objeto de teselación.                                     |
| [*gluTessCallback*](glutess.md)           |                                                                    |
| [**gluBeginPolygon**](glubeginpolygon.md) | Comienza la especificación de polígono.                                  |
| [**gluTessVertex**](glutessvertex.md)     | Especifica un vértice de polígono en un contorno.                           |
| [**gluNextContour**](glunextcontour.md)   | Indica que la siguiente serie de vértices describe un nuevo contorno. |
| [**gluEndPolygon**](gluendpolygon.md)     | Finaliza la especificación de polígono.                                    |



 

 

 





