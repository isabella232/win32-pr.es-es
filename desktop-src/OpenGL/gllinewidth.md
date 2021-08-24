---
title: Función glLineWidth (Gl.h)
description: La función glLineWidth especifica el ancho de las líneas rasterizadas.
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- Función glLineWidth OpenGL
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
ms.openlocfilehash: cad5af24170f47125136e87e055413a576821bf75d3f5f87532d026d0bb2fd0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492975"
---
# <a name="gllinewidth-function"></a>función glLineWidth

La **función glLineWidth** especifica el ancho de las líneas rasterizadas.

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
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *width* era menor o igual que cero.<br/>                                                                                    |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glLineWidth** especifica el ancho rasterizado de las líneas con alias y con suavizado de contorno. El uso de un ancho de línea distinto de 1.0 tiene efectos diferentes, dependiendo de si está habilitado el suavizado de contorno de línea. El suavizado de contorno de línea se controla mediante una llamada [**a glEnable**](glenable.md) y **glDisable** con el argumento GL \_ LINE \_ SMOOTH.

Si el suavizado de contorno de línea está deshabilitado, el ancho real se determina redondeando el ancho proporcionado al entero más cercano. (Si el redondeo da como resultado el valor 0,0, es como si el ancho de línea fuera 1,0) Si \| es ? x \|  =  \| ? y \| , *los píxeles* i se rellenan en cada columna que está rasterizada, donde *i* es el valor redondeado de *width*. De lo contrario, *los* píxeles i se rellenan en cada fila que se rasteriza.

Si el suavizado de contorno está habilitado, la rasterización de línea genera un fragmento para cada cuadrado de píxeles que forma una intersección con la región situada dentro del rectángulo con un ancho igual al ancho de línea actual, una longitud igual a la longitud real de la línea y centrada en el segmento de línea matemático. El valor de cobertura de cada fragmento es el área de coordenadas de ventana de la intersección de la región rectangular con el cuadrado de píxeles correspondiente. Este valor se guarda y se usa en el paso de rasterización final.

No se admiten todos los anchos cuando está habilitado el suavizado de contorno de línea. Si se solicita un ancho no admitido, se usa el ancho admitido más cercano. Solo se garantiza que se admite width 1.0; otros dependen de la implementación. El intervalo de anchos admitidos y la diferencia de tamaño entre los anchos admitidos dentro del intervalo se pueden consultar llamando **a glGet** con argumentos GL LINE WIDTH RANGE y \_ GL LINE WIDTH \_ \_ \_ \_ \_ GRANULARITY.

El ancho de línea especificado por **glLineWidth** siempre se devuelve cuando se consulta GL \_ LINE \_ WIDTH. La fijación y el redondeo de las líneas con alias y suavizado de contorno no tienen ningún efecto en el valor especificado.

El ancho de línea no suavizado se puede fijar a un máximo dependiente de la implementación. Aunque no se puede consultar este máximo, no debe ser menor que el valor máximo de las líneas suavizadas con suavizado de contorno, redondeadas al valor entero más cercano.

Las siguientes funciones recuperan información relacionada **con glLineWidth**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ LINE \_ WIDTH

**glGet con** el argumento GL \_ LINE WIDTH \_ \_ RANGE

**glGet con** el argumento GL \_ LINE WIDTH \_ \_ GRANULARITY

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ LINE \_ SMOOTH

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





