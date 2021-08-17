---
title: Función glIndexi (Gl.h)
description: La función glIndexi establece el índice de color actual.
ms.assetid: c57d2316-4081-40d8-af50-ae0299597803
keywords:
- Función glIndexi OpenGL
topic_type:
- apiref
api_name:
- glIndexi
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d905dba292457654b3f92da132eabbdc58ea316fedf6a11b55c2d1df820bbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359341"
---
# <a name="glindexi-function"></a>función glIndexi

La **función glIndexi** establece el índice de color actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glIndexi(
   GLint c
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*c* 
</dt> <dd>

Nuevo valor para el índice de color actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **función glIndexi** actualiza el índice de color actual (con un solo valor). Toma un argumento: el nuevo valor para el índice de color actual.

El índice actual se almacena como un valor de punto flotante. Los valores enteros se convierten directamente en valores de punto flotante, sin ninguna asignación especial.

Los valores de índice fuera del intervalo representable del búfer de índice de color no están fijos. Sin embargo, antes de que se dithere un índice (si está habilitado) y se escriba en el búfer de fotogramas, se convierte al formato de punto fijo. Los bits de la parte entera del valor de punto fijo resultante que no se correspondan con los bits del búfer de fotogramas se enmascaran.

El índice actual se puede actualizar en cualquier momento. En concreto, se puede llamar a **glIndexi** entre una llamada a [**glBegin**](/windows/desktop/OpenGL/glbegin) y la llamada correspondiente [**a glEnd**](glend.md).

La función siguiente recupera información relacionada con **glIndexi**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ CURRENT \_ INDEX

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

