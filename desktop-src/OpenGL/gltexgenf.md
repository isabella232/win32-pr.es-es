---
title: función glTexGenf (GL. h)
description: Controla la generación de coordenadas de textura. | función glTexGenf (GL. h)
ms.assetid: 43439d34-46df-49c6-8c19-09db9f005520
keywords:
- glTexGenf (función) OpenGL
topic_type:
- apiref
api_name:
- glTexGenf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98829979037aecf49dfca91491dbc89bc7fa7951
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104558924"
---
# <a name="gltexgenf-function"></a>glTexGenf función)

Controla la generación de coordenadas de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTexGenf(
   GLenum  coord,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*coords* 
</dt> <dd>

Coordenada de textura. Debe ser uno de los siguientes: GL \_ S, GL \_ T, GL \_ R o GL \_ Q.

</dd> <dt>

**PName** 
</dt> <dd>

Nombre simbólico de la función de generación de coordenadas de textura.

</dd> <dt>

*param* 
</dt> <dd>

Parámetro de generación de textura con un solo valor, uno de los \_ objetos GL \_ linear, GL \_ ocular \_ lineal o el mapa de la \_ esfera GL \_ .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | no se aceptó el valor de *coords* o *PName* , o bien *PName* era el \_ \_ modo de generación de texturas GL \_ y *params* no era un valor definido.<br/> |
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *PName* era el \_ \_ modo gen \_ de textura GL, *params* era el mapa de la \_ esfera de contabilidad y la \_ de *coordenadas* era GL \_ R o GL \_ Q.<br/>                                     |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md). <br/>                 |



## <a name="remarks"></a>Observaciones

La función **glTexGen** selecciona una función de generación de coordenadas de textura o proporciona coeficientes para una de las funciones. El parámetro *coords* asigna un nombre a una de las coordenadas de textura (s, t, r, q) y debe ser uno de estos símbolos: GL \_ s, GL \_ t, GL \_ r o GL \_ q. El parámetro *PName* debe ser una de estas tres constantes simbólicas: GL \_ Texture, plano de \_ \_ \_ objeto \_ o \_ plano de ojo \_ de contabilidad. Si *PName* es \_ el modo de generación de texturas GL \_ \_ , *param* especifica un modo, uno de los \_ objetos GL \_ linear, GL \_ Eye \_ linear o GL \_ Sphere \_ map. Si *PName* es \_ \_ plano de objeto GL o \_ plano de ojo de contabilidad \_ , *param* contiene coeficientes para la función de generación de textura correspondiente.

Si la función de generación de textura \_ es \_ lineal del objeto GL, la función

! [Ecuación que muestra la función glTexGen cuando la función de generación de textura es GL_OBJECT_LINEAR.]

se usa, donde g es el valor calculado para la coordenada denominada en coordenadas; P1, P2, P3 y P4 son los cuatro valores que se proporcionan en params; y x?, y?, z? y w? son las coordenadas de objeto del vértice. Puede usar esta función para asignar texturas al terreno mediante el nivel de mar como un plano de referencia (definido por P1, P2, P3 y P4). La \_ función de \_ generación de coordenadas lineales del objeto GL calcula la altitud de un vértice de terreno como su distancia desde el nivel de mar; esa altitud se usa para indexar la imagen de textura y asignar la nieve blanca en picos y hierba verdes en Foothills, por ejemplo.

Si la función de generación de textura es \_ lineal en el ojo de contabilidad \_ , la función

! [Ecuación que muestra la función glTexGen cuando la función de generación de textura es GL_EYE_LINEAR.]

se usa, donde

![Ecuación que muestra las coordenadas del ojo del vértice.](images/tex03.png)

y x?, y?, z? y w? ¿las coordenadas oculares del vértice, P1, P2, P3 y P4 son los valores proporcionados en *param* y M es la matriz MODELVIEW cuando se llama a **glTexGen**. Si M está mal acondicionado o singular, las coordenadas de textura generadas por la función resultante pueden ser inexactas o indefinidas.

Tenga en cuenta que los valores de *param* definen un plano de referencia en coordenadas de ojo. La matriz de MODELVIEW que se aplica a ellos puede no ser la misma en vigor cuando se transforman los vértices del polígono. Esta función establece un campo de coordenadas de textura que puede generar líneas de contorno dinámico en el movimiento de objetos.

Si *PName* es el \_ \_ mapa de esfera  de contabilidad y la \_ coordenadas es GL s o GL \_ T, se generan coordenadas de textura s y t como se indica a continuación. Permita que u sea el vector de unidad que apunta desde el origen al vértice del polígono (en coordenadas de ojo). Deje que n sea la normal actual, después de la transformación a las coordenadas del ojo. Let f = (FX () AF () FZ) T es el vector de reflexión tal que

![Ecuación que muestra el vector de reflexión como una función de vector de unidad y normal actual.](images/tex05.png)

Por último, deje que

![Ecuación que muestra m como función del vector de reflexión.](images/tex07.png)

Después, los valores asignados a las coordenadas de textura i y t son

![Ecuación que muestra los valores asignados a las coordenadas de textura i y t.](images/tex06.png)

Puede habilitar o deshabilitar una función de generación de coordenada de textura mediante [**glEnable**](glenable.md) o [**glDisable**](gldisable.md) con uno de los nombres de coordenadas de textura simbólicos (GL \_ Texture \_ gen \_ S, GL \_ Texture \_ gen \_ T, GL \_ Texture \_ gen \_ R o GL \_ Texture \_ gen \_ Q) como argumento. Cuando esta función está habilitada, la coordenada de textura especificada se calcula según la función de generación asociada a esa coordenada. Cuando esta función está deshabilitada, los vértices siguientes toman la coordenada de textura especificada del conjunto actual de coordenadas de textura. Inicialmente, todas las funciones de generación de texturas se establecen en contabilidad \_ ocular \_ lineal y están deshabilitadas. Ambas ecuaciones de plano s son (1, 0, 0, 0); ambas ecuaciones de plano t son (0, 1, 0, 0); y todas las ecuaciones de r y q plano son (0, 0, 0,0).

Las siguientes funciones recuperan información relacionada con glTexGen:

<dl>

[**glGetTexGen**](glgettexgen.md)  
[**glIsEnabled**](glisenabled.md) con el argumento \_ GL \_ Texture \_ S  
[**glIsEnabled**](glisenabled.md) con el argumento GL \_ Texture \_ gen \_ T  
[**glIsEnabled**](glisenabled.md) con el argumento GL de \_ textura \_ gen \_ R  
[**glIsEnabled**](glisenabled.md) con argument GL \_ Texture \_ gen \_ Q  
</dl>

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

[glTexEnv](gltexenv-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[glTexParameter](gltexparameter-functions.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





