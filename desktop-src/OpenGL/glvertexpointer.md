---
title: Función glVertexPointer (Gl.h)
description: La función glVertexPointer define una matriz de datos de vértices.
ms.assetid: e5f97fdc-9448-4389-8533-3855a3213feb
keywords:
- Función glVertexPointer OpenGL
topic_type:
- apiref
api_name:
- glVertexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7526b553bcacfae421541dc3c695611d704a76ae960db61dab2795e80315d951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035455"
---
# <a name="glvertexpointer-function"></a>Función glVertexPointer

La **función glVertexPointer** define una matriz de datos de vértice.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glVertexPointer(
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

Número de coordenadas por vértice. El valor de *size* debe ser 2, 3 o 4.

</dd> <dt>

*type* 
</dt> <dd>

Tipo de datos de cada coordenada de la matriz mediante las siguientes constantes simbólicas: GL \_ SHORT, GL \_ INT, GL \_ FLOAT y GL \_ DOUBLE.

</dd> <dt>

*Paso* 
</dt> <dd>

Desplazamiento de bytes entre vértices consecutivos. Cuando *stride* es cero, los vértices se empaquetan estrechamente en la matriz.

</dd> <dt>

*Puntero* 
</dt> <dd>

Puntero a la primera coordenada del primer vértice de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                              | Significado                                       |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl> | *el* tamaño no era 2, 3 o 4. <br/>        |
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>  | *Type* no era un valor aceptado.<br/>  |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl> | *stride* o *count era* negativo. <br/> |



## <a name="remarks"></a>Comentarios

La **función glVertexPointer** especifica la ubicación y los datos de una matriz de coordenadas de vértice que se usarán al representar. El *parámetro size* especifica el número de coordenadas por vértice. El *parámetro type* especifica el tipo de datos de cada coordenada de vértice. El *parámetro stride* determina el desplazamiento de bytes de un vértice al siguiente, lo que permite el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes. En algunas implementaciones, almacenar los vértices y atributos en una sola matriz puede ser más eficaz que usar matrices independientes (vea [**glInterleavedArrays**](glinterleavedarrays.md)).

Se habilita una matriz de vértices cuando se especifica la constante GL \_ VERTEX \_ ARRAY con [**glEnableClientState**](glenableclientstate.md). Cuando se habilita, [**glDrawArrays,**](gldrawarrays.md) [**glDrawElements**](gldrawelements.md)y [**glArrayElement**](glarrayelement.md) usan la matriz de vértices. De forma predeterminada, la matriz de vértices está deshabilitada.

No se puede **incluir glVertexPointer en** las listas para mostrar.

Cuando se especifica una matriz de vértices mediante **glVertexPointer**, los valores de todos los parámetros de la matriz de vértices de la función se guardan en un estado del lado cliente y los elementos de la matriz estática se pueden almacenar en caché. Dado que los parámetros de la matriz de vértices son de estado del lado cliente, [**glPushAttrib**](glpushattrib.md) y **glPopAttrib** no guardan ni restauran sus valores.

Aunque no se genera ningún error si se llama **a glVertexPointer** dentro de los pares [**glBegin**](glbegin.md) y [**glEnd,**](glend.md) los resultados son indefinidos.

Las siguientes funciones recuperan información relacionada **con glVertexPointer**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ VERTEX ARRAY \_ \_ SIZE

**glGet con** el argumento GL \_ VERTEX ARRAY \_ \_ STRIDE

**glGet con** el argumento GL \_ VERTEX ARRAY \_ \_ COUNT

**glGet con** el argumento GL \_ VERTEX ARRAY \_ \_ TYPE

[**glGetPointerv con el**](glgetpointerv.md) argumento GL \_ VERTEX ARRAY \_ \_ POINTER

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ VERTEX \_ ARRAY

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

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
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

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> </dl>

 

 





