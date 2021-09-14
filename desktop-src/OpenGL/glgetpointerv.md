---
title: Función glGetPointerv (Gl.h)
description: La función glGetPointerv devuelve la dirección de una matriz de datos de vértices.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- Función glGetPointerv OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260199"
---
# <a name="glgetpointerv-function"></a>Función glGetPointerv

La **función glGetPointerv** devuelve la dirección de una matriz de datos de vértices.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pname* 
</dt> <dd>

Tipo de puntero de matriz que se devuelve de las siguientes constantes simbólicas: GL \_ COLOR \_ ARRAY \_ POINTER, GL EDGE FLAG ARRAY \_ \_ \_ \_ POINTER, GL FEEDBACK BUFFER \_ \_ \_ POINTER, GL INDEX ARRAY \_ \_ \_ POINTER, GL NORMAL ARRAY \_ \_ \_ POINTER, GL TEXTURE \_ \_ COORD \_ ARRAY POINTER, GL SELECTION BUFFER \_ \_ POINTER \_ \_ \_ \_ \_ y GL VERTEX ARRAY POINTER.

</dd> <dt>

*params* 
</dt> <dd>

Devuelve el valor del puntero de matriz especificado por *pname*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                             | Significado                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl> | *pname* no era un valor aceptado.<br/> |



## <a name="remarks"></a>Observaciones

La **función glGetPointerv** devuelve información de puntero de matriz. El *parámetro pname* es una constante simbólica que especifica el tipo de puntero de matriz que se va a devolver y *params* es un puntero a una ubicación para colocar los datos devueltos.

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

 

 





