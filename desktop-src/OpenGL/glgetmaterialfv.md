---
title: Función glGetMaterialfv (Gl.h)
description: Las funciones glGetMaterialfv y glGetMaterialiv devuelven parámetros de material. | Función glGetMaterialfv (Gl.h)
ms.assetid: b61dbe0c-5cc2-4397-9d7c-b99507a9f037
keywords:
- Función glGetMaterialfv OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260220"
---
# <a name="glgetmaterialfv-function"></a>Función glGetMaterialfv

Las **funciones glGetMaterialfv** [**y glGetMaterialiv**](glgetmaterialiv.md) devuelven parámetros de material.

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

*Cara* 
</dt> <dd>

Especifica cuál de los dos materiales se está consultando. Se aceptan GL FRONT o GL BACK, que representan los materiales frontal y \_ \_ posterior, respectivamente.

</dd> <dt>

*pname* 
</dt> <dd>

Parámetro de material que se devuelve. Se aceptan los valores siguientes.



| Value                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ AMBIENT**</dt> </dl>                    | El *parámetro params* devuelve cuatro valores enteros o de punto flotante que representan la reflectancia ambiente del material. Los valores enteros, cuando se solicitan, se asignan linealmente desde la representación interna de punto flotante, de modo que 1,0 se asigna al valor entero que se puede representar más positivo y -1,0 se asigna al valor entero que se puede representar más negativo. Si el valor interno está fuera del \[ intervalo -1,1 , el valor devuelto entero \] correspondiente no está definido.<br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFUSO**</dt> </dl>                    | El *parámetro params* devuelve cuatro valores enteros o de punto flotante que representan la reflectancia difusa del material. Los valores enteros, cuando se solicitan, se asignan linealmente desde la representación interna de punto flotante, de modo que 1,0 se asigna al valor entero que se puede representar más positivo y -1,0 se asigna al valor entero que se puede representar más negativo. Si el valor interno está fuera del \[ intervalo -1,1 , el valor devuelto entero \] correspondiente no está definido.<br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ SPECULAR**</dt> </dl>                 | El *parámetro params* devuelve cuatro valores enteros o de punto flotante que representan la reflectancia especular del material. Los valores enteros, cuando se solicitan, se asignan linealmente desde la representación interna de punto flotante, de modo que 1,0 se asigna al valor entero que se puede representar más positivo y -1,0 se asigna al valor entero que se puede representar más negativo. Si el valor interno está fuera del \[ intervalo -1,1 , el valor devuelto entero \] correspondiente no está definido.<br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**EMISIÓN \_ DE GL**</dt> </dl>                 | El *parámetro params* devuelve cuatro valores enteros o de punto flotante que representan la intensidad de luz emitida del material. Los valores enteros, cuando se solicitan, se asignan linealmente desde la representación interna de punto flotante, de modo que 1,0 se asigna al valor entero que se puede representar más positivo y -1,0 se asigna al valor entero que se puede representar más negativo. Si el valor interno está fuera del \[ intervalo -1,1 , el valor devuelto entero \] correspondiente no está definido.<br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**GL \_ GLINESS**</dt> </dl>              | El *parámetro params* devuelve un valor entero o de punto flotante que representa el exponente especular del material. Los valores enteros, cuando se solicitan, se calculan redondeando el valor de punto flotante interno al valor entero más cercano.<br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**ÍNDICES \_ DE COLOR \_ GL**</dt> </dl> | El *parámetro params* devuelve tres valores enteros o de punto flotante que representan los índices ambiente, difuso y especular del material. Use estos índices solo para la iluminación de índice de color. (Los demás parámetros solo se usan para la iluminación RGBA). Los valores enteros, cuando se solicitan, se calculan redondeando los valores de punto flotante internos a los valores enteros más cercanos.<br/>                                                                                            |



 

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
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *target* o *query* no era un valor aceptado.<br/>                                                                             |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glGetMaterial** devuelve en *parámetros* el valor o los valores del parámetro *pname* de la cara del *material.*

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

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





