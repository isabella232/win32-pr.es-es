---
title: Función glTranslatef (Gl.h)
description: La función glTranslatef multiplica la matriz actual por una matriz de traducción.
ms.assetid: 2354ad52-e80f-49fc-82e7-ac6c146aa59d
keywords:
- Función glTranslatef OpenGL
topic_type:
- apiref
api_name:
- glTranslatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5b52c3890b70ecb931211af1788afe2b8e6ad4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169230"
---
# <a name="gltranslatef-function"></a>Función glTranslatef

La [**función glTranslatef**](gltranslate.md) multiplica la matriz actual por una matriz de traducción.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTranslatef(
   GLfloat x,
   GLfloat y,
   GLfloat z
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

La **función glTranslatef** genera la traducción especificada por (*x*, *y*, *z*). El vector de traducción se usa para calcular una matriz de traducción 4x4:

![Diagrama que muestra la matriz de traducción de 4x4 especificada por x, y, z.](images/trans01.png)

La matriz actual (vea [**glMatrixMode)**](glmatrixmode.md)se multiplica por esta matriz de traducción, con el producto reemplazando la matriz actual. Es decir, si M es la matriz actual y T es la matriz de traducción, M se reemplaza por M T.

Si el modo de matriz es GL MODELVIEW o GL PROJECTION, se traducen todos los objetos dibujados después de \_ \_ llamar a **glTranslatef.** Use [**glPushMatrix**](glpushmatrix.md) y **glPopMatrix para** guardar y restaurar el sistema de coordenadas sin traducir.

Las funciones siguientes recuperan información relacionada [**con glTranslated**](gltranslate.md) **y glTranslatef**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MATRIX \_ MODE

**glGet con** el argumento GL \_ MODELVIEW \_ MATRIX

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

 

 





