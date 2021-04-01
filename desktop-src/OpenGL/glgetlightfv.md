---
title: función glGetLightfv (GL. h)
description: Las funciones glGetLightfv y glGetLightiv devuelven los valores de los parámetros de origen Light. | función glGetLightfv (GL. h)
ms.assetid: 81049726-426e-4f90-bb8e-e5d467870260
keywords:
- glGetLightfv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetLightfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf90cb9567822ef578bdf01805648a2dabd02db
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914402"
---
# <a name="glgetlightfv-function"></a>glGetLightfv función)

Las funciones **glGetLightfv** y [**glGetLightiv**](glgetlightiv.md) devuelven los valores de los parámetros de origen Light.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetLightfv(
   GLenum  light,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*light* 
</dt> <dd>

Fuente de luz. El número de posibles luces depende de la implementación, pero se admiten al menos ocho luces. Se identifican por nombres simbólicos con el formato de GL de la era, \_ donde 0 = *i* < las luces de GL  \_ máx \_ .

</dd> <dt>

*PName* 
</dt> <dd>

Parámetro de origen de luz para *Light*. Se aceptan los siguientes nombres simbólicos.



| Value                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**ambiente de contabilidad general \_**</dt> </dl>                                            | El parámetro *params* devuelve cuatro valores enteros o de punto flotante que representan la intensidad ambiente de la fuente de luz. Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación de punto flotante interna, de modo que 1,0 se asigna al valor entero representable más positivo y-1,0 se asigna al valor entero representable más negativo. Si el valor interno está fuera del intervalo \[ -1, 1 \] , el valor devuelto de tipo entero correspondiente es indefinido.<br/>                                                                                                                                                                  |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**difusión en contab. \_**</dt> </dl>                                            | El parámetro *params* devuelve cuatro valores enteros o de punto flotante que representan la intensidad difusa de la fuente de luz. Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación de punto flotante interna, de modo que 1,0 se asigna al valor entero representable más positivo y-1,0 se asigna al valor entero representable más negativo. Si el valor interno está fuera del intervalo \[ -1, 1 \] , el valor devuelto de tipo entero correspondiente es indefinido.<br/>                                                                                                                                                                  |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_especular GL**</dt> </dl>                                         | El parámetro *params* devuelve cuatro valores enteros o de punto flotante que representan la intensidad especular de la fuente de luz. Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación de punto flotante interna, de modo que 1,0 se asigna al valor entero representable más positivo y-1,0 se asigna al valor entero representable más negativo. Si el valor interno está fuera del intervalo \[ -1, 1 \] , el valor devuelto de tipo entero correspondiente es indefinido.<br/>                                                                                                                                                                 |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**posición de contabilidad \_**</dt> </dl>                                         | El parámetro *params* devuelve cuatro valores enteros o de punto flotante que representan la posición de la fuente de luz. Los valores enteros, cuando se solicitan, se calculan Redondeando los valores de punto flotante internos al valor entero más cercano. Los valores devueltos son los que se mantienen en coordenadas oculares. No serán iguales a los valores especificados mediante [**glLight**](gllight-functions.md), a menos que se haya identificado la matriz MODELVIEW en el momento en que se llamó a **glLight** .<br/>                                                                                                                                                             |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**Dirección de la zona de contabilidad \_ \_**</dt> </dl>                      | El parámetro *params* devuelve tres valores enteros o de punto flotante que representan la dirección de la fuente de luz. Los valores enteros, cuando se solicitan, se calculan Redondeando los valores de punto flotante internos al valor entero más cercano. Los valores devueltos son los que se mantienen en coordenadas oculares. No serán iguales a los valores especificados mediante **glLight**, a menos que se haya identificado la matriz MODELVIEW en el momento en que se llamó a **glLight** . Aunque la dirección puntual se normaliza antes de usarse en la ecuación de iluminación, los valores devueltos son las versiones transformadas de los valores especificados antes de la normalización.<br/> |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**exponente de la zona de contabilidad \_ \_**</dt> </dl>                         | El parámetro *params* devuelve un único valor entero o de punto flotante que representa el exponente de la luz. Un valor entero, cuando se solicita, se calcula redondeando la representación de punto flotante interna al entero más próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**límite de la zona de contabilidad \_ \_**</dt> </dl>                               | El parámetro *params* devuelve un único valor entero o de punto flotante que representa el ángulo del límite de la luz. Un valor entero, cuando se solicita, se calcula redondeando la representación de punto flotante interna al entero más próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span><dl> <dt>**\_atenuación de constantes de GL \_**</dt> </dl>    | El parámetro *params* devuelve un único valor entero o de punto flotante que representa la atenuación constante (no relacionada con la distancia) de la luz. Un valor entero, cuando se solicita, se calcula redondeando la representación de punto flotante interna al entero más próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span><dl> <dt>**\_atenuación lineal de GL \_**</dt> </dl>          | El parámetro *params* devuelve un único valor entero o de punto flotante que representa la atenuación lineal de la luz. Un valor entero, cuando se solicita, se calcula redondeando la representación de punto flotante interna al entero más próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span><dl> <dt>**\_atenuación cuadrática de GL \_**</dt> </dl> | El parámetro *params* devuelve un único valor entero o de punto flotante que representa la atenuación cuadrática de la luz. Un valor entero, cuando se solicita, se calcula redondeando la representación de punto flotante interna al entero más próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*params* 
</dt> <dd>

Devuelve los datos solicitados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **glGetLight** devuelve en *params* el valor o los valores de un parámetro de origen Light. El parámetro de *luz* asigna un nombre a la luz y es un nombre simbólico con el formato de libro de contabilidad de alta \_ *i* para 0 = *i* < las luces de GL \_ máx., donde la luz de \_ Max de GL \_ \_ es una constante dependiente de la implementación que es mayor o igual que ocho. El parámetro *PName* especifica uno de los diez parámetros de origen ligeros, de nuevo por nombre simbólico.

Siempre es el caso de GL \_ Light *i* = GL \_ LIGHT0 + *i*.

Si se genera un error, no se realiza ningún cambio en el contenido de los *parámetros*.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> </dl>

 

 





