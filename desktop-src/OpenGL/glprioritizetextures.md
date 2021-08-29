---
title: Función glPrioritizeTextures (Gl.h)
description: La función glPrioritizeTextures establece la prioridad de residencia de las texturas.
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
keywords:
- Función glPrioritizeTextures OpenGL
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
ms.openlocfilehash: e27b3679264d9b5830ebf7629e6dbca496123149a20e18ed5431502bde73b6de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492665"
---
# <a name="glprioritizetextures-function"></a>Función glPrioritizeTextures

La **función glPrioritizeTextures** establece la prioridad de residencia de las texturas.

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

Número de texturas que se va a priorizar.

</dd> <dt>

*Texturas* 
</dt> <dd>

Puntero al primer elemento de una matriz que contiene los nombres de las texturas a las que se va a dar prioridad.

</dd> <dt>

*Prioridades* 
</dt> <dd>

Puntero al primer elemento de una matriz que contiene las prioridades de textura. Una prioridad dada en un elemento del parámetro *priorities* se aplica a la textura denominada por el elemento correspondiente *del parámetro textures.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *n* era un valor negativo.<br/>                                                                                                  |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glPrioritizeTextures** asigna las *n* prioridades de textura especificadas en el parámetro *priorities* a *las n* texturas denominadas en el parámetro *textures.* En equipos con una cantidad limitada de memoria de textura, OpenGL establece un "espacio de trabajo" de texturas que residen en la memoria de textura. Estas texturas se pueden enlazar a un destino de textura de forma mucho más eficaz que las texturas que no residen.

Al especificar una prioridad para cada textura, la función **glPrioritizeTextures** permite determinar qué texturas deben ser residentes.

Los elementos de prioridades de textura *de las* prioridades se fijan en el \[ intervalo 0,0, 1,0 \] antes de asignarse. Cero indica la prioridad más baja; por lo tanto, es menos probable que las texturas con prioridad cero sean residentes. El valor 1.0 indica la prioridad más alta; por lo tanto, es más probable que las texturas con prioridad 1.0 sean residentes. Sin embargo, no se garantiza que las texturas sean residentes hasta que se enlazan.

La **función glPrioritizeTextures** omite los intentos de priorizar la textura 0 o cualquier nombre de textura que no se corresponda con una textura existente. Ninguna de las funciones denominadas por el parámetro *textures* debe enlazarse a un destino de textura.

Si una textura está enlazada actualmente, también puede usar la [**función glTexParameter**](gltexparameter-functions.md) para establecer su prioridad. Esta es la única manera de establecer la prioridad de una textura predeterminada.

Puede incluir **glPrioritizeTextures en** listas para mostrar.

La función siguiente recupera la prioridad de una textura enlazada actualmente relacionada con **glPrioritizeTextures**:

-   [**glGetTexParameter con el**](glgettexparameter.md) nombre de parámetro GL \_ TEXTURE \_ PRIORITY

> [!Note]  
> La **función glPrioritizeTextures** solo está disponible en OpenGL versión 1.1 o posterior.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
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

 

 





