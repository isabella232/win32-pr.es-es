---
title: función glDrawElements (GL. h)
description: La función glDrawElements representa primitivos de los datos de la matriz.
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- glDrawElements (función) OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976e779235dc330467d610406156534b5e72841d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534486"
---
# <a name="gldrawelements-function"></a>glDrawElements función)

La función **glDrawElements** representa primitivos de los datos de la matriz.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* 
</dt> <dd>

Tipo de primitivas que se van a representar. Puede suponer uno de los siguientes valores simbólicos: \_ puntos de contabilidad, \_ franja de línea de contabilidad, bucle de línea de libro de contabilidad, \_ \_ \_ líneas de contabilidad general, franja de \_ \_ triángulo de contabilidad \_ , ventilador de triángulo de contabilidad general, \_ \_ \_ triángulos de GL, franja cuádruple de contabilidad, \_ \_ cuádruples de contabilidad \_ y polígono de contabilidad \_ .

</dd> <dt>

*count* 
</dt> <dd>

Número de elementos que se van a representar.

</dd> <dt>

*type* 
</dt> <dd>

Tipo de los valores de los índices. Debe ser un byte sin signo de libro de contabilidad, un valor \_ \_ \_ Short sin signo o un valor entero de GL \_ \_ sin signo \_ .

</dd> <dt>

*índices* 
</dt> <dd>

Puntero a la ubicación donde se almacenan los índices.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *modo* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *Count* era un valor negativo.<br/>                                                                                              |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glDrawElements** permite especificar varias primitivas geométricas con muy pocas llamadas de función. En lugar de llamar a una función de OpenGL para pasar cada vértice, normal o color individual, puede especificar de antemano matrices independientes de vértices, normales y colores y utilizarlos para definir una secuencia de primitivas (todo el mismo tipo) con una única llamada a **glDrawElements**.

Cuando se llama a la función **glDrawElements** , se usan elementos secuenciales de *recuento* de *índices* para construir una secuencia de primitivas geométricas. El parámetro *mode* especifica qué tipo de primitivas se construyen y cómo se usan los elementos de la matriz para construir estos primitivos. Si \_ \_ no está habilitada la matriz de vértices de contabilidad, no se generan primitivas geométricas.

Los atributos de vértices modificados por **glDrawElements** tienen un valor no especificado después de que **glDrawElements** devuelve. Por ejemplo, si \_ \_ la matriz de colores de GL está habilitada, el valor del color actual no está definido después de que se ejecute **glDrawElements** . Los atributos que no se modifican permanecen inalterados.

Puede incluir la función **glDrawElements** en mostrar listas. Cuando **glDrawElements** se incluye en una lista de visualización, los datos de la matriz necesarios (determinados por los punteros de matriz y habilitados) también se especifican en la lista de visualización. Dado que los punteros de matriz y los habilitados son variables de estado de cliente, sus valores afectan a las listas de visualización cuando se crean las listas, no cuando se ejecutan las listas.

> [!Note]  
> La función **glDrawElements** solo está disponible en la versión 1,1 o posterior de OpenGL.

 

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

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





