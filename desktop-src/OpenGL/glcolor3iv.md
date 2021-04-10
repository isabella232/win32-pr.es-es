---
title: función glColor3iv (GL. h)
description: Establece el color actual de una matriz de valores de color ya existente. | función glColor3iv (GL. h)
ms.assetid: b083fd09-fe92-4afa-bcb7-f36e9eeffbab
keywords:
- glColor3iv (función) OpenGL
topic_type:
- apiref
api_name:
- glColor3iv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36734d3e6d5f90283c6298705717e79b98f89474
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280144"
---
# <a name="glcolor3iv-function"></a>glColor3iv función)

Establece el color actual de una matriz de valores de color ya existente.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glColor3iv(
   const GLint *v
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*v* 
</dt> <dd>

Puntero a una matriz que contiene los valores rojo, verde y azul.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El libro de contabilidad almacena un índice de color de un solo valor actual y un color RGBA de cuatro valores actual. **glcolor** establece un nuevo color RGBA de cuatro valores. **glcolor** tiene dos variantes principales: **glcolor3** y **glcolor4**. las variantes de **glcolor3** especifican nuevos valores rojo, verde y azul explícitamente y establecen el valor alfa actual en 1,0 (intensidad total) implícitamente. las variantes de **glcolor4** especifican los cuatro componentes de color explícitamente.

**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** y **glcolor4i** toman tres o cuatro enteros con signo, cortos o largos como argumentos. Cuando se anexa v al nombre, los comandos de color pueden tomar un puntero a una matriz de estos valores.

Los valores de color actuales se almacenan en formato de punto flotante, con la mantisa y los tamaños de exponente no especificados. Los componentes de color de entero sin signo, cuando se especifican, se asignan linealmente a valores de punto flotante, de modo que el mayor valor que se puede representar se asigna a 1,0 (intensidad total) y 0 se asigna a 0,0 (intensidad cero). Los componentes de color de entero con signo, cuando se especifican, se asignan linealmente a valores de punto flotante, de modo que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0. (Tenga en cuenta que esta asignación no convierte 0 exactamente a 0,0). Los valores de punto flotante se asignan directamente.

Ninguno de los valores de punto flotante ni de entero con signo se fijan en el intervalo de \[ 0 a 1 \] antes de que se actualice el color actual. Sin embargo, los componentes de color se fijan en este intervalo antes de que se interpolen o se escriban en un búfer de color.

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

[**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindexd.md)
</dt> </dl>

 

 





