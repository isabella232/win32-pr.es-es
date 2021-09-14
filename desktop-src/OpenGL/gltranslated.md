---
title: Función glTranslated (Gl.h)
description: La función glTranslated multiplica la matriz actual por una matriz de traducción.
ms.assetid: 9f066a92-ee78-44d1-b8f8-0eacde0e1a47
keywords:
- función glTranslated OpenGL
topic_type:
- apiref
api_name:
- glTranslated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705c8dd0635294b066897db99c0770b5f6622c75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071494"
---
# <a name="gltranslated-function"></a>función glTranslated

La **función glTranslated** multiplica la matriz actual por una matriz de traducción.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTranslated(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* 
</dt> <dd>

*Coordenada x* de un vector de traducción.

</dd> <dt>

*y* 
</dt> <dd>

*Coordenada y* de un vector de traducción.

</dd> <dt>

*Z* 
</dt> <dd>

*Coordenada z* de un vector de traducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La **función glTranslated** genera la traducción especificada por (*x*, *y*, *z*). El vector de traducción se usa para calcular una matriz de traducción 4x4:

![Diagrama que muestra la matriz de traducción de 4x4 especificada por x, y, z.](images/trans01.png)

La matriz actual [**(vea glMatrixMode)**](glmatrixmode.md)se multiplica por esta matriz de traducción, con el producto reemplazando la matriz actual. Es decir, si M es la matriz actual y T es la matriz de traducción, M se reemplaza por M T.

Si el modo de matriz es GL MODELVIEW o GL PROJECTION, se traducen todos los objetos dibujados después de llamar a \_ \_ **glTranslated.** Use [**glPushMatrix**](glpushmatrix.md) y **glPopMatrix** para guardar y restaurar el sistema de coordenadas sin traducir.

Las siguientes funciones recuperan información relacionada [**con glTranslated**](gltranslate.md):

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

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> </dl>

 

 





