---
title: función gluNurbsProperty (GLU. h)
description: La función gluNurbsProperty establece una propiedad no uniforme B-spline racional (NURBS).
ms.assetid: c8c3b0c3-11b8-4123-91b6-75fed78932ce
keywords:
- gluNurbsProperty (función) OpenGL
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
ms.openlocfilehash: 55eb8ed1914f500052c8565f6cc73e56f83bea1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488956"
---
# <a name="glunurbsproperty-function"></a>gluNurbsProperty función)

La función **gluNurbsProperty** establece una propiedad no uniforme B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)).

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

El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*property* 
</dt> <dd>

Propiedad que se va a establecer. Valores válidos son:



| Value                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_SAMPLING_TOLERANCE"></span><span id="glu_sampling_tolerance"></span><dl> <dt>**\_tolerancia de muestreo de Glu \_**</dt> </dl>       | Especifica la longitud máxima, en píxeles, que se va a usar cuando el método de muestreo se establezca en la longitud de la \_ ruta de acceso Glu \_ . El valor predeterminado es 50,0 píxeles.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GLU_DISPLAY_MODE"></span><span id="glu_display_mode"></span><dl> <dt>**\_modo de presentación de Glu \_**</dt> </dl>                         | El parámetro *Value* define cómo se va a representar una superficie NURBS. Puede establecer el *valor* en Glu \_ Fill, Glu \_ Outline \_ Polygon o Glu \_ Outline \_ patch. <br/> GLU \_ relleno. La superficie se representa como un conjunto de polígonos. Este es el valor predeterminado. <br/> GLU \_ : Polígono de contorno \_ . La biblioteca de NURBS solo dibuja los contornos de los polígonos creados por la teselación. <br/> \_revisión del esquema Glu \_ . Solo se dibujan los contornos de las revisiones y las curvas de recorte definidas por el usuario.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CULLING"></span><span id="glu_culling"></span><dl> <dt>**selección de GLU \_**</dt> </dl>                                         | El parámetro *Value* es un valor booleano. Cuando valor se establece en GL \_ true, las curvas NURBS cuyos puntos de control se encuentran fuera de la ventanilla actual se descartan antes de la teselación. El valor predeterminado es GL \_ false (porque una curva NURBS no puede estar completamente dentro del casco convexo de sus puntos de control).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GLU_AUTO_LOAD_MATRIX"></span><span id="glu_auto_load_matrix"></span><dl> <dt>**GLU \_ \_ matriz de carga automática \_**</dt> </dl>            | El parámetro *Value* es un valor booleano. Cuando se establece en GL \_ es true, el código NURBS descarga la matriz de proyección, la matriz de MODELVIEW y la ventanilla del servidor OpenGL para calcular el muestreo y las matrices de selección para cada curva de NURBS que se representa. Se requieren matrices de muestreo y selección para determinar la teselación de una superficie de NURBS en segmentos de línea o polígonos, y para seleccionar una superficie de NURBS si está fuera de la ventanilla. <br/> Si este modo se establece en GL \_ false, debe proporcionar una matriz de proyección, una matriz de MODELVIEW y una ventanilla para que el representador de NURBS pueda usarlos para construir matrices de muestreo y selección. Puede hacerlo con la función [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md) .<br/> El valor predeterminado de este modo es GL \_ true. Si se cambia este modo de GL \_ true a GL \_ false, no se verán afectadas las matrices de muestreo y selección hasta que se llame a [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md). <br/> Los siguientes parámetros de propiedad se admiten en la versión 1,1 de GLU o posterior y no son válidos para la versión 1,0 de GLU: \_ tolerancia paramétrica Glu \_ , \_ método de muestreo Glu \_ , GLU \_ U \_ STEP y Glu \_ V \_ Step.<br/> Los siguientes parámetros de valor se admiten en la versión 1,1 de GLU o posterior y no son válidos para la versión 1,0 de la ruta de acceso de GLU: GLU \_ \_ , error de Glu \_ paramétricos \_ y \_ distancia del dominio Glu \_ .<br/> |
| <span id="GLU_PARAMETRIC_TOLERANCE"></span><span id="glu_parametric_tolerance"></span><dl> <dt>**\_tolerancia paramétrica \_ Glu**</dt> </dl> | Especifica la distancia máxima, en píxeles, que se va a usar cuando el método de muestreo se establezca en GLU \_ Parametric \_ error. El valor predeterminado es 0,5.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_SAMPLING_METHOD"></span><span id="glu_sampling_method"></span><dl> <dt>**\_método de muestreo Glu \_**</dt> </dl>                | Especifica cómo tessallate una superficie NURBS. \_El método de muestreo Glu \_ puede tener uno de los tres valores siguientes. <br/> longitud de la \_ ruta de acceso Glu \_ . Valor predeterminado. Especifica que las superficies representadas con la longitud máxima, en píxeles, de los bordes de los polígonos de teselación no son mayores que el valor especificado por la tolerancia de muestreo de GLU \_ \_ . <br/> \_error paramétrico de Glu \_ . Especifica que, al representar la superficie, el valor de la \_ tolerancia paramétrica Glu \_ especifica la distancia máxima, en píxeles, entre los polígonos de teselación y las superficies aproximadas. <br/> \_distancia del dominio Glu \_ . Especifica, en coordenadas paramétricas, el número de puntos de ejemplo por longitud de unidad que se van a tomar en las dimensiones de *u* y *v* .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GLU_U_STEP"></span><span id="glu_u_step"></span><dl> <dt>**paso de GLU \_ U \_**</dt> </dl>                                           | Especifica el número de puntos de ejemplo por longitud de unidad tomadas a lo largo de la dimensión *u* en coordenadas paramétricas. El valor del \_ paso Glu U \_ se usa cuando el \_ método de muestreo Glu \_ se establece en Glu de la \_ distancia del dominio \_ . El valor predeterminado es 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_V_STEP"></span><span id="glu_v_step"></span><dl> <dt>**paso de GLU \_ V \_**</dt> </dl>                                           | Especifica el número de puntos de ejemplo por longitud de unidad tomadas a lo largo de la dimensión *v* en coordenadas paramétricas. El valor de GLU \_ V \_ STEP se usa cuando el \_ método de muestreo Glu \_ se establece en Glu de la \_ distancia del dominio \_ . El valor predeterminado es 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*value* 
</dt> <dd>

Valor en el que se va a establecer la propiedad indicada. El parámetro de *valor* puede ser un valor numérico o uno de los tres valores siguientes: Glu longitud de la \_ ruta \_ de acceso, Glu de \_ error paramétrico \_ o distancia del dominio de Glu \_ \_ .



| Value                                                                                                                                                                               | Significado                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_PATH_LENGTH"></span><span id="glu_path_length"></span><dl> <dt>**longitud de la \_ ruta de acceso Glu \_**</dt> </dl>                | Valor predeterminado. Especifica que las superficies representadas con la longitud máxima, en píxeles, de los bordes de los polígonos de teselación no son mayores que el valor especificado por la tolerancia de muestreo de GLU \_ \_ .<br/> |
| <span id="GLU_PARAMETRIC_ERROR"></span><span id="glu_parametric_error"></span><dl> <dt>**ERROR paraGLU \_ Parametric \_**</dt> </dl> | Especifica que, al representar la superficie, el valor de la \_ tolerancia paramétrica Glu \_ especifica la distancia máxima, en píxeles, entre los polígonos de teselación y las superficies aproximadas.<br/>       |
| <span id="GLU_DOMAIN_DISTANCE"></span><span id="glu_domain_distance"></span><dl> <dt>**\_distancia del dominio de Glu \_**</dt> </dl>    | Especifica, en coordenadas paramétricas, el número de puntos de ejemplo por longitud de unidad que se van a tomar en las dimensiones de *u* y *v* .<br/>                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use **gluNurbsProperty** para controlar las propiedades almacenadas en un objeto NURBS. Estas propiedades afectan a la manera en que se representa una curva de NURBS.





 

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

[**gluGetNurbsProperty**](glugetnurbsproperty.md)
</dt> <dt>

[**gluGetString**](glugetstring.md)
</dt> <dt>

[**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





