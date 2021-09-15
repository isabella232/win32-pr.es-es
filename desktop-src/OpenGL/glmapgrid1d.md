---
title: Función glMapGrid1d (Gl.h)
description: Define una malla unidimensional. | Función glMapGrid1d (Gl.h)
ms.assetid: a0bc822e-dd98-4586-a322-2779e11f38ca
keywords:
- Función glMapGrid1d OpenGL
topic_type:
- apiref
api_name:
- glMapGrid1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b1900f5597e8c516100504ca7288137ed99ded
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272039"
---
# <a name="glmapgrid1d-function"></a>Función glMapGrid1d

Define una malla unidimensional.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glMapGrid1d(
   GLint    un,
   GLdouble u1,
   GLdouble u2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*un* 
</dt> <dd>

Número de particiones en el intervalo de intervalo de cuadrícula \[ u1, u2 \] . Este valor debe ser positivo.

</dd> <dt>

*u1* 
</dt> <dd>

Valor que se usa como asignación para el valor de dominio de cuadrícula de enteros i = 0.

</dd> <dt>

*u2* 
</dt> <dd>

Valor que se usa como asignación para el valor de dominio de cuadrícula de enteros i = un.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | Un *o* *vn no* fueron positivos.<br/>                                                                                      |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Use las **funciones glMapGrid** y [glEvalMesh](glevalmesh-functions.md) juntos para generar y evaluar eficazmente una serie de valores de dominio de mapa espaciados uniformemente. La función glEvalMesh pasa por el dominio entero de una cuadrícula unidimensional o bidimensional, cuyo intervalo es el dominio de los mapas de evaluación especificados por [**glMap1**](glmap1.md) y [**glMap2.**](glmap2.md)

Las **funciones glMapGrid1** y [**glMapGrid2**](glmapgrid2d.md) especifican las asignaciones de cuadrícula lineal entre las coordenadas de cuadrícula de enteros i (o i y j), a las coordenadas del mapa de evaluación de punto flotante u (o usted y v). Consulte [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md) para obtener más información sobre cómo se evalúan las coordenadas v y usted.

La **función glMapGrid1** especifica una asignación lineal única, de modo que la  coordenada de cuadrícula de enteros 0 se asigna exactamente a u1 y la coordenada de cuadrícula de enteros se asigna exactamente a *u2.* Todas las demás coordenadas de cuadrícula *de enteros i* se asignan de forma que:

*u = i(u2 u1)/un + u1*

La [**función glMapGrid2**](glmapgrid2d.md) especifica dos asignaciones lineales de este tipo. Una asigna la coordenada de cuadrícula *de enteros i = 0* exactamente *a u1* y la coordenada de cuadrícula de *enteros i = un* exactamente a *u2*. El otro asigna la coordenada de cuadrícula de *enteros j = 0* exactamente *a v1* y la coordenada de cuadrícula de *enteros j = vn* exactamente a *v2*. Otras coordenadas de cuadrícula de enteros i y j se asignan de forma que

*u = i(u2 u1)/un + u1*

*v = j (v2 v1)/vn + v1*

[GlEvalMesh](glevalmesh-functions.md) y [**glEvalPoint**](glevalpoint.md)usan de forma idéntica las asignaciones especificadas por **glMapGrid.**

Las funciones siguientes recuperan información relacionada **con glMapGrid**:

<dl>

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAP1 \_ GRID \_ DOMAIN  
[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAP2 \_ GRID \_ DOMAIN  
[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAP1 \_ GRID \_ SEGMENTS  
[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAP2 \_ GRID \_ SEGMENTS  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[glEvalMesh](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





