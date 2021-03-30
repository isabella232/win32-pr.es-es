---
title: función glPrioritizeTextures (GL. h)
description: La función glPrioritizeTextures establece la prioridad de residencia de las texturas.
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
keywords:
- glPrioritizeTextures (función) OpenGL
topic_type:
- apiref
api_name:
- glPrioritizeTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38ab4b1bd6b5f9682b4d8753e7e84f1f2b58a09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801634"
---
# <a name="glprioritizetextures-function"></a>glPrioritizeTextures función)

La función **glPrioritizeTextures** establece la prioridad de residencia de las texturas.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPrioritizeTextures(
         GLsizei  n,
   const GLuint   *textures,
   const GLclampf *priorities
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*n* 
</dt> <dd>

Número de texturas que se van a clasificar por orden de prioridad.

</dd> <dt>

*texturas* 
</dt> <dd>

Puntero al primer elemento de una matriz que contiene los nombres de las texturas que se van a priorizar.

</dd> <dt>

*fija* 
</dt> <dd>

Puntero al primer elemento de una matriz que contiene las prioridades de textura. Una prioridad especificada en un elemento del parámetro de *prioridades* se aplica a la textura denominada por el elemento correspondiente del parámetro *Textures* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *n* era un valor negativo.<br/>                                                                                                  |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glPrioritizeTextures** asigna las *n* prioridades de textura especificadas en el parámetro de *prioridades* a las *n* texturas mencionadas en el parámetro *Textures* . En los equipos con una cantidad limitada de memoria de textura, OpenGL establece un "conjunto de trabajo" de texturas que residen en la memoria de textura. Estas texturas se pueden enlazar a un destino de textura mucho más eficaz que las texturas que no son residentes.

Al especificar una prioridad para cada textura, la función **glPrioritizeTextures** le permite determinar qué texturas deben ser residentes.

Los elementos de prioridades de textura en las *prioridades* se fijan al intervalo \[ 0,0, 1,0 \] antes de que se asignen. Cero indica la prioridad más baja; por lo tanto, es menos probable que las texturas con prioridad cero sean residentes. El valor 1,0 indica la prioridad máxima; por lo tanto, es más probable que las texturas con prioridad 1,0 sean residentes. Sin embargo, no se garantiza que las texturas sean residentes hasta que se enlazan.

La función **glPrioritizeTextures** omite los intentos de dar prioridad a la textura 0 o cualquier nombre de textura que no corresponda a una textura existente. Ninguna de las funciones nombradas por el parámetro *Textures* debe estar enlazada a un destino de textura.

Si una textura está actualmente enlazada, también puede usar la función [**glTexParameter**](gltexparameter-functions.md) para establecer su prioridad. Esta es la única manera de establecer la prioridad de una textura predeterminada.

Puede incluir **glPrioritizeTextures** en las listas de visualización.

La siguiente función recupera la prioridad de una textura enlazada actualmente relacionada con **glPrioritizeTextures**:

-   [**glGetTexParameter**](glgettexparameter.md) con el nombre de parámetro \_ prioridad de textura GL \_

> [!Note]  
> La función **glPrioritizeTextures** solo está disponible en la versión 1,1 o posterior de OpenGL.

 

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

[**glAreTexturesResident**](glaretexturesresident.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





