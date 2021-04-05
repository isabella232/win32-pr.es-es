---
title: función glEdgeFlagPointer (GL. h)
description: La función glEdgeFlagPointer define una matriz de marcas de borde.
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- glEdgeFlagPointer (función) OpenGL
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
ms.openlocfilehash: 4390a9838fef418763aa4bcafbf815ab0cdf3466
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802804"
---
# <a name="gledgeflagpointer-function"></a>glEdgeFlagPointer función)

La función **glEdgeFlagPointer** define una matriz de marcas de borde.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*STRI* 
</dt> <dd>

El desplazamiento de bytes entre las marcas de borde consecutivas. Cuando *STRIDE* es cero, las marcas de borde están estrechamente empaquetadas en la matriz.

</dd> <dt>

*puntero* 
</dt> <dd>

Puntero a la primera marca de borde de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                             | Significado                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl> | *STRIDE* o *Count* era negativo.<br/> |



## <a name="remarks"></a>Observaciones

La función **glEdgeFlagPointer** especifica la ubicación y los datos de una matriz de marcas de borde booleanos que se van a usar en la representación. El parámetro *STRIDE* determina el desplazamiento de bytes de una marca perimetral a la siguiente, que habilita el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes. En algunas implementaciones, el almacenamiento de vértices y atributos en una sola matriz puede ser más eficaz que el uso de matrices independientes.

Una matriz de marcas de borde se habilita al especificar la constante de la matriz de marca de borde de GL \_ \_ \_ con [**glEnableClientState**](glenableclientstate.md). Cuando está habilitado, [**glDrawArrays**](gldrawarrays.md) o [**glArrayElement**](glarrayelement.md) usa la matriz de marcas de borde. De forma predeterminada, la matriz de marcas de borde está deshabilitada.

Use **glDrawArrays** para construir una secuencia de primitivas (todo el mismo tipo) a partir de matrices de atributos de vértices y vértices predeterminados. Use **glArrayElement** para especificar primitivos mediante la indexación de vértices y atributos de vértice, y [**glDrawElements**](gldrawelements.md) para construir una secuencia de primitivas mediante la indexación de vértices y atributos de vértice.

No se puede incluir **glEdgeFlagPointer** en las listas de visualización.

Cuando se especifica una matriz de marcas de borde con **glEdgeFlagPointer**, los valores de todos los parámetros de matriz de marcas de borde de la función se guardan en un estado del lado cliente y los elementos de matriz estáticos se pueden almacenar en caché. Dado que los parámetros de matriz perimetral-Flag están en un estado de cliente, [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md) no guardan ni restauran sus valores.

Aunque llamar a **glEdgeFlagPointer** dentro de un par glend de [**glBegin**](glbegin.md)no / [](glend.md) genera un error, los resultados son indefinidos.

Las siguientes funciones recuperan información relacionada con la función **glEdgeFlagPointer** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento \_ intervalo de \_ matriz de marca de margen de \_ Contabilidad \_

**glGet** con argumento \_ \_ \_ recuento de matriz de marcas de margen de contabilidad \_

[**glGetPointerv**](glgetpointerv.md) con argumento de \_ \_ matriz de marca de borde de \_ contabilidad de argumentos \_

[**glIsEnabled**](glisenabled.md) con el argumento \_ \_ matriz de marca del borde de contabilidad \_

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

 

 





