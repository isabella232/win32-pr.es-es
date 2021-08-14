---
title: Función glFlush (Gl.h)
description: La función glFlush fuerza la ejecución de funciones OpenGL en tiempo finito.
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- Función glFlush OpenGL
topic_type:
- apiref
api_name:
- glFlush
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece5f0aa96140b6fa16b5fbde1a857f1e14f1570ad7fc734626a27ac660a65ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360412"
---
# <a name="glflush-function"></a>función glFlush

La **función glFlush** fuerza la ejecución de funciones OpenGL en tiempo finito.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glFlush(void);
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

Diferentes comandos de búfer de implementaciones de OpenGL en varias ubicaciones diferentes, incluidos los búferes de red y el propio acelerador de gráficos. La **función glFlush** vacía todos estos búferes, lo que hace que todos los comandos emitidos se ejecuten tan rápido como los acepte el motor de representación real. Aunque es posible que esta ejecución no se complete en un período de tiempo determinado, se completa en una cantidad finita de tiempo.

Dado que cualquier programa OpenGL puede ejecutarse a través de una red o en un acelerador que almacena en búfer los comandos, asegúrese de llamar a **glFlush** en cualquier programa que requiera que se hayan completado todos sus comandos emitidos previamente. Por ejemplo, llame **a glFlush antes** de esperar la entrada del usuario que depende de la imagen generada.

La **función glFlush** puede devolver en cualquier momento. No espera hasta que se complete la ejecución de todas las funciones de OpenGL emitidas anteriormente.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glFinish**](glfinish.md)
</dt> </dl>

 

 





