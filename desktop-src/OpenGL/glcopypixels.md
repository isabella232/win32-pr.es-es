---
title: Función glCopyPixels (Gl.h)
description: La función glCopyPixels copia píxeles en el búfer de fotogramas.
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- Función glCopyPixels OpenGL
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
ms.openlocfilehash: 43c399b4ce63f84c41bcb2d65140356ac20a6ddd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362094"
---
# <a name="glcopypixels-function"></a>Función glCopyPixels

La **función glCopyPixels** copia píxeles en el búfer de fotogramas.

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

Coordenada del plano x de la ventana de la esquina inferior izquierda de la región rectangular de píxeles que se va a copiar.

</dd> <dt>

*y* 
</dt> <dd>

Coordenada del plano Y de la ventana de la esquina inferior izquierda de la región rectangular de píxeles que se va a copiar.

</dd> <dt>

*width* 
</dt> <dd>

Dimensión de ancho de la región rectangular de píxeles que se va a copiar. No debe ser negativo.

</dd> <dt>

*height* 
</dt> <dd>

Dimensión de alto de la región rectangular de píxeles que se va a copiar. No debe ser negativo.

</dd> <dt>

*type* 
</dt> <dd>

Especifica si **glCopyPixels** va a copiar valores de color, valores de profundidad o valores de galería de símbolos. Las constantes simbólicas aceptables son .




| Value | Significado | 
|-------|---------|
| <span id="GL_COLOR"></span><span id="gl_color"></span><dl><dt><strong>GL_COLOR</strong></dt></dl> | La <strong>función glCopyPixels</strong> lee índices o colores RGBA del búfer especificado actualmente como búfer de origen de lectura <a href="glreadbuffer.md"><strong>(vea glReadBuffer</strong></a>). <br /> Si OpenGL está en modo de índice de color:<br /><ol><li>Cada índice que se lee de este búfer se convierte a un formato de punto fijo con un número no especificado de bits a la derecha del punto binario.</li><li>Cada índice se desplaza a la izquierda GL_INDEX_SHIFT bits y se agrega a GL_INDEX_OFFSET. Si GL_INDEX_SHIFT es negativo, el desplazamiento es a la derecha. En cualquier caso, los bits cero rellenan ubicaciones de bits no especificadas en el resultado.<br /></li><li>Si GL_MAP_COLOR es true, el índice se reemplaza por el valor al que hace referencia en la tabla de GL_PIXEL_MAP_I_TO_I.</li><li>Tanto si la sustitución de búsqueda del índice se realiza como si no, la parte entera del índice es <strong>ENTONCES AND</strong>ed con 2<em><sup>b</sup></em> 1, donde <em>b</em> es el número de bits de un búfer de índice de color.</li></ol>Si OpenGL está en modo RGBA:<br /><ol><li>Los componentes rojo, verde, azul y alfa de cada píxel que se lee se convierten a un formato de punto flotante interno con precisión no especificada.</li><li>La conversión asigna el mayor valor de componente representable a 1,0 y el valor de componente cero a 0,0.</li><li>A continuación, los valores de color de punto flotante resultantes se multiplican por GL_c_SCALE y se agregan a GL_c_BIAS, donde <em>c</em> es RED, GREEN, BLUE y ALPHA para los componentes de color respectivos.</li><li>Los resultados se fijan en el intervalo [0,1].</li><li>Si GL_MAP_COLOR es true, cada componente de color se escala por el tamaño de la tabla de búsqueda GL_PIXEL_MAP_c_TO_c y, a continuación, se reemplaza por el valor al que hace referencia en esa tabla; <em>c</em> es R, G, B o A, respectivamente. A continuación, los índices resultantes o los colores RGBA se convierten en fragmentos adjuntando la posición de trama <em>actual z</em>-coordenada y coordenadas de textura a cada píxel y, a continuación, asignando coordenadas de ventana<em>(x</em><sub>r</sub> + i, <em>y</em><sub>r</sub>j ), donde ( x r , y r ) es la posición de trama actual y el píxel era el píxel en la posición i de la  +  <em></em>fila <em></em><sub></sub> <em>j.</em> <em></em><sub></sub> <em></em> Estos fragmentos de píxeles se tratan como los fragmentos generados al rasterizar puntos, líneas o polígonos. La asignación de texturas, los grados y todas las operaciones de fragmento se aplican antes de que los fragmentos se escriban en el búfer de fotogramas.<br /></li></ol> | 
| <span id="GL_DEPTH"></span><span id="gl_depth"></span><dl><dt><strong>GL_DEPTH</strong></dt></dl> | Los valores de profundidad se leen desde el búfer de profundidad y se convierten directamente en un formato de punto flotante interno con precisión no especificada. A continuación, el valor de profundidad de punto flotante resultante se multiplica por GL_DEPTH_SCALE y se agrega a GL_DEPTH_BIAS. El resultado se fija en el intervalo [0,1]. <br /> A continuación, los componentes de profundidad resultantes se convierten en fragmentos adjuntando el color de la posición de trama actual o el índice de color y las coordenadas de textura a cada píxel y, a continuación, asignando coordenadas de ventana<em>(x</em><sub>r</sub> + i, <em>y</em><sub>r</sub>j ), donde ( x r , y r ) es la posición de trama actual y el píxel era el píxel en la posición i de la fila  +  <em></em> <em></em><sub></sub> <em>j.</em> <em></em><sub></sub> <em></em> Estos fragmentos de píxeles se tratan como los fragmentos generados al rasterizar puntos, líneas o polígonos. La asignación de texturas, los grados y todas las operaciones de fragmento se aplican antes de que los fragmentos se escriban en el búfer de fotogramas.<br /> | 
| <span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl><dt><strong>GL_STENCIL</strong></dt></dl> | Los índices de galería de símbolos se leen desde el búfer de la galería de símbolos y se convierten a un formato de punto fijo interno con un número no especificado de bits a la derecha del punto binario. A continuación, cada índice de punto fijo se desplaza a la izquierda GL_INDEX_SHIFT bits y se agrega a GL_INDEX_OFFSET. Si GL_INDEX_SHIFT es negativo, el desplazamiento es a la derecha. En cualquier caso, los bits cero rellenan ubicaciones de bits no especificadas en el resultado. Si GL_MAP_STENCIL es true, el índice se reemplaza por el valor al que hace referencia en la tabla de búsqueda GL_PIXEL_MAP_S_TO_S. Independientemente de si la sustitución de búsqueda del índice se realiza o no, la parte entera del índice es <strong>ENTONCES AND</strong>ed con 2<sup>b</sup> - 1, donde <em>b</em> es el número de bits en el búfer de galería de símbolos. A continuación, los índices de galería de símbolos resultantes se escriben en el búfer de la galería de símbolos para que el índice leído de la ubicación <em>i</em> de la fila <em>j</em> se escriba en la ubicación (<em>x</em><sub>r</sub>  +  <em>i</em>, <em>y</em><sub>r</sub>j ), donde ( x r , y r ) es la posición de trama  +  <em></em> <em></em><sub></sub> <em></em><sub></sub> actual. Solo la prueba de propiedad de píxeles, la prueba de desenlazamiento y la máscara de escritura de galería de símbolos afectan a estas escrituras.<br /> | 




 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *Type* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | El *ancho o* alto era negativo.<br/>                                                                                     |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | *El tipo* era GL \_ DEPTH y no había ningún búfer de profundidad.<br/>                                                                        |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | *El* tipo era GL \_ STENCIL y no había ningún búfer de galería de símbolos.<br/>                                                                    |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glCopyPixels** copia un rectángulo alineado con la pantalla de píxeles de la ubicación del búfer de fotogramas especificado en una región con respecto a la posición de trama actual. Su operación solo está bien definida si toda la región de origen de píxeles está dentro de la parte expuesta de la ventana. Los resultados de copias desde fuera de la ventana, o desde regiones de la ventana que no están expuestas, dependen del hardware y no están definidos.

Los *parámetros x* e *y* especifican las coordenadas de ventana de la esquina inferior izquierda de la región rectangular que se va a copiar. Los *parámetros* de *ancho y* alto especifican las dimensiones de la región rectangular que se va a copiar. Tanto *el ancho* como *el* alto deben ser no reontes.

Varios parámetros controlan el procesamiento de los datos de píxeles mientras se copian. Estos parámetros se establecen con tres funciones: [**glPixelTransfer,**](glpixeltransfer.md) [**glPixelMap**](glpixelmap.md)y [**glPixelZoom.**](glpixelzoom.md) En este tema se describen los efectos en **glCopyPixels** de la mayoría, pero no todos, de los parámetros especificados por estas tres funciones.

La **función glCopyPixels** copia los valores de cada píxel con la esquina inferior izquierda en (*x*  +  *i*, *y* j ) para 0 = i width y  +     <   0 = *j*  <  *height*. Se dice que este píxel es el *píxel i* de la *fila j.* Los píxeles se copian en orden de fila de la fila más baja a la más alta, de izquierda a derecha en cada fila.

El *parámetro* type especifica si se van a copiar los datos de color, profundidad o galería de símbolos.

La rasterización descrita hasta ahora supone factores de zoom de píxeles de 1,0. Si usa [**glPixelZoom**](glpixelzoom.md) para  cambiar los factores de zoom de píxel x e *y,* los píxeles se convierten en fragmentos como se muestra a continuación. Si (*x*<sub>r</sub> , *y*<sub>r</sub> ) es la posición de trama actual y un píxel determinado está en la ubicación *i* de la fila *j* del rectángulo de píxeles de origen, se generan fragmentos para píxeles cuyos centros están en el rectángulo con esquinas en

(*x*<sub>r</sub>  +  *zoom*? i, y <sub>r</sub>  +  *zoom*<sub>y</sub> *j*)

y

(*x*<sub>r</sub>  +  *zoom*? (*i* + 1), *y*<sub>r</sub>  +  *zoom*<sub>y</sub> *(j* + 1))

where *zoom*? es el valor de GL \_ ZOOM X y \_ *zoom*<sub>y</sub> es el valor de GL \_ ZOOM \_ Y.

Los modos especificados por [**glPixelStore**](glpixelstore-functions.md) no tienen ningún efecto en el funcionamiento de **glCopyPixels.**

Las siguientes funciones recuperan información relacionada **con glCopyPixels**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ CURRENT RASTER \_ \_ POSITION

**glGet con** el argumento GL \_ CURRENT RASTER POSITION \_ \_ \_ VALID

Para copiar el píxel de color de la esquina inferior izquierda de la ventana en la posición de trama actual, use

**glCopyPixels**( 0, 0, 1, 1, GL \_ COLOR );

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 





