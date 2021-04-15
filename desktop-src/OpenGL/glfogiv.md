---
title: Función glFogiv (Gl.h)
description: La función glFogiv especifica los parámetros de niebla. | función glFogiv (GL. h)
ms.assetid: 8d920ddc-6155-412d-af10-585932cb149f
keywords:
- glFogiv (función) OpenGL
topic_type:
- apiref
api_name:
- glFogiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fa4fefece05529cf5ff3906f19c5ad6e444249
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547614"
---
# <a name="glfogiv-function"></a>glFogiv función)

La función **glFogfv** especifica los parámetros de niebla.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glFogiv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PName* 
</dt> <dd>

Especifica un parámetro de niebla.

Acepta uno de los valores siguientes.



| Value                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <dt>**\_modo de niebla de contabilidad \_**</dt> </dl>          | El parámetro *params* es un valor entero único que especifica la ecuación que se va a utilizar para calcular el factor de mezcla de niebla, *f*. Se aceptan tres constantes simbólicas: GL \_ lineal, GL \_ EXP y GL \_ EXP2. Las ecuaciones correspondientes a estas constantes simbólicas se definen en la sección Comentarios siguiente. El modo de niebla predeterminado es GL \_ exp.<br/>                                                                                      |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <dt>**\_densidad de niebla de GL \_**</dt> </dl> | El parámetro *params* es un valor entero único que especifica la *densidad*, la densidad de niebla utilizada en ambas ecuaciones de niebla exponencial. Solo se aceptan las densidades no negativas. La densidad de niebla predeterminada es 1,0.<br/>                                                                                                                                                                                                                         |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <dt>**\_Inicio de niebla de GL \_**</dt> </dl>       | El parámetro *params* es un valor entero único que especifica *Start*, la distancia cercana utilizada en la ecuación de niebla lineal. El valor predeterminado cerca de la distancia es 0,0.<br/>                                                                                                                                                                                                                                                                       |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <dt>**finalización de la niebla de GL \_ \_**</dt> </dl>             | El parámetro *params* es un valor entero único que especifica *End*, la distancia lejana utilizada en la ecuación de niebla lineal. La distancia predeterminada es 1,0.<br/>                                                                                                                                                                                                                                                                           |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <dt>**\_Índice de niebla de GL \_**</dt> </dl>       | El parámetro *params* es un valor entero único que especifica *i*<sub>f</sub> , el índice de color de niebla. El índice de niebla predeterminado es 0,0.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <dt>**\_color de niebla de GL \_**</dt> </dl>       | El parámetro *params* contiene cuatro valores enteros o de punto flotante que especifican *C*<sub>f</sub> , el color de niebla. Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0. Los valores de punto flotante se asignan directamente. Después de la conversión, todos los componentes de color se fijan en el intervalo \[ 0, 1 \] . El color de niebla predeterminado es (0, 0, 0,0).<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Especifica el valor o los valores que se van a asignar a *PName*. El \_ \_ color de niebla de contabilidad requiere una matriz de cuatro valores. Todos los demás parámetros aceptan una matriz que contiene un solo valor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *PName* no era un valor aceptado.<br/>                                                                                         |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Para habilitar y deshabilitar la niebla con [**glEnable**](glenable.md) y [**glDisable**](gldisable.md), use el argumento niebla de contabilidad \_ . Mientras está habilitada, la niebla afecta a la geometría rasterizada, mapas de bits y bloques de píxeles, pero no operaciones de borrado de búfer.

La función **glFogiv** asigna el valor o los *valores de los* parámetros al parámetro de niebla especificado por *PName*.

La niebla combina un color de niebla con el color de posttexturización de cada fragmento de píxel rasterizado mediante un factor de mezcla *f*. Factor *f* se calcula de una de estas tres maneras, según el modo de niebla. Deje que *z* sea la distancia en coordenadas de ojo desde el origen al fragmento que se va a la luneta térmica. La ecuación para la \_ niebla lineal de GL es:

![Ecuación que muestra el valor del factor de fusión en GL_LINEAR modo de niebla como una función de distancia.](images/fog01.png)

La ecuación para la niebla de contabilidad de contabilidad \_ es:

![Ecuación que muestra el valor del factor de mezcla en el modo de niebla de GL_EXP.](images/fog02.png)

La ecuación para la \_ niebla de EXP2 de GL es:

![Ecuación que muestra el valor del factor de mezcla en el modo de niebla de GL_EXP2.](images/fog03.png)

Independientemente del modo de niebla, *f* se fija en el intervalo de \[ 0 a 1 \] después de su cálculo. A continuación, si OpenGL está en modo de color RGBA, el color *C*<sub>r</sub> del fragmento se sustituye por

![Ecuación que muestra el color del fragmento de la luneta térmica como función del factor de fusión y del color de la niebla.](images/fog04.png)

En el modo de índice de color, el índice de color del fragmento *i*<sub>r</sub> se sustituye por

![Ecuación que muestra el índice de color del fragmento de la luneta térmica como una función de factor de fusión y color indexado.](images/fog05.png)

Las siguientes funciones recuperan información relacionada con las funciones de **glFog** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento del \_ color de niebla de contabilidad \_

**glGet** con el argumento \_ Índice de niebla de GL \_

**glGet** con el argumento \_ densidad de niebla de contabilidad \_

**glGet** con el argumento \_ Inicio de niebla de contabilidad \_

**glGet** con el argumento \_ final de niebla de contabilidad \_

**glGet** con el \_ modo de niebla de contabilidad de argumentos \_

[**glIsEnabled**](glisenabled.md) con niebla de contabilidad de argumentos \_

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





