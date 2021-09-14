---
title: Función glGetLightiv (Gl.h)
description: Las funciones glGetLightfv y glGetLightiv devuelven valores de parámetro de origen claro. | Función glGetLightiv (Gl.h)
ms.assetid: be4316ca-dc49-4bfa-929a-fa25f5057fde
keywords:
- Función glGetLightiv OpenGL
topic_type:
- apiref
api_name:
- glGetLightiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fdf19bcc27a3ab80e176707ee5b1d481ee6a658
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260255"
---
# <a name="glgetlightiv-function"></a>Función glGetLightiv

Las [**funciones glGetLightfv**](glgetlightfv.md) y **glGetLightiv** devuelven valores de parámetro de origen claro.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetLightiv(
   GLenum light,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*light* 
</dt> <dd>

Una fuente de luz. El número de posibles luces depende de la implementación, pero se admiten al menos ocho luces. Se identifican mediante nombres simbólicos de la forma GL \_ LIGHT *i* donde 0 = *i <* GL \_ MAX \_ LIGHTS.

</dd> <dt>

*pname* 
</dt> <dd>

Parámetro de origen de luz para *light*. Se aceptan los siguientes nombres simbólicos.



| Value                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ AMBIENT**</dt> </dl>                                            | El *parámetro params* devuelve cuatro valores enteros o de punto flotante que representan la intensidad ambiental de la fuente de luz. Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación interna de punto flotante, de modo que 1,0 se asigna al valor entero más positivo que se puede representar y -1,0 se asigna al valor entero que se puede representar más negativo. Si el valor interno está fuera del \[ intervalo -1,1 , el valor devuelto \] entero correspondiente no está definido.<br/>                                                                                                                                                                  |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFUSO**</dt> </dl>                                            | El *parámetro params* devuelve cuatro valores enteros o de punto flotante que representan la intensidad difusa del origen de la luz. Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación interna de punto flotante, de modo que 1,0 se asigna al valor entero más positivo que se puede representar y -1,0 se asigna al valor entero que se puede representar más negativo. Si el valor interno está fuera del \[ intervalo -1,1 , el valor devuelto \] entero correspondiente no está definido.<br/>                                                                                                                                                                  |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ SPECULAR**</dt> </dl>                                         | El *parámetro params* devuelve cuatro valores enteros o de punto flotante que representan la intensidad especular de la fuente de luz. Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación interna de punto flotante, de modo que 1,0 se asigna al valor entero más positivo que se puede representar y -1,0 se asigna al valor entero que se puede representar más negativo. Si el valor interno está fuera del \[ intervalo -1,1 , el valor devuelto \] entero correspondiente no está definido.<br/>                                                                                                                                                                 |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**POSICIÓN \_ DE GL**</dt> </dl>                                         | El *parámetro params* devuelve cuatro valores enteros o de punto flotante que representan la posición del origen de luz. Los valores enteros, cuando se solicitan, se calculan redondeando los valores de punto flotante internos al valor entero más cercano. Los valores devueltos son los que se mantienen en coordenadas oculares. No serán iguales a los valores especificados mediante [**glLight**](gllight-functions.md), a menos que se identificara la matriz modelview en el momento en que se llamó **a glLight.**<br/>                                                                                                                                                             |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**DIRECCIÓN \_ DE SPOT DE \_ GL**</dt> </dl>                      | El *parámetro params* devuelve tres valores enteros o de punto flotante que representan la dirección del origen de luz. Los valores enteros, cuando se solicitan, se calculan redondeando los valores de punto flotante internos al valor entero más cercano. Los valores devueltos son los que se mantienen en coordenadas oculares. No serán iguales a los valores especificados mediante **glLight**, a menos que se identificara la matriz modelview en el momento en que se llamó **a glLight.** Aunque la dirección del punto se normaliza antes de usarse en la ecuación de iluminación, los valores devueltos son las versiones transformadas de los valores especificados antes de la normalización.<br/> |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**EXPONENTE \_ DE SPOT \_ DE GL**</dt> </dl>                         | El *parámetro params* devuelve un único valor entero o de punto flotante que representa el exponente de spot de la luz. Un valor entero, cuando se solicita, se calcula redondeando la representación interna de punto flotante al entero más cercano.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**GL \_ SPOT \_ CUTOFF**</dt> </dl>                               | El *parámetro params* devuelve un único valor entero o de punto flotante que representa el ángulo de límite de acceso al espacio de la luz. Un valor entero, cuando se solicita, se calcula redondeando la representación interna de punto flotante al entero más cercano.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span><dl> <dt>**ATENUACIÓN \_ \_ CONSTANTE DE GL**</dt> </dl>    | El *parámetro params* devuelve un único valor entero o de punto flotante que representa la atenuación constante (no relacionada con la distancia) de la luz. Un valor entero, cuando se solicita, se calcula redondeando la representación interna de punto flotante al entero más cercano.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span><dl> <dt>**ATENUACIÓN \_ LINEAL \_ DE GL**</dt> </dl>          | El *parámetro params* devuelve un único valor entero o de punto flotante que representa la atenuación lineal de la luz. Un valor entero, cuando se solicita, se calcula redondeando la representación interna de punto flotante al entero más cercano.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span><dl> <dt>**ATENUACIÓN \_ CUADRÁTICA DE GL \_**</dt> </dl> | El *parámetro params* devuelve un único valor entero o de punto flotante que representa la atenuación cuadrática de la luz. Un valor entero, cuando se solicita, se calcula redondeando la representación interna de punto flotante al entero más cercano.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*params* 
</dt> <dd>

Devuelve los datos solicitados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La **función glGetLight** devuelve en *parámetros* el valor o los valores de un parámetro de origen de luz. El  parámetro light denomina la luz y es un nombre simbólico de la forma GL \_ LIGHT *i* for 0 = *i* < GL MAX LIGHTS, donde GL MAX LIGHTS es una constante dependiente de la implementación que es mayor o igual que \_ \_ \_ \_ ocho. El *parámetro pname* especifica uno de los diez parámetros de origen claro, de nuevo por nombre simbólico.

Siempre es el caso de GL \_ LIGHT *i* = GL \_ LIGHT0 + *i*.

Si se genera un error, no se realiza ningún cambio en el contenido de *params*.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> </dl>

 

 





