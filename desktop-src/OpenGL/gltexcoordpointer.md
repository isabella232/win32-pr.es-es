---
title: Función glTexCoordPointer (Gl.h)
description: La función glTexCoordPointer define una matriz de coordenadas de textura.
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- Función GlTexCoordPointer OpenGL
topic_type:
- apiref
api_name:
- glTexCoordPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0892f06b3fd5027939710be9ac74a2ae18c0dc0d712572d094b9a54fd6bb5b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888255"
---
# <a name="gltexcoordpointer-function"></a>Función glTexCoordPointer

La **función glTexCoordPointer** define una matriz de coordenadas de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTexCoordPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*size* 
</dt> <dd>

Número de coordenadas por elemento de matriz. El valor de *size* debe ser 1, 2, 3 o 4.

</dd> <dt>

*type* 
</dt> <dd>

El tipo de datos de cada coordenada de textura de la matriz con las siguientes constantes simbólicas: **GL \_ SHORT,** **GL \_ INT,** **GL \_ FLOAT** y **GL \_ DOUBLE.**

</dd> <dt>

*Paso* 
</dt> <dd>

Desplazamiento de bytes entre elementos de matriz consecutivos. Cuando *stride* es cero, los elementos de la matriz se empaquetan estrechamente en la matriz.

</dd> <dt>

*Puntero* 
</dt> <dd>

Puntero a la primera coordenada del primer elemento de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                              | Significado                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>  | *Type* no era un valor aceptado.<br/> |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl> | *el* tamaño no era 1, 2, 3 o 4.<br/>     |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl> | *stride* era negativo.<br/>            |



## <a name="remarks"></a>Comentarios

La **función glTexCoordPointer** especifica la ubicación y los datos de una matriz de coordenadas de textura que se usarán al representar. El *parámetro size* especifica el número de coordenadas usadas para cada elemento de la matriz. El *parámetro type* especifica el tipo de datos de cada coordenada de textura. El *parámetro stride* determina el desplazamiento de bytes de un elemento de matriz al siguiente, lo que permite el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes. En algunas implementaciones, almacenar los vértices y atributos en una sola matriz puede ser más eficaz que usar matrices independientes. Para obtener más información, [**vea glInterleavedArrays**](glinterleavedarrays.md). Cuando se especifica una matriz de coordenadas de textura, el tamaño, el tipo, el paso y el puntero se guardan en el estado del lado cliente.

Se habilita una matriz de coordenadas de textura cuando se especifica la **constante GL \_ TEXTURE \_ COORD \_ ARRAY** [**con glEnableClientState**](glenableclientstate.md). Cuando se habilita, [**glDrawArrays,**](gldrawarrays.md) [**glDrawElements**](gldrawelements.md)y [**glArrayElement**](glarrayelement.md) usan la matriz de coordenadas de textura. De forma predeterminada, la matriz de coordenadas de textura está deshabilitada.

No se puede **incluir glTexCoordPointer en** listas para mostrar.

Cuando se especifica una matriz de coordenadas de textura mediante **glTexCoordPointer**, los valores de todos los parámetros de la matriz de coordenadas de textura de la función se guardan en un estado del lado cliente y los elementos de la matriz estática se pueden almacenar en caché. Dado que los parámetros de la matriz de coordenadas de textura son de estado del lado cliente, [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md)no guardan ni restauran sus valores.

Aunque no se genera ningún error al llamar **a glTexCoordPointer** dentro de los pares [**glBegin**](glbegin.md) y [**glEnd,**](glend.md) los resultados no están definidos.

Las siguientes funciones recuperan información relacionada **con glTexCoordPointer**:

[**glIsEnabled con**](glisenabled.md) el argumento **GL TEXTURE \_ \_ COORD \_ ARRAY**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento **GL TEXTURE \_ \_ COORD \_ ARRAY \_ SIZE**

**glGet con** argumento **GL TEXTURE \_ \_ COORD \_ ARRAY \_ STRIDE**

**glGet con** el argumento **GL TEXTURE \_ \_ COORD \_ ARRAY \_ COUNT**

**glGet con** el argumento **GL TEXTURE \_ \_ COORD \_ ARRAY \_ TYPE**

[**glGetPointerv con el**](glgetpointerv.md) argumento **GL TEXTURE \_ \_ COORD \_ ARRAY \_ POINTER**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPopClientAttrib**](glpopclientattrib.md)
</dt> <dt>

[**glPushClientAttrib**](glpushclientattrib.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





