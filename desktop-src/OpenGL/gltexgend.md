---
title: Función glTexGend (Gl.h)
description: Controla la generación de coordenadas de textura. | Función glTexGend (Gl.h)
ms.assetid: 75ab3468-281d-4c8d-95cc-138d75646cdf
keywords:
- Función glTexGend OpenGL
topic_type:
- apiref
api_name:
- glTexGend
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b05d390c935047065febdb86e9d9c4c68758648b76641c346629c0cde4be5dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490454"
---
# <a name="gltexgend-function"></a>Función glTexGend

Controla la generación de coordenadas de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTexGend(
   GLenum   coord,
   GLenum   pname,
   GLdouble param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Coord* 
</dt> <dd>

Coordenada de textura. Debe ser uno de los siguientes: GL \_ S, GL \_ T, GL \_ R o GL \_ Q.

</dd> <dt>

**pname** 
</dt> <dd>

Nombre simbólico de la función de generación de coordenadas de textura.

</dd> <dt>

*param* 
</dt> <dd>

Un parámetro de generación de textura con un solo valor, uno de GL \_ OBJECT \_ LINEAR, GL \_ EYE LINEAR o GL SPHERE \_ \_ \_ MAP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *coord* o *pname* no era un valor definido aceptado, o *pname* era GL TEXTURE GEN MODE y params no era un \_ \_ valor definido \_ aceptado. <br/> |
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *pname era* GL \_ TEXTURE GEN \_ \_ MODE, *params* era GL SPHERE MAP y \_ \_ *coord* era GL \_ R o GL \_ Q<br/>                                     |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md). <br/>                 |



## <a name="remarks"></a>Comentarios

La **función glTexGen** selecciona una función de generación de coordenadas de textura o proporciona coeficientes para una de las funciones. El *parámetro coord* denomina una de las coordenadas de textura (s,t,r,q) y debe ser uno de estos símbolos: GL \_ S, GL T, GL R o GL \_ \_ \_ Q. El *parámetro pname* debe ser una de las tres constantes simbólicas: GL \_ TEXTURE GEN \_ \_ MODE, GL OBJECT PLANE o GL \_ EYE \_ \_ \_ PLANE. Si *pname es* GL \_ TEXTURE GEN \_ \_ MODE, *param* especifica un modo, uno de GL OBJECT LINEAR, GL EYE LINEAR o \_ GL SPHERE \_ \_ \_ \_ \_ MAP. Si *pname es* GL OBJECT PLANE o \_ GL EYE \_ \_ \_ PLANE, *param* contiene coeficientes para la función de generación de textura correspondiente.

Si la función de generación de texturas es GL \_ OBJECT \_ LINEAR, la función

![Ecuación que muestra la función glTexGen cuando la función de generación de texturas GL_OBJECT_LINEAR.](images/tex02.png)

se usa , donde g es el valor calculado para la coordenada denominada en coord; p1, p2, p3 y p4 son los cuatro valores proporcionados en params; y x?, y?, z?, and w? son las coordenadas de objeto del vértice. Puede usar esta función para texturar el terreno mediante el nivel del mar como plano de referencia (definido por p1, p2, p3 y p4). La función de generación de coordenadas GL OBJECT LINEAR calcula la altitud de un vértice de terreno como su distancia desde el nivel del mar; esa altitud se usa para indexar la imagen de textura para asignar la nieve blanca a picos y el verde a las \_ \_ montañas, por ejemplo.

Si la función de generación de textura es GL \_ EYE \_ LINEAR, la función

![Ecuación que muestra la función glTexGen cuando la función de generación de texturas GL_EYE_LINEAR.](images/tex02.png)

se usa , donde

![Ecuación que muestra las coordenadas oculares del vértice.](images/tex03.png)

y x?, y?, z?, and w? son las coordenadas de los ojos del vértice, p1, p2, p3 y p4 son los valores proporcionados en *param*, y M es la matriz modelview cuando se llama **a glTexGen**. Si M está mal condición o singular, las coordenadas de textura generadas por la función resultante pueden ser inexactas o indefinidos.

Los valores de *param definen* un plano de referencia en coordenadas de los ojos. La matriz modelview que se les aplica no puede ser la misma en vigor cuando se transforman los vértices de polígono. Esta función establece un campo de coordenadas de textura que puede generar líneas dinámicas de contorno en objetos en movimiento.

Si *pname es* GL SPHERE MAP y coord es GL S o GL T, las coordenadas de textura s y t se generan \_ como se muestra a \_  \_ \_ continuación. Vamos a ser el vector de unidad que apunta desde el origen al vértice del polígono (en coordenadas de los ojos). Deje que n sea el normal actual, después de la transformación a las coordenadas de los ojos. Let f = (fx ( ) fy ( ) fz)T be the reflection vector such that

![Ecuación que muestra el vector de reflexión como una función de vector de unidad y normal actual.](images/tex05.png)

Por último, let

![Ecuación que muestra m como función del vector de reflexión.](images/tex07.png)

A continuación, los valores asignados a las coordenadas de textura i y t son

![Ecuación que muestra los valores asignados a las coordenadas de textura i y t.](images/tex06.png)

Puede habilitar o deshabilitar una función de generación de coordenadas de textura mediante [**glEnable**](glenable.md) o [**glDisable**](gldisable.md) con uno de los nombres simbólicos de coordenadas de textura (GL \_ TEXTURE GEN \_ \_ S, GL TEXTURE GEN T, GL TEXTURE GEN R o GL TEXTURE GEN Q) como \_ \_ \_ \_ \_ \_ \_ \_ \_ argumento. Cuando esta función está habilitada, la coordenada de textura especificada se calcula según la función de generación asociada a esa coordenada. Cuando la función está deshabilitada, los vértices posteriores toman la coordenada de textura especificada del conjunto actual de coordenadas de textura. Inicialmente, todas las funciones de generación de texturas se establecen en GL \_ EYE LINEAR y están \_ deshabilitadas. Ambas ecuaciones de plano son (1,0,0,0); ambas ecuaciones de plano t son (0,1,0,0); y todas las ecuaciones de plano r y q son (0,0,0,0).

Las siguientes funciones recuperan información relacionada con glTexGen:

<dl>

[**glGetTexGen**](glgettexgen.md)  
[**glIsEnabled con**](glisenabled.md) el argumento GL \_ TEXTURE GEN \_ \_ S  
[**glIsEnabled con**](glisenabled.md) el argumento GL \_ TEXTURE GEN \_ \_ T  
[**glIsEnabled con**](glisenabled.md) el argumento GL \_ TEXTURE GEN \_ \_ R  
[**glIsEnabled con**](glisenabled.md) el argumento GL \_ TEXTURE GEN \_ \_ Q  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





