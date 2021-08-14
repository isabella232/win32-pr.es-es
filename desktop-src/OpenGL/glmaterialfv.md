---
title: Función glMaterialfv (Gl.h)
description: La función glMaterialfv especifica parámetros de material para el modelo de iluminación.
ms.assetid: cd357686-4d6f-49fd-a111-308b5485ac21
keywords:
- Función glMaterialfv OpenGL
topic_type:
- apiref
api_name:
- glMaterialfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05c4d8fc3f1e141f9913fe997da0b9982200f6be77edc5e4ef190970ee2fca87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358953"
---
# <a name="glmaterialfv-function"></a>función glMaterialfv

La **función glMaterialfv** especifica parámetros de material para el modelo de iluminación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glMaterialfv(
         GLenum  face,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cara* 
</dt> <dd>

La cara o las caras que se están actualizando. Debe ser uno de los siguientes: GL \_ FRONT, GL \_ BACK o GL FRONT y GL \_ \_ BACK.

</dd> <dt>

*pname* 
</dt> <dd>

Parámetro material de la cara o caras que se están actualizando. Los parámetros que se pueden especificar mediante **glMaterialfv** y sus interpretaciones por la ecuación de iluminación son los siguientes.



| Valor                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ AMBIENT**</dt> </dl>                                       | El parámetro params contiene cuatro valores de punto flotante que especifican la reflectancia RGBA ambiente del material. Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a -1,0. Los valores de punto flotante se asignan directamente. No se fijan valores enteros ni de punto flotante. La reflectancia ambiente predeterminada para los materiales orientados hacia delante y hacia atrás es (0,2, 0,2, 0,2, 1,0). <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFUSO**</dt> </dl>                                       | El parámetro params contiene cuatro valores de punto flotante que especifican la reflectancia RGBA difusa del material. Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a -1,0. Los valores de punto flotante se asignan directamente. No se fijan valores enteros ni de punto flotante. La reflectancia difusa predeterminada para los materiales orientados hacia delante y hacia atrás es (0,8, 0,8, 0,8, 1,0). <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ SPECULAR**</dt> </dl>                                    | El parámetro params contiene cuatro valores de punto flotante que especifican la reflectancia RGBA especular del material. Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a -1,0. Los valores de punto flotante se asignan directamente. No se fijan valores enteros ni de punto flotante. La reflectancia especular predeterminada para los materiales orientados hacia delante y hacia atrás es (0,0, 0,0, 0,0, 1,0). <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**EMISIÓN DE GL \_**</dt> </dl>                                    | El parámetro params contiene cuatro valores de punto flotante que especifican la intensidad de luz emitida RGBA del material. Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a -1,0. Los valores de punto flotante se asignan directamente. No se fijan valores enteros ni de punto flotante. La intensidad de emisión predeterminada para los materiales orientados hacia delante y hacia atrás es (0,0, 0,0, 0,0, 1,0). <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**GL \_ GLINESS**</dt> </dl>                                 | El *parámetro param* es un valor entero único que especifica el exponente especular RGBA del material. Los valores enteros se asignan directamente. Solo se aceptan los valores \[ del intervalo 0, 128. \] El exponente especular predeterminado para los materiales orientados hacia delante y hacia atrás es 0. <br/>                                                                                                                                                                                                      |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <dt>**AMBIENTE \_ Y \_ \_ DIFUSO DE GL**</dt> </dl> | Equivalente a llamar [**a glMaterial dos**](glmaterial-functions.md) veces con los mismos valores de parámetro, una con \_ GL AMBIENT y otra con GL \_ DIFFUSE. <br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**ÍNDICES \_ DE COLOR \_ GL**</dt> </dl>                    | El parámetro params contiene tres valores de punto flotante que especifican los índices de color para la iluminación ambiental, difusa y especular. Estos tres valores, y GL GLTICOINESS, son los únicos valores materiales utilizados por la ecuación de iluminación \_ del modo de índice de color. Consulte [**glLightModel para**](gllightmodel-functions.md) obtener una explicación de la iluminación de índice de color.<br/>                                                                                                                                  |



 

</dd> <dt>

*params* 
</dt> <dd>

Valor en el que se establecerá el \_ parámetro GLCULEINESS.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                              | Significado                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>  | Face *o* *pname* no era un valor aceptado.<br/>                |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl> | Se especificó un exponente especular fuera del \[ intervalo de 0, 128. \]<br/> |



## <a name="remarks"></a>Comentarios

La [**función glMaterialfv**](glmaterialf.md) asigna valores a parámetros de material. Hay dos conjuntos coincidentes de parámetros de material. Uno,  el conjunto de orientación frontal, se usa para sombrear puntos, líneas, mapas de bits y todos los polígonos (cuando la iluminación de dos lados está deshabilitada) o simplemente los polígonos orientados al frente (cuando la iluminación de dos lados está habilitada). El otro conjunto, *orientado hacia atrás,* se usa para sombrear polígonos orientados hacia atrás solo cuando la iluminación de dos lados está habilitada. Consulte [**glLightModel para**](gllightmodel-functions.md) obtener más información sobre los cálculos de iluminación de uno y dos lados.

La [**función glMaterialfv**](glmaterialf.md) toma tres argumentos. La primera, *face*, especifica si se modificarán los materiales GL \_ FRONT, GL \_ BACK o GL FRONT Y \_ \_ \_ BACK. El segundo, *pname*, especifica cuál de varios parámetros de uno o ambos conjuntos se modificará. El tercer *parámetro, param*, especifica qué valor se asignará al parámetro especificado.

Los parámetros de material se usan en la ecuación de iluminación que se aplica opcionalmente a cada vértice. La ecuación se describe en [**glLightModel**](gllightmodel-functions.md).

Los parámetros de material se pueden actualizar en cualquier momento. En concreto, se puede llamar a [**glMaterialfv**](glmaterialf.md) entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md). Si solo se va a cambiar un parámetro de material por vértice, se prefiere [**glColorMaterial**](glcolormaterial.md) sobre **glMaterialfv.**

La función siguiente recupera información relacionada con [**glMaterialfv**](glmaterialf.md):

[**glGetMaterial**](glgetmaterial.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





