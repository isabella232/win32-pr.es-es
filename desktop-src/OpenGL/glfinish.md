---
title: Función glFinish (Gl.h)
description: La función glFinish se bloquea hasta que se completa toda la ejecución de OpenGL.
ms.assetid: 1dcb4767-02ea-41d8-bf1f-d61d20873d4f
keywords:
- Función glFinish OpenGL
topic_type:
- apiref
api_name:
- glFinish
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99d4cb185beb09cb882667b80dbd06a25546fb9209da38a775cefa887443617
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580185"
---
# <a name="glfinish-function"></a>función glFinish

La **función glFinish se** bloquea hasta que se completa toda la ejecución de OpenGL.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glFinish(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glFinish** no se devuelve hasta que se completan los efectos de todas las funciones de OpenGL llamadas anteriormente. Estos efectos incluyen todos los cambios en el estado OpenGL, todos los cambios en el estado de conexión y todos los cambios en el contenido del búfer de fotogramas.

La **función glFinish** requiere un recorrido de ida y vuelta al servidor.

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

[**glFlush**](glflush.md)
</dt> </dl>

 

 





