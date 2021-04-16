---
title: función glViewport (GL. h)
description: La función glViewport establece la ventanilla.
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- glViewport (función) OpenGL
topic_type:
- apiref
api_name:
- glViewport
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5e8eedb9c66211deda92ef6a84e8c1dd2073362
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104562016"
---
# <a name="glviewport-function"></a>glViewport función)

La función **glViewport** establece la ventanilla.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glViewport(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* 
</dt> <dd>

Esquina inferior izquierda del rectángulo de la ventanilla, en píxeles. El valor predeterminado es (0,0).

</dd> <dt>

*y* 
</dt> <dd>

Esquina inferior izquierda del rectángulo de la ventanilla, en píxeles. El valor predeterminado es (0,0).

</dd> <dt>

*width* 
</dt> <dd>

Ancho de la ventanilla. Cuando un contexto OpenGL se adjunta primero a una ventana, el *ancho* y el *alto* se establecen en las dimensiones de esa ventana.

</dd> <dt>

*height* 
</dt> <dd>

Alto de la ventanilla. Cuando un contexto OpenGL se adjunta primero a una ventana, el *ancho* y el *alto* se establecen en las dimensiones de esa ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | El *ancho* o el *alto* era negativo.<br/>                                                                                   |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glViewport** especifica la transformación afín de *x* e y desde las *coordenadas del dispositivo* normalizado a las coordenadas de la ventana. Let (*x*<sub>ND</sub> , *y*<sub>ND</sub> ) son coordenadas de dispositivo normalizadas. Las coordenadas de la ventana (*x*<sub>w</sub> , *y*<sub>w</sub> ) se calculan de la siguiente manera:

![Ecuación que muestra el cálculo de las coordenadas de la ventana.](images/view01.png)

El ancho y el alto de la ventanilla se fijan de forma silenciosa en un intervalo que depende de la implementación. Este intervalo se consulta mediante una llamada a **glGet** con el argumento de la \_ ventanilla Max Max \_ \_ .

Las siguientes funciones recuperan información relacionada con **glViewport**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ ventanilla de GL

**glGet** con el argumento \_ la \_ ventanilla Max Max \_ DiMS

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

[**glDepthRange**](gldepthrange.md)
</dt> </dl>

 

 





