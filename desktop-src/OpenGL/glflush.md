---
title: función glFlush (GL. h)
description: La función glFlush fuerza la ejecución de funciones OpenGL en tiempo finito.
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- glFlush (función) OpenGL
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
ms.openlocfilehash: 8366fd5c42f68c495d544c20c3382b4e9fd37665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804057"
---
# <a name="glflush-function"></a>glFlush función)

La función **glFlush** fuerza la ejecución de funciones OpenGL en tiempo finito.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glFlush(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Distintos comandos de búfer de implementación de OpenGL en varias ubicaciones diferentes, incluidos los búferes de red y el propio acelerador de gráficos. La función **glFlush** vacía todos estos búferes, lo que hace que todos los comandos emitidos se ejecuten tan pronto como los acepte el motor de representación real. Aunque es posible que esta ejecución no se complete en un período de tiempo determinado, se completa en un intervalo de tiempo finito.

Dado que cualquier programa de OpenGL puede ejecutarse a través de una red o en un acelerador que almacene en búfer comandos, asegúrese de llamar a **glFlush** en cualquier programa que requiera que se hayan completado todos los comandos previamente emitidos. Por ejemplo, llame a **glFlush** antes de esperar la entrada del usuario que depende de la imagen generada.

La función **glFlush** puede devolver en cualquier momento. No espera hasta que se complete la ejecución de todas las funciones OpenGL emitidas previamente.

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

[**glFinish**](glfinish.md)
</dt> </dl>

 

 





