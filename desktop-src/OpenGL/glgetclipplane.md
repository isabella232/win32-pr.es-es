---
title: función glGetClipPlane (GL. h)
description: La función glGetClipPlane devuelve los coeficientes del plano de recorte especificado.
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- glGetClipPlane (función) OpenGL
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
ms.openlocfilehash: 5b3e29d730c09bcc7c2b12082116e174cb39eb74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686251"
---
# <a name="glgetclipplane-function"></a>glGetClipPlane función)

La función **glGetClipPlane** devuelve los coeficientes del plano de recorte especificado.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*plano* 
</dt> <dd>

Plano de recorte. El número de planos de recorte depende de la implementación, pero se admiten al menos seis planos de recorte. Se identifican por nombres simbólicos con el formato libro de clips de contabilidad \_ \_ *i* , donde 0 = *i* < \_ planos de \_ recortes de contab \_ .

</dd> <dt>

*ecuación* 
</dt> <dd>

Devuelve cuatro valores de precisión doble que son los coeficientes de la ecuación de plano de *plano* en coordenadas de ojo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *plano* no era un valor aceptado.<br/>                                                                                         |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glGetClipPlane** devuelve en la *ecuación* los cuatro coeficientes de la ecuación del plano para el *plano*.

Siempre es el caso de que el \_ plano de clip GL \_ *i* = \_ recorte de GL \_ PLANE0 + *i*.

Si se genera un error, no se realiza ningún cambio en el contenido de la *ecuación*.

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

[**glClipPlane**](glclipplane.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





