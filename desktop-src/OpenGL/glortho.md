---
title: Función glOrtho (Gl.h)
description: La función glOrtho multiplica la matriz actual por una matriz ortográfica.
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- Función glOrtho OpenGL
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
ms.openlocfilehash: b1e06c1740e908c34652a6d39bc7a2334763199d222ff9d1dc00ae733803ada0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795237"
---
# <a name="glortho-function"></a>función glOrtho

La **función glOrtho** multiplica la matriz actual por una matriz ortográfica.

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

*Izquierda* 
</dt> <dd>

Coordenadas del plano de recorte vertical izquierdo.

</dd> <dt>

*Correcto* 
</dt> <dd>

Coordenadas del plano de recorte vertical derecho.

</dd> <dt>

*Parte inferior* 
</dt> <dd>

Coordenadas del plano de recorte horizontal inferior.

</dd> <dt>

*top* 
</dt> <dd>

Coordenadas de los planes de recorte horizontales superiores.

</dd> <dt>

*zNear* 
</dt> <dd>

Distancias al plano de recorte de profundidad más cercano. Esta distancia es negativa si el plano va a estar detrás del visor.

</dd> <dt>

*zFar* 
</dt> <dd>

Distancias al plano de recorte de profundidad más alejado. Esta distancia es negativa si el plano va a estar detrás del visor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glOrtho** describe una matriz de perspectiva que genera una proyección paralela. Los *parámetros (* left , *bottom*, *near*) y (*right*, *top*, *near*) especifican los puntos del plano de recorte cercano que se asignan a las esquinas inferior izquierda y superior derecha de la ventana, respectivamente, suponiendo que el ojo se encuentra en (0, 0, 0). El *parámetro far* especifica la ubicación del plano de recorte lejano. Tanto *zNear* como *zFar* pueden ser positivos o negativos. La matriz correspondiente se muestra en la siguiente imagen.

![Diagrama que muestra la matriz de perspectiva que describe la función glOrtho.](images/ortho1.png)

where

![Ecuaciones que describen la matriz de perspectiva.](images/ortho2.png)

La matriz actual se multiplica por esta matriz con el resultado reemplazando la matriz actual. Es decir, si M es la matriz actual y O es la matriz de ortos, M se reemplaza por M O.

Use [**glPushMatrix**](glpushmatrix.md) y **glPopMatrix para** guardar y restaurar la pila de matriz actual. Use [**glMatrixMode para**](glmatrixmode.md) establecer la matriz actual.

Las siguientes funciones recuperan información relacionada con **glOrtho**:

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

 

 





