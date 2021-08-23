---
title: Función glIndexiv (Gl.h)
description: La función glIndexiv establece el índice de color actual.
ms.assetid: 642c243f-046d-474e-8075-ef5692797020
keywords:
- Función glIndexiv OpenGL
topic_type:
- apiref
api_name:
- glIndexiv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fecb1cad302b4a302c5079f2af3dd72158d4b98ce57794b8f080a8919b9cad5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493445"
---
# <a name="glindexiv-function"></a>Función glIndexiv

La **función glIndexiv** establece el índice de color actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glIndexiv(
   const GLint *c
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

La **función glIndexiv** actualiza el índice de color actual (con un solo valor). Toma un argumento: el nuevo valor para el índice de color actual.

El índice actual se almacena como un valor de punto flotante. Los valores enteros se convierten directamente en valores de punto flotante, sin ninguna asignación especial.

Los valores de índice fuera del intervalo representable del búfer de índice de color no están fijas. Sin embargo, antes de que se dithere un índice (si está habilitado) y se escriba en el búfer de fotogramas, se convierte al formato de punto fijo. Los bits de la parte entera del valor de punto fijo resultante que no se correspondan con los bits del búfer de fotogramas se enmascaran.

El índice actual se puede actualizar en cualquier momento. En concreto, se puede llamar a **glIndexiv** entre una llamada a [**glBegin**](/windows/desktop/OpenGL/glbegin) y la llamada correspondiente [**a glEnd**](glend.md).

La función siguiente recupera información relacionada con **glIndexiv**:

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

 

