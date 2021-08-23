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
ms.openlocfilehash: 12975095aa78d143aaaf096e8b0141f37d45a56286e7d607a9253e59e27ba5bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489854"
---
# <a name="gltranslatef-function"></a>función glTranslatef

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

## <a name="remarks"></a>Comentarios

La **función glTranslatef** genera la traducción especificada por (*x*, *y*, *z*). El vector de traducción se usa para calcular una matriz de traducción 4x4:

![Diagrama que muestra la matriz de traducción de 4x4 especificada por x, y, z.](images/trans01.png)

La matriz actual [**(vea glMatrixMode**](glmatrixmode.md)) se multiplica por esta matriz de traducción, con el producto reemplazando la matriz actual. Es decir, si M es la matriz actual y T es la matriz de traducción, M se reemplaza por M T.

Si el modo de matriz es GL MODELVIEW o GL PROJECTION, se traducen todos los objetos dibujados después de llamar a \_ \_ **glTranslatef.** Use [**glPushMatrix**](glpushmatrix.md) y **glPopMatrix para** guardar y restaurar el sistema de coordenadas sin traducir.

Las siguientes funciones recuperan información relacionada [**con glTranslated**](gltranslate.md) **y glTranslatef**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MATRIX \_ MODE

**glGet** con el argumento GL \_ MODELVIEW \_ MATRIX

**glGet con** el argumento GL \_ PROJECTION \_ MATRIX

**glGet con** el argumento GL \_ TEXTURE \_ MATRIX

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





