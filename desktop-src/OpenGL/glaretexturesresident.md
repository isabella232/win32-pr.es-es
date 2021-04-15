---
title: función glAreTexturesResident (GL. h)
description: La función glAreTexturesResident determina si los objetos de textura especificados están residentes en la memoria de textura.
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- glAreTexturesResident (función) OpenGL
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
ms.openlocfilehash: 8e2e7e5965da9604c690384301de6f1879a98994
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676787"
---
# <a name="glaretexturesresident-function"></a>glAreTexturesResident función)

La función **glAreTexturesResident** determina si los objetos de textura especificados están residentes en la memoria de textura.

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

Número de texturas que se van a consultar.

</dd> <dt>

*texturas* 
</dt> <dd>

Dirección de una matriz que contiene los nombres de las texturas que se van a consultar.

</dd> <dt>

*residencias* 
</dt> <dd>

Dirección de una matriz en la que se devuelve el estado de residencia de la textura. El estado de residencia de una textura denominada por un elemento de *texturas* se devuelve en el elemento de *residencias* correspondiente.

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *n* era un valor negativo, un elemento en las *texturas* era cero o un elemento de las *texturas* no contenía un identificador de textura.<br/> |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/>     |



## <a name="remarks"></a>Observaciones

En los equipos con una cantidad limitada de memoria de textura, OpenGL establece un conjunto de trabajo de texturas que residen en la memoria de textura. Estas texturas se pueden enlazar a un destino de textura mucho más eficaz que las texturas que no son residentes.

La función **glAreTexturesResident** consulta el estado de residencia de la textura de las *n* texturas nombradas por los elementos de las *texturas*. Si todas las texturas con nombre son residentes, **glAreTexturesResident** devuelve GL \_ true y el contenido de *residencias* no se ve afectado. Si alguna de las texturas con nombre no es residente, **glAreTexturesResident** devuelve GL \_ false y se devuelve el estado detallado en los *n* elementos de *residencias*.

Si un elemento de *residencias* es un \_ valor de GL, la textura denominada por el elemento de *texturas* correspondiente se encuentra residente en la memoria de textura.

Para consultar el estado de residencia de una sola textura enlazada, llame a [**glGetTexParameter**](glgettexparameter.md) con el parámetro de *destino* establecido en la textura de destino a la que está enlazado el destino y establezca el parámetro *PName* en residente de textura de contabilidad \_ \_ . Debe utilizar este método para consultar el estado residente de una textura predeterminada.

No se puede incluir **glAreTexturesResident** en las listas de visualización.

La función **glAreTexturesResident** devuelve el estado de residencia de las texturas en el momento de la invocación. No garantiza que las texturas seguirán siendo residentes en cualquier otro momento.

Si las texturas residen en la memoria virtual (no hay memoria de textura), se consideran siempre residentes.

> [!Note]  
> La función **glAreTexturesResident** solo está disponible en la versión 1,1 o posterior de OpenGL.

 

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

 

 





