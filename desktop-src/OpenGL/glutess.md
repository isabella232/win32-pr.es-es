---
title: función gluTessCallback (GLU. h)
description: La función gluTessCallback define una devolución de llamada para un objeto de teselación.
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- gluTessCallback (función) OpenGL
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
ms.openlocfilehash: 17cdba8b9dd9a3e762a93923a3c353fbc9578377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997000"
---
# <a name="glutesscallback-function"></a>gluTessCallback función)

La función **gluTessCallback** define una devolución de llamada para un objeto de teselación.

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

*tess* 
</dt> <dd>

Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*cuales* 
</dt> <dd>

Devolución de llamada que se está definiendo. Los valores siguientes son válidos: GLU \_ Tess \_ Begin, Glu \_ Tess \_ Begin \_ Data, GLU \_ Tess \_ Edge \_ Flag, Glu \_ Tess \_ Edge \_ Flag \_ Data, Glu \_ Tess \_ Vertex, GLU \_ Tess \_ Vertex \_ Data, Glu \_ Tess \_ End, Glu \_ Tess \_ End \_ Data, Glu \_ Tess \_ combine, Glu \_ Tess \_ combine \_ Data, Glu \_ Tess \_ error y Glu Tess \_ \_ error \_ Data.

Para obtener más información sobre estas devoluciones de llamada, vea la sección Comentarios siguiente.

</dd> <dt>

*fn* 
</dt> <dd>

Función a la que se va a llamar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use **gluTessCallback** para especificar una devolución de llamada que va a usar un objeto de teselación. Si la devolución de llamada especificada ya está definida, se reemplaza. Si *FN* es **null**, la devolución de llamada existente queda sin definir.

El objeto de teselación utiliza estas devoluciones de llamada para describir cómo un polígono que se especifica se divide en triángulos.

Hay dos versiones de cada devolución de llamada, una con datos de polígono que puede definir y otra sin. Si se especifican ambas versiones de una devolución de llamada determinada, se usará la devolución de llamada con los datos de polígono que especifique. El parámetro de *\_ datos Polygon* de [**gluTessBeginPolygon**](glutessbeginpolygon.md) es una copia del puntero que se especificó cuando se llamó a **gluTessBeginPolygon** .

A continuación se indican las devoluciones de llamada válidas:



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
<td>La devolución de llamada de GLU_TESS_BEGIN se invoca como <a href="glbegin.md"><strong>glBegin</strong></a> para indicar el inicio de una primitiva (triángulo). La función toma un único argumento de tipo <strong>GLenum</strong>. Si establece la propiedad GLU_TESS_BOUNDARY_ONLY en GL_FALSE, el argumento se establece en GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP o GL_TRIANGLES. Si establece la propiedad GLU_TESS_BOUNDARY_ONLY en GL_TRUE, el argumento se establece en GL_LINE_LOOP. El prototipo de función para esta devolución de llamada es el siguiente: <strong>void</strong> <strong>Begin</strong> ( <em>tipo</em><strong>GLenum</strong> );<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_BEGIN_DATA</td>
<td>GLU_TESS_BEGIN_DATA es igual que la devolución de llamada de GLU_TESS_BEGIN, salvo que toma un argumento de puntero adicional. Este puntero es idéntico al puntero opaco que se proporciona al llamar a <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>beginData</strong> ( <em>tipo</em><strong>GLenum</strong> , <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_EDGE_FLAG</td>
<td>La devolución de llamada GLU_TESS_EDGE_FLAG es similar a <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>. La función toma una única marca booleana que indica qué bordes se encuentran en el límite del polígono. Si la marca es GL_TRUE, cada vértice siguiente comienza un borde que se encuentra en el límite del polígono; es decir, un borde que separa una región interior de una exterior. Si la marca es GL_FALSE, cada vértice siguiente comienza un borde que se encuentra en el interior del polígono. La devolución de llamada de GLU_TESS_EDGE_FLAG (si se define) se invoca antes de que se realice la primera devolución de llamada de vértice. Dado que los ventiladores de triángulo y las tiras de triángulos no admiten marcas de borde, la devolución de llamada de inicio no se llama con GL_TRIANGLE_FAN o GL_TRIANGLE_STRIP si se proporciona una devolución de llamada de marca perimetral. En su lugar, los ventiladores y las franjas se convierten en triángulos independientes. El prototipo de función para esta devolución de llamada es:<br/> <strong>void</strong> <strong>edgeFlag</strong> (<strong></strong> <em>marca</em>GLboolean);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_EDGE_FLAG_DATA</td>
<td>La devolución de llamada de GLU_TESS_EDGE_FLAG_DATA es igual que la devolución de llamada de GLU_TESS_EDGE_FLAG, salvo que toma un argumento de puntero adicional. Este puntero es idéntico al puntero opaco que se proporciona al llamar a <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>edgeFlagData</strong> ( <em>marca</em><strong>GLboolean</strong> , <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_VERTEX</td>
<td>Se invoca la devolución de llamada de GLU_TESS_VERTEX entre las devoluciones de llamada Begin y end. Es similar a glVertex y define los vértices de los triángulos creados por el proceso de teselación. La función toma un puntero como único argumento. Este puntero es idéntico al puntero opaco que proporcionó al definir el vértice (vea <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>). El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> * <em>vertex_data</em>);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_VERTEX_DATA</td>
<td>La GLU_TESS_VERTEX_DATA es igual que la devolución de llamada de GLU_TESS_VERTEX, salvo que toma un argumento de puntero adicional. Este puntero es idéntico al puntero opaco que se proporciona al llamar a <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. El prototipo de función para esta devolución de llamada es: <strong>void</strong>  <strong>vertexData</strong> (void * <em>vertex_data</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_END</td>
<td>La devolución de llamada de GLU_TESS_END tiene el mismo propósito que <a href="glend.md"><strong>glEnd</strong></a>. Indica el final de un primitivo y no toma ningún argumento. El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>End</strong> (<strong>void</strong>);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_END_DATA</td>
<td>La devolución de llamada de GLU_TESS_END_DATA es igual que la devolución de llamada de GLU_TESS_END, salvo que toma un argumento de puntero adicional. Este puntero es idéntico al puntero opaco que se proporciona al llamar a <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_COMBINE</td>
<td>Llame a la GLU_TESS_COMBINE devolución de llamada para crear un nuevo vértice cuando la teselación detecta una intersección o para combinar características. La función toma cuatro argumentos: una matriz de tres elementos, cada uno de los cuales es de tipo Gldouble.<br/> Matriz de cuatro punteros.<br/> Una matriz de cuatro elementos, cada uno de los cuales es de tipo GLfloat.<br/> Puntero a un puntero.<br/> El prototipo de función para esta devolución de llamada es: <br/> <strong>void</strong> <strong>combine</strong>(<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> * <em>vertex_data</em>[4], <strong>GLfloat</strong> <em>Weight</em>[4], <strong>void</strong>  ** <em>outdata</em>);<br/> El vértice se define como una combinación lineal de hasta cuatro vértices existentes, almacenados en vertex_data. Los coeficientes de la combinación lineal se proporcionan por peso; Estos pesos siempre suman a 1,0. Todos los punteros de vértice son válidos aunque algunos de los pesos sean cero. El parámetro coords proporciona la ubicación del nuevo vértice.<br/> Asigne otro vértice, interpole los parámetros con vertex_data y peso, y devuelva el nuevo puntero de vértice en outdata. Este identificador se proporciona durante las devoluciones de llamada de representación. Libere memoria después de llamar a <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.<br/> Por ejemplo, si el polígono se encuentra en un plano arbitrario en un espacio tridimensional y asocia un color a cada vértice, la devolución de llamada de GLU_TESS_COMBINE podría ser similar a la siguiente:<br/>
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
Cuando la teselación detecta una intersección, se debe definir el GLU_TESS_COMBINE o GLU_TESS_COMBINE_DATA devolución de llamada (vea a continuación) y debe escribir un puntero no<strong>nulo</strong> en dataOut. En caso contrario, se produce el error GLU_TESS_NEED_COMBINE_CALLBACK y no se genera ninguna salida. (Este es el único error que se puede producir durante la representación y la teselación).<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_COMBINE_DATA</td>
<td>La devolución de llamada de GLU_TESS_COMBINE_DATA es igual que la devolución de llamada de GLU_TESS_COMBINE, salvo que toma un argumento de puntero adicional. Este puntero es idéntico al puntero opaco que se proporciona al llamar a <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> *<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>Weight</em>[4], <strong>void</strong>  ** <em>outdata</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_ERROR</td>
<td>Se llama a la devolución de llamada de GLU_TESS_ERROR cuando se produce un error. El único argumento es de tipo <strong>GLenum</strong>; indica el error específico que se ha producido y está establecido en uno de los siguientes: GLU_TESS_MISSING_BEGIN_POLYGON<br/> GLU_TESS_MISSING_END_POLYGON<br/> GLU_TESS_MISSING_BEGIN_CONTOUR<br/> GLU_TESS_MISSING_END_CONTOUR<br/> GLU_TESS_COORD_TOO_LARGE<br/> GLU_TESS_NEED_COMBINE_CALLBACK<br/> Llame a gluErrorString para recuperar las cadenas de caracteres que describen estos errores. El prototipo de función para esta devolución de llamada es el siguiente:<br/> <strong></strong> <strong>error</strong> void (<strong>GLenum</strong> <em>errno</em>);<br/> La biblioteca GLU se recupera de los cuatro primeros errores mediante la inserción de la llamada o llamadas que faltan. GLU_TESS_COORD_TOO_LARGE indica que alguna coordenada de vértices superó la constante predefinida GLU_TESS_MAX_COORD en el valor absoluto y que el valor se ha fijado. (Los valores de las coordenadas deben ser lo suficientemente pequeños como para multiplicarlos sin desbordamiento). GLU_TESS_NEED_COMBINE_CALLBACK indica que la teselación detectó una intersección entre dos bordes en los datos de entrada y no se proporcionó la devolución de llamada de GLU_TESS_COMBINE o GLU_TESS_COMBINE_DATA. No se generará ninguna salida.<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_ERROR_DATA</td>
<td>La devolución de llamada de GLU_TESS_ERROR_DATA es igual que la devolución de llamada de GLU_TESS_ERROR, salvo que toma un argumento de puntero adicional. Este puntero es idéntico al puntero opaco que se proporciona al llamar a <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>datoserror</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
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

 

 





