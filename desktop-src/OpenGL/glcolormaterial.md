---
title: función glColorMaterial (GL. h)
description: La función glColorMaterial hace que un color material realice un seguimiento del color actual.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- glColorMaterial (función) OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32823eaa82e6a260790dd6fa23747f2b4228649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422395"
---
# <a name="glcolormaterial-function"></a>glColorMaterial función)

La función **glColorMaterial** hace que un color material realice un seguimiento del color actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Portada* 
</dt> <dd>

Especifica si los parámetros de material delantero, trasero o ambos deben realizar un seguimiento del color actual. Los valores aceptados son el \_ front-end de contab \_ \_ \_ \_ . El valor predeterminado es GL \_ Front \_ y \_ back.

</dd> <dt>

*mode* 
</dt> <dd>

Especifica cuál de los diversos parámetros de material realiza un seguimiento del color actual. Los valores aceptados son \_ emisión de contabilidad, ambiente de contabilidad general \_ , difusión de contab \_ \_ \_ \_ \_ . El valor predeterminado es \_ ambiente \_ de contabilidad y \_ difuso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | la *esfera* o el *modo* no era un valor aceptado.<br/>                                                                                |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glColorMaterial** especifica qué parámetros de material hacen un seguimiento del color actual. Cuando se habilita \_ el material de color GL \_ , para cada uno de los materiales especificados por la *esfera*, el parámetro de material o los parámetros especificados por el *modo* realizan el seguimiento del color actual en todo momento. Habilitar y deshabilitar \_ \_ el material de color de GL con las funciones [**glEnable**](glenable.md) y [**glDisable**](gldisable.md), que se llama con el material de \_ color GL \_ como su argumento. De forma predeterminada, el \_ material de color GL \_ está deshabilitado.

Con **glColorMaterial**, puede cambiar un subconjunto de parámetros de material para cada vértice usando solo la función [**glColor**](glcolor-functions.md) , sin llamar a [**glMaterial**](glmaterial-functions.md). Si va a especificar solo este tipo de subconjunto de parámetros para cada vértice, es mejor hacerlo con **glColorMaterial** que con **glMaterial**.

Las siguientes funciones recuperan información relacionada con **glColorMaterial**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ parámetro de \_ material de color GL de argument \_

**glGet** con el argumento del \_ material de color de GL \_ \_

[**glIsEnabled**](glisenabled.md) con el argumento \_ material de color GL \_

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





