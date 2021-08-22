---
title: Función glEdgeFlagPointer (Gl.h)
description: La función glEdgeFlagPointer define una matriz de marcas perimetrales.
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- Función glEdgeFlagPointer OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa648a15542a3f3f2f35f577760991da74bc978c0464c1373c8eddea38941a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061643"
---
# <a name="gledgeflagpointer-function"></a>Función glEdgeFlagPointer

La **función glEdgeFlagPointer** define una matriz de marcas perimetrales.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Paso* 
</dt> <dd>

Desplazamiento de bytes entre marcas de borde consecutivas. Cuando *stride* es cero, las marcas de borde se empaquetan estrechamente en la matriz.

</dd> <dt>

*Puntero* 
</dt> <dd>

Puntero a la primera marca perimetral de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                             | Significado                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl> | *stride* o *count era* negativo.<br/> |



## <a name="remarks"></a>Comentarios

La **función glEdgeFlagPointer** especifica la ubicación y los datos de una matriz de marcas de borde booleanas que se usarán al representar. El *parámetro stride* determina el desplazamiento de bytes de una marca perimetral a la siguiente, lo que permite el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes. En algunas implementaciones, almacenar los vértices y atributos en una sola matriz puede ser más eficaz que usar matrices independientes.

Se habilita una matriz de marcas perimetrales cuando se especifica la constante GL \_ EDGE FLAG ARRAY con \_ \_ [**glEnableClientState**](glenableclientstate.md). Cuando se habilita, [**glDrawArrays**](gldrawarrays.md) o [**glArrayElement**](glarrayelement.md) usa la matriz de marcas perimetrales. De forma predeterminada, la matriz de marcas perimetrales está deshabilitada.

Use **glDrawArrays para** construir una secuencia de primitivas (todas del mismo tipo) a partir de matrices de atributos de vértices y vértices especificados previamente. Use **glArrayElement para** especificar primitivas mediante la indexación de vértices y atributos de vértice, y [**glDrawElements**](gldrawelements.md) para construir una secuencia de primitivas mediante la indexación de vértices y atributos de vértice.

No se puede incluir **glEdgeFlagPointer en** las listas para mostrar.

Cuando se especifica una matriz de marcas perimetrales mediante **glEdgeFlagPointer**, los valores de todos los parámetros de matriz de marcas perimetrales de la función se guardan en un estado del lado cliente y los elementos de la matriz estática se pueden almacenar en caché. Dado que los parámetros de matriz de marca perimetral están en estado de cliente, [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md) no guardarán ni restaurarán sus valores.

Aunque llamar **a glEdgeFlagPointer** dentro de un par [**glBegin**](glbegin.md)no genera un / [](glend.md) error, los resultados son indefinidos.

Las siguientes funciones recuperan información relacionada con **la función glEdgeFlagPointer:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ EDGE FLAG ARRAY \_ \_ \_ STRIDE

**glGet con** el argumento GL \_ EDGE FLAG ARRAY \_ \_ \_ COUNT

[**glGetPointerv con el**](glgetpointerv.md) argumento GL \_ EDGE FLAG ARRAY \_ \_ \_ POINTER

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ EDGE FLAG \_ \_ ARRAY

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
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

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





