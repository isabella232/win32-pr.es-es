---
title: Función glAreTexturesResident (Gl.h)
description: La función glAreTexturesResident determina si los objetos de textura especificados residen en la memoria de textura.
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- Función glAreTexturesResident OpenGL
topic_type:
- apiref
api_name:
- glAreTexturesResident
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c503cac59bbec912c535120161d27991118dab818a185c1f39d8f48cb2a5939
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082245"
---
# <a name="glaretexturesresident-function"></a>Función glAreTexturesResident

La **función glAreTexturesResident** determina si los objetos de textura especificados residen en la memoria de textura.

## <a name="syntax"></a>Sintaxis


```C++
GLboolean WINAPI glAreTexturesResident(
         GLsizei   n,
   const GLuint    *textures,
         GLboolean *residences
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*n* 
</dt> <dd>

Número de texturas que se consultarán.

</dd> <dt>

*Texturas* 
</dt> <dd>

Dirección de una matriz que contiene los nombres de las texturas que se consultarán.

</dd> <dt>

*Residencias* 
</dt> <dd>

Dirección de una matriz en la que se devuelve el estado de la residencia de textura. El estado de residencia de una textura denominada por un elemento de *texturas* se devuelve en el elemento correspondiente de *residencias*.

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *n* era un valor negativo, un elemento de *texturas* era cero o un elemento de *texturas* no contenía un identificador de textura.<br/> |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/>     |



## <a name="remarks"></a>Comentarios

En máquinas con una cantidad limitada de memoria de textura, OpenGL establece un conjunto de trabajo de texturas que residen en la memoria de textura. Estas texturas se pueden enlazar a un destino de textura de forma mucho más eficaz que las texturas que no son residentes.

La **función glAreTexturesResident** consulta el estado de la textura de las *n* texturas denominadas por los elementos de *texturas*. Si todas las texturas con nombre residen, **glAreTexturesResident** devuelve GL TRUE y el contenido de las \_ *residencias* no está alterado. Si alguna de las texturas con nombre no es residentes, **glAreTexturesResident** devuelve GL FALSE y se devuelve el estado detallado en los n elementos \_ de las *residencias*. 

Si un elemento de *residencias* es GL TRUE, la textura denominada por el elemento correspondiente de \_ *texturas* se encuentra en la memoria de textura.

Para consultar el estado de residencia de una textura  enlazada única, llame a [**glGetTexParameter**](glgettexparameter.md) con el parámetro de destino establecido en la textura de destino a la que está enlazado el destino y establezca el parámetro *pname* en GL \_ TEXTURE \_ RESIDENT. Debe usar este método para consultar el estado de residencia de una textura predeterminada.

No puede incluir **glAreTexturesResident en** listas para mostrar.

La **función glAreTexturesResident** devuelve el estado de residencia de las texturas en el momento de la invocación. No garantiza que las texturas permanezcan residentes en cualquier otro momento.

Si las texturas residen en memoria virtual (no hay memoria de textura), se consideran siempre residentes.

> [!Note]  
> La **función glAreTexturesResident** solo está disponible en OpenGL versión 1.1 o posterior.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





