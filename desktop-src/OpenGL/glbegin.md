---
title: Función glBegin (Gl.h)
description: Las funciones glBegin y glBegin delimitan los vértices de una primitiva o un grupo de primitivas similares. | Función glBegin (Gl.h)
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- Función glBegin OpenGL
topic_type:
- apiref
api_name:
- glBegin
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c497542e345b412bdc7955870405e6ee6cfe0503cee22f9320a031e835853345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361160"
---
# <a name="glbegin-function"></a>función glBegin

Las **funciones glBegin y glBegin** [**delimitan**](glend.md) los vértices de una primitiva o un grupo de primitivas similares.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glBegin(
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* 
</dt> <dd>

Primitivos o primitivos que se crearán a partir de vértices presentados entre **glBegin** y el subsecuentemente. [](glend.md) Las siguientes son constantes simbólicas aceptadas y sus significados:



| Valor                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <dt>**PUNTOS \_ DE GL**</dt> </dl>                          | Trata cada vértice como un único punto. El vértice *n* define el punto *n*. *Se dibujan* N puntos.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <dt>**LÍNEAS \_ DE GL**</dt> </dl>                             | Trata cada par de vértices como un segmento de línea independiente. Los vértices *2n - 1* y *2n* definen la línea *n*. *Se dibujan N/2* líneas.<br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <dt>**FRANJA \_ DE LÍNEA \_ GL**</dt> </dl>             | Dibuja un grupo conectado de segmentos de línea desde el primer vértice hasta el último. Los vértices *n y* *n+1* definen la línea *n*. *N : se dibujan 1* líneas.<br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <dt>**BUCLE \_ DE LÍNEA \_ GL**</dt> </dl>                | Dibuja un grupo conectado de segmentos de línea desde el primer vértice hasta el último y, a continuación, vuelve al primero. Los vértices *n y* *n + 1* definen la línea *n*. Sin embargo, la última línea se define mediante los vértices *N* y *1*. *Se dibujan* N líneas.<br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <dt>**TRIÁNGULOS \_ GL**</dt> </dl>                 | Trata cada triplete de vértices como un triángulo independiente. Los vértices *3n - 2*, *3n - 1* y *3n* definen triángulo *n*. *Se dibujan n/3* triángulos.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <dt>**FRANJA \_ DE TRIÁNGULO \_ GL**</dt> </dl> | Dibuja un grupo conectado de triángulos. Se define un triángulo para cada vértice presentado después de los dos primeros vértices. Para los *n impares,* los vértices *n*, n + *1* y n + *2* definen el triángulo *n*. Para incluso *n*, los vértices *n + 1*, *n* y n *+ 2* definen triángulo *n*. *N : se dibujan 2* triángulos.<br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <dt>**VENTILADOR \_ DE TRIÁNGULO \_ GL**</dt> </dl>       | Dibuja un grupo conectado de triángulos. Se define un triángulo para cada vértice presentado después de los dos primeros vértices. Los vértices *1,* *n + 1,* *n + 2* definen triángulo *n*. *N : se dibujan 2* triángulos.<br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <dt>**GL \_ QUADS**</dt> </dl>                             | Trata cada grupo de cuatro vértices como un cuadrículo independiente. Los vértices *4n - 3*, *4n - 2*, *4n - 1* y *4n* definen cuadrículo *n*. *Se dibujan n/4* cuadráteros.<br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <dt>**GL \_ QUAD \_ STRIP**</dt> </dl>             | Dibuja un grupo conectado de cuadriláteros. Se define un cuadrículo para cada par de vértices que se presentan después del primer par. Los vértices *2n - 1*, *2n*, *2n + 2* y *2n + 1* definen cuadrículo *n*. *N/2: se dibujan 1* cuadráteros. Tenga en cuenta que el orden en el que se usan los vértices para construir un cuadrículo a partir de datos de franja es diferente del que se usa con datos independientes.<br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <dt>**POLÍGONO \_ GL**</dt> </dl>                       | Dibuja un único polígono convexa. Los vértices *del 1* al *N* definen este polígono.<br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *el* modo se estableció en un valor noceptado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a una función que no sea [glVertex,](glvertex-functions.md) [glColor,](glcolor-functions.md) [glIndex](glindex-functions.md), [glNormal,](glnormal-functions.md) [glTexCoord,](gltexcoord-functions.md) [glEvalCoord,](glevalcoord-functions.md) [glEvalPoint,](glevalpoint.md) [glMaterial,](glmaterial-functions.md) [glEdgeFlag,](gledgeflag-functions.md) [**glCallList**](glcalllist.md)o [**glCallLists**](glcalllists.md) entre **glBegin** y el [**correspondiente .**](glend.md) Antes de **llamar** a la función **glBegin** correspondiente, se llamó a **glBegin** dentro de una **secuencia de glBegin.** /  <br/> |



## <a name="remarks"></a>Comentarios

Las **funciones glBegin y glBegin** [**delimitan**](glend.md) los vértices que definen una primitiva o un grupo de primitivas similares. La **función glBegin** acepta un único argumento que especifica cuál de diez primitivos componen los vértices. Tomando *n* como número entero a partir de uno y *N* como número total de vértices especificados, las interpretaciones son las siguientes:

-   Solo puede usar un subconjunto de funciones de OpenGL entre **glBegin** [**y .**](glend.md) Las funciones que puede usar son:

    [**glVertex**](glvertex-functions.md)

     

    [**glColor**](glcolor-functions.md)

     

    [**glIndex**](glindex-functions.md)

     

    [**glNormal**](glnormal-functions.md)

     

    [**glTexCoord**](gltexcoord-functions.md)

     

    [**glEvalCoord**](glevalcoord-functions.md)

     

    [**glEvalPoint**](glevalpoint.md)

     

    [**glMaterial**](glmaterial-functions.md)

     

    [**glEdgeFlag**](gledgeflag-functions.md)

    También puede usar [**glCallList o**](glcalllist.md) [**glCallLists**](glcalllists.md) para ejecutar listas para mostrar que incluyan solo las funciones anteriores. Si se llama a cualquier otra función openGL entre **glBegin y glbegin,** se establece la marca de error y se omite la función. [](glend.md)

-   Independientemente del valor  elegido para el modo en **glBegin,** no hay ningún límite en el número de vértices que se pueden definir entre **glBegin** y [**.**](glend.md) No se dibujan líneas, triángulos, cuadráteros y polígonos que están especificados de forma incompleta. Resultados de especificación incompletos cuando se proporcionan demasiados vértices para especificar incluso una sola primitiva o cuando se especifica un múltiplo incorrecto de vértices. Se omite la primitiva incompleta; se dibujan las primitivas completas.
-   La especificación mínima de vértices para cada primitivo es: 

    | Número mínimo de vértices | Tipo de primitiva |
    |----------------------------|-------------------|
    | 1                          | point             |
    | 2                          | line              |
    | 3                          | triangle          |
    | 4                          | Cuadrilátero     |
    | 3                          | polygon           |

    

     

-   Los modos que requieren un determinado múltiplo de vértices son GL \_ LINES (2), GL \_ TRIANGLES (3), GL \_ QUADS (4) y GL \_ QUAD STRIP \_ (2).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](/windows/desktop/OpenGL/glend)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

