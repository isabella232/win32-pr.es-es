---
title: función glClipPlane (GL. h)
description: La función glClipPlane especifica un plano en el que se recorta todo el objeto Geometry.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- glClipPlane (función) OpenGL
topic_type:
- apiref
api_name:
- glClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33380203b30b7a3a2e37ee5d58a47fec845cbc1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686044"
---
# <a name="glclipplane-function"></a>glClipPlane función)

La función **glClipPlane** especifica un plano en el que se recorta todo el objeto Geometry.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*plano* 
</dt> <dd>

Plano de recorte que se está colocando. Los nombres simbólicos del formulario de clip de contab \_ \_ .*i*, donde *i* es un entero entre 0 y el \_ número máximo \_ \_ de planos de clips-1, se aceptan.

</dd> <dt>

*ecuación* 
</dt> <dd>

Dirección de una matriz de cuatro valores de punto flotante de precisión doble. Estos valores se interpretan como una ecuación de plano.

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

Geometry siempre se recorta con respecto a los límites de un frustum de seis planos en *x*, *y* y *z*. La función **glClipPlane** permite la especificación de planos adicionales, no necesariamente perpendiculares al eje *x*, eje *y*, o eje *z*, en el que se recortan todas las geometrías. Se \_ pueden especificar los planos de planos de recortes hasta un máximo de GL \_ \_ , donde \_ los planos de clip Max de GL \_ \_ son al menos seis en todas las implementaciones. Dado que la región de recorte resultante es la intersección de los semiespacios definidos, siempre es convexa.

La función **glClipPlane** especifica un medio de espacio mediante una ecuación de plano de cuatro componentes. Cuando se llama a **glClipPlane**, la *ecuación* se transforma por el inverso de la matriz MODELVIEW y se almacena en las coordenadas de ojo resultantes. Los cambios subsiguientes en la matriz MODELVIEW no tienen ningún efecto en los componentes de la ecuación de plano almacenados. Si el producto del punto de las coordenadas del ojo de un vértice con los componentes de la ecuación de plano almacenado es positivo o cero, el vértice está en con respecto a ese plano de recorte. De lo contrario, está fuera.

Use las funciones [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) para habilitar y deshabilitar los planos de recorte. Llame a los planos de recorte con el argumento GL \_ clip \_ plano *i*, donde *i* es el número de plano.

De forma predeterminada, todos los planos de recorte se definen como (0, 0, 0, 0) en las coordenadas de ojo y están deshabilitados.

Siempre es el caso de que el \_ plano de clip GL \_ *i* = \_ recorte de GL \_ PLANE0 + *i*.

Las siguientes funciones recuperan información relacionada con **glClipPlane**:

[**glGetClipPlane**](glgetclipplane.md)

[**glIsEnabled**](glisenabled.md) con el argumento \_ plano de clip de contabilidad \_ 

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

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





