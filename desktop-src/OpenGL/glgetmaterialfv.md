---
title: función glGetMaterialfv (GL. h)
description: Las funciones glGetMaterialfv y glGetMaterialiv devuelven parámetros de material. | función glGetMaterialfv (GL. h)
ms.assetid: b61dbe0c-5cc2-4397-9d7c-b99507a9f037
keywords:
- glGetMaterialfv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce33ee1f88d492f67cf3ebb93c575f8f36d1ffa0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362105"
---
# <a name="glgetmaterialfv-function"></a>glGetMaterialfv función)

Las funciones **glGetMaterialfv** y [**glGetMaterialiv**](glgetmaterialiv.md) devuelven parámetros de material.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetMaterialfv(
   GLenum  face,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Portada* 
</dt> <dd>

Especifica cuál de los dos materiales se está consultando. \_Se aceptan el anverso o el libro de contabilidad \_ , que representan el material delantero y el trasero, respectivamente.

</dd> <dt>

*PName* 
</dt> <dd>

Parámetro de material que se va a devolver. Se aceptan los siguientes valores.



| Value                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**ambiente de contabilidad general \_**</dt> </dl>                    | El parámetro *params* devuelve cuatro valores enteros o de punto flotante que representan la reflectancia ambiente del material. Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación de punto flotante interna, de modo que 1,0 se asigna al valor entero representable más positivo y-1,0 se asigna al valor entero representable más negativo. Si el valor interno está fuera del intervalo \[ -1, 1 \] , el valor devuelto de tipo entero correspondiente es indefinido.<br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**difusión en contab. \_**</dt> </dl>                    | El parámetro *params* devuelve cuatro valores enteros o de punto flotante que representan la reflectancia difusa del material. Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación de punto flotante interna, de modo que 1,0 se asigna al valor entero representable más positivo y-1,0 se asigna al valor entero representable más negativo. Si el valor interno está fuera del intervalo \[ -1, 1 \] , el valor devuelto de tipo entero correspondiente es indefinido.<br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_especular GL**</dt> </dl>                 | El parámetro *params* devuelve cuatro valores enteros o de punto flotante que representan la reflectancia especular del material. Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación de punto flotante interna, de modo que 1,0 se asigna al valor entero representable más positivo y-1,0 se asigna al valor entero representable más negativo. Si el valor interno está fuera del intervalo \[ -1, 1 \] , el valor devuelto de tipo entero correspondiente es indefinido.<br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**emisión de contabilidad \_**</dt> </dl>                 | El parámetro *params* devuelve cuatro valores enteros o de punto flotante que representan la intensidad de luz emitida del material. Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación de punto flotante interna, de modo que 1,0 se asigna al valor entero representable más positivo y-1,0 se asigna al valor entero representable más negativo. Si el valor interno está fuera del intervalo \[ -1, 1 \] , el valor devuelto de tipo entero correspondiente es indefinido.<br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**brillo de GL \_**</dt> </dl>              | El parámetro *params* devuelve un entero o un valor de punto flotante que representa el exponente especular del material. Los valores enteros, cuando se solicitan, se calculan redondeando el valor de punto flotante interno al valor entero más cercano.<br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**\_índices de color de GL \_**</dt> </dl> | El parámetro *params* devuelve tres valores enteros o de punto flotante que representan los índices de ambiente, difusos e especulares del material. Utilice estos índices solo para la iluminación de índice de color. (Los demás parámetros se usan solo para la iluminación RGBA). Los valores enteros, cuando se solicitan, se calculan Redondeando los valores de punto flotante internos a los valores enteros más cercanos.<br/>                                                                                            |



 

</dd> <dt>

*params* 
</dt> <dd>

Devuelve los datos solicitados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *destino* o la *consulta* no era un valor aceptado.<br/>                                                                             |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glGetMaterial** devuelve en *params* el valor o los valores del parámetro *PName* de la *superficie* del material.

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

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





