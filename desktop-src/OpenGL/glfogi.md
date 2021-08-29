---
title: Función glFogi (Gl.h)
description: La función glFogi especifica los parámetros de los parámetros de parámetro.
ms.assetid: c2ffb41d-3d97-4b72-b16d-cfbffa1179d1
keywords:
- Función glFogi OpenGL
topic_type:
- apiref
api_name:
- glFogi
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c60dc078f7755d00a330cea114663054329da445d537448ece8cc9d4f4fe9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625345"
---
# <a name="glfogi-function"></a>Función glFogi

La **función glFogi** especifica los parámetros de los parámetros de parámetro.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glFogi(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pname* 
</dt> <dd>

Especifica un parámetro de punto de referencia con un solo valor.

Acepta uno de los siguientes valores.



| Value                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <dt>**MODO \_ GL GL \_**</dt> </dl>          | El *parámetro params* es un valor entero único que especifica la ecuación que se va a usar para calcular el factor blend de fusión, *f*. Se aceptan tres constantes simbólicas: GL \_ LINEAR, GL \_ EXP y GL \_ EXP2. Las ecuaciones correspondientes a estas constantes simbólicas se definen en la sección Comentarios siguiente. El modo de fusión predeterminado es GL \_ EXP.<br/> |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <dt>**DENSIDAD \_ GL \_ DE GL**</dt> </dl> | El *parámetro params* es un valor entero único que especifica *la* densidad , la densidad de densidad usada en ambas ecuaciones exponenciales. Solo se aceptan las densidades no no preventivas. La densidad de densidad predeterminada es 1,0.<br/>                                                                                                                                    |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <dt>**GL \_ FOG \_ START**</dt> </dl>       | El *parámetro params* es un valor entero único que especifica *start*, la distancia cercana que se usa en la ecuación lineal. La distancia cercana predeterminada es 0,0.<br/>                                                                                                                                                                                  |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <dt>**GL \_ END DE GL \_**</dt> </dl>             | El *parámetro params* es un valor entero único que especifica *end*, la distancia lejana usada en la ecuación lineal de matriz. La distancia lejana predeterminada es 1,0.<br/>                                                                                                                                                                                      |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <dt>**GL \_ FOG \_ INDEX**</dt> </dl>       | El *parámetro params* es un valor entero único que especifica *i*<sub>f</sub> , el índice de color de color. El índice de indexación predeterminado es 0,0.<br/>                                                                                                                                                                                                           |



 

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
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *pname* no era un valor aceptado.<br/>                                                                                         |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

Habilite y deshabilite el acceso con [**glEnable**](glenable.md) y [**glDisable**](gldisable.md)mediante el argumento \_ GL. Mientras está habilitada, el bloqueo afecta a la geometría rasterizada, los mapas de bits y los bloques de píxeles, pero no a las operaciones sin búfer.

La **función glFogi** asigna el valor o los valores de *params* al parámetro parameter especificado por *pname*.

La fusión combina un color de ánxele con el color de texto posterior de cada fragmento de píxel rasterizado mediante un factor de mezcla *f*. El *factor f* se calcula de una de estas tres maneras, dependiendo del modo de fusión. Deje *que z* sea la distancia en coordenadas de los ojos desde el origen hasta el fragmento que se va a fragmentar. La ecuación de gl \_ linearidad es:

![Ecuación que muestra el valor de GL_LINEAR.](images/fog01.png)

La ecuación para gl \_ exp exp es:

![Ecuación que muestra el valor del factor de combinación en GL_EXP modo de fusión.](images/fog02.png)

La ecuación de gl \_ exp2 es:

![Ecuación que muestra el valor del factor de combinación en GL_EXP2 modo de fusión.](images/fog03.png)

Independientemente del modo de bloqueo, *f* se fija al intervalo \[ 0,1 \] después de calcularse. A continuación, si OpenGL está en modo de color RGBA, el color del fragmento *C*<sub>r</sub> se reemplaza por

![Ecuación que muestra el color del fragmento fragmentado como una función del factor de mezcla y el color de color de paleta.](images/fog04.png)

En el modo de índice de colores, el índice de color del fragmento *i*<sub>r</sub> se reemplaza por

![Ecuación que muestra el índice de color del fragmento fragmentado como una función del factor de combinación y el color indexado.](images/fog05.png)

Las funciones siguientes recuperan información relacionada con las **funciones glFog:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ GL COLOR \_

**glGet con** el argumento GL \_ GL INDEX \_

**glGet con** el argumento GL \_ GL GL \_ DENSITY

**glGet con** el argumento GL \_ GL GL \_ START

**glGet con** el argumento GL \_ GL END \_

**glGet con** el argumento GL \_ MODE \_

[**glIsEnabled con**](glisenabled.md) el argumento \_ GL GL

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

 

 





