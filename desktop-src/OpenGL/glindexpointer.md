---
title: función glIndexPointer (GL. h)
description: La función glIndexPointer define una matriz de índices de color.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- glIndexPointer (función) OpenGL
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489154"
---
# <a name="glindexpointer-function"></a>glIndexPointer función)

La función **glIndexPointer** define una matriz de índices de color.

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

El tipo de datos de cada índice de color de la matriz mediante las siguientes constantes simbólicas: GL \_ Short, GL \_ int, GL \_ float, GL \_ Double.

</dd> <dt>

*STRI* 
</dt> <dd>

El desplazamiento de bytes entre índices de color consecutivos. Cuando *STRIDE* es cero, los índices de color están estrechamente empaquetados en la matriz.

</dd> <dt>

*puntero* 
</dt> <dd>

Puntero al primer índice de color de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                              | Significado                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>  | el *tipo* no era un valor aceptado.<br/> |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl> | *STRIDE* o *Count* era negativo.<br/> |



## <a name="remarks"></a>Observaciones

La función **glIndexPointer** especifica la ubicación y los datos de una matriz de índices de color que se van a utilizar al representar. El parámetro de *tipo* especifica el tipo de datos de cada índice de color y *STRIDE* determina el desplazamiento de bytes de un índice de color al siguiente, lo que permite el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes. En algunas implementaciones, el almacenamiento de vértices y atributos en una sola matriz puede ser más eficaz que el uso de matrices independientes. Para obtener más información, vea [**glInterleavedArrays**](glinterleavedarrays.md).

Una matriz de índice de color se habilita al especificar la constante de matriz de índice de GL \_ \_ con [**glEnableClientState**](glenableclientstate.md). Cuando está habilitado, [**glDrawArrays**](gldrawarrays.md) y [**glArrayElement**](glarrayelement.md) usan la matriz de índices de color. De forma predeterminada, la matriz de índices de color está deshabilitada.

No se puede incluir **glIndexPointer** en las listas de visualización.

Cuando se especifica una matriz de índice de color mediante **glIndexPointer**, los valores de todos los parámetros de matriz de índice de color de la función se guardan en un estado del lado cliente y los elementos de matriz estáticos se pueden almacenar en caché. Dado que los parámetros de matriz de índice de color son de cliente, los valores no se guardan ni restauran en [**glPushAttrib**](glpushattrib.md) y **glPopAttrib**.

Aunque no se genera ningún error cuando se llama a **glIndexPointer** en pares [**glBegin**](glbegin.md) y **glEnd** , los resultados son indefinidos.

Las siguientes funciones recuperan información relacionada con **glIndexPointer**:

[**glIsEnabled**](glisenabled.md) con el argumento \_ matriz de índice de GL \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento \_ intervalo de \_ matriz de índice de GL \_

**glGet** con argumento \_ \_ recuento de matriz de índice de GL \_

**glGet** con argumento \_ tipo de \_ matriz de índice de GL \_

**glGet** con el argumento \_ \_ tamaño de matriz de índice de GL \_

[**glGetPointerv**](glgetpointerv.md) con argumento de \_ matriz de índice de contabilidad de argumentos \_ \_

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

 

 





