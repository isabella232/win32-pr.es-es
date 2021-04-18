---
title: función glGetPointerv (GL. h)
description: La función glGetPointerv devuelve la dirección de una matriz de datos de vértice.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- glGetPointerv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetPointerv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569861922514af88835fbb4e313dab3286b7c47d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686117"
---
# <a name="glgetpointerv-function"></a>glGetPointerv función)

La función **glGetPointerv** devuelve la dirección de una matriz de datos de vértice.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PName* 
</dt> <dd>

El tipo de puntero de matriz que se va a devolver desde las siguientes constantes simbólicas: \_ puntero de matriz de color \_ de GL \_ , puntero de matriz de \_ \_ marca de borde de contabilidad \_ \_ , puntero de búfer de \_ comentarios de contabilidad \_ \_ , \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ puntero de matriz de índice de contabilidad, puntero de matriz de índice de contabilidad general, puntero de matriz de textura de GL, puntero de búfer de selección de contabilidad

</dd> <dt>

*params* 
</dt> <dd>

Devuelve el valor del puntero de matriz especificado por *PName*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                             | Significado                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl> | *PName* no era un valor aceptado.<br/> |



## <a name="remarks"></a>Observaciones

La función **glGetPointerv** devuelve información de puntero de matriz. El parámetro *PName* es una constante simbólica que especifica el tipo de puntero de matriz que se va a devolver y *params* es un puntero a una ubicación donde se colocan los datos devueltos.

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





