---
title: Función glFogf (Gl.h)
description: La función glFogf y especifica los parámetros de parámetro de parámetro de parámetro.
ms.assetid: 69961d8f-385c-4353-aef3-38fb654c44f8
keywords:
- Función glFogf OpenGL
topic_type:
- apiref
api_name:
- glFogf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 497a053584df3e6993a8c7cf3965345923e7df0745765b320972f7003bb15bde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580245"
---
# <a name="glfogf-function"></a>función glFogf

La **función glFogf** y especifica los parámetros de parámetro de parámetro de parámetro .

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glFogf(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pname* 
</dt> <dd>

Especifica un parámetro de valor único.

Acepta uno de los siguientes valores.



| Value                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <dt>**MODO \_ GL \_**</dt> </dl>          | El *parámetro params* es un valor de punto flotante único que especifica la ecuación que se va a usar para calcular el factor blend de fusión de mezcla, *f*. Se aceptan tres constantes simbólicas: GL \_ LINEAR, GL \_ EXP y GL \_ EXP2. Las ecuaciones correspondientes a estas constantes simbólicas se definen en la sección Comentarios siguiente. El modo de mode predeterminado es GL \_ EXP.<br/> |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <dt>**DENSIDAD \_ DE GL GL \_ GL**</dt> </dl> | El *parámetro params* es un valor de punto flotante único que especifica la densidad *,* la densidad de densidad usada en ambas ecuaciones exponenciales. Solo se aceptan las densidades no preventivas. La densidad de densidad predeterminada es 1.0.<br/>                                                                                                                                    |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <dt>**GL \_ FOG \_ START**</dt> </dl>       | El *parámetro params* es un valor de punto flotante único que especifica *start*, la distancia cercana usada en la ecuación de matriz lineal. La distancia cercana predeterminada es 0,0.<br/>                                                                                                                                                                                  |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <dt>**GL \_ FOG \_ END**</dt> </dl>             | El *parámetro params* es un valor de punto flotante único que especifica *end*, la distancia lejana usada en la ecuación lineal de la matriz. La distancia lejana predeterminada es 1,0.<br/>                                                                                                                                                                                      |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <dt>**GL \_ FOG \_ INDEX**</dt> </dl>       | El *parámetro params* es un valor de punto flotante único que especifica *i*<sub>f</sub> , el índice de color de punta. El índice de índice de índice predeterminado es 0,0.<br/>                                                                                                                                                                                                           |



 

</dd> <dt>

*param* 
</dt> <dd>

Especifica el valor en el que se establecerá *pname.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *pname* no era un valor aceptado.<br/>                                                                                         |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

Habilite y deshabilite el valor de disable con [**glEnable**](glenable.md) y [**glDisable**](gldisable.md)mediante el argumento \_ GL. Mientras está habilitada, la densidad afecta a la geometría rasterizada, los mapas de bits y los bloques de píxeles, pero no a las operaciones de borrar búfer.

La **función glFogf** asigna el valor o los valores de *params* al parámetro parameter parameter especificado por *pname*.

La fusión combina un color de fusión con el color de posttexturación de cada fragmento de píxel rasterizado mediante un factor de mezcla *f*. El *factor f* se calcula de una de estas tres maneras, dependiendo del modo de "mode" de "mode". Deje *que z* sea la distancia en coordenadas de los ojos desde el origen hasta el fragmento que se va a fragmentar. La ecuación de gl \_ linearidad es:

![Ecuación que muestra el valor de GL_LINEAR de cálculo.](images/fog01.png)

La ecuación para gl \_ expand es:

![Ecuación que muestra el valor del factor de mezcla en GL_EXP modo de fusión.](images/fog02.png)

La ecuación de gl \_ exp2 es:

![Ecuación que muestra el valor del factor de mezcla en GL_EXP2 modo de fusión.](images/fog03.png)

Independientemente del modo de fusión, *f* se fija en el intervalo \[ 0,1 después de \] calcularse. A continuación, si OpenGL está en modo de color RGBA, el color *C*<sub>r</sub> del fragmento se reemplaza por

![Ecuación que muestra el color del fragmento fragmentado como una función del factor de mezcla y el color de la paleta.](images/fog04.png)

En el modo de índice de color, el índice de color del fragmento *i*<sub>r</sub> se reemplaza por

![Ecuación que muestra el índice de color del fragmento fragmentado como una función del factor de mezcla y el color indexado.](images/fog05.png)

Las siguientes funciones recuperan información relacionada con **las funciones glFog:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ GL GL COLOR \_

**glGet con** el argumento GL \_ GL INDEX \_

**glGet con** el argumento \_ GL GL DENSITY \_

**glGet con** el argumento \_ GL GL GL \_ START

**glGet con** el argumento \_ GL GL END \_

**glGet** con el argumento \_ GL GL MODE \_

[**glIsEnabled con**](glisenabled.md) el argumento \_ GL

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

 

 





