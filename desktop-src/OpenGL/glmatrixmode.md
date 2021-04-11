---
title: función glMatrixMode (GL. h)
description: La función glMatrixMode especifica qué matriz es la matriz actual.
ms.assetid: f1006ea3-322a-42a9-b33c-6c7181985ef9
keywords:
- glMatrixMode (función) OpenGL
topic_type:
- apiref
api_name:
- glMatrixMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9877d62fc6e721cc6757206c7c2d07d24f3e879b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150619"
---
# <a name="glmatrixmode-function"></a>glMatrixMode función)

La función **glMatrixMode** especifica qué matriz es la matriz actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glMatrixMode(
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* 
</dt> <dd>

Pila de matriz que es el destino de las operaciones de matriz posteriores. El parámetro de *modo* puede suponer uno de los tres valores.



| Value                                                                                                                                                         | Significado                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="GL_MODELVIEW"></span><span id="gl_modelview"></span><dl> <dt>**GL \_ MODELVIEW**</dt> </dl>    | Aplica las operaciones de matriz subsiguientes a la pila de matriz de MODELVIEW.<br/>  |
| <span id="GL_PROJECTION"></span><span id="gl_projection"></span><dl> <dt>**\_proyección GL**</dt> </dl> | Aplica las operaciones de matriz subsiguientes a la pila de la matriz de proyección.<br/> |
| <span id="GL_TEXTURE"></span><span id="gl_texture"></span><dl> <dt>**\_textura GL**</dt> </dl>          | Aplica las operaciones de matriz subsiguientes a la pila de la matriz de textura.<br/>    |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *modo* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glMatrixMode** establece el modo de matriz actual.

La siguiente función recupera información relacionada con **glMatrixMode**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_

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

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





