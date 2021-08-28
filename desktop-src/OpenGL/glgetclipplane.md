---
title: Función glGetClipPlane (Gl.h)
description: La función glGetClipPlane devuelve los coeficientes del plano de recorte especificado.
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- Función glGetClipPlane OpenGL
topic_type:
- apiref
api_name:
- glGetClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf551356088db2b99b79a28a396be785ab60f2196cc3e27353cb867d4b151dd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742045"
---
# <a name="glgetclipplane-function"></a>Función glGetClipPlane

La **función glGetClipPlane** devuelve los coeficientes del plano de recorte especificado.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*avión* 
</dt> <dd>

Plano de recorte. El número de planos de recorte depende de la implementación, pero se admiten al menos seis planos de recorte. Se identifican mediante nombres simbólicos con el formato GL CLIP PLANE i, donde \_ \_ 0 = i *<* GL MAX CLIP  \_ \_ \_ PLANES.

</dd> <dt>

*Ecuación* 
</dt> <dd>

Devuelve cuatro valores de precisión doble que son los coeficientes de la ecuación de plano del *plano en* coordenadas de los ojos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *plane* no era un valor aceptado.<br/>                                                                                         |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glGetClipPlane** devuelve *en* ecuación los cuatro coeficientes de la ecuación de plano para *el plano*.

Siempre es el caso de GL \_ CLIP \_ PLANE *i* = GL \_ CLIP \_ PLANE0 + *i*.

Si se genera un error, no se realiza ningún cambio en el contenido de la *ecuación*.

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

[**glClipPlane**](glclipplane.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





