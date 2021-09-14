---
title: Función glLighti (Gl.h)
description: La función glLighti devuelve valores de parámetro de origen de luz.
ms.assetid: 4fa5e604-d45d-412e-a08c-c38e0836596f
keywords:
- Función glLighti OpenGL
topic_type:
- apiref
api_name:
- glLighti
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52225c4db8eaa31c17d12a25590b918cf94b4c3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074029"
---
# <a name="gllighti-function"></a>Función glLighti

La **función glLighti** devuelve valores de parámetro de origen de luz.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glLighti(
   GLenum light,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*light* 
</dt> <dd>

Identificador de una luz. El número de posibles luces depende de la implementación, pero se admiten al menos ocho luces. Se identifican mediante nombres simbólicos con la forma GL \_ LIGHT *i,* donde *i* es un valor: 0 a GL \_ MAX LIGHTS - \_ 1.

</dd> <dt>

*pname* 
</dt> <dd>

Un parámetro de origen de luz de un solo valor para *la luz*. Se aceptan los siguientes nombres simbólicos.



| Value                                                                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**EXPONENTE \_ DE SPOT \_ DE GL**</dt> </dl>                                                                                                                                                                             | El *parámetro param* es un valor entero único que especifica la distribución de intensidad de la luz. Los valores enteros y de punto flotante se asignan directamente. Solo se aceptan los valores \[ del intervalo 0, 128. \] <br/> La intensidad de la luz efectiva se atenua mediante el coseno del ángulo entre la dirección de la luz y la dirección desde la luz hasta el vértice que se enciende, elevado a la potencia del exponente de spot. Por lo tanto, los exponentes de punto más altos tienen como resultado una fuente de luz más centrada, independientemente del ángulo de límite de la zona. El exponente de spot predeterminado es 0, lo que da lugar a una distribución uniforme de la luz.<br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**GL \_ SPOT \_ CUTOFF**</dt> </dl>                                                                                                                                                                                   | El *parámetro param* es un valor entero único que especifica el ángulo de propagación máximo de una fuente de luz. Los valores enteros y de punto flotante se asignan directamente. Solo se aceptan los \[ valores del intervalo 0, 90 y \] el valor especial 180. <br/> Si el ángulo entre la dirección de la luz y la dirección desde la luz hasta el vértice que se va a encender es mayor que el ángulo de límite de acceso al punto, la luz se enmascara completamente. De lo contrario, su intensidad se controla mediante el exponente de spot y los factores de atenuación. El límite de spot predeterminado es 180, lo que da lugar a una distribución uniforme de la luz.<br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <dt>**ATENUACIÓN \_ \_ CONSTANTE DE GL, \_ ATENUACIÓN LINEAL \_ GL, \_ ATENUACIÓN \_ CUADRÁTICA DE GL**</dt> </dl> | El *parámetro param* es un valor entero único que especifica uno de los tres factores de atenuación de luz. Los valores enteros y de punto flotante se asignan directamente. Solo se aceptan valores no negativos. <br/> Si la luz es posicional, en lugar de direccional, su intensidad se atenua por el recíproco de la suma de: el factor constante, el factor lineal multiplicado por la distancia entre la luz y el vértice que se enciende, y el factor cuadrático multiplicado por el cuadrado de la misma distancia. Los factores de atenuación predeterminados son (1,0,0), lo que no produce atenuación.<br/>                   |



 

</dd> <dt>

*param* 
</dt> <dd>

Especifica el valor en el que  se establecerá el *parámetro pname* de la luz de origen de luz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *light* o *pname* no era un valor aceptado.<br/>                                                                                                                                                                  |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | Se especificó un valor de exponente de spot fuera del intervalo 0, 128, o bien se especificó un límite de spot fuera del intervalo 0, 90 (excepto el valor especial \[ \] \[ 180) o se especificó un factor de atenuación \] negativo.<br/> |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/>                                                                                     |



## <a name="remarks"></a>Observaciones

La **función glLighti** establece el valor o los valores de los parámetros de origen de luz individuales. El *parámetro light* denomina la luz y es un nombre simbólico de la forma GL LIGHT i , donde \_ 0 = i *<* GL MAX \_ \_ LIGHTS.

El *parámetro pname* especifica uno de los parámetros de origen de luz, de nuevo por nombre simbólico. El *parámetro param* es un valor único o un puntero a una matriz que contiene los nuevos valores.

El cálculo de iluminación está habilitado y deshabilitado mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento GL \_ LIGHTING. Cuando la iluminación está habilitada, las fuentes de luz habilitadas contribuyen al cálculo de la iluminación. La fuente *de luz i* está habilitada y deshabilitada mediante **glEnable** y **glDisable** con el argumento GL \_ LIGHT *i*.

Siempre es el caso de GL \_ LIGHT *i* = GL \_ LIGHT0 + *i*.

Las funciones siguientes recuperan información relacionada con la **función glLighti:**

[**glGetLight**](glgetlight.md)

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ LIGHTING

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





