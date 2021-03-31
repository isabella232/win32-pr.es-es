---
title: función glCopyPixels (GL. h)
description: La función glCopyPixels copia píxeles en el fotogramas.
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- glCopyPixels (función) OpenGL
topic_type:
- apiref
api_name:
- glCopyPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7ba0833534d21e48c251da6491fee2996c3ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996526"
---
# <a name="glcopypixels-function"></a>glCopyPixels función)

La función **glCopyPixels** copia píxeles en el fotogramas.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glCopyPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* 
</dt> <dd>

Coordenada x del plano de la ventana de la esquina inferior izquierda de la región rectangular de píxeles que se va a copiar.

</dd> <dt>

*y* 
</dt> <dd>

Coordenada y del plano de la ventana de la esquina inferior izquierda de la región rectangular de píxeles que se va a copiar.

</dd> <dt>

*width* 
</dt> <dd>

Dimensión de ancho de la región rectangular de píxeles que se va a copiar. No debe ser negativo.

</dd> <dt>

*height* 
</dt> <dd>

La dimensión de alto de la región rectangular de píxeles que se va a copiar. No debe ser negativo.

</dd> <dt>

*type* 
</dt> <dd>

Especifica si **glCopyPixels** es copiar valores de color, valores de profundidad o valores de estarcido. Las constantes simbólicas aceptables son.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR"></span><span id="gl_color"></span><dl> <dt><strong>GL_COLOR</strong></dt> </dl></td>
<td>La función <strong>glCopyPixels</strong> Lee índices o colores RGBA del búfer especificado actualmente como búfer de origen de lectura (vea <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>). <br/> Si OpenGL está en modo de índice de color:<br/>
<ol>
<li>Cada índice que se lee desde este búfer se convierte en un formato de punto fijo con un número no especificado de bits a la derecha del punto binario.</li>
<li>Cada índice se desplaza a la izquierda GL_INDEX_SHIFT bits y se agrega a GL_INDEX_OFFSET. Si GL_INDEX_SHIFT es negativo, el desplazamiento está a la derecha. En cualquier caso, cero bits rellenan de otro modo las ubicaciones de bits no especificadas en el resultado.<br/></li>
<li>Si GL_MAP_COLOR es true, el índice se reemplaza por el valor al que hace referencia en la tabla de búsqueda GL_PIXEL_MAP_I_TO_I.</li>
<li>Tanto si el reemplazo de búsqueda del índice se realiza como si no, la parte entera del índice es then <strong>y</strong>Ed con 2<em><sup>b</sup></em> 1, donde <em>b</em> es el número de bits de un búfer de índice de color.</li>
</ol>
Si OpenGL está en modo RGBA:<br/>
<ol>
<li>Los componentes rojo, verde, azul y alfa de cada píxel que se lee se convierten a un formato de punto flotante interno con una precisión no especificada.</li>
<li>La conversión asigna el mayor valor de componente representable a 1,0 y el valor de componente de cero a 0,0.</li>
<li>Los valores de color de punto flotante resultantes se multiplican por GL_c_SCALE y se agregan a GL_c_BIAS, donde <em>c</em> es rojo, verde, azul y alfa para los componentes de color respectivos.</li>
<li>Los resultados se fijan en el intervalo [0, 1].</li>
<li>Si GL_MAP_COLOR es true, cada componente de color se escala según el tamaño de la tabla de búsqueda GL_PIXEL_MAP_c_TO_c y, a continuación, se reemplaza por el valor al que hace referencia en esa tabla; <em>c</em> es R, G, B o A, respectivamente. Los índices resultantes o los colores RGBA se convierten a fragmentos adjuntando las coordenadas <em>z</em>y de textura actuales de la posición de la línea de rasterizada a cada píxel y asignando después coordenadas de ventana (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de la trama actual y el píxel era el <em></em> píxel en la posición <em>i</em> Estos fragmentos de píxeles se tratan a continuación como los fragmentos generados mediante la rasterización de puntos, líneas o polígonos. La asignación de texturas, la niebla y todas las operaciones de fragmento se aplican antes de que los fragmentos se escriban en el fotogramas.<br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_DEPTH"></span><span id="gl_depth"></span><dl> <dt><strong>GL_DEPTH</strong></dt> </dl></td>
<td>Los valores de profundidad se leen desde el búfer de profundidad y se convierten directamente a un formato de punto flotante interno con una precisión no especificada. A continuación, el valor de profundidad de punto flotante resultante se multiplica por GL_DEPTH_SCALE y se agrega a GL_DEPTH_BIAS. El resultado se fija en el intervalo [0, 1]. <br/> Los componentes de profundidad resultantes se convierten a fragmentos adjuntando el color de posición de la trama actual o el índice de color y las coordenadas de textura a cada píxel, asignando después coordenadas de ventana (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de la trama actual y el <em></em> píxel era el píxel de la posición <em>i</em> Estos fragmentos de píxeles se tratan a continuación como los fragmentos generados mediante la rasterización de puntos, líneas o polígonos. La asignación de texturas, la niebla y todas las operaciones de fragmento se aplican antes de que los fragmentos se escriban en el fotogramas.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl> <dt><strong>GL_STENCIL</strong></dt> </dl></td>
<td>Los índices de estarcido se leen desde el búfer de estarcido y se convierten a un formato de punto fijo interno con un número no especificado de bits a la derecha del punto binario. A continuación, cada índice de punto fijo se desplaza a la izquierda GL_INDEX_SHIFT bits y se agrega a GL_INDEX_OFFSET. Si GL_INDEX_SHIFT es negativo, el desplazamiento está a la derecha. En cualquier caso, cero bits rellenan de otro modo las ubicaciones de bits no especificadas en el resultado. Si GL_MAP_STENCIL es true, el índice se reemplaza por el valor al que hace referencia en la tabla de búsqueda GL_PIXEL_MAP_S_TO_S. Tanto si el reemplazo de búsqueda del índice se realiza como si no, la parte entera del índice es entonces <strong>y</strong>Ed con 2<sup>b</sup> - 1, donde <em>b</em> es el número de bits del búfer de estarcido. Los índices de estarcido resultantes se escriben en el búfer de la galería de símbolos, de modo que el índice leído desde la ubicación <em>i</em> de la fila <em>j</em> se escribe en la ubicación (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de la trama actual. Solo la prueba de propiedad de píxeles, la prueba de tijera y la galería de símbolos writemask afectan a estas escrituras.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *tipo* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | El *ancho* o el alto era negativo.<br/>                                                                                     |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | el *tipo* era \_ profundidad de libro de contabilidad y no había ningún búfer de profundidad.<br/>                                                                        |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | el *tipo* es la \_ Galería de símbolos GL y no hay ningún búfer de estarcido.<br/>                                                                    |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glCopyPixels** copia un rectángulo alineado en la pantalla de píxeles desde la ubicación fotogramas especificada a una región relativa a la posición de la trama actual. Su funcionamiento está bien definido solo si toda la región de origen de píxeles está dentro de la parte expuesta de la ventana. Los resultados de las copias desde fuera de la ventana de, o desde las regiones de la ventana que no están expuestas, dependen del hardware y no están definidas.

Los  parámetros x *e y* especifican las coordenadas de la ventana de la esquina inferior izquierda de la región rectangular que se va a copiar. Los parámetros de *ancho* y *alto* especifican las dimensiones de la región rectangular que se va a copiar. *Width* y *height* no deben ser negativos.

Varios parámetros controlan el procesamiento de los datos de píxeles mientras se copian. Estos parámetros se establecen con tres funciones: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)y [**glPixelZoom**](glpixelzoom.md). En este tema se describen los efectos de **glCopyPixels** de la mayoría de los parámetros especificados por estas tres funciones, pero no todos.

La función **glCopyPixels** copia los valores de cada píxel con la esquina inferior izquierda en (*x*  +  *i*, *y*  +  *j*) para 0 = *i*  <  *width* y 0 = *j*  <  *height*. Este píxel se dice que es el píxel *i* de la fila *j* . Los píxeles se copian en orden de fila desde la fila más baja hasta la más alta, de izquierda a derecha en cada fila.

El parámetro de *tipo* especifica si se copiarán los datos de color, profundidad o estarcido.

La rasterización descrita hasta ahora supone un factor de zoom de píxeles de 1,0. Si usa [**glPixelZoom**](glpixelzoom.md) para cambiar los factores de zoom de píxeles *x* *e y, los píxeles se* convierten en fragmentos como se indica a continuación. Si (*x*<sub>r</sub> , *y*<sub>r</sub> ) es la posición de la trama actual y un píxel determinado está en la ubicación *i* de la fila *j* del rectángulo de píxeles de origen, se generan fragmentos para los píxeles cuyos centros se encuentran en el rectángulo con esquinas en

(*x*<sub>r</sub>  +  ¿ *zoom*? i, y <sub>r</sub>  +  *zoom*<sub>y</sub> *j*

y

(*x*<sub>r</sub>  +  ¿ *zoom*? (*i* + 1), *y*<sub>r</sub>  +  *zoom*<sub>y</sub> (*j* + 1))

¿Dónde *hacer zoom*? es el valor de zoom de GL \_ \_ X y *zoom*<sub>y</sub> es el valor de zoom de GL \_ \_ y.

Los modos especificados por [**glPixelStore**](glpixelstore-functions.md) no tienen ningún efecto en el funcionamiento de **glCopyPixels**.

Las siguientes funciones recuperan información relacionada con **glCopyPixels**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ posición de RASTERIZAción actual de GL \_

**glGet** con argumento de \_ posición de rasterizado actual de GL \_ \_ \_ válido

Para copiar el píxel de color en la esquina inferior izquierda de la ventana a la posición de la trama actual, use

**glCopyPixels**(0, 0, 1, 1, color de GL \_ );

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





