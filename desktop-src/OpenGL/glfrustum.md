---
title: Función glFrustum (Gl.h)
description: La función glFrustum multiplica la matriz actual por una matriz de perspectiva.
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- Función glFrustum OpenGL
topic_type:
- apiref
api_name:
- glFrustum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1ca2375206165576405c96528d0590596f4d4d870121f0a30884c8e448ca93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625271"
---
# <a name="glfrustum-function"></a>función glFrustum

La **función glFrustum** multiplica la matriz actual por una matriz de perspectiva.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glFrustum(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Izquierda* 
</dt> <dd>

Coordenada del plano de recorte vertical izquierdo.

</dd> <dt>

*Correcto* 
</dt> <dd>

Coordenada del plano de recorte vertical derecho.

</dd> <dt>

*Parte inferior* 
</dt> <dd>

Coordenada del plano de recorte horizontal inferior.

</dd> <dt>

*top* 
</dt> <dd>

Coordenada del plano de recorte horizontal inferior.

</dd> <dt>

*zNear* 
</dt> <dd>

Distancias al plano de recorte de profundidad cercana. Debe ser positivo.

</dd> <dt>

*zFar* 
</dt> <dd>

Distancias a los planos de recorte de profundidad lejana. Debe ser positivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *zNear* o *zFar* no era postitivo.<br/>                                                                                       |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glFrustum** describe una matriz de perspectiva que genera una proyección de perspectiva. Los *parámetros (* left , *bottom*, *zNear*) y (*right*, *top*, *zNear*) especifican los puntos del plano de recorte cercano que se asignan a las esquinas inferior izquierda y superior derecha de la ventana, respectivamente, suponiendo que el ojo se encuentra en (0,0,0). El *parámetro zFar* especifica la ubicación del plano de recorte lejano. Tanto *zNear* como *zFar* deben ser positivos. La matriz correspondiente se muestra en la siguiente imagen.

![Diagrama que muestra la matriz de perspectiva que genera una proyección de perspectiva.](images/frust01.png)![Ecuaciones que muestran la función glFrustum que describe una matriz de perspectiva.](images/frust02.png)

La **función glFrustum** multiplica la matriz actual por esta matriz, con el resultado reemplazando la matriz actual. Es decir, si M es la matriz actual y F es la matriz de perspectiva frustum, **glFrustum** reemplaza a M por M F.

Use [**glPushMatrix**](glpushmatrix.md) y [**glPopMatrix para**](glpopmatrix.md) guardar y restaurar la pila de matriz actual.

La precisión del búfer de profundidad se ve afectada por los valores especificados para *zNear* y *zFar*. Cuando mayor sea la proporción de *zFar* a *zNear,* menos eficaz será el búfer de profundidad para distinguir entre las superficies que están cerca unas de otras. Si

![Ecuación que muestra la proporción de lejos a cerca.](images/frust03.png)

se pierden *aproximadamente* 2 bits *(r)* de precisión del búfer de profundidad. Dado *que r* se aproxima al infinito a medida que *zNear* se aproxima a cero, nunca debe establecer *zNear* en cero.

Las siguientes funciones recuperan información sobre **glFrustum**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MATRIX \_ MODE

**glGet** con el argumento GL \_ MODELVIEW \_ MATRIX

**glGet con** el argumento GL \_ PROJECTION \_ MATRIX

**glGet con** el argumento GL \_ TEXTURE \_ MATRIX

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





