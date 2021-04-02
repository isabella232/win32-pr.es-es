---
title: función glGenTextures (GL. h)
description: La función glGenTextures genera nombres de textura.
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- glGenTextures (función) OpenGL
topic_type:
- apiref
api_name:
- glGenTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204a5d4fb736a88cf615577f4c740cde15d75829
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997004"
---
# <a name="glgentextures-function"></a>glGenTextures función)

La función **glGenTextures** genera nombres de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGenTextures(
   GLsizei n,
   GLuint  *textures
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*n* 
</dt> <dd>

El número de nombres de textura que se van a generar.

</dd> <dt>

*texturas* 
</dt> <dd>

Puntero al primer elemento de una matriz en la que se almacenan los nombres de textura generados.

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

La función **glGenTextures** devuelve *n* nombres de textura en el parámetro *Textures* . Los nombres de las texturas no son necesariamente un conjunto contiguo de enteros; sin embargo, ninguno de los nombres devueltos se puede haber estado usando inmediatamente antes de llamar a la función **glGenTextures** . Las texturas generadas suponen la dimensionalidad del destino de textura al que se enlazan por primera vez con la función [**glBindTexture**](glbindtexture.md) . Los nombres de textura devueltos por **glGenTextures** no se devuelven en las llamadas subsiguientes a **glGenTextures** , a menos que se eliminen primero llamando a [**glDeleteTextures**](gldeletetextures.md).

No se puede incluir **glGenTextures** en las listas de visualización.

> [!Note]  
> La función **glGenTextures** solo está disponible en la versión 1,1 o posterior de OpenGL.

 

La siguiente función recupera información relacionada con **glGenTextures**:

-   [**glIsTexture**](glistexture.md)

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

[**glDeleteTextures**](gldeletetextures.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





