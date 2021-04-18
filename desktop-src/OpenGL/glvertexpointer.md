---
title: función glVertexPointer (GL. h)
description: La función glVertexPointer define una matriz de datos de vértice.
ms.assetid: e5f97fdc-9448-4389-8533-3855a3213feb
keywords:
- glVertexPointer (función) OpenGL
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
ms.openlocfilehash: 422dd1a7938cc5adb183ff7e17c59a8f52eb4909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492119"
---
# <a name="glvertexpointer-function"></a>glVertexPointer función)

La función **glVertexPointer** define una matriz de datos de vértice.

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

Número de coordenadas por vértice. El valor de *size* debe ser 2, 3 ó 4.

</dd> <dt>

*type* 
</dt> <dd>

El tipo de datos de cada coordenada de la matriz mediante las siguientes constantes simbólicas: GL \_ Short, GL \_ int, GL \_ float y GL \_ Double.

</dd> <dt>

*STRI* 
</dt> <dd>

Desplazamiento de bytes entre los vértices consecutivos. Cuando *STRIDE* es cero, los vértices están estrechamente empaquetados en la matriz.

</dd> <dt>

*puntero* 
</dt> <dd>

Puntero a la primera coordenada del primer vértice de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                              | Significado                                       |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl> | *el tamaño* no era 2, 3 o 4. <br/>        |
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>  | el *tipo* no era un valor aceptado.<br/>  |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl> | *STRIDE* o *Count* era negativo. <br/> |



## <a name="remarks"></a>Observaciones

La función **glVertexPointer** especifica la ubicación y los datos de una matriz de coordenadas de vértice que se van a usar en la representación. El parámetro *size* especifica el número de coordenadas por vértice. El parámetro de *tipo* especifica el tipo de datos de cada coordenada del vértice. El parámetro *STRIDE* determina el desplazamiento de bytes de un vértice al siguiente, lo que permite el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes. En algunas implementaciones, el almacenamiento de vértices y atributos en una sola matriz puede ser más eficaz que el uso de matrices independientes (vea [**glInterleavedArrays**](glinterleavedarrays.md)).

Una matriz de vértices se habilita al especificar la \_ \_ constante de matriz de vértices de GL con [**glEnableClientState**](glenableclientstate.md). Cuando está habilitado, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)y [**glArrayElement**](glarrayelement.md) usan la matriz de vértices. De forma predeterminada, la matriz de vértices está deshabilitada.

No se puede incluir **glVertexPointer** en las listas de visualización.

Cuando se especifica una matriz de vértices mediante **glVertexPointer**, los valores de todos los parámetros de matriz de vértices de la función se guardan en un estado del lado cliente y los elementos de matriz estáticos se pueden almacenar en caché. Dado que los parámetros de la matriz de vértices son de cliente, los valores no se guardan ni restauran en [**glPushAttrib**](glpushattrib.md) y **glPopAttrib**.

Aunque no se genera ningún error si se llama a **glVertexPointer** en pares [**glBegin**](glbegin.md) y [**glEnd**](glend.md) , los resultados son indefinidos.

Las siguientes funciones recuperan información relacionada con **glVertexPointer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ tamaño de matriz de vértices de GL \_

**glGet** con argumento \_ intervalo de matriz de VÉRTICEs de GL \_ \_

**glGet** con el argumento \_ \_ Count de matriz de vértices de contabilidad \_

**glGet** con argumento \_ tipo de matriz de VÉRTICEs de contabilidad \_ \_

[**glGetPointerv**](glgetpointerv.md) con el argumento de \_ matriz de vértices de contabilidad de argumentos \_ \_

[**glIsEnabled**](glisenabled.md) con el argumento \_ matriz de VÉRTICEs de GL \_

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

 

 





