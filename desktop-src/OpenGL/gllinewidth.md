---
title: función glLineWidth (GL. h)
description: La función glLineWidth especifica el ancho de las líneas rasterizadas.
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- glLineWidth (función) OpenGL
topic_type:
- apiref
api_name:
- glLineWidth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa4cecafc9e5d8e0f55c6e9d0dbfe49924d54f14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666083"
---
# <a name="gllinewidth-function"></a>glLineWidth función)

La función **glLineWidth** especifica el ancho de las líneas rasterizadas.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glLineWidth(
   GLfloat width
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*width* 
</dt> <dd>

Ancho de las líneas rasterizadas. El valor predeterminado es 1.0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *ancho* era menor o igual que cero.<br/>                                                                                    |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glLineWidth** especifica el ancho rasterizado de las líneas con alias y antialias. El uso de un ancho de línea distinto de 1,0 tiene efectos diferentes, en función de si está habilitado el suavizado de línea. El suavizado de línea se controla mediante una llamada a [**glEnable**](glenable.md) y **glDisable** con el argumento de línea de contabilidad \_ \_ Smooth.

Si el suavizado de línea está deshabilitado, el ancho real se determina redondeando el ancho proporcionado al entero más próximo. (Si el redondeo da como resultado el valor 0,0, es como si el ancho de línea fuera 1,0) \| ¿Si? x \|  =  \| ? y \| , *i* píxeles se rellenan en cada columna que está rasterizada, donde *i* es el valor redondeado de *ancho*. De lo contrario, *i* píxeles se rellenan en cada fila que se rasteriza.

Si el suavizado de contorno está habilitado, la rasterización de línea produce un fragmento para cada cuadrado de píxeles que forma una intersección con la región que se encuentra en el rectángulo que tiene un ancho igual al ancho de línea actual, la longitud es igual a la longitud real de la línea y se centra en el segmento de línea matemática. El valor de cobertura de cada fragmento es el área de coordenadas de la ventana de la intersección de la región rectangular con el cuadrado de píxeles correspondiente. Este valor se guarda y se usa en el paso de rasterización final.

No se admiten todos los anchos cuando está habilitado el suavizado de línea. Si se solicita un ancho no compatible, se utiliza el ancho compatible más cercano. Solo se garantiza la compatibilidad con el ancho 1,0; otros dependen de la implementación. El intervalo de anchos admitidos y la diferencia de tamaño entre los anchos admitidos en el intervalo se pueden consultar llamando a **glGet** con argumentos \_ rango de ancho de línea de contabilidad \_ \_ y granularidad de ancho de línea de contabilidad \_ \_ \_ .

El ancho de línea especificado por **glLineWidth** siempre se devuelve cuando \_ \_ se consulta el ancho de línea de contabilidad. La compresión y el redondeo de las líneas con alias y antialias no tienen ningún efecto en el valor especificado.

El ancho de línea sin suavizado se puede fijar en un máximo dependiente de la implementación. Aunque no se puede consultar este máximo, no debe ser menor que el valor máximo de las líneas alisadas, redondeado al valor entero más cercano.

Las siguientes funciones recuperan información relacionada con **glLineWidth**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ ancho de línea de contabilidad \_

**glGet** con argumento de \_ ancho de línea de libro de contabilidad \_ \_

**glGet** con el argumento \_ \_ granularidad del ancho de línea de contabilidad \_

[**glIsEnabled**](glisenabled.md) con el argumento de línea de contabilidad \_ \_ Smooth

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

 

 





