---
title: Función glIndexPointer (Gl.h)
description: La función glIndexPointer define una matriz de índices de color.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- Función glIndexPointer OpenGL
topic_type:
- apiref
api_name:
- glIndexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca6858d7d1e3f13e4155bd40307a53b22e80a56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260108"
---
# <a name="glindexpointer-function"></a>Función glIndexPointer

La **función glIndexPointer** define una matriz de índices de color.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glIndexPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*type* 
</dt> <dd>

El tipo de datos de cada índice de color de la matriz mediante las siguientes constantes simbólicas: GL \_ SHORT, GL \_ INT, GL \_ FLOAT, GL \_ DOUBLE.

</dd> <dt>

*Paso* 
</dt> <dd>

Desplazamiento de bytes entre índices de color consecutivos. Cuando *stride* es cero, los índices de color se empaquetan estrechamente en la matriz.

</dd> <dt>

*Puntero* 
</dt> <dd>

Puntero al primer índice de color de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                              | Significado                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>  | *Type* no era un valor aceptado.<br/> |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl> | *stride* o *count era* negativo.<br/> |



## <a name="remarks"></a>Observaciones

La **función glIndexPointer** especifica la ubicación y los datos de una matriz de índices de color que se usarán al representar. El  parámetro type especifica el tipo de datos de cada índice de color y *stride* determina el desplazamiento de bytes de un índice de color al siguiente, lo que permite el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes. En algunas implementaciones, almacenar los vértices y atributos en una sola matriz puede ser más eficaz que usar matrices independientes. Para obtener más información, [**vea glInterleavedArrays**](glinterleavedarrays.md).

Se habilita una matriz de índice de colores cuando se especifica la constante GL \_ INDEX \_ ARRAY con [**glEnableClientState**](glenableclientstate.md). Cuando se habilita, [**glDrawArrays**](gldrawarrays.md) y [**glArrayElement**](glarrayelement.md) usan la matriz de índice de colores. De forma predeterminada, la matriz de índice de colores está deshabilitada.

No se puede **incluir glIndexPointer en** listas para mostrar.

Cuando se especifica una matriz de índice de colores mediante **glIndexPointer**, los valores de todos los parámetros de la matriz de índice de colores de la función se guardan en un estado del lado cliente y los elementos de la matriz estática se pueden almacenar en caché. Dado que los parámetros de matriz de índice de color son de estado del lado cliente, [**glPushAttrib**](glpushattrib.md) y **glPopAttrib** no guardan ni restauran sus valores.

Aunque no se genera ningún error al llamar **a glIndexPointer** dentro de los pares [**glBegin**](glbegin.md) y **glEnd,** los resultados no están definidos.

Las funciones siguientes recuperan información relacionada **con glIndexPointer**:

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ INDEX \_ ARRAY

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ INDEX ARRAY \_ \_ STRIDE

**glGet con** el argumento GL \_ INDEX ARRAY \_ \_ COUNT

**glGet con** el argumento GL \_ INDEX ARRAY \_ \_ TYPE

**glGet con** el argumento GL \_ INDEX ARRAY \_ \_ SIZE

[**glGetPointerv con el**](glgetpointerv.md) argumento GL \_ INDEX ARRAY \_ \_ POINTER

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

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





