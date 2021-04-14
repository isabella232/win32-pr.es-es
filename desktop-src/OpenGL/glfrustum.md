---
title: función glFrustum (GL. h)
description: La función glFrustum multiplica la matriz actual por una matriz de perspectiva.
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- glFrustum (función) OpenGL
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
ms.openlocfilehash: ce67879ca20819713e61a9392bf77be2f15211d5
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104565625"
---
# <a name="glfrustum-function"></a>glFrustum función)

La función **glFrustum** multiplica la matriz actual por una matriz de perspectiva.

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

*salido* 
</dt> <dd>

La coordenada del plano de recorte izquierdo-vertical.

</dd> <dt>

*correcta* 
</dt> <dd>

Coordenada del plano de recorte vertical derecha.

</dd> <dt>

*descendente* 
</dt> <dd>

Coordenada del plano de recorte horizontal inferior.

</dd> <dt>

*top* 
</dt> <dd>

Coordenada del plano de recorte horizontal inferior.

</dd> <dt>

*zNear* 
</dt> <dd>

Distancias al plano de recorte más profundo. Debe ser positivo.

</dd> <dt>

*zFar* 
</dt> <dd>

Las distancias a los planos de recorte de profundidad. Debe ser positivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *zNear* o *zFar* no postitive.<br/>                                                                                       |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glFrustum** describe una matriz de perspectiva que genera una proyección en perspectiva. Los parámetros (*left*, *Bottom*, *zNear*) y (*right*, *Top*, *zNear*) especifican los puntos del plano de recorte cercano que se asignan a las esquinas inferior izquierda y superior derecha de la ventana, respectivamente, suponiendo que el ojo está ubicado en (0,0). El parámetro *zFar* especifica la ubicación del plano de recorte lejano. Tanto *zNear* como *zFar* deben ser positivos. La matriz correspondiente se muestra en la siguiente imagen.

![Diagrama que muestra la matriz de perspectiva que genera una proyección en perspectiva.](images/frust01.png)![Ecuaciones que muestran la función glFrustum que describe una matriz de perspectiva.](images/frust02.png)

La función **glFrustum** multiplica la matriz actual por esta matriz, con el resultado que reemplaza la matriz actual. Es decir, si M es la matriz actual y F es la matriz de perspectiva del frustum, **glFrustum** reemplaza a M por m F.

Use [**glPushMatrix**](glpushmatrix.md) y [**glPopMatrix**](glpopmatrix.md) para guardar y restaurar la pila de matriz actual.

La precisión del búfer de profundidad se ve afectada por los valores especificados para *zNear* y *zFar*. Cuanto mayor sea la relación de *zFar* con *zNear* , más eficaz será el búfer de profundidad a la distinción entre superficies que están cerca unas de otras. Si

![Ecuación que muestra la relación de lejos a near.](images/frust03.png)

se pierden aproximadamente los bits de *registro* 2 (*r*) de la precisión del búfer de profundidad. Dado que *r* se aproxima al infinito como *zNear* se aproxima a cero, nunca debe establecer *zNear* en cero.

Las siguientes funciones recuperan información sobre **glFrustum**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_

**glGet** con el argumento \_ MODELVIEW \_ matriz de contabilidad

**glGet** con el argumento \_ matriz de proyección de contabilidad \_

**glGet** con el argumento \_ matriz de textura de GL \_

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

 

 





