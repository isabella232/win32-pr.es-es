---
title: Función glClipPlane (Gl.h)
description: La función glClipPlane especifica un plano en el que se recorta toda la geometría.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- Función glClipPlane OpenGL
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
ms.openlocfilehash: cb55edd88b8c8dcd6b4481e60dfc05a012bb79f4f484fde8987e9ed23239d837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618045"
---
# <a name="glclipplane-function"></a>Función glClipPlane

La **función glClipPlane** especifica un plano en el que se recorta toda la geometría.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*avión* 
</dt> <dd>

Plano de recorte que se está colocando. Se aceptan nombres simbólicos con el formato GL CLIP PLANE i , donde i es un entero entre 0 y \_ GL MAX CLIP PLANES - \_   \_ \_ \_ 1.

</dd> <dt>

*Ecuación* 
</dt> <dd>

Dirección de una matriz de cuatro valores de punto flotante de precisión doble. Estos valores se interpretan como una ecuación de plano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *plane* no era un valor aceptado.<br/>                                                                                         |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La geometría siempre se recorta en los límites de un frustum de seis planos *en x*, *y* y *z.* La **función glClipPlane** permite la especificación de planos adicionales, no necesariamente a los ejes *x,* *y o* *z,* en los que se recorta toda la geometría. Se pueden especificar hasta 6 planos de GL MAX CLIP PLANES, donde GL MAX CLIP PLANES es al menos seis \_ \_ en todas las \_ \_ \_ \_ implementaciones. Dado que la región de recorte resultante es la intersección de los espacios medio definidos, siempre es convexa.

La **función glClipPlane** especifica un espacio medio mediante una ecuación de plano de cuatro componentes. Cuando se llama **a glClipPlane**,*la* ecuación se transforma mediante el inverso de la matriz modelview y se almacena en las coordenadas de los ojos resultantes. Los cambios posteriores en la matriz modelview no tienen ningún efecto en los componentes almacenados de ecuación de plano. Si el producto de puntos de las coordenadas de los ojos de un vértice con los componentes de ecuación del plano almacenados es positivo o cero, el vértice está en con respecto a ese plano de recorte. De lo contrario, está fuera.

Use las [**funciones glEnable**](glenable.md) [**y glDisable**](gldisable.md) para habilitar y deshabilitar los planos de recorte. Llame a planos de recorte con el argumento GL \_ CLIP \_ PLANE *i*, donde *i* es el número de plano.

De forma predeterminada, todos los planos de recorte se definen como (0,0,0,0) en coordenadas de los ojos y están deshabilitados.

Siempre es el caso de GL \_ CLIP \_ PLANE *i* = GL \_ CLIP \_ PLANE0 + *i*.

Las siguientes funciones recuperan información relacionada con **glClipPlane**:

[**glGetClipPlane**](glgetclipplane.md)

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ CLIP PLANE \_ *i*

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

 

 





