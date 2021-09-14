---
title: Función glPointSize (Gl.h)
description: La función glPointSize especifica el diámetro de los puntos rasterizados.
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- Función glPointSize OpenGL
topic_type:
- apiref
api_name:
- glPointSize
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6b9525e302cad1eb940184eb5eb83e11744bba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171409"
---
# <a name="glpointsize-function"></a>función glPointSize

La **función glPointSize** especifica el diámetro de los puntos rasterizados.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPointSize(
   GLfloat size
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*size* 
</dt> <dd>

El diámetro de los puntos rasterizados. El valor predeterminado es 1.0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *size* era menor o igual que cero.<br/>                                                                                     |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glPointSize** especifica el contorno rasterizado de los puntos con alias y suavizado de contorno. El uso de un tamaño de punto distinto de 1.0 tiene efectos diferentes, dependiendo de si está habilitado el suavizado de contorno de punto. El suavizado de contorno de punto se controla mediante una llamada [**a glEnable**](glenable.md) y **glDisable** con el argumento GL \_ POINT \_ SMOOTH.

Si el suavizado de contorno de punto está deshabilitado, el tamaño real se determina redondeando el tamaño proporcionado al entero más cercano. (Si el redondeo da como resultado el valor 0, es como si el tamaño del punto fuera 1). Si el tamaño redondeado es impar, el punto central (*x*,*y*) del fragmento de píxeles que representa el punto se calcula como

(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)

donde los subíndices *w* indican coordenadas de ventana. Todos los píxeles que se encuentran dentro de la cuadrícula cuadrada del tamaño redondeado centrado en (*x*,*y*) son el fragmento. Si el tamaño es par, el punto central es

(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)

y los centros del fragmento rasterizado son las coordenadas de ventana de medio entero dentro del cuadrado del tamaño redondeado centrado en (*x*,*y*). A todos los fragmentos de píxeles generados al rasterizar un punto no con contorno se les asignan los mismos datos asociados; del vértice correspondiente al punto.

Si el suavizado de contorno está habilitado, la rasterización de punto genera un fragmento para cada cuadrado de píxeles que forma una intersección con la región situada dentro del círculo que tiene un ancho igual al tamaño del punto actual y centrado en los puntos *(x*<sub>w</sub> ,*y*<sub>w</sub> ). El valor de cobertura de cada fragmento es el área de coordenadas de ventana de la intersección de la región circular con el cuadrado de píxeles correspondiente. Este valor se guarda y se usa en el paso de rasterización final. Los datos asociados a cada fragmento son los datos asociados al punto que se va a rasterizar.

No todos los tamaños se admiten cuando el suavizado de contorno de punto está habilitado. Si se solicita un tamaño no compatible, se usa el tamaño admitido más cercano. Solo se garantiza que se admite el tamaño 1.0; otros dependen de la implementación. El intervalo de tamaños admitidos y la diferencia de tamaño entre los tamaños admitidos dentro del intervalo se pueden consultar mediante una llamada [**a glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con los argumentos GL POINT SIZE RANGE y \_ GL POINT SIZE \_ \_ \_ \_ \_ GRANULARITY.

El tamaño de punto especificado por **glPointSize** siempre se devuelve cuando se consulta GL \_ POINT \_ SIZE. La fijación y el redondeo de los puntos con alias y suavizado de contorno no tienen ningún efecto en el valor especificado.

El tamaño de punto no suavizado se puede fijar a un máximo dependiente de la implementación. Aunque no se puede consultar este máximo, no debe ser menor que el valor máximo de los puntos suavizados de contorno, redondeado al valor entero más cercano.

Las siguientes funciones recuperan información relacionada con **glPointSize**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ POINT \_ SIZE

**glGet con** el argumento GL \_ POINT SIZE \_ \_ RANGE

**glGet** con el argumento GL \_ POINT \_ SIZE \_ GRANULARITY

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ POINT \_ SMOOTH

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





