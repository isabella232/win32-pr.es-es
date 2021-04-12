---
title: función glColorPointer (GL. h)
description: La función glColorPointer define una matriz de colores.
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- glColorPointer (función) OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abced52f0d0664e998ad8380e33d43d4af36bcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489737"
---
# <a name="glcolorpointer-function"></a>glColorPointer función)

La función **glColorPointer** define una matriz de colores.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glColorPointer(
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

El número de componentes por color. El valor debe ser 3 ó 4.

</dd> <dt>

*type* 
</dt> <dd>

El tipo de datos de cada componente de color de una matriz de colores. Los tipos de datos aceptables se especifican con las siguientes constantes: \_ bytes de GL, \_ bytes sin signo de contabilidad general, \_ GL \_ Short, GL \_ sin signo \_ corto, GL \_ int, libro de contabilidad \_ sin signo de contabilidad flotante, \_ GL \_ float o GL \_ doble.

</dd> <dt>

*STRI* 
</dt> <dd>

Desplazamiento de bytes entre colores consecutivos. Cuando *STRIDE* es cero, los colores se empaquetan estrechamente en la matriz.

</dd> <dt>

*puntero* 
</dt> <dd>

Puntero al primer componente del primer elemento de color de una matriz de colores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                              | Significado                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl> | *el tamaño* no era 3 ó 4.<br/>            |
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>  | el *tipo* no era un valor aceptado.<br/> |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl> | *STRIDE* o *Count* era negativo.<br/> |



## <a name="remarks"></a>Observaciones

La función **glColorPointer** especifica la ubicación y el formato de datos de una matriz de componentes de color que se va a utilizar al representar. El parámetro *STRIDE* determina el desplazamiento de bytes de un color a la siguiente, lo que permite el empaquetado de atributos de vértice en una sola matriz o almacenamiento en matrices independientes. En algunas implementaciones, el almacenamiento de atributos de vértices en una sola matriz puede ser más eficaz que el uso de matrices independientes.

La matriz de colores se habilita especificando la \_ \_ constante de matriz de colores GL con [**glEnableClientState**](glenableclientstate.md). La llamada a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md) usa la matriz de colores que, por tanto, está habilitada. De forma predeterminada, la matriz de colores está deshabilitada. Las llamadas a **glColorPointer** no se pueden escribir en las listas de visualización.

Cuando se especifica una matriz de colores mediante **glColorPointer**, los valores de todos los parámetros de la matriz de colores de la función se guardan en un estado de cliente y se pueden almacenar en caché los elementos de matriz estáticos. Dado que los parámetros de la matriz de colores están en un estado de cliente, [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md) no guardan ni restauran los valores de los parámetros.

Aunque si se especifica la matriz de colores en pares [**glBegin**](glbegin.md) y [**glend**](glend.md) no se genera un error, los resultados son indefinidos.

Las siguientes funciones recuperan información relacionada con la función **glColorPointer** :

[**glIsEnabled**](glisenabled.md) con el argumento \_ matriz de color de GL \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento de \_ \_ tamaño de matriz de color de GL \_

**glGet** con el argumento \_ \_ tipo de matriz de color GL \_

**glGet** con argumento \_ intervalo de \_ matriz de color de GL \_

**glGet** con el argumento \_ \_ número de matriz de color de GL \_

[**glGetPointerv**](glgetpointerv.md) con el argumento de \_ matriz de color de GL \_ \_

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

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
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

 

 





