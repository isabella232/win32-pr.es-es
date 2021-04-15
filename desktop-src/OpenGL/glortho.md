---
title: función glOrtho (GL. h)
description: La función glOrtho multiplica la matriz actual por una matriz ortográfica.
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- glOrtho (función) OpenGL
topic_type:
- apiref
api_name:
- glOrtho
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46abbb0edd2dfc7fc51aaf7fa6519dc5367b109c
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104569741"
---
# <a name="glortho-function"></a>glOrtho función)

La función **glOrtho** multiplica la matriz actual por una matriz ortográfica.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glOrtho(
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

Coordenadas del plano de recorte vertical izquierdo.

</dd> <dt>

*correcta* 
</dt> <dd>

Coordenadas del plano de recorte vertical derecho.

</dd> <dt>

*descendente* 
</dt> <dd>

Coordenadas del plano de recorte horizontal inferior.

</dd> <dt>

*top* 
</dt> <dd>

Coordenadas para los planes de recorte horizontal superior.

</dd> <dt>

*zNear* 
</dt> <dd>

Las distancias al plano de recorte de profundidad más cercana. Esta distancia es negativa si el plano va a estar detrás del visor.

</dd> <dt>

*zFar* 
</dt> <dd>

Las distancias al plano de recorte de profundidad más lejano. Esta distancia es negativa si el plano va a estar detrás del visor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glOrtho** describe una matriz de perspectiva que genera una proyección paralela. Los parámetros (*izquierda*, *inferior*, *Near*) y (*derecho*, *superior*, *Near*) especifican los puntos del plano de recorte cercano que se asignan a las esquinas inferior izquierda y superior derecha de la ventana, respectivamente, suponiendo que el ojo está ubicado en (0,0). El parámetro *Far* especifica la ubicación del plano de recorte lejano. Tanto *zNear* como *zFar* pueden ser positivos o negativos. La matriz correspondiente se muestra en la siguiente imagen.

![Diagrama que muestra la matriz de perspectiva que describe la función glOrtho.](images/ortho1.png)

where

![Ecuaciones que describen la matriz de perspectiva.](images/ortho2.png)

Esta matriz multiplica la matriz actual con el resultado que reemplaza la matriz actual. Es decir, si M es la matriz actual y O es la matriz Ortho, M se reemplaza por M O.

Use [**glPushMatrix**](glpushmatrix.md) y **glPopMatrix** para guardar y restaurar la pila de matriz actual. Use [**glMatrixMode**](glmatrixmode.md) para establecer la matriz actual.

Las siguientes funciones recuperan información relacionada con **glOrtho**:

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





