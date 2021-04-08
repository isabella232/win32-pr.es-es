---
title: función glCullFace (GL. h)
description: La función glCullFace especifica si se pueden seleccionar las caras con conexión frontal o hacia delante.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- glCullFace (función) OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c20370e0fa8bcf746d1b835ee45725f76158fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996043"
---
# <a name="glcullface-function"></a>glCullFace función)

La función **glCullFace** especifica si se pueden seleccionar las caras con conexión frontal o hacia delante.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* 
</dt> <dd>

Especifica si las caras delanteras o las orientadas hacia atrás son candidatas para la selección. Se aceptan las constantes simbólicas GL \_ Front, GL \_ back y GL \_ Front \_ y \_ back. El valor predeterminado es GL \_ .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *modo* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glCullFace** especifica si se seleccionan las facetas con conexión frontal o hacia delante (como se especifica en el *modo*) cuando está habilitada la selección de facetas. Puede habilitar y deshabilitar la selección de facetas mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento de la cara de selección de contabilidad \_ \_ . Las caras incluyen triángulos, quadrilaterals, polígonos y rectángulos.

La función [**glFrontFace**](glfrontface.md) especifica cuál de las caras en el sentido de las agujas del reloj y en el sentido de las agujas del reloj está orientada hacia delante y hacia atrás.

Si el *modo* es de \_ primer plano \_ y \_ viceversa, no se dibujan las caras, pero se dibujan otras primitivas, como puntos y líneas.

Las siguientes funciones recuperan información relacionada con **glCullFace**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de \_ cara de selección de libro de contabilidad \_

[**glIsEnabled**](glisenabled.md) con el argumento de la cara de selección de contabilidad \_ \_

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFrontFace**](glfrontface.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





