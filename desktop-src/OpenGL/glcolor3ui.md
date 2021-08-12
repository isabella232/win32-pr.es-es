---
title: Función glColor3ui (Gl.h)
description: Establece el color actual. | Función glColor3ui (Gl.h)
ms.assetid: 4a04ad4d-91a8-4d70-93e5-9c8f4ec4d9d2
keywords:
- Función glColor3ui OpenGL
topic_type:
- apiref
api_name:
- glColor3ui
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062ec8fbbcb135c28c3bb7454ad3ca2782c7d60068b9da82dcd980cf9cfb20a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617417"
---
# <a name="glcolor3ui-function"></a>Función glColor3ui

Establece el color actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glColor3ui(
   GLuint red,
   GLuint green,
   GLuint blue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Rojo* 
</dt> <dd>

Nuevo valor rojo para el color actual.

</dd> <dt>

*Verde* 
</dt> <dd>

Nuevo valor verde para el color actual.

</dd> <dt>

*Azul* 
</dt> <dd>

Nuevo valor azul del color actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El GL almacena un índice de color actual de un solo valor y un color RGBA de cuatro valores actual. **glcolor** establece un nuevo color RGBA de cuatro valores. **glcolor** tiene dos variantes principales: **glcolor3** y **glcolor4.** Las **variantes glcolor3** especifican los nuevos valores rojo, verde y azul explícitamente y establecen el valor alfa actual en 1,0 (intensidad completa) implícitamente. **Las variantes glcolor4** especifican explícitamente los cuatro componentes de color.

**glcolor3b,** **glcolor4b,** **glcolor3s,** **glcolor4s,** **glcolor3i** y **glcolor4i** toman tres o cuatro enteros de bytes con signo, cortos o largos como argumentos. Cuando v se anexa al nombre, los comandos de color pueden tomar un puntero a una matriz de estos valores.

Los valores de color actuales se almacenan en formato de punto flotante, con tamaños de mantisa y exponente no especificados. Los componentes de color entero sin signo, cuando se especifican, se asignan linealmente a valores de punto flotante, de modo que el valor representable más grande se asigna a 1,0 (intensidad completa) y 0 a 0,0 (intensidad cero). Los componentes de color entero con signo, cuando se especifican, se asignan linealmente a valores de punto flotante, de modo que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a -1,0. (Tenga en cuenta que esta asignación no convierte 0 de forma precisa en 0,0). Los valores de punto flotante se asignan directamente.

Ni los valores de punto flotante ni entero con signo se fijan en el \[ intervalo 0,1 antes de actualizar \] el color actual. Sin embargo, los componentes de color se fijan a este intervalo antes de interpolarse o escribirse en un búfer de color.

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

[**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindexd.md)
</dt> </dl>

 

 





