---
title: función glGetMapiv (GL. h)
description: Las funciones glGetMapdv, glGetMapfv y glGetMapiv devuelven parámetros de evaluador. | función glGetMapiv (GL. h)
ms.assetid: bc055451-7c20-4a8a-96dd-55c877700714
keywords:
- glGetMapiv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetMapiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fc8bf74a80916434f806e2e1f46b633b7243e61
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670151"
---
# <a name="glgetmapiv-function"></a>glGetMapiv función)

Las funciones [**glGetMapdv**](glgetmapdv.md), [**glGetMapfv**](glgetmapfv.md)y **glGetMapiv** devuelven parámetros de evaluador.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetMapiv(
   GLenum target,
   GLenum query,
   GLint  *v
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Nombre simbólico de un mapa. A continuación se indican los valores aceptados: GL \_ MAP1 \_ color \_ 4, GL \_ MAP1 \_ index, GL \_ MAP1 \_ normal, GL \_ MAP1 \_ Texture \_ coordenadas \_ 1, GL \_ MAP1 \_ Texture \_ coordenadas \_ 2, GL \_ MAP1 \_ Texture \_ coordenadas \_ 3, GL \_ MAP1 \_ Texture \_ \_ 4, GL \_ MAP1 \_ Vertex \_ 3, GL \_ MAP1 \_ Vertex \_ 4, GL \_ MAP2 ( \_ color \_ 4, GL \_ MAP2 ( \_ index, GL \_ MAP2 ( \_ normal, GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 1, GL MAP2 (Texture 3, GL MAP2 ( \_ \_ \_ \_ \_ \_ Texture \_ \_ 4, GL \_ MAP2 ( \_ Texture \_ \_ 4, GL \_ MAP2 (Texture \_ \_ y \_ \_ \_ GL MAP2 (.

</dd> <dt>

*consulta* 
</dt> <dd>

Especifica el parámetro que se va a devolver. Se aceptan los siguientes nombres simbólicos.



| Value                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <dt>**GL \_ COEFF**</dt> </dl>    | El parámetro *v* devuelve los puntos de control de la función Evaluator. Los evaluadores unidimensionales devuelven puntos de control de *orden* y los evaluadores bidimensionales devuelven puntos de control *uorder* *x* *Vorder* . Cada punto de control se compone de uno, dos, tres o cuatro valores de punto flotante de precisión simple o de punto flotante de precisión sencilla, dependiendo del tipo de evaluador. Los puntos de control bidimensionales se devuelven en orden principal de fila, incrementando rápidamente el índice de *uorder* y el índice de *Vorder* después de cada fila. Los valores enteros, cuando se solicitan, se calculan Redondeando los valores de punto flotante internos a los valores enteros más cercanos.<br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <dt>**orden de contabilidad \_**</dt> </dl>    | El parámetro *v* devuelve el orden de la función evaluadora. Los evaluadores unidimensionales devuelven un único valor, *Order*. Los evaluadores bidimensionales devuelven dos valores, *uorder* y *Vorder*.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <dt>**dominio de contabilidad general \_**</dt> </dl> | El parámetro *v* devuelve los parámetros de asignación lineal de *u* y *v* . Los evaluadores unidimensionales devuelven dos valores, *u* 1 y *u* 2, según se especifica en [**glMap1**](glmap1.md). Los evaluadores bidimensionales devuelven cuatro valores (*U1*, *U2*, *v1* y *V2*), tal y como se especifica en [**glMap2**](glmap2.md). Los valores enteros, cuando se solicitan, se calculan Redondeando los valores de punto flotante internos a los valores enteros más cercanos.<br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

*v* 
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

Las funciones **glGetMap** devuelven parámetros de evaluador. (Las funciones **glMap1** y **glMap2** definen evaluadores). El parámetro de *destino* especifica un mapa, la *consulta* selecciona un parámetro específico y *v* apunta al almacenamiento donde se devolverán los valores.

Los valores aceptables para el parámetro de *destino* se describen en [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md).

Si se genera un error, no se realiza ningún cambio en el contenido de *v*.

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

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





