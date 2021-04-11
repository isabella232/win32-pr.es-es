---
title: función glBegin (GL. h)
description: Las funciones glBegin y glend delimitan los vértices de un primitivo o un grupo de primitivos similares. | función glBegin (GL. h)
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- glBegin (función) OpenGL
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
ms.openlocfilehash: 8227d30adf97bf27fecc19603a5e5e32e4f44822
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003638"
---
# <a name="glbegin-function"></a>glBegin función)

Las funciones **glBegin** y [**glend**](glend.md) delimitan los vértices de un primitivo o un grupo de primitivos similares.

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

Primitivas o primitivas que se crearán a partir de los vértices presentados entre **glBegin** y los [**glend**](glend.md)posteriores. A continuación se indican las constantes simbólicas aceptadas y su significado:



| Value                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <dt>**puntos de contabilidad \_**</dt> </dl>                          | Trata cada vértice como un único punto. El vértice *n* define el punto *n*. Se dibujan *N* puntos.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <dt>**líneas de contabilidad \_**</dt> </dl>                             | Trata cada par de vértices como un segmento de línea independiente. Los vértices *2N-1* y *2N* definen la línea *n*. Se dibujan *N/2* líneas.<br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <dt>**\_franja de línea de contabilidad \_**</dt> </dl>             | Dibuja un grupo conectado de segmentos de línea desde el primer vértice hasta el último. Los vértices *n* y *n + 1* definen la línea *n*. Se dibujan *N-1* líneas.<br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <dt>**\_bucle de línea de contabilidad \_**</dt> </dl>                | Dibuja un grupo conectado de segmentos de línea desde el primer vértice hasta el último y después vuelve al primer. Los vértices *n* y *n + 1* definen la línea *n*. La última línea, sin embargo, se define mediante los vértices *N* y *1*. Se dibujan *N* líneas.<br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <dt>**triángulos de contabilidad \_**</dt> </dl>                 | Trata cada tríptico de los vértices como un triángulo independiente. Los vértices *3N-2*, *3N-1* y *3N* definen el triángulo *n*. Se dibujan los triángulos *N/3* .<br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <dt>**\_franja de triángulo de GL \_**</dt> </dl> | Dibuja un grupo de triángulos conectado. Se define un triángulo para cada vértice presentado después de los dos primeros vértices. Para *n* impar, los vértices *n*, *n + 1* y *n + 2* definen el triángulo *n*. Para incluso *n*, los vértices *n + 1*, *n* y *n + 2* definen el triángulo *n*. Se dibujan los triángulos *N-2* .<br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <dt>**\_ventilador de triángulo GL \_**</dt> </dl>       | Dibuja un grupo de triángulos conectado. se define un triángulo para cada vértice presentado después de los dos primeros vértices. Los vértices *1*, *n + 1*, *n + 2* definen el triángulo *n*. Se dibujan los triángulos *N-2* .<br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <dt>**\_cuádruples de GL**</dt> </dl>                             | Trata cada grupo de cuatro vértices como un cuadrangular independiente. Los vértices *4N-3*, *4N-2*, *4N-1* y *4N* definen cuadrangular *n*. Se dibujan *N/4* quadrilaterals.<br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <dt>**\_banda cuádruple de GL \_**</dt> </dl>             | Dibuja un grupo conectado de quadrilaterals. Se define un cuadrangular para cada par de vértices presentados después del primer par. Los vértices *2N-1*, *2N*, *2N + 2* y *2N + 1* definen cuadrangular *n*. *N/2-1* quadrilaterals se dibujan. Tenga en cuenta que el orden en que se usan los vértices para construir un cuadrangular a partir de datos de franja es diferente del que se usa con datos independientes.<br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <dt>**Polígono de GL \_**</dt> </dl>                       | Dibuja un solo polígono convexo. Los vértices *1* a *N* definen este polígono.<br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *modo* se estableció en un valor no aceptado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a una función que no sea [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [glEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md)o [**glCallLists**](glcalllists.md) entre **glBegin** y el [**glend**](glend.md)correspondiente. Se llamó a la función **glend** antes de que se llamara al **glBegin** correspondiente, o bien se llamó a **glBegin** dentro de una secuencia **glBegin** / **glend** . <br/> |



## <a name="remarks"></a>Observaciones

Las funciones **glBegin** y [**glend**](glend.md) delimitan los vértices que definen un primitivo o un grupo de primitivos similares. La función **glBegin** acepta un solo argumento que especifica los diez primitivos que componen los vértices. Tomando *n* como un recuento entero a partir de uno, y *n* como el número total de vértices especificado, las interpretaciones son las siguientes:

-   Solo se puede usar un subconjunto de funciones de OpenGL entre **glBegin** y [**glend**](glend.md). Las funciones que puede usar son:

    [**glVertex**](glvertex-functions.md)

     

    [**glColor**](glcolor-functions.md)

     

    [**glIndex**](glindex-functions.md)

     

    [**glNormal**](glnormal-functions.md)

     

    [**glTexCoord**](gltexcoord-functions.md)

     

    [**glEvalCoord**](glevalcoord-functions.md)

     

    [**glEvalPoint**](glevalpoint.md)

     

    [**glMaterial**](glmaterial-functions.md)

     

    [**glEdgeFlag**](gledgeflag-functions.md)

    También puede usar [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) para ejecutar listas de presentación que incluyen solo las funciones anteriores. Si se llama a cualquier otra función de OpenGL entre **glBegin** y [**glend**](glend.md), se establece la marca de error y se omite la función.

-   Independientemente del valor elegido para el *modo* en **glBegin**, no hay ningún límite en el número de vértices que puede definir entre **glBegin** y [**glend**](glend.md). No se dibujan líneas, triángulos, quadrilaterals ni polígonos que se hayan especificado de una vez incompleta. Resultados de especificación incompletos cuando se proporcionan muy pocos vértices para especificar incluso un único primitivo o cuando se especifica un múltiplo incorrecto de vértices. Se omite el primitivo incompleto; se dibujan los primitivos completos.
-   La especificación mínima de los vértices para cada primitiva es: 

    | Número mínimo de vértices | Tipo de primitivo |
    |----------------------------|-------------------|
    | 1                          | point             |
    | 2                          | line              |
    | 3                          | triangle          |
    | 4                          | cuadrangular     |
    | 3                          | polygon           |

    

     

-   Los modos que requieren un determinado múltiplo de vértices son \_ las líneas de libro de contabilidad (2), los \_ triángulos de contabilidad (3), los \_ cuatro cuádruples (4) y la \_ franja cuádruple de GL \_ (2).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

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

 

