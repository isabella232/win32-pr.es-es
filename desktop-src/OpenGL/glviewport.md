---
title: Función glViewport (Gl.h)
description: La función glViewport establece la ventanilla.
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- Función glViewport OpenGL
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
ms.openlocfilehash: 70fc727265ce4af1db2be808ae7eee3f59246874659a815c66292bcab3d7ecfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035415"
---
# <a name="glviewport-function"></a>Función glViewport

La **función glViewport** establece la ventanilla.

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

Ancho de la ventanilla. Cuando un contexto OpenGL se adjunta por  primera vez a una ventana, *el* ancho y el alto se establecen en las dimensiones de esa ventana.

</dd> <dt>

*height* 
</dt> <dd>

Alto de la ventanilla. Cuando un contexto OpenGL se adjunta por  primera vez a una ventana, *el* ancho y el alto se establecen en las dimensiones de esa ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | El *ancho o* alto *era* negativo.<br/>                                                                                   |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glViewport** especifica la transformación afín de *x* e *y* de coordenadas de dispositivo normalizadas a coordenadas de ventana. Permita que (*x*<sub>nd</sub> , *y*<sub>nd</sub> ) sean coordenadas de dispositivo normalizadas. A continuación, las coordenadas de ventana *(x*<sub>w,</sub> *y*<sub>w</sub> ) se calculan de la siguiente manera:

![Ecuación que muestra el cálculo de las coordenadas de la ventana.](images/view01.png)

El ancho y el alto de la ventanilla se fijan silenciosamente a un intervalo que depende de la implementación. Este intervalo se consulta mediante una llamada **a glGet** con el argumento GL \_ MAX VIEWPORT \_ \_ DIMS.

Las funciones siguientes recuperan información relacionada con **glViewport**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ VIEWPORT

**glGet con** el argumento GL \_ MAX VIEWPORT \_ \_ DIMS

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**glDepthRange**](gldepthrange.md)
</dt> </dl>

 

 





