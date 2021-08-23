---
title: Función gluTessCallback (Glu.h)
description: La función gluTessCallback define una devolución de llamada para un objeto de teselación.
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- Función GluTessCallback OpenGL
topic_type:
- apiref
api_name:
- gluTessCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48ec252b9badc784726110300792c6479bed379b799c3c0499f59f0fdeb6632d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554135"
---
# <a name="glutesscallback-function"></a>función gluTessCallback

La **función gluTessCallback** define una devolución de llamada para un objeto de teselación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluTessCallback(
   GLUtesselator *tess,
   GLenum        which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tess* 
</dt> <dd>

Objeto de teselación (creado [**con gluNewTess).**](glunewtess.md)

</dd> <dt>

*Que* 
</dt> <dd>

Devolución de llamada que se está definindo. Los valores siguientes son válidos: GLU \_ TESS \_ BEGIN, GLU \_ TESS \_ BEGIN \_ DATA, GLU \_ TESS \_ EDGE \_ FLAG, GLU \_ TESS \_ EDGE FLAG \_ \_ DATA, GLU \_ TESS \_ VERTEX, GLU \_ TESS \_ VERTEX \_ DATA, GLU TESS \_ \_ END, GLU TESS END \_ \_ \_ DATA, GLU \_ TESS \_ COMBINE, GLU \_ TESS \_ COMBINE \_ DATA, GLU \_ TESS ERROR y GLU \_ \_ TESS \_ ERROR \_ DATA.

Para obtener más información sobre estas devoluciones de llamada, vea la sección Comentarios siguiente.

</dd> <dt>

*fn* 
</dt> <dd>

Función a la que se va a llamar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Use **gluTessCallback para** especificar una devolución de llamada que usará un objeto de teselación. Si la devolución de llamada especificada ya está definida, se reemplaza. Si *fn es* **NULL,** la devolución de llamada existente se convierte en indefinido.

El objeto de teselación usa estas devoluciones de llamada para describir cómo un polígono que especifique se divide en triángulos.

Hay dos versiones de cada devolución de llamada, una con datos de polígono que puede definir y otra sin ella. Si se especifican ambas versiones de una devolución de llamada determinada, se usará la devolución de llamada con los datos de polígono que especifique. El *parámetro \_ de datos* polygon de [**gluTessBeginPolygon**](glutessbeginpolygon.md) es una copia del puntero que se especificó cuando se llamó a **gluTessBeginPolygon.**

Las siguientes son devoluciones de llamada válidas:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Devolución de llamada</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GLU_TESS_BEGIN</td>
<td>La GLU_TESS_BEGIN de llamada se invoca como <a href="glbegin.md"><strong>glBegin</strong></a> para indicar el inicio de una primitiva (triángulo). La función toma un único argumento de tipo <strong>GLenum.</strong> Si establece la propiedad GLU_TESS_BOUNDARY_ONLY en GL_FALSE, el argumento se establece en GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP o GL_TRIANGLES. Si establece la propiedad GLU_TESS_BOUNDARY_ONLY en GL_TRUE, el argumento se establece en GL_LINE_LOOP. El prototipo de función para esta devolución de llamada es el siguiente: <strong>void</strong> <strong>begin</strong> <strong>(tipo GLenum</strong> <em>);</em><br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_BEGIN_DATA</td>
<td>GLU_TESS_BEGIN_DATA es igual que la devolución GLU_TESS_BEGIN de llamada, salvo que toma un argumento de puntero adicional. Este puntero es idéntico al puntero opaco que se proporciona al llamar <a href="glutessbeginpolygon.md"><strong>a gluTessBeginPolygon.</strong></a> El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>beginData</strong> (<strong>tipo GLenum</strong> <em>,</em> <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_EDGE_FLAG</td>
<td>La GLU_TESS_EDGE_FLAG de llamada es similar <a href="gledgeflag-functions.md"><strong>a glEdgeFlag</strong></a>. La función toma una única marca booleana que indica qué bordes se encuentran en el límite del polígono. Si la marca está GL_TRUE, cada vértice que sigue comienza un borde que se encuentra en el límite del polígono. Es decir, un borde que separa una región interior de una exterior. Si la marca está GL_FALSE, cada vértice que sigue comienza un borde que se encuentra en el interior del polígono. La GLU_TESS_EDGE_FLAG de llamada (si se define) se invoca antes de que se realiza la primera devolución de llamada de vértice. Dado que los ventiladores de triángulo y las franjas de triángulo no admiten marcas de borde, no se llama a la devolución de llamada de inicio con GL_TRIANGLE_FAN o GL_TRIANGLE_STRIP si se proporciona una devolución de llamada de marca de borde. En su lugar, los ventiladores y las bandas se convierten en triángulos independientes. El prototipo de función para esta devolución de llamada es:<br/> <strong>void</strong> <strong>edgeFlag</strong> (<strong>marca GLboolean</strong> <em>);</em><br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_EDGE_FLAG_DATA</td>
<td>La GLU_TESS_EDGE_FLAG_DATA de llamada es la misma que la GLU_TESS_EDGE_FLAG de llamada, salvo que toma un argumento de puntero adicional. Este puntero es idéntico al puntero opaco que se proporciona al llamar <a href="glutessbeginpolygon.md"><strong>a gluTessBeginPolygon.</strong></a> El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>edgeFlagData</strong> (<strong>marca GLboolean</strong> <em>,</em> <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_VERTEX</td>
<td>La GLU_TESS_VERTEX de llamada se invoca entre las devoluciones de llamada de inicio y fin. Es similar a glVertex y define los vértices de los triángulos creados por el proceso de teselación. La función toma un puntero como único argumento. Este puntero es idéntico al puntero opaco que proporcionó al definir el vértice (vea <a href="glutessvertex.md"><strong>gluTessVertex).</strong></a> El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> * <em>vertex_data</em>);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_VERTEX_DATA</td>
<td>La GLU_TESS_VERTEX_DATA es la misma que la devolución GLU_TESS_VERTEX de llamada, salvo que toma un argumento de puntero adicional. Este puntero es idéntico al puntero opaco que se proporciona al llamar <a href="glutessbeginpolygon.md"><strong>a gluTessBeginPolygon.</strong></a> El prototipo de función para esta devolución de llamada es: <strong>void</strong>  <strong>vertexData</strong> (void * <em>vertex_data</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_END</td>
<td>La GLU_TESS_END de devolución de llamada sirve para el mismo propósito <a href="glend.md"><strong>que glEnd</strong></a>. Indica el final de una primitiva y no toma ningún argumento. El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>end</strong> (<strong>void</strong>);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_END_DATA</td>
<td>La GLU_TESS_END_DATA de llamada es la misma que la GLU_TESS_END de llamada, salvo que toma un argumento de puntero adicional. Este puntero es idéntico al puntero opaco que se proporciona al llamar <a href="glutessbeginpolygon.md"><strong>a gluTessBeginPolygon.</strong></a> El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_COMBINE</td>
<td>Llame a la GLU_TESS_COMBINE de llamada para crear un nuevo vértice cuando la teselación detecte una intersección o para combinar características. La función toma cuatro argumentos: una matriz de tres elementos, cada uno de tipo Gldouble.<br/> Matriz de cuatro punteros.<br/> Matriz de cuatro elementos, cada uno de tipo GLfloat.<br/> Puntero a un puntero.<br/> El prototipo de función para esta devolución de llamada es: <br/> <strong>void</strong> <strong>combine</strong>(<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> * <em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong>  ** <em>outData</em>);<br/> El vértice se define como una combinación lineal de hasta cuatro vértices existentes, almacenados en vertex_data. Los coeficientes de la combinación lineal se dan por peso; estos pesos siempre suman 1,0. Todos los punteros de vértice son válidos incluso cuando algunas de las ponderaciones son cero. El parámetro coords proporciona la ubicación del nuevo vértice.<br/> Asigne otro vértice, interpola los parámetros mediante vertex_data y peso, y devuelva el nuevo puntero de vértice en outData. Este identificador se proporciona durante las devoluciones de llamada de representación. Libera la memoria en algún momento después de <a href="glutessendpolygon.md"><strong>llamar a gluTessEndPolygon.</strong></a><br/> Por ejemplo, si el polígono se encuentra en un plano arbitrario en un espacio tridimensional y asocia un color a cada vértice, la devolución de llamada GLU_TESS_COMBINE podría tener el siguiente aspecto:<br/>
<pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4], 
                GLfloat w[4], VERTEX **dataOut ) 
{ 
    VERTEX *newVertex = new_vertex(); 
    newVertex->x = coords[0]; 
    newVertex->y = coords[1]; 
    newVertex->z = coords[2]; 
    newVertex->r = w[0]*d[0]->r + w[1]*d[1]->r + w[2]*d[2]->r + 
                   w[3]*d[3]->r; 
    newVertex->g = w[0]*d[0]->g + w[1]*d[1]->g + w[2]*d[2]->g + 
                   w[3]*d[3]->g; 
    newVertex->b = w[0]*d[0]->b + w[1]*d[1]->b + w[2]*d[2]->b + 
                   w[3]*d[3]->b; 
    newVertex->a = w[0]*d[0]->a + w[1]*d[1]->a + w[2]*d[2]->a + 
                   w[3]*d[3]->a; 
    *dataOut = newVertex; 
}</code></pre>
Cuando la teselación detecta una intersección, se debe definir la devolución de llamada GLU_TESS_COMBINE o GLU_TESS_COMBINE_DATA (consulte a continuación) y debe escribir un puntero que no sea<strong>NULL</strong> en dataOut. De lo GLU_TESS_NEED_COMBINE_CALLBACK se produce el error y no se genera ninguna salida. (Este es el único error que puede producirse durante la teselación y la representación).<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_COMBINE_DATA</td>
<td>La GLU_TESS_COMBINE_DATA de llamada es la misma que la GLU_TESS_COMBINE de llamada, salvo que toma un argumento de puntero adicional. Este puntero es idéntico al puntero opaco que se proporciona al llamar <a href="glutessbeginpolygon.md"><strong>a gluTessBeginPolygon.</strong></a> El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> *<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong>  ** <em>outData</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_ERROR</td>
<td>Se GLU_TESS_ERROR devolución de llamada cuando se encuentra un error. El único argumento es de tipo <strong>GLenum</strong>; indica el error específico que se produjo y se establece en uno de los siguientes: GLU_TESS_MISSING_BEGIN_POLYGON<br/> GLU_TESS_MISSING_END_POLYGON<br/> GLU_TESS_MISSING_BEGIN_CONTOUR<br/> GLU_TESS_MISSING_END_CONTOUR<br/> GLU_TESS_COORD_TOO_LARGE<br/> GLU_TESS_NEED_COMBINE_CALLBACK<br/> Llame a gluErrorString para recuperar cadenas de caracteres que describen estos errores. El prototipo de función para esta devolución de llamada es el siguiente:<br/> <strong>void</strong> <strong>error</strong> (<strong>GLenum</strong> <em>errno</em>);<br/> La biblioteca GLU se recupera de los cuatro primeros errores insertando la llamada o las llamadas que faltan. GLU_TESS_COORD_TOO_LARGE indica que alguna coordenada de vértice superó la constante predefinida GLU_TESS_MAX_COORD valor absoluto y que el valor se ha fijado. (Los valores de coordenadas deben ser lo suficientemente pequeños como para que dos se puedan multiplicar juntos sin desbordamiento). GLU_TESS_NEED_COMBINE_CALLBACK indica que la teselación detectó una intersección entre dos bordes de los datos de entrada y no se proporcionó la devolución de llamada GLU_TESS_COMBINE o GLU_TESS_COMBINE_DATA de llamada. No se generará ninguna salida.<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_ERROR_DATA</td>
<td>La GLU_TESS_ERROR_DATA de llamada es la misma que la GLU_TESS_ERROR de llamada, salvo que toma un argumento de puntero adicional. Este puntero es idéntico al puntero opaco que se proporciona al llamar <a href="glutessbeginpolygon.md"><strong>a gluTessBeginPolygon.</strong></a> El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>errorData</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> <dt>

[**gluDeleteTess**](gludeletetess.md)
</dt> <dt>

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





