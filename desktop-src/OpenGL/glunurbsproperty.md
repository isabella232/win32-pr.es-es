---
title: Función gluNurbsProperty (Glu.h)
description: La función gluNurbsProperty establece una propiedad non-Uniform Rational B-Spline (SPLINEBS).
ms.assetid: c8c3b0c3-11b8-4123-91b6-75fed78932ce
keywords:
- Función gluNurbsProperty OpenGL
topic_type:
- apiref
api_name:
- gluNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cbc52bd1405d15967db4aa1ef4941d0c4e166420d25d6d1fcb1ba4db0a6e744
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489035"
---
# <a name="glunurbsproperty-function"></a>función gluNurbsProperty

La **función gluNurbsProperty** establece una propiedad Non-Uniform Rational B-Spline [(SPLINEBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nobj* 
</dt> <dd>

El objeto RGBBS (creado [**con gluNewNurbsRenderer).**](glunewnurbsrenderer.md)

</dd> <dt>

*property* 
</dt> <dd>

Propiedad que se va a establecer. Valores válidos son:



| Valor                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_SAMPLING_TOLERANCE"></span><span id="glu_sampling_tolerance"></span><dl> <dt>**TOLERANCIA \_ DE MUESTREO DE \_ GLU**</dt> </dl>       | Especifica la longitud máxima, en píxeles, que se usará cuando el método de muestreo se establezca en GLU \_ PATH \_ LENGTH. El valor predeterminado es 50,0 píxeles.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GLU_DISPLAY_MODE"></span><span id="glu_display_mode"></span><dl> <dt>**MODO DE VISUALIZACIÓN DE GLU \_ \_**</dt> </dl>                         | El *parámetro* value define cómo se va a representar una superficie DE LABS. Puede establecer el *valor en* GLU \_ FILL, GLU OUTLINE POLYGON o GLU \_ OUTLINE \_ \_ \_ PATCH. <br/> GLU \_ FILL. La superficie se representa como un conjunto de polígonos. Este es el valor predeterminado. <br/> POLÍGONO \_ DE CONTORNO DE \_ GLU. La biblioteca DEIBERBERS dibuja solo los contornos de los polígonos creados por teselación. <br/> REVISIÓN \_ DE CONTORNO \_ DE GLU. Solo se dibujan los contornos de las revisiones y las curvas de recorte definidas por el usuario.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CULLING"></span><span id="glu_culling"></span><dl> <dt>**GLU \_ CULLING**</dt> </dl>                                         | El *parámetro value* es un valor booleano. Cuando el valor se establece en GL TRUE, las curvas DE ASEBS cuyos puntos de control se encuentran fuera de la ventanilla actual se descartan antes de \_ la teselación. El valor predeterminado es GL FALSE (porque una curva DESTEBS no puede estar completamente dentro de la casco \_ convexa de sus puntos de control).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GLU_AUTO_LOAD_MATRIX"></span><span id="glu_auto_load_matrix"></span><dl> <dt>**MATRIZ \_ DE \_ CARGA AUTOMÁTICA DE GLU \_**</dt> </dl>            | El *parámetro value* es un valor booleano. Cuando se establece en GL TRUE, el código DESCRIPTBS descarga la matriz de proyección, la matriz modelview y la ventanilla desde el servidor OpenGL para calcular el muestreo y la selección de matrices para cada curva DE ASEBS que se \_ representa. Las matrices de muestreo y de selección son necesarias para determinar la teselación de una superficie DE LANBS en segmentos de línea o polígonos, y para crear una superficie DE LABS si se encuentra fuera de la ventanilla. <br/> Si este modo se establece en GL FALSE, debe proporcionar una matriz de proyección, una matriz modelview y una ventanilla para que el representador de LABS use para construir matrices de muestreo \_ y de selección. Puede hacerlo con la función [**gluLoadSamplingMatrices.**](gluloadsamplingmatrices.md)<br/> El valor predeterminado para este modo es GL \_ TRUE. El cambio de este modo de GL TRUE a GL FALSE no afecta a las matrices de muestreo y selección hasta que llame \_ \_ a [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md). <br/> Los siguientes parámetros de propiedad se admiten en glu versión 1.1 o posterior y no son válidos para la versión 1.0 de GLU: GLU \_ PARAMETRIC \_ TOLERANCE, GLU SAMPLING METHOD, GLU U STEP y \_ GLU V \_ \_ \_ \_ \_ STEP.<br/> Los siguientes parámetros de valor se admiten en glu versión 1.1 o posterior y no son válidos para la versión 1.0 de GLU: GLU \_ PATH \_ LENGTH, GLU PARAMETRIC ERROR y GLU \_ DOMAIN \_ \_ \_ DISTANCE.<br/> |
| <span id="GLU_PARAMETRIC_TOLERANCE"></span><span id="glu_parametric_tolerance"></span><dl> <dt>**TOLERANCIA \_ PARAMÉTRICA DE GLU \_**</dt> </dl> | Especifica la distancia máxima, en píxeles, que se usará cuando el método de muestreo se establezca en GLU \_ PARAMETRIC \_ ERROR. El valor predeterminado es 0,5.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_SAMPLING_METHOD"></span><span id="glu_sampling_method"></span><dl> <dt>**MÉTODO \_ DE MUESTREO DE \_ GLU**</dt> </dl>                | Especifica cómo tessallate a una superficie DE LABS. GLU \_ SAMPLING METHOD puede tener uno de los tres valores \_ siguientes. <br/> LONGITUD \_ DE LA RUTA DE ACCESO DE \_ GLU. Valor predeterminado. Especifica que las superficies que se representan con la longitud máxima, en píxeles, de los bordes de los polígonos de teselación no son mayores que el valor especificado por GLU \_ SAMPLING \_ TOLERANCE. <br/> \_ \_ ERROR PARAMÉTRICO DE GLU. Especifica que, al representar la superficie, el valor de GLU PARAMETRIC TOLERANCE especifica la distancia máxima, en píxeles, entre los polígonos de teselación y las \_ \_ superficies aproximadas. <br/> DISTANCIA \_ DE DOMINIO DE \_ GLU. Especifica, en coordenadas paramétricas, cuántos puntos de muestra por longitud de unidad se tomarán en las *dimensiones u* y *v.*<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GLU_U_STEP"></span><span id="glu_u_step"></span><dl> <dt>**PASO \_ DE GLU U \_**</dt> </dl>                                           | Especifica el número de puntos de muestra por longitud de unidad tomada a lo largo de la dimensión *u* en coordenadas paramétricas. El valor de GLU \_ U STEP se usa cuando GLU SAMPLING METHOD se establece en GLU DOMAIN \_ \_ \_ \_ \_ DISTANCE. El valor predeterminado es 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_V_STEP"></span><span id="glu_v_step"></span><dl> <dt>**PASO DE GLU \_ V \_**</dt> </dl>                                           | Especifica el número de puntos de muestra por longitud de unidad tomada a lo largo de la *dimensión v* en coordenadas paramétricas. El valor de GLU \_ V STEP se usa cuando GLU SAMPLING METHOD se establece en GLU DOMAIN \_ \_ \_ \_ \_ DISTANCE. El valor predeterminado es 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*value* 
</dt> <dd>

Valor en el que se va a establecer la propiedad indicada. El *parámetro* value puede ser un valor numérico o uno de los tres valores siguientes: GLU \_ PATH \_ LENGTH, GLU \_ PARAMETRIC ERROR o GLU DOMAIN \_ \_ \_ DISTANCE.



| Valor                                                                                                                                                                               | Significado                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_PATH_LENGTH"></span><span id="glu_path_length"></span><dl> <dt>**LONGITUD DE \_ LA RUTA DE ACCESO DE GLU \_**</dt> </dl>                | Valor predeterminado. Especifica que las superficies que se representan con la longitud máxima, en píxeles, de los bordes de los polígonos de teselación no son mayores que el valor especificado por GLU \_ SAMPLING \_ TOLERANCE.<br/> |
| <span id="GLU_PARAMETRIC_ERROR"></span><span id="glu_parametric_error"></span><dl> <dt>**\_ERROR PARAMÉTRICO DE GLU \_**</dt> </dl> | Especifica que, al representar la superficie, el valor de GLU PARAMETRIC TOLERANCE especifica la distancia máxima, en píxeles, entre los polígonos de teselación y las \_ \_ superficies aproximadas.<br/>       |
| <span id="GLU_DOMAIN_DISTANCE"></span><span id="glu_domain_distance"></span><dl> <dt>**DISTANCIA DE DOMINIO DE GLU \_ \_**</dt> </dl>    | Especifica, en coordenadas paramétricas, cuántos puntos de muestra por longitud de unidad se tomarán en las *dimensiones u* y *v.*<br/>                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Use **gluNurbsProperty para** controlar las propiedades almacenadas en un objeto DEBS. Estas propiedades afectan a la forma en que se representa una curva DE ASEBS.





 

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

[**gluGetNurbsProperty**](glugetnurbsproperty.md)
</dt> <dt>

[**gluGetString**](glugetstring.md)
</dt> <dt>

[**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





