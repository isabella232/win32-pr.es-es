---
title: función glGetTexParameterfv (GL. h)
description: Las funciones glGetTexParameterfv y glGetTexParameteriv devuelven los valores de los parámetros de textura. | función glGetTexParameterfv (GL. h)
ms.assetid: 616292ea-222c-4efe-bb69-3058d9c99910
keywords:
- glGetTexParameterfv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0af6e5fd91d38240dd3463b9440333b5da431d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689824"
---
# <a name="glgettexparameterfv-function"></a>glGetTexParameterfv función)

Las funciones **glGetTexParameterfv** y [**glGetTexParameteriv**](glgettexparameteriv.md) devuelven los valores de los parámetros de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetTexParameterfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Nombre simbólico de la textura de destino. Se aceptan las texturas GL \_ \_ 1D y GL Texture \_ \_ 2D.

</dd> <dt>

*PName* 
</dt> <dd>

Nombre simbólico de un parámetro de textura. Se aceptan los siguientes valores.



| Value                                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**\_filtro de textura de GL \_ \_**</dt> </dl>       | Devuelve el filtro de aumento de la textura de un solo valor, una constante simbólica.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**\_ \_ filtro mínimo de textura de GL \_**</dt> </dl>       | Devuelve el filtro minificación de textura de un solo valor, una constante simbólica.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**\_ajuste de textura de GL \_ \_**</dt> </dl>                   | Devuelve la función de ajuste de un solo valor para las coordenadas de textura *s*, una constante simbólica.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**ajuste de textura de GL \_ \_ \_ T**</dt> </dl>                   | Devuelve la función de ajuste de un solo valor para la coordenada de textura *t*, una constante simbólica.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**\_color de \_ borde de textura GL \_**</dt> </dl> | Devuelve cuatro números enteros o de punto flotante que conforman el color RGBA del borde de la textura. Los valores de punto flotante se devuelven en el intervalo de \[ 0 a 1 \] . Los valores enteros se devuelven como una asignación lineal de la representación de punto flotante interna, de modo que 1,0 se asigna al entero representable más positivo y-1,0 se asigna al entero representable más negativo.<br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**\_prioridad de textura de GL \_**</dt> </dl>              | Devuelve la prioridad de residencia de la textura de destino (o la textura con nombre enlazada a ella). El valor inicial es 1. Vea [**glPrioritizeTextures**](glprioritizetextures.md).<br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <dt>**\_residente de textura GL \_**</dt> </dl>              | Devuelve el estado de residencia de la textura de destino. Si el valor devuelto en params es GL \_ true, la textura es residente en la memoria de textura. Vea [**glAreTexturesResident**](glaretexturesresident.md).<br/>                                                                                                                                                                           |



 

</dd> <dt>

*params* 
</dt> <dd>

Devuelve los parámetros de textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *destino* o *el nombre* no eran un valor aceptado.<br/>                                                                              |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glGetTexParameter** devuelve en *params* el valor o los valores del parámetro Texture especificado como *PName*. El parámetro de *destino* define la textura de destino, ya sea la textura de GL \_ \_ 1D o la \_ textura \_ de GL 2D, para especificar una texturización unidimensional o bidimensional. El parámetro *PName* acepta los mismos símbolos que [**glTexParameter**](gltexparameter-functions.md), con las mismas interpretaciones.

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

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





