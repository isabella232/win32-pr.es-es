---
title: Función glIsTexture (Gl.h)
description: La función glIsTexture determina si un nombre corresponde a una textura.
ms.assetid: 89d06642-ff28-4a67-ac7f-ca58150f301e
keywords:
- Función glIsTexture OpenGL
topic_type:
- apiref
api_name:
- glIsTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8897cc0eb004da701f28b410f2ca28b6194c9d26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074039"
---
# <a name="glistexture-function"></a>Función glIsTexture

La **función glIsTexture** determina si un nombre corresponde a una textura.

## <a name="syntax"></a>Sintaxis


```C++
GLboolean WINAPI glIsTexture(
   GLuint texture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Textura* 
</dt> <dd>

Valor que es el nombre de una textura.

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Si el *parámetro texture* es actualmente el nombre de una textura, la **función glIsTexture** devuelve GL \_ TRUE. La **función glIsTexture** devuelve GL \_ FALSE si la *textura* es cero. También devuelve GL FALSE si es un valor distinto de cero que no es actualmente el nombre de una textura o si \_ se produce un error.

No se pueden incluir llamadas **a glIsTexture en** listas para mostrar.

> [!Note]  
> La **función glIsTexture** solo está disponible en OpenGL versión 1.1 o posterior.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenTextures**](glgentextures.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





