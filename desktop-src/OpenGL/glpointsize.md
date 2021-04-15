---
title: función glPointSize (GL. h)
description: La función glPointSize especifica el diámetro de los puntos rasterizados.
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- glPointSize (función) OpenGL
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666024"
---
# <a name="glpointsize-function"></a>glPointSize función)

La función **glPointSize** especifica el diámetro de los puntos rasterizados.

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

Diámetro de los puntos rasterizados. El valor predeterminado es 1.0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *el tamaño* era menor o igual que cero.<br/>                                                                                     |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glPointSize** especifica el diámetro rasterizado de los puntos con alias y antialias. El uso de un tamaño de punto distinto de 1,0 tiene efectos diferentes, en función de si está habilitado el suavizado de contorno. El suavizado de contorno de punto se controla mediante una llamada a [**glEnable**](glenable.md) y **glDisable** con un argumento de punto de contabilidad \_ \_ suave.

Si el suavizado de contorno de punto está deshabilitado, el tamaño real se determina redondeando el tamaño proporcionado al entero más próximo. (Si el redondeo da como resultado el valor 0, es como si el tamaño del punto fuera 1). Si el tamaño redondeado es impar, el punto central (*x*,*y*) del fragmento de píxel que representa el punto se calcula como

(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> + 5)

donde *w* los subíndices indican las coordenadas de la ventana. Todos los píxeles que se encuentran dentro de la cuadrícula cuadrada del tamaño redondeado centrado en (*x*,*y*) componen el fragmento. Si el tamaño es par, el punto central es

(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> + 5)

y los centros del fragmento rasterizado son las coordenadas de la ventana de medio entero dentro del cuadrado del tamaño redondeado centrado en (*x*,*y*). A todos los fragmentos de píxeles producidos en la rasterización de un punto nonantialiased se les asignan los mismos datos asociados. del vértice correspondiente al punto.

Si el suavizado de contorno está habilitado, la rasterización de puntos produce un fragmento para cada cuadrado de píxeles que forma una intersección con la región en el círculo que tiene un diámetro igual al tamaño de punto actual y se centra en los puntos (*x*<sub>w</sub> ,*y*<sub>w</sub> ). El valor de cobertura de cada fragmento es el área de coordenadas de la ventana de la intersección de la región circular con el cuadrado de píxeles correspondiente. Este valor se guarda y se usa en el paso de rasterización final. Los datos asociados a cada fragmento son los datos asociados con el punto que se va a Rasterizar.

No se admiten todos los tamaños cuando está habilitado el suavizado de contorno. Si se solicita un tamaño no compatible, se usa el tamaño admitido más cercano. Solo se garantiza que el tamaño 1,0 es compatible; otros dependen de la implementación. El intervalo de tamaños admitidos y la diferencia de tamaño entre los tamaños admitidos en el intervalo se pueden consultar mediante una llamada a [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con los argumentos de \_ intervalo de \_ tamaño de punto de contabilidad \_ y granularidad de tamaño de punto de contabilidad \_ \_ \_ .

Siempre se devuelve el tamaño de punto especificado por **glPointSize** cuando \_ se consulta el tamaño de los puntos de contabilidad \_ . La compresión y el redondeo de los puntos con alias y sin alias no tienen ningún efecto en el valor especificado.

El tamaño de los puntos sin alias se puede fijar en un máximo dependiente de la implementación. Aunque no se puede consultar este máximo, no debe ser menor que el valor máximo de los puntos alisados, redondeado al valor entero más cercano.

Las siguientes funciones recuperan información relacionada con **glPointSize**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento de tamaño de los puntos de contabilidad \_ \_

**glGet** con \_ \_ el intervalo de tamaño de punto de contabilidad de argumento \_

**glGet** con granularidad de \_ tamaño de punto de contabilidad de argumento \_ \_

[**glIsEnabled**](glisenabled.md) con un argumento de punto de contabilidad \_ \_ suave

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





