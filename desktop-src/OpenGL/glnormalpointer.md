---
title: Función glNormalPointer (Gl.h)
description: La función glNormalPointer define una matriz de normales.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- Función glNormalPointer OpenGL
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
ms.openlocfilehash: 4f188a65a0a2bff0438188ae7521615de45341147b138a849d2fd375ed8a959b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938414"
---
# <a name="glnormalpointer-function"></a>función glNormalPointer

La **función glNormalPointer** define una matriz de normales.

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

Tipo de datos de cada coordenada de la matriz mediante las siguientes constantes simbólicas: GL \_ BYTE, GL \_ SHORT, GL \_ INT, GL \_ FLOAT y GL \_ DOUBLE.

</dd> <dt>

*Paso* 
</dt> <dd>

Desplazamiento de bytes entre normales consecutivas. Cuando *stride* es cero, las normales se empaquetan estrechamente en la matriz.

</dd> <dt>

*Puntero* 
</dt> <dd>

Puntero al primer elemento normal de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *Type* no era un valor aceptado.<br/> |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | *stride* o *count era* negativo.<br/> |



## <a name="remarks"></a>Comentarios

La **función glNormalPointer** especifica la ubicación y los datos de una matriz de normales que se usará al representar. El *parámetro type* especifica el tipo de datos de cada coordenada normal. El *parámetro stride* determina el desplazamiento de bytes de una normal a la siguiente, lo que permite el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes. En algunas implementaciones, almacenar los vértices y atributos en una sola matriz puede ser más eficaz que usar matrices independientes. vea [**glInterleavedArrays para**](glinterleavedarrays.md) obtener más información.

Se habilita una matriz normal cuando se especifica la constante GL \_ NORMAL \_ ARRAY con [**glEnableClientState**](glenableclientstate.md). Cuando se habilita, [**glDrawArrays,**](gldrawarrays.md) [**glDrawElements**](gldrawelements.md) y [**glArrayElement**](glarrayelement.md) usan la matriz normal. De forma predeterminada, la matriz normal está deshabilitada.

No se puede incluir **glNormalPointer en** las listas para mostrar.

Cuando se especifica una matriz normal mediante **glNormalPointer**, los valores de todos los parámetros de matriz normales de la función se guardan en un estado del lado cliente. Dado que los parámetros de matriz normales se guardan en un estado del lado cliente, [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md)no guardan ni restauran sus valores.

Aunque no se genera ningún error al llamar **a glNormalPointer** dentro de los pares [**glBegin**](glbegin.md) y [**glEnd,**](glend.md) los resultados son indefinidos.

Las funciones siguientes están asociadas **a glNormalPointer**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ NORMAL ARRAY \_ \_ STRIDE

**glGet con** el argumento GL \_ NORMAL ARRAY \_ \_ COUNT

**glGet con** el argumento GL \_ NORMAL ARRAY \_ \_ TYPE

**glGetPointerv con el** argumento GL \_ NORMAL ARRAY \_ \_ POINTER

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ NORMAL \_ ARRAY

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





