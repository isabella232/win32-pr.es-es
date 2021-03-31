---
title: función glIndexdv (GL. h)
description: La función glIndexdv establece el índice de color actual.
ms.assetid: e718e8c5-66e4-472c-9138-177c5ee697d3
keywords:
- glIndexdv (función) OpenGL
topic_type:
- apiref
api_name:
- glIndexdv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2512e9100c4b3f68f644eb51c3d5d460787f49b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801640"
---
# <a name="glindexdv-function"></a>glIndexdv función)

La función **glIndexdv** establece el índice de color actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glIndexdv(
   const GLdouble *c
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

## <a name="remarks"></a>Observaciones

La función **glIndexdv** actualiza el índice de color actual (de un solo valor). Toma un argumento: el nuevo valor para el índice de color actual.

El índice actual se almacena como un valor de punto flotante. Los valores enteros se convierten directamente en valores de punto flotante, sin asignación especial.

Los valores de índice fuera del intervalo representable del búfer de índice de color no se fijan. Sin embargo, antes de que un índice esté desactivado (si está habilitado) y escrito en el fotogramas, se convierte al formato de punto fijo. Los bits de la parte entera del valor de punto fijo resultante que no se correspondan con bits del fotogramas se enmascaran.

El índice actual se puede actualizar en cualquier momento. En concreto, se puede llamar a **glIndexdv** entre una llamada a [**glBegin**](/windows/desktop/OpenGL/glbegin) y la llamada correspondiente a [**glEnd**](glend.md).

La siguiente función recupera información relacionada con **glIndexdv**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ índice actual de GL \_

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

