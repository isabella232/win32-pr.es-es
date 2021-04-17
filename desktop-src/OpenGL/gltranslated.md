---
title: función glTranslated (GL. h)
description: La función glTranslated multiplica la matriz actual por una matriz de traslación.
ms.assetid: 9f066a92-ee78-44d1-b8f8-0eacde0e1a47
keywords:
- glTranslated (función) OpenGL
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
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105689612"
---
# <a name="gltranslated-function"></a>glTranslated función)

La función **glTranslated** multiplica la matriz actual por una matriz de traslación.

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

Coordenada *x* de un vector de traslación.

</dd> <dt>

*y* 
</dt> <dd>

Coordenada *y* de un vector de traslación.

</dd> <dt>

*z* 
</dt> <dd>

Coordenada *z* de un vector de traslación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **glTranslated** produce la traducción especificada por (*x*, *y*, *z*). El vector de conversión se usa para calcular una matriz de traslación 4x4:

![Diagrama que muestra la matriz de traslación 4x4 especificada por x, y, z.](images/trans01.png)

La matriz actual (vea [**glMatrixMode**](glmatrixmode.md)) se multiplica por esta matriz de traducción, con el producto que reemplaza la matriz actual. Es decir, si M es la matriz actual y T es la matriz de traslación, M se reemplaza por M T.

Si el modo de matriz es \_ MODELVIEW de GL o \_ proyección de contabilidad, se traducen todos los objetos dibujados después de **glTranslated** . Use [**glPushMatrix**](glpushmatrix.md) y **glPopMatrix** para guardar y restaurar el sistema de coordenadas sin traducir.

Las siguientes funciones recuperan información relacionada con [**glTranslated**](gltranslate.md):

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

 

 





