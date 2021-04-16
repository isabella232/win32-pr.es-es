---
title: función glTexCoordPointer (GL. h)
description: La función glTexCoordPointer define una matriz de coordenadas de textura.
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- glTexCoordPointer (función) OpenGL
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
ms.openlocfilehash: febc9c79bdbc4a1ed1c14380af47f36309f12662
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686248"
---
# <a name="gltexcoordpointer-function"></a>glTexCoordPointer función)

La función **glTexCoordPointer** define una matriz de coordenadas de textura.

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

El tipo de datos de cada coordenada de textura de la matriz mediante las siguientes constantes simbólicas: **GL \_ Short**, **GL \_ int**, **GL \_ float** y **GL \_ Double**.

</dd> <dt>

*STRI* 
</dt> <dd>

El desplazamiento de bytes entre los elementos de la matriz consecutivos. Cuando *STRIDE* es cero, los elementos de la matriz están estrechamente empaquetados en la matriz.

</dd> <dt>

*puntero* 
</dt> <dd>

Puntero a la primera coordenada del primer elemento de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                              | Significado                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>  | el *tipo* no era un valor aceptado.<br/> |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl> | *el tamaño* no era 1, 2, 3 o 4.<br/>     |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl> | *STRIDE* es negativo.<br/>            |



## <a name="remarks"></a>Observaciones

La función **glTexCoordPointer** especifica la ubicación y los datos de una matriz de coordenadas de textura que se van a utilizar al representar. El parámetro *size* especifica el número de coordenadas utilizadas para cada elemento de la matriz. El parámetro de *tipo* especifica el tipo de datos de cada coordenada de textura. El parámetro *STRIDE* determina el desplazamiento de bytes de un elemento de matriz al siguiente, lo que permite el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes. En algunas implementaciones, el almacenamiento de vértices y atributos en una sola matriz puede ser más eficaz que el uso de matrices independientes. Para obtener más información, vea [**glInterleavedArrays**](glinterleavedarrays.md). Cuando se especifica una matriz de coordenadas de textura, el tamaño, el tipo, el intervalo y el puntero se guardan en el estado del lado cliente.

Una matriz de coordenadas de textura se habilita al especificar la constante de la **\_ \_ \_ matriz de textura de GL** con [**glEnableClientState**](glenableclientstate.md). Cuando está habilitado, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)y [**glArrayElement**](glarrayelement.md) usan la matriz de coordenadas de textura. De forma predeterminada, la matriz de coordenadas de textura está deshabilitada.

No se puede incluir **glTexCoordPointer** en las listas de visualización.

Cuando se especifica una matriz de coordenadas de textura mediante **glTexCoordPointer**, los valores de todos los parámetros de matriz de coordenadas de textura de la función se guardan en un estado del lado cliente y los elementos de matriz estáticos se pueden almacenar en caché. Dado que los parámetros de la matriz de coordenadas de textura son de cliente, los valores no se guardan ni restauran en [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md).

Aunque no se genera ningún error cuando se llama a **glTexCoordPointer** en pares [**glBegin**](glbegin.md) y [**glEnd**](glend.md) , los resultados son indefinidos.

Las siguientes funciones recuperan información relacionada con **glTexCoordPointer**:

[**glIsEnabled**](glisenabled.md) con la **\_ matriz de \_ coordenadas \_ de textura de GL** de argumento

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con **el argumento GL Texture de la \_ \_ \_ matriz \_ tamaño** de la matriz

**glGet** con argumento **GL de la \_ \_ \_ matriz \_ coordenadas de textura de contabilidad**

**glGet** con el **argumento \_ \_ número de \_ matriz \_ de textura de GL de contabilidad**

**glGet** con el **argumento \_ GL \_ Texture \_ \_ tipo de matriz**

[**glGetPointerv**](glgetpointerv.md) con el argumento GL de la **\_ \_ \_ \_ matriz coordenadas de textura de contabilidad**

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

 

 





