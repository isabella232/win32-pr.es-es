---
title: Función glIndexfv (Gl.h)
description: La función glIndexfv establece el índice de color actual.
ms.assetid: 355d1896-ea9d-4a80-9dee-285f3bf638e5
keywords:
- Función glIndexfv OpenGL
topic_type:
- apiref
api_name:
- glIndexfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77a64c7c51d442d5e0dff14d8377e387b8da183bb3b74e7f2c8a1bceef189cad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493485"
---
# <a name="glindexfv-function"></a>Función glIndexfv

La **función glIndexfv** establece el índice de color actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glIndexfv(
   const GLfloat *c
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*c* 
</dt> <dd>

Puntero a una matriz de un elemento que contiene el nuevo valor para el índice de color actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **función glIndexfv** actualiza el índice de color actual (con un solo valor). Toma un argumento: el nuevo valor para el índice de color actual.

El índice actual se almacena como un valor de punto flotante. Los valores enteros se convierten directamente en valores de punto flotante, sin ninguna asignación especial.

Los valores de índice fuera del intervalo representable del búfer de índice de color no están fijas. Sin embargo, antes de que se dithere un índice (si está habilitado) y se escriba en el búfer de fotogramas, se convierte al formato de punto fijo. Los bits de la parte entera del valor de punto fijo resultante que no se correspondan con los bits del búfer de fotogramas se enmascaran.

El índice actual se puede actualizar en cualquier momento. En concreto, se puede llamar a **glIndexfv** entre una llamada a [**glBegin**](/windows/desktop/OpenGL/glbegin) y la llamada correspondiente [**a glEnd.**](glend.md)

La función siguiente recupera información relacionada con **glIndexfv**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ CURRENT \_ INDEX

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

