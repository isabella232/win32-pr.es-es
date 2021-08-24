---
title: Función glGenTextures (Gl.h)
description: La función glGenTextures genera nombres de textura.
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- Función glGenTextures OpenGL
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
ms.openlocfilehash: b28275bef054b26c2145ab9779ec776297ac7838d0313769123fb1be904a3bd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625235"
---
# <a name="glgentextures-function"></a>Función glGenTextures

La **función glGenTextures** genera nombres de textura.

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

Número de nombres de textura que se generarán.

</dd> <dt>

*Texturas* 
</dt> <dd>

Puntero al primer elemento de una matriz en la que se almacenan los nombres de textura generados.

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

La **función glGenTextures** devuelve *n nombres* de textura en el parámetro *textures.* Los nombres de textura no son necesariamente un conjunto contiguo de enteros, pero ninguno de los nombres devueltos puede haber estado en uso inmediatamente antes de llamar a la **función glGenTextures.** Las texturas generadas asumen la dimensionalidad del destino de textura al que se enlazan primero con la [**función glBindTexture.**](glbindtexture.md) Las llamadas posteriores a **glGenTextures** no devuelven nombres de textura devueltos por **glGenTextures** a menos que se eliminen primero mediante una llamada [**a glDeleteTextures**](gldeletetextures.md).

No se puede **incluir glGenTextures en** las listas para mostrar.

> [!Note]  
> La **función glGenTextures** solo está disponible en OpenGL versión 1.1 o posterior.

 

La función siguiente recupera información relacionada con **glGenTextures**:

-   [**glIsTexture**](glistexture.md)

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

 

 





