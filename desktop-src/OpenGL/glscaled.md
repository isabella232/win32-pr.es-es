---
title: Función glScaled (Gl.h)
description: Las funciones glScaled y glScalef multiplican la matriz actual por una matriz de escalado general. | Función glScaled (Gl.h)
ms.assetid: 3846289f-5c7b-4bb6-95a8-90a58dd8b9d9
keywords:
- Función glScaled OpenGL
topic_type:
- apiref
api_name:
- glScaled
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46742831eaa0a014de0f6ae50271b28c922893133588758119cbf5bff7ba628b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491795"
---
# <a name="glscaled-function"></a>Función glScaled

Las **funciones glScaled** y [**glScalef**](glscalef.md) multiplican la matriz actual por una matriz de escalado general.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glScaled(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* 
</dt> <dd>

Factores de escala a lo largo *del eje X.*

</dd> <dt>

*y* 
</dt> <dd>

Factores de escala a lo largo *del eje y.*

</dd> <dt>

*Z* 
</dt> <dd>

Factores de escala a lo largo *del eje Z.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glScaled** genera un escalado general a lo largo de los *ejes x*, *y* y *z.* Los tres argumentos indican los factores de escala deseados a lo largo de cada uno de los tres ejes. La matriz resultante es

![Diagrama que muestra la matriz de factores de escala a lo largo de los ejes x, y y z.](images/scale01.png)

La matriz actual [**(vea glMatrixMode)**](glmatrixmode.md)se multiplica por esta matriz de escala, con el producto reemplazando la matriz actual. Es decir, si M es la matriz actual y S es la matriz de escala, M se reemplaza por M S.

Si el modo de matriz es GL MODELVIEW o GL PROJECTION, se escalan todos los objetos dibujados después de llamar a \_ \_ **glScaled.** Use [**glPushMatrix**](glpushmatrix.md) y [**glPopMatrix para**](glpopmatrix.md) guardar y restaurar el sistema de coordenadas sin escalar.

Si se aplican factores de escala distintos de 1.0 a la matriz modelview y la iluminación está habilitada, es probable que también se habilite la normalización automática de normales [**(glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento GL \_ NORMALIZE).

Las siguientes funciones recuperan información relacionada **con glScaled**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MATRIX \_ MODE

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MODELVIEW \_ MATRIX

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ PROJECTION \_ MATRIX

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ TEXTURE \_ MATRIX

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

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotated**](glrotated.md)
</dt> <dt>

[**glRotatef**](glrotatef.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





