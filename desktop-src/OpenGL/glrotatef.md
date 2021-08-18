---
title: Función glRotatef (Gl.h)
description: La función glRotatef multiplica la matriz actual por una matriz de rotación.
ms.assetid: 8216a125-de8c-44e5-afb3-3d4e5ffc600d
keywords:
- Función glRotatef OpenGL
topic_type:
- apiref
api_name:
- glRotatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f466ca73a826d9a12f97093c90c41cd1c753b01f25853096dd3f3219628654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937935"
---
# <a name="glrotatef-function"></a>función glRotatef

La **función glRotatef** multiplica la matriz actual por una matriz de rotación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glRotatef(
   GLfloat angle,
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*angle* 
</dt> <dd>

Ángulo de rotación, en grados.

</dd> <dt>

*x* 
</dt> <dd>

*Coordenada x* de un vector.

</dd> <dt>

*y* 
</dt> <dd>

*Coordenada y* de un vector.

</dd> <dt>

*Z* 
</dt> <dd>

*Coordenada z* de un vector.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glRotatef** calcula una matriz que realiza  una rotación en sentido contrario a las agujas del reloj de grados angulares sobre el vector desde el origen hasta el punto (*x*, *y*, *z*).

La matriz actual [**(vea glMatrixMode**](glmatrixmode.md)) se multiplica por esta matriz de rotación, con el producto reemplazando la matriz actual. Es decir, si M es la matriz actual y R es la matriz de traducción, M se reemplaza por M R.

Si el modo de matriz es GL MODELVIEW o GL PROJECTION, se giran todos los objetos dibujados después de llamar a \_ \_ **glRotatef.** Use [**glPushMatrix**](glpushmatrix.md) y [**glPopMatrix para**](glpopmatrix.md) guardar y restaurar el sistema de coordenadas sin cargar.

Las siguientes funciones recuperan información relacionada **con glRotatef**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ RENDER \_ MODE

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MATRIX \_ MODE

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MODELVIEW \_ MATRIX

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

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





