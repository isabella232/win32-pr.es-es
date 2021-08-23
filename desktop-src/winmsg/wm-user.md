---
description: Se usa para definir mensajes privados para su uso por clases de ventana privadas, normalmente con el formato WM \_ USER+x, donde x es un valor entero.
ms.assetid: 4115c587-fcb4-4170-9948-fe33bcb8742a
title: WM_USER (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1cb14e8ef69ae35cedd4e246f253aa7b3c16451623eb7043774d1f0940cb64f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705735"
---
# <a name="wm_user"></a>WM \_ USER

Se usa para definir mensajes privados para su uso por clases de ventana privadas, normalmente con el formato **WM \_ USER** x , donde +  *x* es un valor entero.

``` syntax
#define WM_USER                         0x0400
```

## <a name="remarks"></a>Comentarios

Los siguientes son los intervalos de números de mensaje.



| Intervalo                                                        | Significado                                                        |
|--------------------------------------------------------------|----------------------------------------------------------------|
| 0 a **WM \_ USER** –1<br/>                         | Mensajes reservados para su uso por el sistema.<br/>            |
| **WM \_ USUARIO** a 0x7FFF<br/>                       | Mensajes enteros para su uso por clases de ventana privadas.<br/> |
| [**WM \_ Aplicación**](wm-app.md) (0x8000) a 0xBFFF<br/> | Mensajes disponibles para su uso por las aplicaciones.<br/>         |
| 0xC000 a través de 0xFFFF<br/>                             | Mensajes de cadena para que los usen las aplicaciones.<br/>            |
| Mayor que 0xFFFF<br/>                               | Reservado por el sistema.<br/>                             |



 

El sistema define los números de mensaje del primer intervalo (de 0 a **WM \_ USER** –1). El sistema reserva los valores de este intervalo que no se definen explícitamente.

Los números de mensaje del segundo intervalo **(WM \_ USER** 0x7FFF) se pueden definir y usar en una aplicación para enviar mensajes dentro de una clase de ventana privada. Estos valores no se pueden usar para definir mensajes significativos en toda una aplicación porque algunas clases de ventana predefinidas ya definen valores en este intervalo. Por ejemplo, las clases de control predefinidas **como BUTTON,** **EDIT,** **LISTBOX** y **COMBOBOX** pueden usar estos valores. Los mensajes de este intervalo no deben enviarse a otras aplicaciones a menos que las aplicaciones se hayan diseñado para intercambiar mensajes y para adjuntar el mismo significado a los números de mensaje.

Los números de mensaje del tercer intervalo (0x8000 a 0xBFFF) están disponibles para que las aplicaciones las usen como mensajes privados. Los mensajes de este intervalo no entren en conflicto con los mensajes del sistema.

Los números de mensaje del cuarto intervalo (0xC000 a 0xFFFF) se definen en tiempo de ejecución cuando una aplicación llama a la función [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) para recuperar un número de mensaje para una cadena. Todas las aplicaciones que registran la misma cadena pueden usar el número de mensaje asociado para intercambiar mensajes. Sin embargo, el número de mensaje real no es una constante y no se puede suponer que sea el mismo entre sesiones diferentes.

El sistema reserva los números de mensaje del quinto intervalo (0xFFFF) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**APLICACIÓN \_ WM**](wm-app.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Mensajes y colas de mensajes](messages-and-message-queues.md)
</dt> </dl>

 

 
