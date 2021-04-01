---
title: función glNormalPointer (GL. h)
description: La función glNormalPointer define una matriz de normales.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- glNormalPointer (función) OpenGL
topic_type:
- apiref
api_name:
- glNormalPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f3abbfbd989351af647557ec64f8ee3172dc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997131"
---
# <a name="glnormalpointer-function"></a>glNormalPointer función)

La función **glNormalPointer** define una matriz de normales.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glNormalPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*type* 
</dt> <dd>

El tipo de datos de cada coordenada de la matriz mediante las siguientes constantes simbólicas: GL \_ byte, GL \_ Short, GL \_ int, GL \_ float y GL \_ Double.

</dd> <dt>

*STRI* 
</dt> <dd>

El desplazamiento de bytes entre las normales consecutivas. Cuando *STRIDE* es cero, los normales están estrechamente empaquetados en la matriz.

</dd> <dt>

*puntero* 
</dt> <dd>

Puntero a la primera normal de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *tipo* no era un valor aceptado.<br/> |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | *STRIDE* o *Count* era negativo.<br/> |



## <a name="remarks"></a>Observaciones

La función **glNormalPointer** especifica la ubicación y los datos de una matriz de normalización que se va a utilizar al representar. El parámetro de *tipo* especifica el tipo de datos de cada coordenada normal. El parámetro *STRIDE* determina el desplazamiento de bytes de una normal a la siguiente, lo que permite el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes. En algunas implementaciones, el almacenamiento de vértices y atributos en una sola matriz puede ser más eficaz que el uso de matrices independientes. consulte [**glInterleavedArrays**](glinterleavedarrays.md) para obtener más información.

Una matriz normal se habilita cuando se especifica la \_ constante de \_ matriz normal de GL con [**glEnableClientState**](glenableclientstate.md). Cuando está habilitado, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) y [**glArrayElement**](glarrayelement.md) usan la matriz normal. De forma predeterminada, la matriz normal está deshabilitada.

No se puede incluir **glNormalPointer** en las listas de visualización.

Cuando se especifica una matriz normal mediante **glNormalPointer**, los valores de todos los parámetros de matriz normales de la función se guardan en un estado del lado cliente. Dado que los parámetros de matriz normales se guardan en un estado de cliente, los valores no se guardan ni restauran en [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md).

Aunque no se genera ningún error cuando se llama a **glNormalPointer** en pares [**glBegin**](glbegin.md) y [**glEnd**](glend.md) , los resultados son indefinidos.

Las siguientes funciones están asociadas a **glNormalPointer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento \_ intervalo de \_ matriz \_ normal de GL

**glGet** con el argumento \_ \_ recuento de matriz normal de contabilidad \_

**glGet** con argumento \_ tipo de \_ matriz \_ normal de contabilidad

**glGetPointerv** con el argumento \_ , \_ puntero de matriz normal de contabilidad \_

[**glIsEnabled**](glisenabled.md) con el argumento \_ matriz normal de GL \_

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

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glInterleavedArrays**](glinterleavedarrays.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> </dl>

 

 





