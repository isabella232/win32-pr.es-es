---
title: función glMaterialiv (GL. h)
description: La función glMaterialiv especifica los parámetros de material para el modelo de iluminación.
ms.assetid: 9d045202-e565-4cf7-946a-60299e1bc1b1
keywords:
- glMaterialfv (función) OpenGL
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
ms.openlocfilehash: 95f12a5d34357a3436ffd6725ad2f1d56901e700
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422217"
---
# <a name="glmaterialiv-function"></a>glMaterialiv función)

La función **glMaterialiv** especifica los parámetros de material para el modelo de iluminación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glMaterialfv(
         GLenum face,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Portada* 
</dt> <dd>

La cara o caras que se están actualizando. Debe ser uno de los siguientes: GL \_ Front, GL \_ back o GL \_ Front y GL \_ back.

</dd> <dt>

*PName* 
</dt> <dd>

Parámetro de material de la cara o caras que se están actualizando. Los parámetros que se pueden especificar mediante [**glMaterialiv**](glmaterialfv.md)y sus interpretaciones por la ecuación de iluminación son los siguientes.



| Value                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**ambiente de contabilidad general \_**</dt> </dl>                                       | El parámetro params contiene cuatro valores enteros que especifican la reflectancia RGBA ambiental del material. Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0. Los valores de punto flotante se asignan directamente. Ninguno de los valores enteros ni de punto flotante está fijado. La reflexión ambiente predeterminada para los materiales de orientación frontal y hacia delante es (0,2, 0,2, 0,2, 1,0). <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**difusión en contab. \_**</dt> </dl>                                       | El parámetro params contiene cuatro valores enteros que especifican la reflectancia RGBA difusa del material. Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0. Los valores de punto flotante se asignan directamente. Ninguno de los valores enteros ni de punto flotante está fijado. La reflexión difusa predeterminada para los materiales de orientación frontal y hacia delante es (0,8, 0,8, 0,8, 1,0). <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_especular GL**</dt> </dl>                                    | El parámetro params contiene cuatro valores enteros que especifican el reflejo de RGBA especular del material. Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0. Los valores de punto flotante se asignan directamente. Ninguno de los valores enteros ni de punto flotante está fijado. La reflexión especular predeterminada para los materiales de orientación frontal y hacia delante es (0,0, 0,0, 0,0, 1,0). <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**emisión de contabilidad \_**</dt> </dl>                                    | El parámetro params contiene cuatro valores enteros que especifican la intensidad clara emitida del RGBA del material. Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0. Los valores de punto flotante se asignan directamente. Ninguno de los valores enteros ni de punto flotante está fijado. La intensidad de emisión predeterminada de los materiales orientados delante y hacia delante es (0,0, 0,0, 0,0, 1,0). <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**brillo de GL \_**</dt> </dl>                                 | El parámetro *param* es un entero único que especifica el exponente especular RGBA del material. Los valores enteros se asignan directamente. Solo se aceptan los valores del intervalo comprendido entre \[ 0 y 128 \] . El exponente especular predeterminado para el material orientado hacia delante y hacia atrás es 0. <br/>                                                                                                                                                                                                     |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <dt>**\_ambiente de contabilidad general \_ y \_ difuso**</dt> </dl> | Equivalente a llamar a [**glMaterial**](glmaterial-functions.md) dos veces con los mismos valores de parámetro, una vez con el ambiente de contabilidad general \_ y otra con el difuso de contabilidad \_ . <br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**\_índices de color de GL \_**</dt> </dl>                    | El parámetro params contiene tres valores enteros que especifican los índices de color para el ambiente, la luz difusa y la iluminación especular. Estos tres valores, y \_ el brillo de contabilidad, son los únicos valores de material usados por la ecuación de iluminación del modo de índice de color. Consulte [**glLightModel**](gllightmodel-functions.md) para obtener una explicación de la iluminación del índice de color.<br/>                                                                                                                                  |



 

</dd> <dt>

*params* 
</dt> <dd>

Valor al que se establecerá el parámetro de brillo de contabilidad \_ .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                              | Significado                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>  | Cualquiera de las *caras* o *PName* no era un valor aceptado.<br/>                |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl> | Se especificó un exponente especular fuera del intervalo de \[ 0, 128 \] .<br/> |



## <a name="remarks"></a>Observaciones

La función [**glMaterialiv**](glmaterialf.md) asigna valores a los parámetros de material. Hay dos conjuntos de parámetros de material coincidentes. Uno, el conjunto *frontal* , se usa para sombrear puntos, líneas, mapas de bits y todos los polígonos (cuando está deshabilitada la iluminación dos caras) o simplemente polígonos frontales (cuando está habilitada la iluminación de dos caras). El otro conjunto, *orientado hacia atrás*, se usa para sombrear polígonos de cara a la inversa solo cuando está habilitada la iluminación de dos caras. Consulte [**glLightModel**](gllightmodel-functions.md) para obtener más información sobre los cálculos de iluminación de una cara y dos caras.

La función [**glMaterialiv**](glmaterialf.md) toma tres argumentos. La primera, *cara*, especifica si se modificarán los materiales de la contabilidad general \_ , los materiales traseros de la contabilidad general o los materiales de la \_ \_ parte delantera y trasera del libro de contabilidad \_ \_ . La segunda, *PName*, especifica cuál de los diversos parámetros de uno o ambos conjuntos se modificarán. El *tercer parámetro especifica* el valor que se asignará al parámetro especificado.

Los parámetros de material se usan en la ecuación de iluminación que se aplica opcionalmente a cada vértice. La ecuación se describe en [**glLightModel**](gllightmodel-functions.md).

Los parámetros de material se pueden actualizar en cualquier momento. En concreto, se puede llamar a [**glMaterialiv**](glmaterialf.md) entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md). Sin embargo, si solo se va a cambiar un parámetro de material por vértice, se prefiere [**glColorMaterial**](glcolormaterial.md) a **glMaterialiv**.

La siguiente función recupera información relacionada con [**glMaterialiv**](glmaterialf.md):

[**glGetMaterial**](glgetmaterial.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





